# Reference
<details><summary><code>client.<a href="src/insion/client.py">moderate_a_record</a>(...) -> ModerateResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create or update a record and return its moderation result immediately.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.moderate_a_record(
    client_id="clientId",
    name="name",
    entity="entity",
    content="content",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**client_id:** `str` — Your unique identifier for the record.
    
</dd>
</dl>

<dl>
<dd>

**name:** `str` — Name or title of the record.
    
</dd>
</dl>

<dl>
<dd>

**entity:** `str` — Type of record, such as post, comment, or message.
    
</dd>
</dl>

<dl>
<dd>

**content:** `Content` 
    
</dd>
</dl>

<dl>
<dd>

**client_url:** `typing.Optional[str]` — URL for the original content.
    
</dd>
</dl>

<dl>
<dd>

**metadata:** `typing.Optional[Metadata]` 
    
</dd>
</dl>

<dl>
<dd>

**user:** `typing.Optional[UserInput]` 
    
</dd>
</dl>

<dl>
<dd>

**passthrough:** `typing.Optional[bool]` — Moderate without persisting the record's name or content, or the user's email, name, or username.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">ingest_a_record</a>(...) -> IngestRecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create or update a content record for asynchronous moderation. Results are delivered through webhook events when moderation is performed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.ingest_a_record(
    client_id="clientId",
    name="name",
    entity="entity",
    content="content",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `IngestRecordRequest` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">delete_a_record</a>(...) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a record from the moderation system by its client ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.delete_a_record(
    client_id="clientId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**client_id:** `str` — Your unique identifier for the record.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">ingest_a_user</a>(...) -> IngestUserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create or update a user without ingesting a record.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.ingest_a_user(
    client_id="clientId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**request:** `UserInput` 
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">list_records</a>(...) -> ListRecordsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the records belonging to the authenticated organization.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.list_records()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**starting_after:** `typing.Optional[str]` — Return items after this Insion ID. Cannot be used with ending_before.
    
</dd>
</dl>

<dl>
<dd>

**ending_before:** `typing.Optional[str]` — Return items before this Insion ID. Cannot be used with starting_after.
    
</dd>
</dl>

<dl>
<dd>

**client_id:** `typing.Optional[str]` — Filter by your record identifier.
    
</dd>
</dl>

<dl>
<dd>

**user:** `typing.Optional[str]` — Filter by Insion user ID.
    
</dd>
</dl>

<dl>
<dd>

**entity:** `typing.Optional[str]` — Filter by record entity.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[GetApiV1RecordsRequestStatus]` — Filter by moderation status.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">retrieve_a_record</a>(...) -> RecordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one record by its Insion record ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.retrieve_a_record(
    record_id="recordId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**record_id:** `str` — Insion record ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">list_users</a>(...) -> ListUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

List the users belonging to the authenticated organization.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.list_users()

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**limit:** `typing.Optional[int]` — Maximum number of items to return.
    
</dd>
</dl>

<dl>
<dd>

**starting_after:** `typing.Optional[str]` — Return items after this Insion ID. Cannot be used with ending_before.
    
</dd>
</dl>

<dl>
<dd>

**ending_before:** `typing.Optional[str]` — Return items before this Insion ID. Cannot be used with starting_after.
    
</dd>
</dl>

<dl>
<dd>

**client_id:** `typing.Optional[str]` — Filter by your user identifier.
    
</dd>
</dl>

<dl>
<dd>

**email:** `typing.Optional[str]` — Filter by user email.
    
</dd>
</dl>

<dl>
<dd>

**status:** `typing.Optional[GetApiV1UsersRequestStatus]` — Filter by user action status.
    
</dd>
</dl>

<dl>
<dd>

**user:** `typing.Optional[str]` — Filter by Insion user ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">retrieve_a_user</a>(...) -> UserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve one user by its Insion user ID.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.retrieve_a_user(
    user_id="userId",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` — Insion user ID.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.<a href="src/insion/client.py">create_an_appeal</a>(...) -> CreateAppealResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an appeal for a suspended user. Appeals must be enabled for the organization.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```python
from insion import InsionClient
from insion.environment import InsionClientEnvironment

client = InsionClient(
    token="<token>",
    environment=InsionClientEnvironment.DEFAULT,
)

client.create_an_appeal(
    user_id="userId",
    text="text",
)

```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**user_id:** `str` — Insion user ID.
    
</dd>
</dl>

<dl>
<dd>

**text:** `str` — The appeal message.
    
</dd>
</dl>

<dl>
<dd>

**request_options:** `typing.Optional[RequestOptions]` — Request-specific configuration.
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

