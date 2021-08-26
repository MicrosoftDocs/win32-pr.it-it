---
description: Contiene un profilo LAN wireless.
ms.assetid: bc97cb49-3891-4a4a-aab4-895cd9ce6908
title: Elemento WLANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f7dae0d600553411a5a0a9287ab78d052a9ab9a0aa3c94220638adaf78dc5f11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912473"
---
# <a name="wlanprofile-element"></a>Elemento WLANProfile

**L'elemento WLANProfile** contiene un profilo LAN wireless. Questo elemento è l'elemento radice univoco per un profilo wireless.

Lo spazio dei nomi di destinazione per l'elemento WLANProfile è `https://www.microsoft.com/networking/WLAN/profile/v1` .

``` syntax
<xs:element name="WLANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="SSIDConfig"
                maxOccurs="256"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="SSID"
                            maxOccurs="256"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="hex"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="hexBinary"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
                                                 />
                                            </xs:restriction>
                                        </xs:simpleType>
                                    </xs:element>
                                    <xs:element name="name"
                                        minOccurs="0"
                                    >
                                        <xs:simpleType>
                                            <xs:restriction
                                                base="string"
                                            >
                                                <xs:minLength
                                                    value="1"
                                                 />
                                                <xs:maxLength
                                                    value="32"
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
                        <xs:element name="nonBroadcast"
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
            <xs:element name="connectionType">
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="IBSS"
                         />
                        <xs:enumeration
                            value="ESS"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="connectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="manual"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="autoSwitch"
                type="boolean"
                minOccurs="0"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
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
            <xs:element name="IHV"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
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
                        <xs:element name="connectivity"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:any
                                        processContents="lax"
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
                                    <xs:any
                                        processContents="lax"
                                        namespace="##other"
                                     />
                                </xs:sequence>
                            </xs:complexType>
                        </xs:element>
                        <xs:element name="useMSOneX"
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

## <a name="child-elements"></a>Elementi figlio



| Elemento                                                                            | Tipo                                                              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**authEncryption**](wlan-profileschema-authencryption-security-element.md)       |                                                                   | Specifica la coppia di autenticazione e crittografia da usare per questo profilo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Specifica il metodo di autenticazione da utilizzare per connettersi alla rete LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**AutoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [boolean](/dotnet/api/system.boolean) | Determina il comportamento di roaming di una rete connessa automaticamente quando è disponibile una rete più preferita. Questo elemento è facoltativo e non ha alcun effetto su una rete connessa manualmente.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Indica se la connessione alla lan wireless deve essere automatica ("auto") o avviata ("manuale") dall'utente. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Connectiontype**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Indica se la rete è infrastruttura ("ESS") o ad hoc ("IBSS").<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Connettività**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contiene varie impostazioni di connettività. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**Connettività**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Contiene le impostazioni di connettività correlate a IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**Crittografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Imposta la crittografia dei dati da utilizzare per la connessione alla rete LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**hex**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Contiene l'SSID di una lan wireless in formato esadecimale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**Ihv**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Contiene le impostazioni IHV (Independent Hardware Vendor) facoltative.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Specifica l'indice delle chiavi da usare per crittografare il traffico wireless. Viene usato solo quando [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) è impostato su "networkKey".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la chiave di rete o la passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo di chiave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**MSM**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Contiene varie impostazioni MSM. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**Nome**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nameType**](wlan-profileschema-nametype-simpletype.md)        | Nome del profilo WLAN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**Nome**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Contiene l'SSID di una rete LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [boolean](/dotnet/api/system.boolean) | Indica se la rete trasmette il relativo SSID.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**Oui**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Contiene un valore hexBinary a 3 byte che identifica l'IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifica l'IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Specifica lo standard LAN wireless 802.11 usato nella lan wireless. Il valore "n" è supportato solo in Windows Vista con SP1 e versioni successive del sistema operativo.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se verrà usata la memorizzazione nella cache PMK. Questo elemento è valido solo per le reti definite da WPA2.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Specifica il numero di voci nella cache PMK nel client. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "enabled". Se **PMKCacheMode è** abilitato e questo elemento è assente, le dimensioni della cache vengono predefinite su 128 voci.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica il periodo di tempo, in minuti, per cui verrà mantenuta una cache PMK. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "enabled".<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se la pre-autenticazione verrà usata dal client. La pre-autenticazione abilita il roaming rapido sicuro WPA2. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "enabled". Se **PMKCacheMode è** abilitato e questo elemento è assente, il valore predefinito è disabilitato.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica il numero di tentativi durante l'autenticazione preliminare agli asp adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "enabled". Se **PMKCacheMode è** abilitato e questo elemento è assente, il numero di tentativi viene impostato su 3.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protetto**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica se la chiave è crittografata.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento deve avere valore **FALSE.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**Sicurezza**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contiene varie impostazioni di sicurezza. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**Sicurezza**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Contiene le impostazioni di sicurezza specifiche di IHV. Le impostazioni di sicurezza Microsoft e le impostazioni di sicurezza IHV si escludono a vicenda. Se entrambi i set di impostazioni di sicurezza sono presenti nello stesso profilo, il profilo non è valido.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene le informazioni sulla chiave condivisa. Questo elemento è obbligatorio solo se le chiavi WEP o PSK sono necessarie per la coppia di autenticazione e crittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**Ssid**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Specifica l'SSID di una rete LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Contiene uno o più SSID insieme ad altre impostazioni comuni. <br/> Un profilo può avere più [**elementi SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) e ogni [**elemento SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) può avere più [**elementi SSID.**](wlan-profileschema-ssid-ssidconfig-element.md) Tuttavia, Windows solo il primo [**elemento SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) in un [**elemento WLANProfile.**](wlan-profileschema-wlanprofile-element.md)<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Al massimo un [**elemento SSID**](wlan-profileschema-ssid-ssidconfig-element.md) può essere visualizzato in un profilo.<br/> |
| [**digitare**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Contiene un valore **hexBinary** di 1 byte usato per distinguere le schede di interfaccia di rete in base allo stesso IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [boolean](/dotnet/api/system.boolean) | Specifica l'origine delle impostazioni di sicurezza 802.1X usate da un componente di sicurezza IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza IHV usano le impostazioni 802.1X definite da Microsoft. Quando **useMSOneX** è false, i componenti di sicurezza IHV usano le impostazioni 802.1X fornite dal fornitore. Per impostazione predefinita, **useMSOneX** è false. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica se viene usato 802.1X. Questo flag è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

La maggior parte degli elementi figlio dell'elemento WLANProfile è nello spazio `https://www.microsoft.com/networking/WLAN/profile/v1` dei nomi . Esistono due eccezioni: [**l'elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) si trova nello spazio dei nomi `https://www.microsoft.com/networking/WLAN/profile/v2` e [**l'elemento OneX**](onexschema-onex-element.md) si trova nello spazio `https://www.microsoft.com/networking/OneX/v1` dei nomi .

[**L'elemento FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption.**](wlan-profileschema-authencryption-security-element.md) [**L'elemento OneX**](onexschema-onex-element.md) può essere inserito come figlio dell'elemento [**security (MSM).**](wlan-profileschema-security-msm-element.md)

Per visualizzare l'elenco degli elementi figlio in una struttura ad albero, vedere [Elementi dello schema del profilo \_ WLAN](wlan-profileschema-elements.md).

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio, vedere [Esempi di profili wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/> |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 
