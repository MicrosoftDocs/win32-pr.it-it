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
ms.openlocfilehash: 227d912128bf3f656fca7aecbaf0fe0640659465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885278"
---
# <a name="wlanprofile-element"></a>Elemento WLANProfile

L'elemento **WLANProfile** contiene un profilo LAN wireless. Questo elemento è l'elemento radice univoco per un profilo wireless.

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
| [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**autoSwitch**](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [boolean](/dotnet/api/system.boolean) | Determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo. Questo elemento è facoltativo e non ha alcun effetto su una rete connessa manualmente.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**connectionMode**](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | Indica se la connessione alla LAN wireless deve essere automatica ("automatica") o avviata ("manuale") dall'utente. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | Indica se la rete è un'infrastruttura ("ESS") o ad hoc ("IBSS").<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**connettività**](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | Contiene diverse impostazioni di connettività. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**connettività**](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | Contiene le impostazioni di connettività correlate a IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [**crittografia**](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [**hex**](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | Contiene l'SSID di una LAN wireless in formato esadecimale.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | Contiene le impostazioni opzionali del fornitore dell'hardware indipendente (IHV).<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**keyIndex**](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | Specifica l'indice della chiave da usare per crittografare il traffico wireless. Viene usato solo quando il [**tipo**](wlan-profileschema-keytype-sharedkey-element.md) di argomento è impostato su "networkKey".<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**keyMaterial**](wlan-profileschema-keymaterial-sharedkey-element.md)            | [string](/dotnet/api/system.string)   | Contiene la chiave di rete o la passphrase.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [**keyType**](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | Tipo di chiave.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**MSM**](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | Contiene varie impostazioni CSM. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [**nome**](wlan-profileschema-name-wlanprofile-element.md)                        | [**nameType**](wlan-profileschema-nametype-simpletype.md)        | Nome del profilo WLAN.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [**nome**](wlan-profileschema-name-ssid-element.md)                               |                                                                   | Contiene l'SSID di una LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**nonBroadcast**](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [boolean](/dotnet/api/system.boolean) | Indica se la rete trasmette il relativo SSID.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**OUI**](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | Contiene un hexBinary di 3 byte che identifica IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**OUIHeader**](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | Identifica IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**phyType**](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | Specifica lo standard LAN wireless 802,11 usato sulla LAN wireless. Il valore "n" è supportato solo in Windows Vista con SP1 e versioni successive del sistema operativo.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | Indica se verrà utilizzata la memorizzazione nella cache PMK. Questo elemento è valido solo per le reti definite da WPA2.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**PMKCacheSize**](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | Specifica il numero di voci nella cache PMK nel client. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled". Se **PMKCacheMode** è abilitato e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                           |
| [**PMKCacheTTL**](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**preAuthMode**](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | Determina se la pre-autenticazione verrà utilizzata dal client. La pre-autenticazione Abilita il roaming veloce sicuro WPA2. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled". Se **PMKCacheMode** è abilitato e questo elemento è assente, il valore predefinito è Disabled.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                         |
| [**preAuthThrottle**](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | Indica il numero di tentativi quando si esegue la preautenticazione ai punti di APs adiacenti. Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled". Se **PMKCacheMode** è abilitato e questo elemento è assente, il numero di tentativi predefinito è 3.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                              |
| [**protetto**](wlan-profileschema-protected-sharedkey-element.md)                | [boolean](/dotnet/api/system.boolean) | Indica se la chiave è crittografata.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere **false**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**sicurezza**](wlan-profileschema-security-msm-element.md)                        |                                                                   | Contiene diverse impostazioni di sicurezza. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**sicurezza**](wlan-profileschema-security-ihv-element.md)                        |                                                                   | Contiene le impostazioni di sicurezza specifiche di IHV. Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda. Se entrambi i set di impostazioni di sicurezza sono presenti nello stesso profilo, il profilo non è valido.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [**sharedKey**](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | Contiene le informazioni sulla chiave condivisa. Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | Specifica il valore SSID di una LAN wireless.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | Contiene uno o più SSID insieme ad altre impostazioni comuni. <br/> Un profilo può avere più elementi [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) e ogni elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) può avere più elementi [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) . Tuttavia, Windows considera sempre il primo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) in un elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .<br/> |
| [**tipo**](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | Contiene un **hexBinary** di 1 byte usato per distinguere le schede di rete con lo stesso IHV.<br/> **Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md)                      | [boolean](/dotnet/api/system.boolean) | Specifica l'origine delle impostazioni di sicurezza 802.1 X utilizzate da un componente di sicurezza IHV. Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x definite da Microsoft. Quando **useMSOneX** è false, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x fornite dal fornitore. Per impostazione predefinita, **useMSOneX** è false. Questo elemento è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [**useOneX**](wlan-profileschema-useonex-authencryption-element.md)               | [boolean](/dotnet/api/system.boolean) | Indica se viene utilizzato 802.1 X. Questo flag è facoltativo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a>Commenti

La maggior parte degli elementi figlio dell'elemento WLANProfile si trova nello `https://www.microsoft.com/networking/WLAN/profile/v1` spazio dei nomi. Ci sono due eccezioni: l'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) si trova nello `https://www.microsoft.com/networking/WLAN/profile/v2` spazio dei nomi e l'elemento [**Onex**](onexschema-onex-element.md) è nello `https://www.microsoft.com/networking/OneX/v1` spazio dei nomi.

L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) . L'elemento [**Onex**](onexschema-onex-element.md) può essere inserito come elemento figlio dell'elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .

Per visualizzare l'elenco di elementi figlio in una struttura ad albero, vedere [ \_ elementi dello schema del profilo WLAN](wlan-profileschema-elements.md).

## <a name="examples"></a>Esempio

Per visualizzare i profili di esempio, vedere esempi di profili [wireless](wireless-profile-samples.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/> |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                 |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di profili wireless](wireless-profile-samples.md)
</dt> </dl>

 

 
