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
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="37b1a-103">Elemento Hotspot2 (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="37b1a-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="37b1a-104">Estende lo schema V1 del profilo WLAN per supportare le reti hotspot 2,0.</span><span class="sxs-lookup"><span data-stu-id="37b1a-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="37b1a-105">Hotspot 2,0 consente la connessione automatica ai servizi Wi-Fi pubblici usando le credenziali esistenti e l'appartenenza alle reti del provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="37b1a-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="37b1a-106">I provider di servizi specificano il modo in cui vengono stabilite le connessioni usando i nuovi elementi dello schema per descrivere le reti da usare e come eseguire l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="37b1a-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

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

<span data-ttu-id="37b1a-107">L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="37b1a-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="37b1a-108">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="37b1a-108">Child elements</span></span>

| <span data-ttu-id="37b1a-109">Elemento</span><span class="sxs-lookup"><span data-stu-id="37b1a-109">Element</span></span> | <span data-ttu-id="37b1a-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="37b1a-110">Type</span></span> | <span data-ttu-id="37b1a-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="37b1a-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="37b1a-112">**NomeDominio**</span><span class="sxs-lookup"><span data-stu-id="37b1a-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="37b1a-113">Nome di dominio del provider di rete domestica del dispositivo, che identifica l'operatore della rete.</span><span class="sxs-lookup"><span data-stu-id="37b1a-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="37b1a-114">**NAIRealm**</span><span class="sxs-lookup"><span data-stu-id="37b1a-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="37b1a-115">Un elenco di identificatori di area di autenticazione NAI (Network Access Identifier).</span><span class="sxs-lookup"><span data-stu-id="37b1a-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="37b1a-116">Le voci in questo elenco sono in genere nel formato user@domain .</span><span class="sxs-lookup"><span data-stu-id="37b1a-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="37b1a-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="37b1a-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="37b1a-118">Elenco di ID PLMN (Public Land Mobile Network).</span><span class="sxs-lookup"><span data-stu-id="37b1a-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="37b1a-119">**RoamingConsortium**</span><span class="sxs-lookup"><span data-stu-id="37b1a-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="37b1a-120">Elenco di identificatori univoci dell'organizzazione (OUI) assegnati da IEEE.</span><span class="sxs-lookup"><span data-stu-id="37b1a-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="37b1a-121">Esempi</span><span class="sxs-lookup"><span data-stu-id="37b1a-121">Examples</span></span>

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
