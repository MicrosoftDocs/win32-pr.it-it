---
description: Contiene diverse impostazioni del modulo CSM (media Specific Module).
ms.assetid: 31f98af8-a577-4f6a-9a0a-b182b5a89cc3
title: Elemento MSM (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSM
api_type:
- Schema
api_location: ''
ms.openlocfilehash: b2e1ffdc5ad27524d3d2fc5b37b3a060a90c7575
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315892"
---
# <a name="msm-wlanprofile-element"></a>Elemento MSM (WLANProfile)

L'elemento MSM (WLANProfile) contiene diverse impostazioni del modulo CSM (media Specific Module).

``` syntax
<xs:element name="MSM"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="phyType"
                            minOccurs="0"
                            maxOccurs="4"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="a"
                                     />
                                    <xs:enumeration
                                        value="b"
                                     />
                                    <xs:enumeration
                                        value="g"
                                     />
                                    <xs:enumeration
                                        value="n"
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

L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Specifica la coppia di autenticazione e crittografia da usare per questo profilo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Specifica la coppia di autenticazione e crittografia da usare per questo profilo.<br/>                                                                                                                                                                                                                                                                                                                                     |
| [**connettività**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contiene diverse impostazioni di connettività. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                 |
| [**crittografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Specifica l'indice della chiave che deve essere utilizzato per crittografare il traffico wireless. Viene usato solo quando il tipo di operazione è impostato su networkKey.<br/>                                                                                                                                                                                                                                                                                          |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la chiave di rete o la passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo di chiave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Specifica lo standard LAN wireless 802,11 usato sulla LAN wireless. Il valore "n" è supportato solo in Windows Vista con SP1 e versioni successive del sistema operativo.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                        |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se verrà utilizzata la memorizzazione nella cache PMK. Questo elemento è valido solo per le reti definite da WPA2.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                 |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Specifica il numero di voci nella cache OMK nel client. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                   |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                  |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se la pre-autenticazione verrà utilizzata dal client. La pre-autenticazione Abilita il roaming veloce sicuro WPA2. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, il valore predefinito è Disabled.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/> |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica il numero di tentativi quando si esegue la preautenticazione ai punti di APs adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled. Se la modalità PMKCache è abilitata e questo elemento è assente, il numero di tentativi predefinito è 3.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                      |
| [**protetto**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica se la chiave è crittografata.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere FALSE.<br/>                                                                                                                                                                                                                                                 |
| [**sicurezza**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contiene diverse impostazioni di sicurezza. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                     |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene le informazioni sulla chiave condivisa. Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.<br/>                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica se viene utilizzato 802.1 X. Questo flag è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a>Commenti

L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . L'elemento [**Onex**](onexschema-onex-element.md) può essere inserito come elemento figlio dell'elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio che usano l'elemento **MSM** , vedere esempi di profili [wireless](wireless-profile-samples.md).

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

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

**Possibile elemento padre immediato nell'istanza dello schema**
</dt> <dt>

[**WLANProfile**](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
