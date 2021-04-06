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
# <a name="wlanprofile-element"></a><span data-ttu-id="f1180-103">Elemento WLANProfile</span><span class="sxs-lookup"><span data-stu-id="f1180-103">WLANProfile Element</span></span>

<span data-ttu-id="f1180-104">L'elemento **WLANProfile** contiene un profilo LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-104">The **WLANProfile** element contains a wireless LAN profile.</span></span> <span data-ttu-id="f1180-105">Questo elemento è l'elemento radice univoco per un profilo wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-105">This element is the unique root element for a wireless profile.</span></span>

<span data-ttu-id="f1180-106">Lo spazio dei nomi di destinazione per l'elemento WLANProfile è `https://www.microsoft.com/networking/WLAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="f1180-106">The target namespace for the WLANProfile element is `https://www.microsoft.com/networking/WLAN/profile/v1`.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="f1180-107">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f1180-107">Child elements</span></span>



| <span data-ttu-id="f1180-108">Elemento</span><span class="sxs-lookup"><span data-stu-id="f1180-108">Element</span></span>                                                                            | <span data-ttu-id="f1180-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="f1180-109">Type</span></span>                                                              | <span data-ttu-id="f1180-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f1180-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1180-111">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="f1180-111">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="f1180-112">Specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="f1180-112">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f1180-113">**autenticazione**</span><span class="sxs-lookup"><span data-stu-id="f1180-113">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="f1180-114">Specifica il metodo di autenticazione da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-114">Specifies the authentication method to be used to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f1180-115">**autoSwitch**</span><span class="sxs-lookup"><span data-stu-id="f1180-115">**autoSwitch**</span></span>](wlan-profileschema-autoswitch-wlanprofile-element.md)            | [<span data-ttu-id="f1180-116">boolean</span><span class="sxs-lookup"><span data-stu-id="f1180-116">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f1180-117">Determina il comportamento di roaming di una rete connessa automaticamente quando una rete più preferita è compresa nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="f1180-117">Determines the roaming behavior of an auto-connected network when a more preferred network is in range.</span></span> <span data-ttu-id="f1180-118">Questo elemento è facoltativo e non ha alcun effetto su una rete connessa manualmente.</span><span class="sxs-lookup"><span data-stu-id="f1180-118">This element is optional and has no effect on a manually connected network.</span></span><br/> <span data-ttu-id="f1180-119">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-119">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f1180-120">**connectionMode**</span><span class="sxs-lookup"><span data-stu-id="f1180-120">**connectionMode**</span></span>](wlan-profileschema-connectionmode-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="f1180-121">Indica se la connessione alla LAN wireless deve essere automatica ("automatica") o avviata ("manuale") dall'utente.</span><span class="sxs-lookup"><span data-stu-id="f1180-121">Indicates whether connection to the wireless LAN should be automatic ("auto") or initiated ("manual") by user.</span></span> <span data-ttu-id="f1180-122">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-122">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="f1180-123">**connectionType**</span><span class="sxs-lookup"><span data-stu-id="f1180-123">**connectionType**</span></span>](wlan-profileschema-connectiontype-wlanprofile-element.md)    |                                                                   | <span data-ttu-id="f1180-124">Indica se la rete è un'infrastruttura ("ESS") o ad hoc ("IBSS").</span><span class="sxs-lookup"><span data-stu-id="f1180-124">Indicates whether the network is infrastructure ("ESS") or ad-hoc ("IBSS").</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f1180-125">**connettività**</span><span class="sxs-lookup"><span data-stu-id="f1180-125">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="f1180-126">Contiene diverse impostazioni di connettività.</span><span class="sxs-lookup"><span data-stu-id="f1180-126">Contains various connectivity settings.</span></span> <span data-ttu-id="f1180-127">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-127">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f1180-128">**connettività**</span><span class="sxs-lookup"><span data-stu-id="f1180-128">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md)                |                                                                   | <span data-ttu-id="f1180-129">Contiene le impostazioni di connettività correlate a IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-129">Contains IHV-related connectivity settings.</span></span><br/> <span data-ttu-id="f1180-130">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="f1180-131">**crittografia**</span><span class="sxs-lookup"><span data-stu-id="f1180-131">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="f1180-132">Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-132">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f1180-133">**hex**</span><span class="sxs-lookup"><span data-stu-id="f1180-133">**hex**</span></span>](wlan-profileschema-hex-ssid-element.md)                                 |                                                                   | <span data-ttu-id="f1180-134">Contiene l'SSID di una LAN wireless in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="f1180-134">Contains the SSID of a wireless LAN in hexadecimal format.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f1180-135">**IHV**</span><span class="sxs-lookup"><span data-stu-id="f1180-135">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="f1180-136">Contiene le impostazioni opzionali del fornitore dell'hardware indipendente (IHV).</span><span class="sxs-lookup"><span data-stu-id="f1180-136">Contains optional independent hardware vendor (IHV) settings.</span></span><br/> <span data-ttu-id="f1180-137">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-137">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f1180-138">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="f1180-138">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="f1180-139">Specifica l'indice della chiave da usare per crittografare il traffico wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-139">Specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="f1180-140">Viene usato solo quando il [**tipo**](wlan-profileschema-keytype-sharedkey-element.md) di argomento è impostato su "networkKey".</span><span class="sxs-lookup"><span data-stu-id="f1180-140">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f1180-141">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="f1180-141">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="f1180-142">string</span><span class="sxs-lookup"><span data-stu-id="f1180-142">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="f1180-143">Contiene la chiave di rete o la passphrase.</span><span class="sxs-lookup"><span data-stu-id="f1180-143">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f1180-144">**keyType**</span><span class="sxs-lookup"><span data-stu-id="f1180-144">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="f1180-145">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="f1180-145">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f1180-146">**MSM**</span><span class="sxs-lookup"><span data-stu-id="f1180-146">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)                          |                                                                   | <span data-ttu-id="f1180-147">Contiene varie impostazioni CSM.</span><span class="sxs-lookup"><span data-stu-id="f1180-147">Contains various MSM settings.</span></span> <span data-ttu-id="f1180-148">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-148">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="f1180-149">**nome**</span><span class="sxs-lookup"><span data-stu-id="f1180-149">**name**</span></span>](wlan-profileschema-name-wlanprofile-element.md)                        | [<span data-ttu-id="f1180-150">**nameType**</span><span class="sxs-lookup"><span data-stu-id="f1180-150">**nameType**</span></span>](wlan-profileschema-nametype-simpletype.md)        | <span data-ttu-id="f1180-151">Nome del profilo WLAN.</span><span class="sxs-lookup"><span data-stu-id="f1180-151">Name of the WLAN profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="f1180-152">**nome**</span><span class="sxs-lookup"><span data-stu-id="f1180-152">**name**</span></span>](wlan-profileschema-name-ssid-element.md)                               |                                                                   | <span data-ttu-id="f1180-153">Contiene l'SSID di una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-153">Contains the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f1180-154">**nonBroadcast**</span><span class="sxs-lookup"><span data-stu-id="f1180-154">**nonBroadcast**</span></span>](wlan-profileschema-nonbroadcast-ssidconfig-element.md)         | [<span data-ttu-id="f1180-155">boolean</span><span class="sxs-lookup"><span data-stu-id="f1180-155">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f1180-156">Indica se la rete trasmette il relativo SSID.</span><span class="sxs-lookup"><span data-stu-id="f1180-156">Indicates whether the network broadcasts its SSID.</span></span><br/> <span data-ttu-id="f1180-157">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-157">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="f1180-158">**OUI**</span><span class="sxs-lookup"><span data-stu-id="f1180-158">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)                            |                                                                   | <span data-ttu-id="f1180-159">Contiene un hexBinary di 3 byte che identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-159">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/> <span data-ttu-id="f1180-160">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-160">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f1180-161">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="f1180-161">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)                      |                                                                   | <span data-ttu-id="f1180-162">Identifica IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-162">Identifies the IHV.</span></span><br/> <span data-ttu-id="f1180-163">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-163">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f1180-164">**phyType**</span><span class="sxs-lookup"><span data-stu-id="f1180-164">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="f1180-165">Specifica lo standard LAN wireless 802,11 usato sulla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-165">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="f1180-166">Il valore "n" è supportato solo in Windows Vista con SP1 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-166">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="f1180-167">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-167">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="f1180-168">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="f1180-168">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="f1180-169">Indica se verrà utilizzata la memorizzazione nella cache PMK.</span><span class="sxs-lookup"><span data-stu-id="f1180-169">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="f1180-170">Questo elemento è valido solo per le reti definite da WPA2.</span><span class="sxs-lookup"><span data-stu-id="f1180-170">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="f1180-171">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-171">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f1180-172">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="f1180-172">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="f1180-173">Specifica il numero di voci nella cache PMK nel client.</span><span class="sxs-lookup"><span data-stu-id="f1180-173">Specifies the number of entries in the PMK cache on the client.</span></span> <span data-ttu-id="f1180-174">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f1180-174">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f1180-175">Se **PMKCacheMode** è abilitato e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.</span><span class="sxs-lookup"><span data-stu-id="f1180-175">If **PMKCacheMode** is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="f1180-176">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-176">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f1180-177">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="f1180-177">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="f1180-178">Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK.</span><span class="sxs-lookup"><span data-stu-id="f1180-178">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="f1180-179">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f1180-179">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span><br/> <span data-ttu-id="f1180-180">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-180">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f1180-181">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="f1180-181">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="f1180-182">Determina se la pre-autenticazione verrà utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="f1180-182">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="f1180-183">La pre-autenticazione Abilita il roaming veloce sicuro WPA2.</span><span class="sxs-lookup"><span data-stu-id="f1180-183">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="f1180-184">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f1180-184">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f1180-185">Se **PMKCacheMode** è abilitato e questo elemento è assente, il valore predefinito è Disabled.</span><span class="sxs-lookup"><span data-stu-id="f1180-185">If **PMKCacheMode** is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="f1180-186">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-186">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f1180-187">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="f1180-187">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="f1180-188">Indica il numero di tentativi quando si esegue la preautenticazione ai punti di APs adiacenti.</span><span class="sxs-lookup"><span data-stu-id="f1180-188">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="f1180-189">Questo elemento è valido solo per le reti definite da WPA2 con [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) impostato su "Enabled".</span><span class="sxs-lookup"><span data-stu-id="f1180-189">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="f1180-190">Se **PMKCacheMode** è abilitato e questo elemento è assente, il numero di tentativi predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="f1180-190">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="f1180-191">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-191">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="f1180-192">**protetto**</span><span class="sxs-lookup"><span data-stu-id="f1180-192">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="f1180-193">boolean</span><span class="sxs-lookup"><span data-stu-id="f1180-193">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f1180-194">Indica se la chiave è crittografata.</span><span class="sxs-lookup"><span data-stu-id="f1180-194">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="f1180-195">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="f1180-195">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f1180-196">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="f1180-196">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="f1180-197">Contiene diverse impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f1180-197">Contains various security settings.</span></span> <span data-ttu-id="f1180-198">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-198">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f1180-199">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="f1180-199">**security**</span></span>](wlan-profileschema-security-ihv-element.md)                        |                                                                   | <span data-ttu-id="f1180-200">Contiene le impostazioni di sicurezza specifiche di IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-200">Contains IHV-specific security settings.</span></span> <span data-ttu-id="f1180-201">Le impostazioni di sicurezza di Microsoft e le impostazioni di sicurezza di IHV si escludono a vicenda.</span><span class="sxs-lookup"><span data-stu-id="f1180-201">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="f1180-202">Se entrambi i set di impostazioni di sicurezza sono presenti nello stesso profilo, il profilo non è valido.</span><span class="sxs-lookup"><span data-stu-id="f1180-202">If both sets of security settings are present in the same profile, the profile is invalid.</span></span><br/> <span data-ttu-id="f1180-203">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-203">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="f1180-204">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="f1180-204">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="f1180-205">Contiene le informazioni sulla chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="f1180-205">Contains the shared key information.</span></span> <span data-ttu-id="f1180-206">Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.</span><span class="sxs-lookup"><span data-stu-id="f1180-206">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="f1180-207">**SSID**</span><span class="sxs-lookup"><span data-stu-id="f1180-207">**SSID**</span></span>](wlan-profileschema-ssid-ssidconfig-element.md)                         |                                                                   | <span data-ttu-id="f1180-208">Specifica il valore SSID di una LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f1180-208">Specifies the SSID of a wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f1180-209">**SSIDConfig**</span><span class="sxs-lookup"><span data-stu-id="f1180-209">**SSIDConfig**</span></span>](wlan-profileschema-ssidconfig-wlanprofile-element.md)            |                                                                   | <span data-ttu-id="f1180-210">Contiene uno o più SSID insieme ad altre impostazioni comuni.</span><span class="sxs-lookup"><span data-stu-id="f1180-210">Contains one or more SSIDs along with other common settings.</span></span> <br/> <span data-ttu-id="f1180-211">Un profilo può avere più elementi [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) e ogni elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) può avere più elementi [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1180-211">A profile can have multiple [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) elements and each [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element can have multiple [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) elements.</span></span> <span data-ttu-id="f1180-212">Tuttavia, Windows considera sempre il primo elemento [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) in un elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1180-212">However, Windows only ever considers the first [**SSIDConfig**](wlan-profileschema-ssidconfig-wlanprofile-element.md) element in a [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span><br/> <span data-ttu-id="f1180-213">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** In un profilo può essere presente al massimo un elemento [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1180-213">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** At most one [**SSID**](wlan-profileschema-ssid-ssidconfig-element.md) element can appear in a profile.</span></span><br/> |
| [<span data-ttu-id="f1180-214">**tipo**</span><span class="sxs-lookup"><span data-stu-id="f1180-214">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)                          |                                                                   | <span data-ttu-id="f1180-215">Contiene un **hexBinary** di 1 byte usato per distinguere le schede di rete con lo stesso IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-215">Contains a 1 byte **hexBinary** that is used to differentiate NICs by the same IHV.</span></span><br/> <span data-ttu-id="f1180-216">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f1180-216">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="f1180-217">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="f1180-217">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)                      | [<span data-ttu-id="f1180-218">boolean</span><span class="sxs-lookup"><span data-stu-id="f1180-218">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f1180-219">Specifica l'origine delle impostazioni di sicurezza 802.1 X utilizzate da un componente di sicurezza IHV.</span><span class="sxs-lookup"><span data-stu-id="f1180-219">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="f1180-220">Quando [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) è true, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x definite da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f1180-220">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="f1180-221">Quando **useMSOneX** è false, i componenti di sicurezza di IHV utilizzano le impostazioni 802.1 x fornite dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="f1180-221">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="f1180-222">Per impostazione predefinita, **useMSOneX** è false.</span><span class="sxs-lookup"><span data-stu-id="f1180-222">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="f1180-223">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-223">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f1180-224">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="f1180-224">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="f1180-225">boolean</span><span class="sxs-lookup"><span data-stu-id="f1180-225">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f1180-226">Indica se viene utilizzato 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="f1180-226">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="f1180-227">Questo flag è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f1180-227">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="f1180-228">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1180-228">Remarks</span></span>

<span data-ttu-id="f1180-229">La maggior parte degli elementi figlio dell'elemento WLANProfile si trova nello `https://www.microsoft.com/networking/WLAN/profile/v1` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1180-229">Most child elements of the WLANProfile element are in the `https://www.microsoft.com/networking/WLAN/profile/v1` namespace.</span></span> <span data-ttu-id="f1180-230">Ci sono due eccezioni: l'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) si trova nello `https://www.microsoft.com/networking/WLAN/profile/v2` spazio dei nomi e l'elemento [**Onex**](onexschema-onex-element.md) è nello `https://www.microsoft.com/networking/OneX/v1` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="f1180-230">There are two exceptions: the [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace and the [**OneX**](onexschema-onex-element.md) element is in the `https://www.microsoft.com/networking/OneX/v1` namespace.</span></span>

