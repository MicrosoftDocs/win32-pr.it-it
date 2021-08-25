---
description: Contiene varie impostazioni di sicurezza.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Elemento security (MSM) (LAN_policy) (WLAN)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c885f330538177cddca40c47cf6a5ad910030c6c5f4c3429ca7bd92c3b437b20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912692"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a>Elemento Security (MSM) (LAN_policy) per WLAN

L'elemento security (MSM) contiene varie impostazioni di sicurezza.

``` syntax
<xs:element name="security"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
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
            <xs:element name="keyIndex"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="0"
                         />
                        <xs:maxInclusive
                            value="3"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="disabled"
                         />
                        <xs:enumeration
                            value="enabled"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheTTL"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="5"
                         />
                        <xs:maxInclusive
                            value="1400"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="PMKCacheSize"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="1"
                         />
                        <xs:maxInclusive
                            value="255"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="preAuthMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="disabled"
                         />
                        <xs:enumeration
                            value="enabled"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="preAuthThrottle"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:minInclusive
                            value="1"
                         />
                        <xs:maxInclusive
                            value="16"
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

L'elemento è definito [**dall'elemento MSM.**](wlan-profileschema-msm-wlanprofile-element.md)

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Specifica la coppia di autenticazione e crittografia da usare per questo profilo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Specifica la coppia di autenticazione e crittografia da usare per questo profilo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**Crittografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Imposta la crittografia dei dati da utilizzare per la connessione alla rete LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Specifica l'indice delle chiavi da usare per crittografare il traffico wireless. Viene usato solo quando keyType è impostato su networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la chiave di rete o la passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo di chiave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se verrà usata la memorizzazione nella cache PMK. Questo elemento è valido solo per le reti definite da WPA2.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Specifica il numero di voci nella cache OMK nel client. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, le dimensioni della cache vengono predefinite su 128 voci.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica il periodo di tempo, in minuti, per cui verrà mantenuta una cache PMK. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su enabled.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se la pre-autenticazione verrà usata dal client. La pre-autenticazione abilita il roaming rapido sicuro WPA2. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, il valore predefinito è disabilitato.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica il numero di tentativi durante l'autenticazione preliminare agli asp adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, il numero di tentativi è 3.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                      |
| [**protetto**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica se la chiave è crittografata.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento deve avere valore **FALSE.**<br/>                                                                                                                                                                                                                                             |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene le informazioni sulla chiave condivisa. Questo elemento è obbligatorio solo se le chiavi WEP o PSK sono necessarie per la coppia di autenticazione e crittografia.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica se viene usato 802.1X. Questo flag è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

[**L'elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption.**](wlan-profileschema-authencryption-security-element.md) [**L'elemento OneX**](onexschema-onex-element.md) può essere inserito come figlio dell'elemento **security (MSM).**

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano **l'elemento di** sicurezza, vedere Esempi di [profili wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> <dt>

**Contesto di definizione dell'elemento nello schema**
</dt> <dt>

[**MSM**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**MSM (WLANProfile)**](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
