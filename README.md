# saga-orchestration-with-kafka

**Saga-pattern Happy path flow**


![alt](https://github.com/nawaz-ch/saga-orchestration-with-kafka/blob/84191aa212ba8950f473ea15e44132c7606b1138/saga-pattern(happy-path).png)



> [!NOTE]
> In case the paymentDB failed to save the payment, the DB can rollback the transcation. To maintain data consistency,the productsDB and orderDB must be rolledback through compensating transcations.

