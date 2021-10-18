+ Single
```
var (
	once  sync.Once
	batch Batch
)

func SyncInstance() *Batch {
	once.Do(func() {
		batch.BatchInit()
	})
	return &batch
}
```