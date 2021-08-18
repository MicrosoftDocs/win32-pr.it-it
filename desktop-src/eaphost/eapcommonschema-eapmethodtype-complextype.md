---
title: Tipo complesso EapMethodType
description: Definisce gli elementi che identificano in modo univoco un singolo metodo EAP Type, VendorId, VendorType e AuthorId.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- Tipo complesso EapMethodType EAPHost
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
ms.openlocfilehash: 059ea8162241c61d88fc93f565fa0aa4ba8aee223212e6fab254ed9d5dec4eea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739171"
---
# <a name="eapmethodtype-complex-type"></a>Tipo complesso EapMethodType

Il tipo complesso **EapMethodType** definisce gli elementi che identificano in modo univoco un singolo metodo EAP: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md)e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).

[**Type**](eapcommonschema-type-eapmethodtype-element.md) e [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) sono elementi obbligatori, mentre [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) e [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) sono obbligatori solo quando l'elemento **Type** è 254 (un metodo EAP espanso).

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
| [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md)     | unsignedInt  | Fa riferimento all'autore del metodo. <br/>                                                                                                                                                                                                                 |
| [**Tipo**](eapcommonschema-type-eapmethodtype-element.md)             | unsignedByte | Fa riferimento al tipo di metodo EAP. <br/>                                                                                                                                                                                                               |
| [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md)     | unsignedInt  | Fa riferimento al fornitore che ha definito il metodo , se [**l'elemento Type**](eapcommonschema-type-eapmethodtype-element.md) è 254 (un metodo EAP espanso). [**VendorId è**](eapcommonschema-vendorid-eapmethodtype-element.md) facoltativo. <br/> |
| [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) | unsignedInt  | Tipo definito dal fornitore per il metodo. [**VendorType è**](eapcommonschema-vendortype-eapmethodtype-element.md) facoltativo. <br/>                                                                                                           |



## <a name="remarks"></a>Commenti

Gli [**elementi AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) [**e VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) non devono essere uguali per un metodo specifico.

Gli [**elementi AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) [**e VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) sono ognuno un numero univoco emesso dall'autorità IANA (Internet Assigned Numbers Authority).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[EAPHost e schema legacy](eaphost-schemas.md)
</dt> <dt>

[Schema eapcommon](eapcommonschema-schema.md)
</dt> </dl>

 

 





