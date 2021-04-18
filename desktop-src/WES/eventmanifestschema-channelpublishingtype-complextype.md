---
title: Tipo complesso ChannelPublishingType
description: Definisce le proprietà di registrazione per la sessione utilizzata dal canale. | Tipo complesso ChannelPublishingType
ms.assetid: 4b3980f4-8652-4070-97c0-99cd1a9fc85a
keywords:
- Log eventi di tipo complesso ChannelPublishingType
topic_type:
- apiref
api_name:
- ChannelPublishingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af84685f25705f6f8c54a85b9befb6df791593ed
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321735"
---
# <a name="channelpublishingtype-complex-type"></a>Tipo complesso ChannelPublishingType

Definisce le proprietà di registrazione per la sessione utilizzata dal canale.

``` syntax
<xs:complexType name="ChannelPublishingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="level"
            type="UInt8Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="UInt64Type"
            default="0"
            minOccurs="0"
         />
        <xs:element name="controlGuid"
            type="GUIDType"
            minOccurs="0"
         />
        <xs:element name="bufferSize"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="minBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="fileMax"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="maxBuffers"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="latency"
            type="UInt32Type"
            minOccurs="0"
         />
        <xs:element name="clockType"
            default="SystemTime"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="SystemTime"
                     />
                    <xs:enumeration
                        value="QPC"
                     />
                </xs:restriction>
            </xs:simpleType>
        </xs:element>
        <xs:element name="sidType"
            minOccurs="0"
        >
            <xs:simpleType>
                <xs:restriction
                    base="xs:string"
                >
                    <xs:enumeration
                        value="None"
                     />
                    <xs:enumeration
                        value="Publishing"
                     />
                </xs:restriction>
            </xs:simpleType>
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



| Elemento                                                                              | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**bufferSize**](eventmanifestschema-buffersize-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Quantità di memoria, in kilobyte, da allocare per ogni buffer. Se si prevede una frequenza di eventi relativamente bassa, le dimensioni del buffer devono essere impostate sulle dimensioni della pagina di memoria. Se la frequenza degli eventi dovrebbe essere relativamente elevata, è necessario specificare una dimensione del buffer maggiore e aumentare il numero massimo di buffer.<br/> La dimensione del buffer influiscono sulla velocità di riempimento dei buffer e deve essere scaricata. Sebbene le dimensioni di un buffer di piccole dimensioni richiedano meno memoria, aumentano la velocità con cui è necessario scaricare i buffer.<br/> Le dimensioni predefinite del buffer per i canali analitici e di debug sono pari a 4 KB e per l'amministratore e la relativa operatività è 64 KB.<br/>                                                                                                                |
| [**clockType**](eventmanifestschema-clocktype-channelpublishingtype-element.md)     |                                                                   | Risoluzione del clock da usare quando si registra il timestamp per ogni evento. È possibile specificare SystemTime o QPC. SystemTime fornisce un indicatore di tempo a bassa risoluzione (10 millisecondi), ma è relativamente meno costoso da recuperare. Il valore predefinito è SystemTime. <br/> Il contatore delle prestazioni delle query (QPC) fornisce un timestamp ad alta risoluzione (100 nanosecondi), ma è relativamente più costoso da recuperare. È necessario QPC se si dispone di un elevato tasso di eventi o se il consumer unisce gli eventi da buffer diversi.<br/>                                                                                                                                                                                                                                 |
| [**controlGuid**](eventmanifestschema-controlguid-channelpublishingtype-element.md) | [**GUIDType**](eventmanifestschema-guidtype-simpletype.md)       | Identifica il GUID della sessione per una sessione ETW che contiene eventi WPP. Questa impostazione è consentita solo per i canali di tipo debug. Non è possibile abilitare completamente questi canali con le parole chiave impostate su zero (0x0000000000000000). Devono essere abilitate con le parole chiave impostate su 0xFFFFFFFFFFFFFFFF.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **fileMax**                                                                          | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Il numero massimo di volte in cui si desidera che il servizio crei un nuovo file di log quando il canale è abilitato (incluso quando il computer viene riavviato). Se il valore è 0 o 1, il servizio sovrascriverà il file di log ogni volta che il canale viene abilitato e gli eventi precedenti andranno perduti. Se il valore è maggiore di 1, il servizio creerà un nuovo file di log ogni volta che il canale viene abilitato per mantenere gli eventi. Il valore predefinito è 1 e il valore massimo che è possibile specificare è 16.<br/> Il servizio aggiunge un numero decimale a tre cifre compreso tra 0 e fileMax 1 e il nome di ogni file. Ad esempio *filename*. etl.xxx, dove xxx è il numero decimale a tre cifre. I file si trovano in% windir% \\ system32 \\ winevt \\ logs.<br/> |
| [**Parole**](eventmanifestschema-keywords-channelpublishingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Maschera di maschera che determina la categoria di eventi scritti nel canale. Se il valore dell'attributo **Keywords** è 0, tutti gli eventi scritti dal provider vengono scritti nel canale. in caso contrario, solo gli eventi che hanno definito una parola chiave inclusa nella maschera di **parole chiave** vengono scritti nel canale. Il valore predefinito è 0.<br/> I canali di debug per i quali è impostato l'attributo controlGuid devono impostare l'attributo **Keywords** su 0xFFFFFFFFFFFFFFFF.<br/> La sessione passa il valore Keywords al provider quando Abilita il provider.<br/>                                                                                                                                                                            |
| [**latenza**](eventmanifestschema-latency-channelpublishingtype-element.md)         | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Tempo di attesa prima dello scaricamento dei buffer, in millisecondi. Se è zero, ETW Scarica i buffer non appena diventano pieni. Se è diverso da zero, ETW Scarica tutti i buffer che contengono eventi in base al valore anche se il buffer non è pieno. In genere, si desidera scaricare i buffer solo quando diventano pieni. La forzatura dei buffer per lo scaricamento può aumentare le dimensioni del file di log con lo spazio del buffer non riempito. Il valore predefinito è 1 secondo per i log amministrativi e operativi e 5 secondi per i log analitici e di debug.<br/>                                                                                                                                                                                                                               |
| [**livello**](eventmanifestschema-level-channelpublishingtype-element.md)             | [**UInt8Type**](eventmanifestschema-hexint8type-simpletype.md)   | Livello di gravità degli eventi da scrivere sul canale. Il servizio scrive gli eventi nel canale che hanno un valore di livello minore o uguale al valore specificato. Il valore predefinito è 0, che indica la registrazione di eventi con qualsiasi valore di livello.<br/> La sessione passa il valore del livello al provider quando Abilita il provider.<br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**maxBuffers**](eventmanifestschema-maxbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Numero massimo di buffer da allocare per la sessione. In genere, questo valore è il numero minimo di buffer più venti. Questo valore deve essere maggiore o uguale al valore specificato per minBuffers.<br/> Il numero massimo predefinito di buffer per i canali analitici e di debug è 10 KB e per l'amministratore e operativo è 64 KB.<br/>                                                                                                                                                                                                                                                                                                                                                                                                |
| [**minBuffers**](eventmanifestschema-minbuffers-channelpublishingtype-element.md)   | [**UInt32Type**](eventmanifestschema-hexint32type-simpletype.md) | Numero minimo di buffer da allocare per la sessione. Il valore predefinito è zero.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**sidType**](eventmanifestschema-sidtype-channelpublishingtype-element.md)         |                                                                   | Determina se includere un ID di sicurezza (SID) dell'entità con ogni evento scritto nel canale. Per includere il SID con l'evento, impostare questo attributo su "Publishing". Il SID viene impostato in base all'identità del thread nel momento in cui viene scritto l'evento. Se non si desidera includere il SID con l'evento, impostare questo attributo su "None". Il valore predefinito è "Publishing".<br/>                                                                                                                                                                                                                                                                                                                                                           |



## <a name="remarks"></a>Commenti

È possibile specificare queste informazioni di pubblicazione per i tipi di canale analitico e di debug o per qualsiasi canale che specifichi l'isolamento personalizzato.

Sebbene sia possibile specificare il livello e le parole chiave, è necessario considerare che questi saranno gli unici eventi che si riceveranno dal provider per il canale.

Quando un buffer è pieno, ETW Scarica il buffer nel file di log. Se i buffer vengono compilati più velocemente di quanto possano essere scaricati, i nuovi buffer vengono allocati e aggiunti al pool di buffer della sessione, fino al numero massimo specificato. Oltre questo limite, la sessione ignora gli eventi in ingresso fino a quando non diventa disponibile un buffer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





