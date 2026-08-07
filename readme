# Audio Playback Scheduler

This guide explains how to automatically play the Gayatri and Temple audio files using a Bash script and cron.

## Step 1: Go to the project folder

```bash
cd ~/sh_pc_v3_device
```

---

## Step 2: Create the script

```bash
nano play_sequence.sh
```

---

## Step 3: Save and exit Nano

Press:

- `Ctrl + O`
- `Enter`
- `Ctrl + X`

---

## Step 4: Make the script executable

```bash
chmod +x ~/sh_pc_v3_device/play_sequence.sh
```

---

## Step 5: Test the script manually

```bash
~/sh_pc_v3_device/play_sequence.sh
```

> **Note:** If the current time does not match the configured playback time, nothing will play. This is expected.

---

## Step 6: Add the cron job

Open crontab:

```bash
crontab -e
```

Add the following line:

```cron
* * * * * /home/sh/sh_pc_v3_device/play_sequence.sh
```

This runs the script every minute. The script checks the current day and time before playing the audio.

---

## Step 7: Save the crontab

Press:

- `Ctrl + O`
- `Enter`
- `Ctrl + X`

---

## Step 8: Verify the cron job

```bash
crontab -l
```

Expected output:

```cron
* * * * * /home/sh/sh_pc_v3_device/play_sequence.sh
```

---

## Step 9: Check the playback log

View the log:

```bash
cat /home/sh/play_sequence.log
```

Or monitor it live:

```bash
tail -f /home/sh/play_sequence.log
```

Example output:

```text
Thu Aug 07 18:50:00 IST 2026: Playing Gayatri
Thu Aug 07 18:50:10 IST 2026: Playing Temple
Thu Aug 07 18:50:45 IST 2026: Finished
```

## Playback Schedule

| Day | Gayatri Start Time |
|------|--------------------|
| Odd Day | 6:50 PM |
| Even Day | 5:50 PM |

After Gayatri finishes, the script waits **10 seconds** and then plays the Temple audio.
