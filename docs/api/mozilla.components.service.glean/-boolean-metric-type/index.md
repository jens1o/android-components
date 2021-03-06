[android-components](../../index.md) / [mozilla.components.service.glean](../index.md) / [BooleanMetricType](./index.md)

# BooleanMetricType

`data class BooleanMetricType : `[`CommonMetricData`](../-common-metric-data/index.md) [(source)](https://github.com/mozilla-mobile/android-components/blob/master/components/service/glean/src/main/java/mozilla/components/service/glean/BooleanMetricType.kt#L21)

This implements the developer facing API for recording boolean metrics.

Instances of this class type are automatically generated by the parsers at build time,
allowing developers to record values that were previously registered in the metrics.yaml file.

The boolean API only exposes the [set](set.md) method.

### Constructors

| Name | Summary |
|---|---|
| [&lt;init&gt;](-init-.md) | `BooleanMetricType(disabled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`, category: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, lifetime: `[`Lifetime`](../-lifetime/index.md)`, name: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`, sendInPings: `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>)`<br>This implements the developer facing API for recording boolean metrics. |

### Properties

| Name | Summary |
|---|---|
| [category](category.md) | `val category: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [defaultStorageDestinations](default-storage-destinations.md) | `val defaultStorageDestinations: `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>`<br>Defines the names of the storages the metric defaults to when "default" is used as the destination storage. Note that every metric type will need to override this. |
| [disabled](disabled.md) | `val disabled: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
| [ioTask](io-task.md) | `var ioTask: Job?` |
| [lifetime](lifetime.md) | `val lifetime: `[`Lifetime`](../-lifetime/index.md) |
| [name](name.md) | `val name: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |
| [sendInPings](send-in-pings.md) | `val sendInPings: `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>` |

### Inherited Properties

| Name | Summary |
|---|---|
| [identifier](../-common-metric-data/identifier.md) | `open val identifier: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html) |

### Functions

| Name | Summary |
|---|---|
| [set](set.md) | `fun set(value: `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)`): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Set a boolean value. |
| [testGetValue](test-get-value.md) | `fun testGetValue(pingName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = getStorageNames().first()): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Returns the stored value for testing purposes only. This function will attempt to await the last task (if any) writing to the the metric's storage engine before returning a value. |
| [testHasValue](test-has-value.md) | `fun testHasValue(pingName: `[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)` = getStorageNames().first()): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html)<br>Tests whether a value is stored for the metric for testing purposes only. This function will attempt to await the last task (if any) writing to the the metric's storage engine before returning a value. |

### Inherited Functions

| Name | Summary |
|---|---|
| [awaitJob](../-common-metric-data/await-job.md) | `open fun awaitJob(job: Job, timeout: `[`Long`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-long/index.html)` = JOB_TIMEOUT_MS): `[`Unit`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-unit/index.html)<br>Helper function to help await Jobs returned from coroutine launch executions used by metrics when recording data.  This is to help ensure that data is updated before test functions check or access them. |
| [getStorageNames](../-common-metric-data/get-storage-names.md) | `open fun getStorageNames(): `[`List`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin.collections/-list/index.html)`<`[`String`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-string/index.html)`>`<br>Get the list of storage names the metric will record to. This automatically expands [DEFAULT_STORAGE_NAME](#) to the list of default storages for the metric. |
| [shouldRecord](../-common-metric-data/should-record.md) | `open fun shouldRecord(logger: `[`Logger`](../../mozilla.components.support.base.log.logger/-logger/index.md)`): `[`Boolean`](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-boolean/index.html) |
