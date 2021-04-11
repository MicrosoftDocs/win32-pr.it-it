---
title: Tipo complesso ChannelLoggingType
description: Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se è sequenziale o circolare. | Tipo complesso ChannelLoggingType
ms.assetid: 58da75dd-d303-4a57-8c9b-5fde575c3cbb
keywords:
- Log eventi di tipo complesso ChannelLoggingType
topic_type:
- apiref
api_name:
- ChannelLoggingType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4cfaf6dfa225799befcd0c7fb068c0f779ea33eb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104132270"
---
# <a name="channelloggingtype-complex-type"></a>Tipo complesso ChannelLoggingType

Definisce le proprietà del file di log che esegue il backup del canale, ad esempio la capacità e se è sequenziale o circolare.

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
| [**Backup automatico**](eventmanifestschema-autobackup-channelloggingtype-element.md) | boolean                                                           | Determina se creare un nuovo file di log quando il file di log corrente raggiunge le dimensioni massime. Impostare su **true** per richiedere che il servizio crei un nuovo file quando il file di log raggiunge la dimensione massima; in caso contrario, **false**. È possibile impostare il [**backup automatico**](eventmanifestschema-autobackup-channelloggingtype-element.md) su **true** solo se la [**conservazione**](eventmanifestschema-retention-channelloggingtype-element.md) è impostata su **true**. Il valore predefinito è **false**.<br/> Non esiste alcun limite al numero di file di backup che il servizio è in grado di creare (limitato solo dallo spazio disponibile su disco). I nomi dei file di backup sono nel formato Archive-*ChannelName* - *timestamp*. evtx e si trovano nella cartella% windir% \\ system32 \\ winevt \\ logs.<br/> |
| [**maxSize**](eventmanifestschema-maxsize-channelloggingtype-element.md)       | [**UInt64Type**](eventmanifestschema-hexint64type-simpletype.md) | Dimensione massima, in byte, del file di log. Il valore predefinito (e minimo) è 1 MB. Se le dimensioni del log fisico sono inferiori alle dimensioni massime configurate ed è necessario spazio aggiuntivo nel log per archiviare gli eventi, il servizio alloca un altro blocco di spazio anche se la dimensione fisica risultante del log sarà maggiore della dimensione massima configurata. Il servizio alloca blocchi di 1 MB in modo che le dimensioni fisiche possano raggiungere un massimo di 1 MB rispetto alla dimensione massima configurata. <br/>                                                                                                                                                                                                                                                      |
| [**conservazione**](eventmanifestschema-retention-channelloggingtype-element.md)   | boolean                                                           | Determina se il file di log è un file di log sequenziale o circolare. Impostare su **true** per un file di log sequenziale e **false** per un file di log circolare. Il valore predefinito è **false** per i tipi di canale operativo e di amministrazione e **true** per i tipi di canale analitico e debug.<br/> Per eseguire una query su un log circolare, è necessario innanzitutto disabilitare il canale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

È possibile specificare l'attributo **MaxSize** per qualsiasi tipo di canale.

È possibile specificare l'attributo **backup automatico** solo per i tipi di canale operativo e di amministrazione.

È possibile impostare l'attributo di **conservazione** su false (registrazione circolare) per i tipi di canale operativo e di amministratore. È possibile impostare l'attributo di **conservazione** su false (registrazione circolare) per i tipi di canale analitici e di debug, ma per visualizzare gli eventi nel Visualizzatore eventi di Windows, sarà necessario disabilitare prima il canale. Si noti che quando si Abilita nuovamente il canale, gli eventi vengono rimossi dal canale.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





