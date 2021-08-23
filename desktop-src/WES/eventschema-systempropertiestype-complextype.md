---
title: Tipo complesso SystemPropertiesType
description: Definisce le informazioni che identificano il provider e come è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID di processo e thread.
ms.assetid: f86f7940-86cf-49ba-8f09-bf6f473d60fd
keywords:
- EventLog di tipo complesso SystemPropertiesType
topic_type:
- apiref
api_name:
- SystemPropertiesType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7391362938502f0c307faab4d7b9166633647b093e5154b3aa56512c6ee4e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119620241"
---
# <a name="systempropertiestype-complex-type"></a>Tipo complesso SystemPropertiesType

Definisce le informazioni che identificano il provider e come è stato abilitato, l'evento, il canale in cui è stato scritto l'evento e le informazioni di sistema, ad esempio gli ID di processo e thread.

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
| [**Channel**](eventschema-channel-systempropertiestype-element.md)             | anyURI                                                      | Canale a cui è stato registrato l'evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Computer**](eventschema-computer-systempropertiestype-element.md)           | string                                                      | nome del computer in cui si è verificato l'evento.<br/>                                                                                                                                                                                                                                                                             |
| [**Correlazione**](eventschema-correlation-systempropertiestype-element.md)     |                                                             | Identificatori di attività che i consumer possono usare per raggruppare gli eventi correlati.<br/>                                                                                                                                                                                                                                                 |
| [**Eventid**](eventschema-eventid-systempropertiestype-element.md)             |                                                             | Identificatore usato dal provider per identificare l'evento.<br/>                                                                                                                                                                                                                                                                      |
| [**EventRecordID**](eventschema-eventrecordid-systempropertiestype-element.md) |                                                             | Numero di record assegnato all'evento al momento della registrazione.<br/>                                                                                                                                                                                                                                                                       |
| [**Esecuzione**](eventschema-execution-systempropertiestype-element.md)         |                                                             | Contiene informazioni sul processo e sul thread che ha registrato l'evento.<br/>                                                                                                                                                                                                                                                          |
| [**Parole chiavi**](eventschema-keywords-systempropertiestype-element.md)           | [**HexInt64Type**](eventschema-hexint64type-simpletype.md) | Maschera di bit delle parole chiave definite nell'evento. Le parole chiave vengono usate per classificare i tipi di eventi, ad esempio gli eventi associati alla lettura dei dati.<br/>                                                                                                                                                                                 |
| [**Livello**](eventschema-level-systempropertiestype-element.md)                 | unsignedByte                                                | Livello di gravità definito nell'evento.<br/>                                                                                                                                                                                                                                                                                          |
| [**Opcode**](eventschema-opcode-systempropertiestype-element.md)               | unsignedByte                                                | Codice operativo definito nell'evento. L'attività e il codice operativo vengono usati in modo tipico per identificare la posizione nell'applicazione da cui è stato registrato l'evento.<br/>                                                                                                                                                                                  |
| [**Provider**](eventschema-provider-systempropertiestype-element.md)           |                                                             | Identifica il provider che ha registrato l'evento. Gli **attributi Name** e **Guid** vengono inclusi se il provider ha usato un manifesto di strumentazione per definirne gli eventi. In caso contrario, **l'attributo EventSourceName** viene incluso se l'evento è stato registrato da un provider di eventi legacy (tramite l'API [Registrazione](/windows/desktop/EventLog/event-logging) eventi).<br/> |
| [**Sicurezza**](eventschema-security-systempropertiestype-element.md)           |                                                             | Identifica l'utente che ha registrato l'evento.<br/>                                                                                                                                                                                                                                                                                        |
| [**Attività**](eventschema-task-systempropertiestype-element.md)                   | unsignedShort                                               | Attività definita nell'evento . Le attività e il codice operativo vengono in genere usati per identificare la posizione nell'applicazione da cui è stato registrato l'evento.<br/>                                                                                                                                                                                    |
| [**TimeCreated**](eventschema-timecreated-systempropertiestype-element.md)     |                                                             | Timestamp che identifica quando è stato registrato l'evento. Il timestamp includerà **l'attributo SystemTime** o **l'attributo RawTime.**<br/>                                                                                                                                                                           |
| [**Versione**](schema-version-systempropertiestype-element.md)                  | unsignedByte                                                | Numero di versione della definizione dell'evento.<br/>                                                                                                                                                                                                                                                                                     |



