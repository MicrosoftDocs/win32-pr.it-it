---
description: Identifica l'IHV.
ms.assetid: a99c231c-afd7-44e6-81af-3d49ffef8714
title: Elemento OUIHeader (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OUIHeader
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5293a6e69c1384922572764674cbadd9980702c49f8945518ff9b0c56beee2d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117797921"
---
# <a name="ouiheader-ihv-element"></a>Elemento OUIHeader (IHV)

L'elemento OUIHeader (IHV) identifica l'IHV.

**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.

``` syntax
<xs:element name="OUIHeader">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUI">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="type">
                <xs:simpleType>
                    <xs:restriction
                        base="hexBinary"
                    >
                        <xs:length
                            value="1"
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
    </xs:complexType>
</xs:element>
```

L'elemento è definito [**dall'elemento IHV.**](wlan-profileschema-ihv-wlanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                   | Tipo | Descrizione                                                                                |
|-----------------------------------------------------------|------|--------------------------------------------------------------------------------------------|
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)   |      | Contiene un oggetto hexBinary a 3 byte che identifica l'IHV.<br/>                            |
| [**digitare**](wlan-profileschema-type-ouiheader-element.md) |      | Contiene un oggetto hexBinary a 1 byte usato per differenziare le schede di interfaccia di rete in base allo stesso IHV.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre diretto nell'istanza dello schema**
</dt> <dt>

[**IHV (WLANProfile)**](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




