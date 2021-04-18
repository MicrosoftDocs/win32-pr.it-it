---
description: Indica se la chiave condivisa sarà una chiave di rete o una passphrase.
ms.assetid: 2cc909bb-7de6-492b-81ca-ddde93c17f63
title: Elemento Type (sharedKey)
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
ms.openlocfilehash: 134f9da4100c9479255507d4686dd19d3d484dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106312843"
---
# <a name="keytype-sharedkey-element"></a>Elemento Type (sharedKey)

L'elemento Key Type (sharedKey) indica se la chiave condivisa sarà una chiave di rete o una passphrase.

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

L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .

## <a name="remarks"></a>Commenti

Quando l'elemento di [**crittografia**](wlan-profileschema-encryption-authencryption-element.md) ha un valore WEP, il **tipo** di elemento deve essere impostato su **networkKey**.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento di **tipo** , vedere esempio di [profilo non broadcast](non-broadcast-profile-sample.md), esempio di profilo [WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
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

 

 




