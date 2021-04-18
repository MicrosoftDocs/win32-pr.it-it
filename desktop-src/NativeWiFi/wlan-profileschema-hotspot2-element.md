---
description: Estende lo schema V1 del profilo WLAN per supportare le reti hotspot 2,0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Elemento Hotspot2 (WLANProfile)
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307823"
---
# <a name="hotspot2-wlanprofile-element"></a>Elemento Hotspot2 (WLANProfile)

Estende lo schema V1 del profilo WLAN per supportare le reti hotspot 2,0. Hotspot 2,0 consente la connessione automatica ai servizi Wi-Fi pubblici usando le credenziali esistenti e l'appartenenza alle reti del provider di servizi. I provider di servizi specificano il modo in cui vengono stabilite le connessioni usando i nuovi elementi dello schema per descrivere le reti da usare e come eseguire l'autenticazione.

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .

## <a name="child-elements"></a>Elementi figlio

| Elemento | Tipo | Descrizione |
|-|-|-|
| [**NomeDominio**](wlan-profileschema-hotspot2-domainname-element.md) | | Nome di dominio del provider di rete domestica del dispositivo, che identifica l'operatore della rete. |
| [**NAIRealm**](wlan-profileschema-hotspot2-nairealm-element.md) | | Un elenco di identificatori di area di autenticazione NAI (Network Access Identifier). Le voci in questo elenco sono in genere nel formato user@domain . |
| [**Network3GPP**](wlan-profileschema-hotspot2-network3gpp-element.md) | | Elenco di ID PLMN (Public Land Mobile Network). |
| [**RoamingConsortium**](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | Elenco di identificatori univoci dell'organizzazione (OUI) assegnati da IEEE.  |

## <a name="examples"></a>Esempi

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
