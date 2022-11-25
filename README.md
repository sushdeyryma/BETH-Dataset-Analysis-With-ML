# BETH-Dataset-Analysis-With-ML

The Beth dataset, a heterogeneously organized real-world
dataset, will be used in this work to examine anomaly
detection and OOD analysis utilizing various machine
learning and Deep Learning algorithms (ANN). This
dataset includes about 8,004,918 data points from
monitoring 23 honeypots that run on the main cloud
provider for around five non-consecutive hours and are
exclusively gathered from the OS and cloud infrastructure
management. Each cell in the Beth dataset has 14 raw
features, and two labels and some raw features have been
transformed to binary form for benchmarking.

Timestamp: Instead of being a time series, this field is
considered a sampling distribution.

ProcessId and parentProcessId: These values are utilized
by OS and need to be mapped to a binary variable.

ThreadId: The process call linking method is suggested.

UserId: The Linux operating system has defined it to
allocate the OS activity by default. Per host, a maximum of
four logins were seen in this instance.

MountNamespace: It regulates a process's ability to access
different mount points. In this case, the mountNamespace
for the userID higher than or equal to 1000 is 4026531840,
but the mountNamespace for the userID less than 1000 is
different.

ProcessName and eventName: In combination with the
eventName, which is specifically linked to the eventId,
processName is a crucial field.

EventId: For each eventName, the Linux operating system
allocates an eventId.

HostName: It aids in dividing the dataset into
corresponding subsets.

Args and argsNum: For sophisticated ML models, these
raw features are vital.

ReturnValue: This indicates if the call was successful or
not. It is specified as -1 (for bad errors), 0 (for success), and
1 (for success and signaling something to the parent
process) in this dataset.

StackAddresses: It is complicated to assess this raw
feature without encoding or further embedding.
Additionally, each record in this dataset is manually
designated as suspicious (sus) and evil (evil) to aid in
analysis. Suspicious records are identified when there is
unusual activity, whilst evil records show an external
malevolent presence and are deemed to be outside of
distribution. This dataset is further subdivided into tuning,
validation, and testing sets.
