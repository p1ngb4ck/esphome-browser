# `pr/remote-desktop`

One part of the topic repo p1ngb4ck/esphome-remote-desktop. The whole topic, with its description, is the branch `main`.

Change of this branch: `remote_desktop`: VNC (RFB, Tight JPEG through the hardware decoder) and SPICE (MJPEG streams, JPEG images through the hardware decoder) on a page canvas of the video output; keys / mouse / touches, cursor, SPICE sound, USB redirection (usbredir; USB/IP with VNC), saved connections, probing (`protocol: auto`), close gestures

Based on these branches, whose changes it holds and builds on:

- `pr/esp32-require-hw-jpeg` of p1ngb4ck/esphome-esp-video: esp32 `require_hw_jpeg()`: the JPEG codec for the chip (P4 hardware JPEG, S2 / S3 esp_new_jpeg, others JPEGDEC)
- `pr/lvgl-remote-input` of p1ngb4ck/esphome-hid: `lvgl` `remote_input`: LVGL from outside (pointer, keys by key binding action, text), keys fire their action while LVGL is paused
- `pr/lvgl-color-depth-32` of p1ngb4ck/esphome-mipi-display: lvgl `color_depth: 32` as RGB888 (3 bytes per pixel)
- `pr/mipi-dsi-scanout` of p1ngb4ck/esphome-mipi-display: mipi_dsi `frame_buffers` (up to 3), the frame buffers handed to a direct client and flipped at the frame end, the scanout interface, LVGL drawing straight into the frame buffers with two of them
- `pr/storage` of p1ngb4ck/esphome-storage-interface: the `storage` component: registry, path / filesystem / network / raw storages, the asynchronous worker (jobs, streams), `storage.*` actions, PSRAM transfer buffer, change feed, ISO 9660 mount
- `pr/usb-host-refactor` of p1ngb4ck/esphome-usb-host: routing by device class to the drivers (named > vendor table > class, interfaces per driver), several devices per client, one shared USB task, unified transfer engine (bulk, interrupt, control, isochronous streams), driver `blacklist`, host channel budget per controller, the patched espressif/usb component (per-port FIFO bias, `fsls_only`, external hub port requests, root port reset recovery)
