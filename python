class CropRecord:
    def __init__(self, record_id, crop_name, area, harvest):
        self.record_id = record_id
        self.crop_name = crop_name
        self.area = area
        self.harvest = harvest

    # Instance method
    def show_record(self):
        productivity = self.harvest / self.area
        print(
            f"ID: {self.record_id} | Crop: {self.crop_name} | "
            f"Productivity: {productivity:.2f} tonnes/hectare"
        )


class CropMonitor:
    app_name = "Crop Yield Monitor"

    def __init__(self):
        self.records = []  # List of CropRecord objects

    # Class method
    @classmethod
    def show_app_name(cls):
        print(cls.app_name)


def add_record(monitor, record):
    """Add a crop object to the list."""
    monitor.records.append(record)


def display_records(monitor):
    """Display the crop objects in the list."""
    if len(monitor.records) == 0:
        print("No records have been added.")
    else:
        for record in monitor.records:
            record.show_record()


def main():
    monitor = CropMonitor()
    CropMonitor.show_app_name()

    while True:
        print("\n1. Add a crop record")
        print("2. Display all records")
        print("3. Search by record ID")
        print("4. Exit")

        choice = input("Choose 1–4: ")

        if choice == "1":
            try:
                record_id = input("Record ID: ")
                crop_name = input("Crop name: ")
                area = float(input("Area in hectares: "))
                harvest = float(input("Harvest in tonnes: "))

                if area <= 0 or harvest < 0:
                    print("Area must be above zero; harvest cannot be negative.")
                    continue

                # Create a CropRecord object
                record = CropRecord(record_id, crop_name, area, harvest)

                # The monitor object stores the record object
                add_record(monitor, record)
                print("Record added.")

            except ValueError:
                print("Please enter valid numbers for area and harvest.")

        elif choice == "2":
            display_records(monitor)

        elif choice == "3":
            search_id = input("Enter the record ID: ")
            found = False

            for record in monitor.records:
                if record.record_id == search_id:
                    record.show_record()
                    found = True

            if not found:
                print("Record not found.")

        elif choice == "4":
            print("Goodbye!")
            break

        else:
            print("Please choose 1, 2, 3, or 4.")


if __name__ == "__main__":
    main()