<span data-ttu-id="f1180-231">L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1180-231">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="f1180-232">L'elemento [**Onex**](onexschema-onex-element.md) può essere inserito come elemento figlio dell'elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1180-232">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

<span data-ttu-id="f1180-233">Per visualizzare l'elenco di elementi figlio in una struttura ad albero, vedere [ \_ elementi dello schema del profilo WLAN](wlan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="f1180-233">To view the list of child elements in a tree-like structure, see [WLAN\_profile Schema Elements](wlan-profileschema-elements.md).</span></span>

## <a name="examples"></a><span data-ttu-id="f1180-234">Esempio</span><span class="sxs-lookup"><span data-stu-id="f1180-234">Examples</span></span>

<span data-ttu-id="f1180-235">Per visualizzare i profili di esempio, vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f1180-235">To view sample profiles, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1180-236">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1180-236">Requirements</span></span>



| <span data-ttu-id="f1180-237">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1180-237">Requirement</span></span> | <span data-ttu-id="f1180-238">Valore</span><span class="sxs-lookup"><span data-stu-id="f1180-238">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f1180-239">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1180-239">Minimum supported client</span></span><br/> | <span data-ttu-id="f1180-240">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="f1180-240">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f1180-241">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1180-241">Minimum supported server</span></span><br/> | <span data-ttu-id="f1180-242">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1180-242">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f1180-243">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f1180-243">Redistributable</span></span><br/>          | <span data-ttu-id="f1180-244">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="f1180-244">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f1180-245">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1180-245">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1180-246">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="f1180-246">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> </dl>

 

 
