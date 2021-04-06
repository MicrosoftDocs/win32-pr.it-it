---
title: Tipo complesso SystemPropertiesType
description: Definisce le informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- Log eventi di tipo complesso SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ce78a804c52ed492bd4b2a42332f8eda36b4c3be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742722"
---
# <a name="systempropertiestype-complex-type"></a>Tipo complesso SystemPropertiesType

Definisce le informazioni che identificano il provider e il modo in cui è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID processo e thread.

``` syntax
<xs:complexType name="SystemPropertiesType">
    <xs:sequence>
        <xs:element name="Provider">
            <xs:complexType>
                <xs:attribute name="Name"
                    type="anyURI"
                    use="optional"
                 />
                <xs:attribute name="Guid"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="EventSourceName"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="EventID">
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedShort"
                    >
                        <xs:attribute name="Qualifiers"
                            type="unsignedShort"
                            use="optional"
                         />
                    </xs:extension>
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Version"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Level"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Task"
            type="unsignedShort"
            minOccurs="0"
         />
        <xs:element name="Opcode"
            type="unsignedByte"
            minOccurs="0"
         />
        <xs:element name="Keywords"
            type="HexInt64Type"
            minOccurs="0"
         />
        <xs:element name="TimeCreated"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="SystemTime"
                    type="dateTime"
                    use="optional"
                 />
                <xs:attribute name="RawTime"
                    type="unsignedLong"
                    use="optional"
                 />
            </xs:complexType>
            <xs:key name="uniqueAtt">
                <xs:selector
                    xpath="."
                 />
                <xs:field
                    xpath="@SystemTime|@RawTime"
                 />
            </xs:key>
        </xs:element>
        <xs:element name="EventRecordID"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:simpleContent>
                    <xs:extension
                        base="unsignedLong"
                     />
                </xs:simpleContent>
            </xs:complexType>
        </xs:element>
        <xs:element name="Correlation"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ActivityID"
                    type="GUIDType"
                    use="optional"
                 />
                <xs:attribute name="RelatedActivityID"
                    type="GUIDType"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Execution"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="ProcessID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ThreadID"
                    type="unsignedInt"
                    use="required"
                 />
                <xs:attribute name="ProcessorID"
                    type="unsignedByte"
                    use="optional"
                 />
                <xs:attribute name="SessionID"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="KernelTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="UserTime"
                    type="unsignedInt"
                    use="optional"
                 />
                <xs:attribute name="ProcessorTime"
                    type="unsignedInt"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="Channel"
            type="anyURI"
            minOccurs="0"
         />
        <xs:element name="Computer"
            type="string"
         />
        <xs:element name="Security"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="UserID"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                         | Tipo                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Canale in cui è stato registrato l'evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | string                                                      | nome del computer in cui si è verificato l'evento.<br/>                                                                                                                                                                                                                                                                             |
| [**Correlazione**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Identificatori di attività che possono essere utilizzati dagli utenti per raggruppare gli eventi correlati.<br/>                                                                                                                                                                                                                                                 |
| [**EventID**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Identificatore utilizzato dal provider per identificare l'evento.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Numero di record assegnato all'evento quando è stato registrato.<br/>                                                                                                                                                                                                                                                                       |
| [**Esecuzione**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contiene informazioni sul processo e sul thread che hanno registrato l'evento.<br/>                                                                                                                                                                                                                                                          |
| [**Parole chiave**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Maschera di maschera delle parole chiave definite nell'evento. Le parole chiave vengono utilizzate per classificare i tipi di eventi (ad esempio, gli eventi associati alla lettura dei dati).<br/>                                                                                                                                                                                 |
| [**Livello**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Livello di gravità definito nell'evento.<br/>                                                                                                                                                                                                                                                                                          |
| [**Opcode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Codice operativo definito nell'evento. Task e OpCode sono typcially usati per identificare la posizione nell'applicazione dalla quale è stato registrato l'evento.<br/>                                                                                                                                                                                  |
| [**Provider**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifica il provider che ha registrato l'evento. Gli attributi **Name** e **GUID** sono inclusi se il provider utilizza un manifesto di strumentazione per definire gli eventi; in caso contrario, l'attributo **eventSourceName** viene incluso se un provider di eventi legacy (usando l'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) ) ha registrato l'evento.<br/> |
| [**Sicurezza**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifica l'utente che ha registrato l'evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Attività**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Attività definita nell'evento. L'attività e il codice operativo vengono in genere utilizzati per identificare la posizione nell'applicazione dalla quale è stato registrato l'evento.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Timestamp che identifica il momento in cui l'evento è stato registrato. Il timestamp includerà l'attributo **SYSTEMTIME** o l'attributo **RawTime** .<br/>                                                                                                                                                                           |
| [**Versione**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Numero di versione della definizione dell'evento.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Attributi



| Nome              | Tipo                                                | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività corrente. Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.<br/>                                                                                                                                         |
| EventSourceName   | string                                              | Nome dell'origine evento che ha pubblicato l'evento (se l'origine evento è dall'API di [registrazione eventi](/windows/desktop/EventLog/event-logging) legacy).<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica in modo univoco il provider.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in unità di tempo della CPU. Se si utilizza una sessione privata ETW, utilizzare invece il valore del membro ProcessorTime. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).<br/>                                               |
| Nome              | anyURI                                              | Nome del provider.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifica il processo che ha generato l'evento.<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Numero di identificazione del processore che ha elaborato l'evento. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | Per le sessioni private ETW, il tempo di esecuzione trascorso per le istruzioni in modalità utente, in cicli della CPU. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).<br/>                                                                                                                    |
| Qualificatori        | **unsignedShort**                                   | Un provider Legacy utilizza un numero a 32 bit per identificare gli eventi. Se l'evento viene registrato da un provider Legacy, il valore dell'elemento **eventId** contiene i 16 bit di ordine inferiore dell'identificatore dell'evento e l'attributo **Qualifier** contiene i 16 bit più significativi dell'identificatore di evento.<br/> |
| RawTime           | unsignedLong                                        | Valore del timestamp non elaborato; il formato del timestamp dipende dall'origine dell'ora utilizzata per raccogliere la traccia. Il timestamp non elaborato offre una precisione maggiore rispetto all'ora di sistema. L'output dell'evento di cui è stato eseguito il rendering conterrà solo l'ora RAW se si usa TraceRpt.exe con l'opzione-RTS.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo. Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Numero di identificazione per la sessione di Terminal Server in cui si è verificato l'evento. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Ora di sistema del momento in cui l'evento è stato registrato.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifica il thread che ha generato l'evento.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | ID di sicurezza (SID) dell'utente in formato stringa.<br/>                                                                                                                                                                                                                                    |
| Tempi          | unsignedInt                                         | Tempo di esecuzione trascorso per le istruzioni in modalità utente, in unità di tempo della CPU. Se si utilizza una sessione privata ETW, utilizzare invece il valore del membro ProcessorTime. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file ETL).<br/>                                                 |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'evento contiene il nome di dominio completo (FQDN) di un computer. Per usare il nome NETBIOS anziché il nome di dominio completo, è necessario creare un valore DWORD del registro di sistema denominato CompatFlags nella seguente chiave del registro di sistema e impostare il valore di CompatFlags su 0x2.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               WINEVT
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

