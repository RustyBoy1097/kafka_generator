用于kafka的代码生成

## 1. core

```
-p  kafka.internals.generated 
-o  src/generated/java/kafka/internals/generated 
-i  src/main/resources/core/common/message 
-m  MessageDataGenerator
```

## 2. metadata

```
-p org.apache.kafka.common.metadata
-o src/generated/java/org/apache/kafka/common/metadata
-i src/main/resources/metadata/common/metadata
-m MessageDataGenerator JsonConverterGenerator
-t MetadataRecordTypeGenerator MetadataJsonConvertersGenerator
```

## 3. clients

```
-p org.apache.kafka.common.message
-o src/generated/java/org/apache/kafka/common/message
-i src/main/resources/clients/common/message
-t ApiMessageTypeGenerator
-m MessageDataGenerator JsonConverterGenerator
```

## 4. clients (test)

```
-p org.apache.kafka.common.message
-o src/generated-test/java/org/apache/kafka/common/message
-i src/test/resources/clients/common/message
-m MessageDataGenerator JsonConverterGenerator
```

## 5. raft

```
-p org.apache.kafka.raft.generated
-o src/generated/java/org/apache/kafka/raft/generated
-i src/main/resources/raft/common/message
-m MessageDataGenerator JsonConverterGenerator
```

## 6. storage

```
-p org.apache.kafka.server.log.remote.metadata.storage.generated
-o src/generated/java/org/apache/kafka/server/log/remote/metadata/storage/generated
-i src/main/resources/storage/message
-m MessageDataGenerator JsonConverterGenerator
-t MetadataRecordTypeGenerator MetadataJsonConvertersGenerator
```

## 7. streams

```
-p org.apache.kafka.streams.internals.generated
-o src/generated/java/org/apache/kafka/streams/internals/generated
-i src/main/resources/streams/common/message
-m MessageDataGenerator
```
