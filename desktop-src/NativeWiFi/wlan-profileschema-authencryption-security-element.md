---
description: Specifica la coppia di autenticazione e crittografia da usare per questo profilo.
ms.assetid: d7a69b82-3f04-49eb-80cc-675d5a0a559a
title: Elemento authEncryption (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authEncryption
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 03d132bf75a68154f7e2b7d2408b2be7564c7a67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308890"
---
# <a name="authencryption-security-element"></a>Elemento authEncryption (Security)

L'elemento authEncryption (Security) specifica la coppia di autenticazione e crittografia da usare per questo profilo.

``` syntax
<xs:element name="authEncryption">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="authentication">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="open"
                         />
                        <xs:enumeration
                            value="shared"
                         />
                        <xs:enumeration
                            value="WPA"
                         />
                        <xs:enumeration
                            value="WPAPSK"
                         />
                        <xs:enumeration
                            value="WPA2"
                         />
                        <xs:enumeration
                            value="WPA2PSK"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
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
            <xs:element name="useOneX"
                type="boolean"
                minOccurs="0"
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



| Elemento                                                                            | Tipo                                                              | Descrizione                                                                                      |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.<br/> |
| [**crittografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.<br/>                       |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica se viene utilizzato 802.1 X.<br/>                                                     |



## <a name="remarks"></a>Commenti

L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento **authEncryption** .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **authEncryption** , vedere esempi di profili [wireless](wireless-profile-samples.md). Per visualizzare un profilo di esempio che usa l'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) , vedere [esempio di profilo FIPS](fips-profile-sample.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**sicurezza**](wlan-profileschema-security-msm-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**sicurezza (MSM)**](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 
