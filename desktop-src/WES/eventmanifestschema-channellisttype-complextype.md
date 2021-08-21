---
title: Tipo complesso ChannelListType
description: Definisce un elenco di canali in cui i provider possono registrare gli eventi. | Tipo complesso ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- EventLog di tipo complesso ChannelListType
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8602594bdbdf6d39532213b0be660b5b3cfb6a90cd8281d9555ed2ff3a9d401
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121051"
---
# <a name="channellisttype-complex-type"></a>Tipo complesso ChannelListType

Definisce un elenco di canali in cui i provider possono registrare gli eventi.

``` syntax
<xs:complexType name="ChannelListType">
    <xs:choice
        minOccurs="0"
        maxOccurs="8"
    >
        <xs:element name="importChannel"
            type="ImportChannelType"
         />
        <xs:element name="channel"
            type="ChannelType"
         />
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:choice>
    <xs:anyAttribute
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo                                                                           | Descrizione                                                                                                                  |
|------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**Canale**](eventmanifestschema-channel-channellisttype-element.md)             | [**ChannelType**](eventmanifestschema-channeltype-complextype.md)             | Definisce un canale in cui è possibile eseguire la registrazione degli eventi.<br/>                                                                  |
| [**importChannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md) | Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.<br/> |



## <a name="remarks"></a>Commenti

È possibile specificare fino a otto canali (qualsiasi combinazione di canali importati o canali definiti dall'utente).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



 

 





