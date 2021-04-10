---
title: Tipo complesso ImportChannelType
description: Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.
ms.assetid: da14d837-0ed8-4d85-9820-46c77753768d
keywords:
- Log eventi di tipo complesso ImportChannelType
topic_type:
- apiref
api_name:
- ImportChannelType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7500d52179c3282c7f15dcdd5dd5a32620bbc076
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119694"
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
| figlio   | token                                                             | Identificatore che identifica in modo univoco il canale nell'elenco di canali che il provider definisce o importa. Utilizzare questo valore quando si fa riferimento a questo canale in una definizione di evento. Se non si specifica un identificatore di canale, utilizzare il nome del canale per fare riferimento a questo canale in una definizione di evento.<br/>  |
| name   | anyURI                                                            | Nome del canale da importare.<br/>                                                                                                                                                                                                                                                                          |
| simbolo | [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md) | Simbolo da utilizzare per fare riferimento al canale nell'applicazione. Il [**compilatore di messaggi (MC.exe)**](message-compiler--mc-exe-.md) usa il simbolo per creare una costante per il canale nel file di intestazione generato dal compilatore. Se non si specifica un simbolo, il compilatore ne genera uno automaticamente.<br/> |



## <a name="remarks"></a>Commenti

Il manifesto che ha definito il canale importato deve essere installato prima che il provider scriva gli eventi; in caso contrario, gli eventi non possono essere scritti nel canale (l'operazione di scrittura ha esito positivo, gli eventi non vengono semplicemente scritti nel canale).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





