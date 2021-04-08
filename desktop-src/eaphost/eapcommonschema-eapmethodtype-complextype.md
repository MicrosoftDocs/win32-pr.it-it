---
title: Tipo complesso EapMethodType
description: Definisce gli elementi che identificano in modo univoco un solo tipo di metodo EAP, VendorId, VendorType e autorizzazione.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType di tipo complesso EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741842"
---
# <a name="eapmethodtype-complex-type"></a>Tipo complesso EapMethodType

Il tipo complesso **EapMethodType** definisce gli elementi che identificano in modo univoco un singolo metodo EAP, ovvero [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)e [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md).

Il [**tipo**](eapcommonschema-type-eapmethodtype-element.md) e l' [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md) sono elementi obbligatori, mentre [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) sono obbligatori solo quando l'elemento **Type** è 254 (un metodo EAP espanso).

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                | Tipo         | Descrizione                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Si riferisce all'autore del metodo. <br/>                                                                                                                                                                                                                 |
| [**Tipo**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Si riferisce al tipo di metodo EAP. <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Fa riferimento al fornitore che ha definito il metodo, se l'elemento [**Type**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso). [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) è facoltativo. <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | È il tipo definito dal fornitore per il metodo. [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) è facoltativo. <br/>                                                                                                           |



## <a name="remarks"></a>Commenti

Gli elementi [**autorizzazioned**](eapcommonschema-authorid-eapmethodtype-element.md) e [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.

Gli elementi [**autorizzazione**](eapcommonschema-authorid-eapmethodtype-element.md), [**tipo**](eapcommonschema-type-eapmethodtype-element.md), [**VendorID**](eapcommonschema-vendorid-eapmethodtype-element.md) e [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) sono ciascuno un numero univoco emesso da IANA (Internet Assigned Numbers Authority).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





