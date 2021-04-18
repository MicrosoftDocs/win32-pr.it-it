---
title: Tipo complesso ChannelListType
description: Definisce un elenco di canali a cui i provider possono registrare gli eventi. | Tipo complesso ChannelListType
ms.assetid: 01685955-7149-45ce-a47f-6344fcf07826
keywords:
- Log eventi di tipo complesso ChannelListType
topic_type:
- apiref
api_name:
- ChannelListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 53293687fd4ab0d87155b86edd026189f6d7c925
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321939"
---
# <a name="channellisttype-complex-type"></a>Tipo complesso ChannelListType

Definisce un elenco di canali a cui i provider possono registrare gli eventi.

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
| [**canale**](eventmanifestschema-channel-channellisttype-element.md)             | [**ChannelType**](eventmanifestschema-channeltype-complextype.md)             | Definisce un canale a cui è possibile registrare gli eventi.<br/>                                                                  |
| [**importChannel**](eventmanifestschema-importchannel-channellisttype-element.md) | [**ImportChannelType**](eventmanifestschema-importchanneltype-complextype.md) | Identifica un canale definito da un altro provider o in un manifesto che contiene una sezione di metadati.<br/> |



## <a name="remarks"></a>Commenti

È possibile specificare fino a otto canali (qualsiasi combinazione di canali o canali importati definiti).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



 

 





