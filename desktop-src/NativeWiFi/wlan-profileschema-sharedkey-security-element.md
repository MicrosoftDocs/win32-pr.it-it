---
description: Contiene informazioni sulla chiave condivisa.
ms.assetid: 9f401441-256c-4702-9503-f87b2b9cf0ee
title: Elemento sharedKey (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sharedKey
api_type:
- Schema
api_location: ''
ms.openlocfilehash: bfd138044e4849e5b0a42ab396561331bea9a338
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313322"
---
# <a name="sharedkey-security-element"></a>Elemento sharedKey (Security)

L'elemento sharedKey (Security) contiene informazioni sulla chiave condivisa. Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.

``` syntax
<xs:element name="sharedKey"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="protected"
                type="boolean"
             />
            <xs:element name="keyMaterial"
                type="string"
             />
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

L'elemento è definito dall'elemento di [**sicurezza**](wlan-profileschema-security-msm-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                 | Tipo                                                              | Descrizione                                                                                                                                                                  |
|-------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md) | [string](/dotnet/api/system.string)   | Contiene la chiave di rete o la passphrase.<br/>                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)         |                                                                   | Tipo di chiave.<br/>                                                                                                                                                      |
| [**protetto**](wlan-profileschema-protected-sharedkey-element.md)     | [boolean](/dotnet/api/system.boolean) | Indica se la chiave è crittografata.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere FALSE.<br/> |



## <a name="remarks"></a>Commenti

Per Windows Vista e Windows Server 2008, i dati associati all'elemento **sharedKey** vengono crittografati prima di essere salvati nell'archivio profili.

Per Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2, i dati non vengono crittografati.

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **sharedKey** , vedere esempio di [profilo non broadcast](non-broadcast-profile-sample.md), esempio di profilo [WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).

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

[**sicurezza**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