## <a name="attributes"></a>Attributi



| Nome              | Tipo                                                | Descrizione                                                                                                                                                                                                                                                                                             |
|-------------------|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ActivityID        | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività corrente. Gli eventi pubblicati con questo identificatore fanno parte della stessa attività.<br/>                                                                                                                                         |
| EventSourceName   | string                                              | Nome dell'origine evento che ha pubblicato l'evento (se l'origine evento deriva dall'API [di registrazione eventi](/windows/desktop/EventLog/event-logging) legacy).<br/>                                                                                                                                                      |
| Guid              | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica in modo univoco il provider.<br/>                                                                                                                                                                                                                        |
| KernelTime        | unsignedInt                                         | Tempo di esecuzione trascorso per le istruzioni in modalità kernel, in unità di tempo CPU. Se si usa una sessione privata ETW, usare invece il valore nel membro ProcessorTime. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file con estensione etl).<br/>                                               |
| Nome              | anyURI                                              | Nome del provider.<br/>                                                                                                                                                                                                                                                                    |
| ProcessID         | unsignedInt                                         | Identifica il processo che ha generato l'evento.<br/>                                                                                                                                                                                                                                             |
| ProcessorID       | unsignedByte                                        | Numero di identificazione del processore che ha elaborato l'evento. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file con estensione etl).<br/>                                                                                                                                             |
| ProcessorTime     | unsignedInt                                         | Per le sessioni private ETW, il tempo di esecuzione trascorso per le istruzioni in modalità utente, in tick CPU. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file con estensione etl).<br/>                                                                                                                    |
| Qualificatori        | **unsignedShort**                                   | Un provider legacy usa un numero a 32 bit per identificare i relativi eventi. Se l'evento viene registrato da un provider legacy, il valore dell'elemento **EventID** contiene i 16 bit meno elevati dell'identificatore dell'evento e l'attributo **Qualifier** contiene i 16 bit più alti dell'identificatore dell'evento.<br/> |
| RawTime           | unsignedLong                                        | Valore di timestamp non elaborato. Il formato del timestamp dipende dall'origine dell'ora usata per raccogliere la traccia. Il timestamp non elaborato offre una precisione maggiore rispetto all'ora di sistema. L'output dell'evento sottoposto a rendering conterrà l'ora non elaborata solo se si usa TraceRpt.exe con l'opzione -rts.<br/>                 |
| RelatedActivityID | [**GUIDType**](eventschema-guidtype-simpletype.md) | Identificatore univoco globale che identifica l'attività a cui è stato trasferito il controllo. Gli eventi correlati avrebbero quindi questo identificatore come identificatore ActivityID.<br/>                                                                                                            |
| SessionID         | unsignedInt                                         | Numero di identificazione per la sessione del server terminal in cui si è verificato l'evento. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file con estensione etl).<br/>                                                                                                                            |
| SystemTime        | dateTime                                            | Ora di sistema in cui è stato registrato l'evento.<br/>                                                                                                                                                                                                                                                |
| ThreadID          | unsignedInt                                         | Identifica il thread che ha generato l'evento.<br/>                                                                                                                                                                                                                                              |
| UserID            | string                                              | ID di sicurezza (SID) dell'utente in formato stringa.<br/>                                                                                                                                                                                                                                    |
| Tempi          | unsignedInt                                         | Tempo di esecuzione trascorso per le istruzioni in modalità utente, in unità di tempo della CPU. Se si usa una sessione privata ETW, usare invece il valore nel membro ProcessorTime. Disponibile solo per gli eventi registrati in un file di log di traccia eventi (file con estensione etl).<br/>                                                 |



## <a name="remarks"></a>Commenti

Per impostazione predefinita, l'evento contiene il nome di dominio completo (FQDN) di un computer. Per usare il nome NETBIOS anziché il nome FQDN, è necessario creare un valore DWORD del Registro di sistema denominato CompatFlags nella chiave del Registro di sistema seguente e impostare il valore di CompatFlags su 0x2.

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
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

