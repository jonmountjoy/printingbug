`flutter build apk`

Fails with

```
FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':printing:generateReleaseRFile'.
> A failure occurred while executing com.android.build.gradle.internal.res.GenerateLibraryRFileTask$GenerateLibRFileRunnable
   > /Users/jonmountjoy/.gradle/caches/transforms-3/e8f76a0f126409abcd369d60caf05481/transformed/androidx.fragment-r.txt

* Try:
> Run with --stacktrace option to get the stack trace.
> Run with --info or --debug option to get more log output.
> Run with --scan to get full insights.

* Get more help at https://help.gradle.org
```


The full error:

```
FAILURE: Build failed with an exception.
[        ] * What went wrong:
[        ] Execution failed for task ':printing:generateReleaseRFile'.
[        ] > A failure occurred while executing com.android.build.gradle.internal.res.GenerateLibraryRFileTask$GenerateLibRFileRunnable
[        ]    > /Users/jonmountjoy/.gradle/caches/transforms-3/e8f76a0f126409abcd369d60caf05481/transformed/androidx.fragment-r.txt
[        ] * Try:
[        ] > Run with --debug option to get more log output.
[        ] > Run with --scan to get full insights.
[        ] * Exception is:
[        ] org.gradle.api.tasks.TaskExecutionException: Execution failed for task ':printing:generateReleaseRFile'.
[        ] 	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.lambda$executeIfValid$1(ExecuteActionsTaskExecuter.java:142)
[        ] 	at org.gradle.internal.Try$Failure.ifSuccessfulOrElse(Try.java:282)
[        ] 	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeIfValid(ExecuteActionsTaskExecuter.java:140)
[        ] 	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.execute(ExecuteActionsTaskExecuter.java:128)
[        ] 	at org.gradle.api.internal.tasks.execution.CleanupStaleOutputsExecuter.execute(CleanupStaleOutputsExecuter.java:77)
[        ] 	at org.gradle.api.internal.tasks.execution.FinalizePropertiesTaskExecuter.execute(FinalizePropertiesTaskExecuter.java:46)
[        ] 	at org.gradle.api.internal.tasks.execution.ResolveTaskExecutionModeExecuter.execute(ResolveTaskExecutionModeExecuter.java:51)
[        ] 	at org.gradle.api.internal.tasks.execution.SkipTaskWithNoActionsExecuter.execute(SkipTaskWithNoActionsExecuter.java:57)
[        ] 	at org.gradle.api.internal.tasks.execution.SkipOnlyIfTaskExecuter.execute(SkipOnlyIfTaskExecuter.java:57)
[        ] 	at org.gradle.api.internal.tasks.execution.CatchExceptionTaskExecuter.execute(CatchExceptionTaskExecuter.java:36)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.executeTask(EventFiringTaskExecuter.java:77)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:55)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:52)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:199)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:157)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationExecutor.call(DefaultBuildOperationExecutor.java:73)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter.execute(EventFiringTaskExecuter.java:52)
[        ] 	at org.gradle.execution.plan.LocalTaskNodeExecutor.execute(LocalTaskNodeExecutor.java:69)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:322)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:309)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:302)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:288)
[        ] 	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.execute(DefaultPlanExecutor.java:462)
[        ] 	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.run(DefaultPlanExecutor.java:379)
[        ] 	at org.gradle.internal.concurrent.ExecutorPolicy$CatchAndRecordFailures.onExecute(ExecutorPolicy.java:64)
[        ] 	at org.gradle.internal.concurrent.ManagedExecutorImpl$1.run(ManagedExecutorImpl.java:49)
[        ] 	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(Unknown Source)
[        ] 	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(Unknown Source)
[        ] 	at java.base/java.lang.Thread.run(Unknown Source)
[        ] Caused by: org.gradle.workers.internal.DefaultWorkerExecutor$WorkExecutionException: A failure occurred while executing com.android.build.gradle.internal.res.GenerateLibraryRFileTask$GenerateLibRFileRunnable
[        ] 	at org.gradle.workers.internal.DefaultWorkerExecutor$WorkItemExecution.waitForCompletion(DefaultWorkerExecutor.java:348)
[        ] 	at org.gradle.internal.work.DefaultAsyncWorkTracker.lambda$waitForItemsAndGatherFailures$2(DefaultAsyncWorkTracker.java:130)
[        ] 	at org.gradle.internal.Factories$1.create(Factories.java:31)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.withoutLocks(DefaultWorkerLeaseService.java:321)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.withoutLocks(DefaultWorkerLeaseService.java:304)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.withoutLock(DefaultWorkerLeaseService.java:309)
[        ] 	at org.gradle.internal.work.DefaultAsyncWorkTracker.waitForItemsAndGatherFailures(DefaultAsyncWorkTracker.java:126)
[        ] 	at org.gradle.internal.work.DefaultAsyncWorkTracker.waitForItemsAndGatherFailures(DefaultAsyncWorkTracker.java:92)
[        ] 	at org.gradle.internal.work.DefaultAsyncWorkTracker.waitForAll(DefaultAsyncWorkTracker.java:78)
[        ] 	at org.gradle.internal.work.DefaultAsyncWorkTracker.waitForCompletion(DefaultAsyncWorkTracker.java:66)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution$3.run(TaskExecution.java:244)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$1.execute(DefaultBuildOperationRunner.java:29)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$1.execute(DefaultBuildOperationRunner.java:26)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:157)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.run(DefaultBuildOperationRunner.java:47)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationExecutor.run(DefaultBuildOperationExecutor.java:68)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution.executeAction(TaskExecution.java:221)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution.executeActions(TaskExecution.java:204)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution.executeWithPreviousOutputFiles(TaskExecution.java:187)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution.execute(TaskExecution.java:165)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep.executeInternal(ExecuteStep.java:89)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep.access$000(ExecuteStep.java:40)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep$1.call(ExecuteStep.java:53)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep$1.call(ExecuteStep.java:50)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:199)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:157)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationExecutor.call(DefaultBuildOperationExecutor.java:73)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep.execute(ExecuteStep.java:50)
[        ] 	at org.gradle.internal.execution.steps.ExecuteStep.execute(ExecuteStep.java:40)
[        ] 	at org.gradle.internal.execution.steps.RemovePreviousOutputsStep.execute(RemovePreviousOutputsStep.java:68)
[        ] 	at org.gradle.internal.execution.steps.RemovePreviousOutputsStep.execute(RemovePreviousOutputsStep.java:38)
[        ] 	at org.gradle.internal.execution.steps.CancelExecutionStep.execute(CancelExecutionStep.java:41)
[        ] 	at org.gradle.internal.execution.steps.TimeoutStep.executeWithoutTimeout(TimeoutStep.java:74)
[        ] 	at org.gradle.internal.execution.steps.TimeoutStep.execute(TimeoutStep.java:55)
[        ] 	at org.gradle.internal.execution.steps.CreateOutputsStep.execute(CreateOutputsStep.java:51)
[        ] 	at org.gradle.internal.execution.steps.CreateOutputsStep.execute(CreateOutputsStep.java:29)
[        ] 	at org.gradle.internal.execution.steps.CaptureStateAfterExecutionStep.executeDelegateBroadcastingChanges(CaptureStateAfterExecutionStep.java:124)
[        ] 	at org.gradle.internal.execution.steps.CaptureStateAfterExecutionStep.execute(CaptureStateAfterExecutionStep.java:80)
[        ] 	at org.gradle.internal.execution.steps.CaptureStateAfterExecutionStep.execute(CaptureStateAfterExecutionStep.java:58)
[        ] 	at org.gradle.internal.execution.steps.ResolveInputChangesStep.execute(ResolveInputChangesStep.java:48)
[        ] 	at org.gradle.internal.execution.steps.ResolveInputChangesStep.execute(ResolveInputChangesStep.java:36)
[        ] 	at org.gradle.internal.execution.steps.BuildCacheStep.executeWithoutCache(BuildCacheStep.java:181)
[        ] 	at org.gradle.internal.execution.steps.BuildCacheStep.lambda$execute$1(BuildCacheStep.java:71)
[        ] 	at org.gradle.internal.Either$Right.fold(Either.java:175)
[        ] 	at org.gradle.internal.execution.caching.CachingState.fold(CachingState.java:59)
[        ] 	at org.gradle.internal.execution.steps.BuildCacheStep.execute(BuildCacheStep.java:69)
[        ] 	at org.gradle.internal.execution.steps.BuildCacheStep.execute(BuildCacheStep.java:47)
[        ] 	at org.gradle.internal.execution.steps.StoreExecutionStateStep.execute(StoreExecutionStateStep.java:36)
[        ] 	at org.gradle.internal.execution.steps.StoreExecutionStateStep.execute(StoreExecutionStateStep.java:25)
[        ] 	at org.gradle.internal.execution.steps.RecordOutputsStep.execute(RecordOutputsStep.java:36)
[        ] 	at org.gradle.internal.execution.steps.RecordOutputsStep.execute(RecordOutputsStep.java:22)
[        ] 	at org.gradle.internal.execution.steps.SkipUpToDateStep.executeBecause(SkipUpToDateStep.java:110)
[        ] 	at org.gradle.internal.execution.steps.SkipUpToDateStep.lambda$execute$2(SkipUpToDateStep.java:56)
[        ] 	at java.base/java.util.Optional.orElseGet(Unknown Source)
[        ] 	at org.gradle.internal.execution.steps.SkipUpToDateStep.execute(SkipUpToDateStep.java:56)
[        ] 	at org.gradle.internal.execution.steps.SkipUpToDateStep.execute(SkipUpToDateStep.java:38)
[        ] 	at org.gradle.internal.execution.steps.ResolveChangesStep.execute(ResolveChangesStep.java:73)
[        ] 	at org.gradle.internal.execution.steps.ResolveChangesStep.execute(ResolveChangesStep.java:44)
[        ] 	at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsFinishedStep.execute(MarkSnapshottingInputsFinishedStep.java:37)
[        ] 	at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsFinishedStep.execute(MarkSnapshottingInputsFinishedStep.java:27)
[        ] 	at org.gradle.internal.execution.steps.ResolveCachingStateStep.execute(ResolveCachingStateStep.java:89)
[        ] 	at org.gradle.internal.execution.steps.ResolveCachingStateStep.execute(ResolveCachingStateStep.java:50)
[        ] 	at org.gradle.internal.execution.steps.ValidateStep.execute(ValidateStep.java:102)
[        ] 	at org.gradle.internal.execution.steps.ValidateStep.execute(ValidateStep.java:57)
[        ] 	at org.gradle.internal.execution.steps.CaptureStateBeforeExecutionStep.execute(CaptureStateBeforeExecutionStep.java:76)
[        ] 	at org.gradle.internal.execution.steps.CaptureStateBeforeExecutionStep.execute(CaptureStateBeforeExecutionStep.java:50)
[        ] 	at org.gradle.internal.execution.steps.SkipEmptyWorkStep.executeWithNoEmptySources(SkipEmptyWorkStep.java:254)
[        ] 	at org.gradle.internal.execution.steps.SkipEmptyWorkStep.execute(SkipEmptyWorkStep.java:91)
[        ] 	at org.gradle.internal.execution.steps.SkipEmptyWorkStep.execute(SkipEmptyWorkStep.java:56)
[        ] 	at org.gradle.internal.execution.steps.RemoveUntrackedExecutionStateStep.execute(RemoveUntrackedExecutionStateStep.java:32)
[        ] 	at org.gradle.internal.execution.steps.RemoveUntrackedExecutionStateStep.execute(RemoveUntrackedExecutionStateStep.java:21)
[        ] 	at org.gradle.internal.execution.steps.legacy.MarkSnapshottingInputsStartedStep.execute(MarkSnapshottingInputsStartedStep.java:38)
[        ] 	at org.gradle.internal.execution.steps.LoadPreviousExecutionStateStep.execute(LoadPreviousExecutionStateStep.java:43)
[        ] 	at org.gradle.internal.execution.steps.LoadPreviousExecutionStateStep.execute(LoadPreviousExecutionStateStep.java:31)
[        ] 	at org.gradle.internal.execution.steps.AssignWorkspaceStep.lambda$execute$0(AssignWorkspaceStep.java:40)
[        ] 	at org.gradle.api.internal.tasks.execution.TaskExecution$4.withWorkspace(TaskExecution.java:281)
[        ] 	at org.gradle.internal.execution.steps.AssignWorkspaceStep.execute(AssignWorkspaceStep.java:40)
[        ] 	at org.gradle.internal.execution.steps.AssignWorkspaceStep.execute(AssignWorkspaceStep.java:30)
[        ] 	at org.gradle.internal.execution.steps.IdentityCacheStep.execute(IdentityCacheStep.java:37)
[        ] 	at org.gradle.internal.execution.steps.IdentityCacheStep.execute(IdentityCacheStep.java:27)
[        ] 	at org.gradle.internal.execution.steps.IdentifyStep.execute(IdentifyStep.java:44)
[        ] 	at org.gradle.internal.execution.steps.IdentifyStep.execute(IdentifyStep.java:33)
[        ] 	at org.gradle.internal.execution.impl.DefaultExecutionEngine$1.execute(DefaultExecutionEngine.java:76)
[        ] 	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.executeIfValid(ExecuteActionsTaskExecuter.java:139)
[        ] 	at org.gradle.api.internal.tasks.execution.ExecuteActionsTaskExecuter.execute(ExecuteActionsTaskExecuter.java:128)
[        ] 	at org.gradle.api.internal.tasks.execution.CleanupStaleOutputsExecuter.execute(CleanupStaleOutputsExecuter.java:77)
[        ] 	at org.gradle.api.internal.tasks.execution.FinalizePropertiesTaskExecuter.execute(FinalizePropertiesTaskExecuter.java:46)
[        ] 	at org.gradle.api.internal.tasks.execution.ResolveTaskExecutionModeExecuter.execute(ResolveTaskExecutionModeExecuter.java:51)
[        ] 	at org.gradle.api.internal.tasks.execution.SkipTaskWithNoActionsExecuter.execute(SkipTaskWithNoActionsExecuter.java:57)
[        ] 	at org.gradle.api.internal.tasks.execution.SkipOnlyIfTaskExecuter.execute(SkipOnlyIfTaskExecuter.java:57)
[        ] 	at org.gradle.api.internal.tasks.execution.CatchExceptionTaskExecuter.execute(CatchExceptionTaskExecuter.java:36)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.executeTask(EventFiringTaskExecuter.java:77)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:55)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter$1.call(EventFiringTaskExecuter.java:52)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:199)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:157)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationExecutor.call(DefaultBuildOperationExecutor.java:73)
[        ] 	at org.gradle.api.internal.tasks.execution.EventFiringTaskExecuter.execute(EventFiringTaskExecuter.java:52)
[        ] 	at org.gradle.execution.plan.LocalTaskNodeExecutor.execute(LocalTaskNodeExecutor.java:69)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:322)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$InvokeNodeExecutorsAction.execute(DefaultTaskExecutionGraph.java:309)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:302)
[        ] 	at org.gradle.execution.taskgraph.DefaultTaskExecutionGraph$BuildOperationAwareExecutionAction.execute(DefaultTaskExecutionGraph.java:288)
[        ] 	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.execute(DefaultPlanExecutor.java:462)
[        ] 	at org.gradle.execution.plan.DefaultPlanExecutor$ExecutorWorker.run(DefaultPlanExecutor.java:379)
[        ] 	at org.gradle.internal.concurrent.ExecutorPolicy$CatchAndRecordFailures.onExecute(ExecutorPolicy.java:64)
[        ] 	at org.gradle.internal.concurrent.ManagedExecutorImpl$1.run(ManagedExecutorImpl.java:49)
[        ] 	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(Unknown Source)
[        ] 	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(Unknown Source)
[        ] 	at java.base/java.lang.Thread.run(Unknown Source)
[        ] Caused by: java.nio.file.NoSuchFileException: /Users/jonmountjoy/.gradle/caches/transforms-3/e8f76a0f126409abcd369d60caf05481/transformed/androidx.fragment-r.txt
[        ] 	at java.base/sun.nio.fs.UnixException.translateToIOException(Unknown Source)
[        ] 	at java.base/sun.nio.fs.UnixException.rethrowAsIOException(Unknown Source)
[        ] 	at java.base/sun.nio.fs.UnixException.rethrowAsIOException(Unknown Source)
[        ] 	at java.base/sun.nio.fs.UnixFileAttributeViews$Basic.readAttributes(Unknown Source)
[        ] 	at java.base/sun.nio.fs.UnixFileSystemProvider.readAttributes(Unknown Source)
[        ] 	at java.base/java.nio.file.Files.readAttributes(Unknown Source)
[        ] 	at com.android.build.gradle.internal.services.SymbolTableBuildService$FileCacheKey.<init>(SymbolTableBuildService.kt:111)
[        ] 	at com.android.build.gradle.internal.services.SymbolTableBuildService.getSymbolTablesCached(SymbolTableBuildService.kt:148)
[        ] 	at com.android.build.gradle.internal.services.SymbolTableBuildService.loadClasspath(SymbolTableBuildService.kt:69)
[        ] 	at com.android.build.gradle.internal.res.GenerateLibraryRFileTask$GenerateLibRFileRunnable.run(GenerateLibraryRFileTask.kt:159)
[        ] 	at com.android.build.gradle.internal.profile.ProfileAwareWorkAction.execute(ProfileAwareWorkAction.kt:74)
[        ] 	at org.gradle.workers.internal.DefaultWorkerServer.execute(DefaultWorkerServer.java:63)
[        ] 	at org.gradle.workers.internal.NoIsolationWorkerFactory$1$1.create(NoIsolationWorkerFactory.java:66)
[        ] 	at org.gradle.workers.internal.NoIsolationWorkerFactory$1$1.create(NoIsolationWorkerFactory.java:62)
[        ] 	at org.gradle.internal.classloader.ClassLoaderUtils.executeInClassloader(ClassLoaderUtils.java:100)
[        ] 	at org.gradle.workers.internal.NoIsolationWorkerFactory$1.lambda$execute$0(NoIsolationWorkerFactory.java:62)
[        ] 	at org.gradle.workers.internal.AbstractWorker$1.call(AbstractWorker.java:44)
[        ] 	at org.gradle.workers.internal.AbstractWorker$1.call(AbstractWorker.java:41)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:204)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$CallableBuildOperationWorker.execute(DefaultBuildOperationRunner.java:199)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:66)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner$2.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:157)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.execute(DefaultBuildOperationRunner.java:59)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationRunner.call(DefaultBuildOperationRunner.java:53)
[        ] 	at org.gradle.internal.operations.DefaultBuildOperationExecutor.call(DefaultBuildOperationExecutor.java:73)
[        ] 	at org.gradle.workers.internal.AbstractWorker.executeWrappedInBuildOperation(AbstractWorker.java:41)
[        ] 	at org.gradle.workers.internal.NoIsolationWorkerFactory$1.execute(NoIsolationWorkerFactory.java:59)
[        ] 	at org.gradle.workers.internal.DefaultWorkerExecutor.lambda$submitWork$2(DefaultWorkerExecutor.java:212)
[        ] 	at java.base/java.util.concurrent.FutureTask.run(Unknown Source)
[        ] 	at org.gradle.internal.work.DefaultConditionalExecutionQueue$ExecutionRunner.runExecution(DefaultConditionalExecutionQueue.java:187)
[        ] 	at org.gradle.internal.work.DefaultConditionalExecutionQueue$ExecutionRunner.access$700(DefaultConditionalExecutionQueue.java:120)
[        ] 	at org.gradle.internal.work.DefaultConditionalExecutionQueue$ExecutionRunner$1.run(DefaultConditionalExecutionQueue.java:162)
[        ] 	at org.gradle.internal.Factories$1.create(Factories.java:31)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.withLocks(DefaultWorkerLeaseService.java:249)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.runAsWorkerThread(DefaultWorkerLeaseService.java:109)
[        ] 	at org.gradle.internal.work.DefaultWorkerLeaseService.runAsWorkerThread(DefaultWorkerLeaseService.java:114)
[        ] 	at org.gradle.internal.work.DefaultConditionalExecutionQueue$ExecutionRunner.runBatch(DefaultConditionalExecutionQueue.java:157)
[        ] 	at org.gradle.internal.work.DefaultConditionalExecutionQueue$ExecutionRunner.run(DefaultConditionalExecutionQueue.java:126)
[        ] 	at java.base/java.util.concurrent.Executors$RunnableAdapter.call(Unknown Source)
[        ] 	at java.base/java.util.concurrent.FutureTask.run(Unknown Source)
[        ] 	... 5 more
[        ] * Get more help at https://help.gradle.org
[        ] BUILD FAILED in 527ms
[ +392 ms] Running Gradle task 'assembleRelease'... (completed in 1,021ms)
[  +30 ms] "flutter apk" took 1,628ms.
[  +20 ms] Gradle task assembleRelease failed with exit code 1
[        ]
           #0      throwToolExit (package:flutter_tools/src/base/common.dart:10:3)
           #1      AndroidGradleBuilder.buildGradleApp (package:flutter_tools/src/android/gradle.dart:500:9)
           <asynchronous suspension>
           #2      AndroidGradleBuilder.buildApk (package:flutter_tools/src/android/gradle.dart:224:5)
           <asynchronous suspension>
           #3      BuildApkCommand.runCommand (package:flutter_tools/src/commands/build_apk.dart:141:5)
           <asynchronous suspension>
           #4      FlutterCommand.run.<anonymous closure> (package:flutter_tools/src/runner/flutter_command.dart:1408:27)
           <asynchronous suspension>
           #5      AppContext.run.<anonymous closure> (package:flutter_tools/src/base/context.dart:153:19)
           <asynchronous suspension>
           #6      CommandRunner.runCommand (package:args/command_runner.dart:212:13)
           <asynchronous suspension>
           #7      FlutterCommandRunner.runCommand.<anonymous closure> (package:flutter_tools/src/runner/flutter_command_runner.dart:420:9)
           <asynchronous suspension>
           #8      AppContext.run.<anonymous closure> (package:flutter_tools/src/base/context.dart:153:19)
           <asynchronous suspension>
           #9      FlutterCommandRunner.runCommand (package:flutter_tools/src/runner/flutter_command_runner.dart:364:5)
           <asynchronous suspension>
           #10     run.<anonymous closure>.<anonymous closure> (package:flutter_tools/runner.dart:130:9)
           <asynchronous suspension>
           #11     AppContext.run.<anonymous closure> (package:flutter_tools/src/base/context.dart:153:19)
           <asynchronous suspension>
           #12     main (package:flutter_tools/executable.dart:93:3)
           <asynchronous suspension>

```
