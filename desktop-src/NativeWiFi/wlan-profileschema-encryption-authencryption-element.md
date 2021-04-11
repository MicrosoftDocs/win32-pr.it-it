---
description: Specifica il tipo di crittografia dei dati da utilizzare per la connessione a una LAN wireless.
ms.assetid: 0ba24106-bd6f-465a-af80-ce85501756b9
title: Elemento Encryption (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- encryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 7efd9e0865cb489a7d033772112b0aaeb8a8fb23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129730"
---
# <a name="encryption-authencryption-element"></a>Elemento Encryption (authEncryption)

L'elemento Encryption (authEncryption) specifica il tipo di crittografia dei dati da utilizzare per la connessione a una LAN wireless.

``` syntax
<xs:element name="encryption">
    <xs:simpleType>
        <xs:restriction
            base="string"
        >
            <xs:enumeration
                value="none"
             />
            <xs:enumeration
                value="WEP"
             />
            <xs:enumeration
                value="TKIP"
             />
            <xs:enumeration
                value="AES"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .

## <a name="remarks"></a>Commenti

Quando l'elemento di **crittografia** ha un valore WEP, il [**tipo**](wlan-profileschema-keytype-sharedkey-element.md) di elemento deve essere impostato su **networkKey**.

Il metodo di crittografia AES è come specificato nelle specifiche [802.1 x](https://ieeexplore.ieee.org/document/1438730) e [802.11 i](https://standards.ieee.org/findstds/standard/802.11i-2004.html) .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **Encryption** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**authEncryption**](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**authEncryption (sicurezza)**](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 




