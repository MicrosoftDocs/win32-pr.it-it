---
title: Tipo complesso ImportChannelType
description: Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- EventLog di tipo complesso ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66136ee767c16aa85bfcef33fd23d5d42817f844fc309f7633d2a3d2bd35f2e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119471052"
---
# <a name="importchanneltype-complex-type"></a>Tipo complesso ImportChannelType

Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.

``` syntax
<xs:complexType name="ImportChannelType"
    mixed="true"
>
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="chid"
                type="token"
                use="optional"
             />
            <xs:attribute name="name"
                type="anyURI"
                use="required"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a>Attributi



| Nome   | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                            |
|--------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| chid   | token                                                             | Identificatore che identifica in modo univoco il canale nell'elenco di canali definiti o importati dal provider. Usare questo valore quando si fa riferimento a questo canale in una definizione di evento. Se non si specifica un identificatore di canale, usare il nome del canale per fare riferimento a questo canale in una definizione di evento.<br/>  |
| name   | anyURI                                                            | Nome del canale da importare.<br/>                                                                                                                                                                                                                                                                          |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da usare per fare riferimento al canale nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il canale nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="remarks"></a>Commenti

Il manifesto che ha definito il canale importato deve essere installato prima che il provider scrive gli eventi. In caso contrario, gli eventi non possono essere scritti nel canale (l'operazione di scrittura ha esito positivo, gli eventi non vengono semplicemente scritti nel canale).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



 

 





