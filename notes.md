## Space Apps Data Notes
- catalog tells which events happen when in the data
    - includes name of file, absolute & relative time, etc.
    - we do NOT need to predict type of moonquake
    - ** IMPORTANT **: Be sure to include whether we use abs or rel time in header

### Lunar Data
- Passive seismic experiments were deployed with Apollo 11 (1969), Apollo 12 (1969), Apollo 14 (1971), Apollo 15 (1971) and Apollo 16 (1972) [10]. Apollo 11 returned seismic data for around twenty days. The remaining stations operated nearly continuously from their installation until September 1977
-  The timestamps have a sampling interval of ~0.6038 s, and so typically the first valid timestamp falls in the first 0.6038 s. If the data were not valid, the first timestamp will be later.
- sampling times which overrun past midnight (but the original
timestamps are in the current day) are included in the trace for the current day.
- The PSE team do not correct for the 1.2–1.4 s delay time when transmitting from the Moon to
Earth. Additionally, the team do not correct for the apparent variations in sampling rate which
are caused by changes in the orbital parameters of the Moon-Earth system, such as by the
rotation of the Earth, the libration of the Moon or changes in Moon-Earth distance
- The directory and filename convention for continuous data is:
directory name data/<NETWORK>/continuous_waveform/<STATION>/<YEAR>/<JDAY>
file name NET.STA.[LOC].CHAN.YEAR.JDAY.REV.EXT
where:
- NET is the Network ID,
- STA is the Station ID,
- LOC is the location ID,
- CHAN is the channel ID,
- YEAR is the earth year of the measurement,
- JDAY is the day-of-year (on Earth),
- REV is the revision of the file,
- EXT is file name extension (mseed for SEED format or csv for ASCII Table format).
An example file name is xa.s12.01.mhz.1976.061.0.mseed.
Channel codes (CHAN) specify one of MHZ, MH1, MH2 (mid-period sensor), SHZ (short-
period sensor) or ATT (timing trace). Location codes are specified for the mid-period channels:
‘00’ for peaked mode operation and ‘01’ for flat mode operation.
The files include the following default fields for specifying the data encoding in Mini-SEED
(described in [5]): ‘byteorder’, ‘dataquality', 'encoding', ’filesize’, 'number_of_records',
'record_length'. ‘Dataquality’ is set to ‘D’, 'The state of quality control of the data is
indeterminate