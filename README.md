# Boot / Unboot your USB drive

Boot or unboot your USB device using your windows command prompt in administrator mode. All you need to do is to follow the commands below:

## 🖥️ How to Make a USB Drive Bootable using Command Prompt

Follow these steps carefully to make your USB drive bootable:

### Step 1: Open Command Prompt as Administrator

**Press `Win + X` ➔ Select Command Prompt (Admin) or Windows PowerShell (Admin).**

### Step 2: Launch DiskPart

```bash
diskpart
```

### Step 3: List all disks

```bash
list disk
```

> *Identify your USB drive by its size.*

### Step 4: Select your USB disk

```bash
select disk X
# for e.g., select disk 1 (may be different on your system)
```

> *Replace `X` with your USB's number.*

### Step 5: Clean the drive

```bash
clean
```

> **_(⚠️ This will erase everything.)_**

### Step 6: Create a new partition

```bash
create partition primary
```

### Step 7: Select the new partition

```bash
select partition 1
```

### Step 8: Make it active

```bash
active
```

### Step 9: Format the drive (choose file system)

```bash
# Choose one of the following:
# for fat32
format fs=fat32 quick
# for ntfs
format fs=ntfs quick
```

### Step 10: Assign a drive letter

```bash
assign
```

### Step 11: Exit DiskPart

```bash
exit
```

**✅ Your USB is now bootable!**

*(You still need to manually copy your boot files or ISO contents onto it.)*
