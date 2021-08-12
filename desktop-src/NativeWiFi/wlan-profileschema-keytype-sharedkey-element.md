---
description: Indica se la chiave condivisa sarà una chiave di rete o una pass phrase.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento keyType (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 88c9a48d1c70cd156fa3d8f63bd3b70d69a99a1151a18c95ffd556b2503c9575
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619284"
---
# <a name="keytype-sharedkey-element"></a>Elemento keyType (sharedKey)

L'elemento keyType (sharedKey) indica se la chiave condivisa sarà una chiave di rete o una pass phrase.

``` syntax
<xs:element name="keyType">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="networkKey"
             />
            <xs:enumeration
                value="passPhrase"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito [**dall'elemento sharedKey.**](wlan-profileschema-sharedkey-security-element.md)

## <a name="remarks"></a>Commenti

Quando [**l'elemento**](wlan-profileschema-encryption-authencryption-element.md) di crittografia ha un valore WEP, **keyType** deve essere impostato su **networkKey**.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **keyType,** vedere [Esempio](non-broadcast-profile-sample.md)di profilo non broadcast , Esempio di profilo [personale WPA](wpa-personal-profile-sample.md)e Esempio di profilo [WPA2-Personale](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**sharedKey**](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sharedKey (sicurezza)**](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 




