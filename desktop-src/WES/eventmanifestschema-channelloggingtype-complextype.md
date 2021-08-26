---
title: Tipo complesso ChannelLoggingType
description: Definisce le proprietà del file di log che si trova a backup del canale, ad esempio la capacità e se è sequenziale o circolare. | Tipo complesso ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- EventLog di tipo complesso ChannelLoggingType
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e696837b1132a0b82ad428e7404892ae73de88e4435325d988b7936b3a6ba534
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032281"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complesso ChannelLoggingType

Definisce le proprietà del file di log che si trova a backup del canale, ad esempio la capacità e se è sequenziale o circolare.

``` syntax
<xs:complexType name="ChannelLoggingType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="autoBackup"
            type="boolean"
            minOccurs="0"
         />
        <xs:element name="retention"
            type="boolean"
            default="0"
            minOccurs="0"
         />
        <xs:element name="maxSize"
            type="UInt64Type"
            default="1048576"
            minOccurs="0"
         />
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



| Elemento                                                                         | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Autobackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Determina se creare un nuovo file di log quando il file di log corrente raggiunge le dimensioni massime. Impostare su **true per** richiedere che il servizio crei un nuovo file quando il file di log raggiunge le dimensioni massime; in caso contrario, **false.** È possibile impostare [**autoBackup**](eventmanifestschema-autobackup-channelloggingtype-element.md) su **true solo** se [**retention**](eventmanifestschema-retention-channelloggingtype-element.md) è impostato su **true.** Il valore predefinito è **false**.<br/> Non esiste alcun limite al numero di file di backup che il servizio può creare (limitato solo dallo spazio disponibile su disco). I nomi dei file di backup sono nel formato Archive-*channelName* timestamp .evtx e si trovano - nella cartella %windir% \\ System32 \\ winevt \\ Logs.<br/> |
| [**Maxsize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Dimensione massima, in byte, del file di log. Il valore predefinito (e minimo) è 1 MB. Se le dimensioni fisiche del log sono inferiori alle dimensioni massime configurate ed è necessario spazio aggiuntivo nel log per archiviare gli eventi, il servizio alloca un altro blocco di spazio anche se le dimensioni fisiche risultanti del log saranno maggiori delle dimensioni massime configurate. Il servizio alloca blocchi di 1 MB in modo che le dimensioni fisiche potrebbero aumentare fino a 1 MB rispetto alle dimensioni massime configurate. <br/>                                                                                                                                                                                                                                                      |
| [**detenzione**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Determina se il file di log è un file di log sequenziale o circolare. Impostare su **true per** un file di log sequenziale e **su false** per un file di log circolare. Il valore predefinito **è false** per i tipi di canale Admin e Operational e **true** per i tipi di canale Analisi e Debug.<br/> Per eseguire query su un log circolare, è prima necessario disabilitare il canale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

È possibile specificare **l'attributo maxSize** per qualsiasi tipo di canale.

È possibile specificare **l'attributo autoBackup** solo per i tipi di canale Admin e Operational.

È possibile impostare **l'attributo retention** su false (registrazione circolare) per i tipi di canale Admin e Operational. È possibile impostare l'attributo **retention** su false (registrazione circolare) per i tipi di canale Analitico e Debug, ma per visualizzare gli eventi nel Windows Visualizzatore eventi, è prima necessario disabilitare il canale. Si noti che quando si abilita nuovamente il canale, gli eventi vengono rimossi dal canale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





