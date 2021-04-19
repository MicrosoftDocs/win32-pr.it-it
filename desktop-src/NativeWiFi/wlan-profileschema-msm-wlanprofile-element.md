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
# <a name="msm-wlanprofile-element"></a><span data-ttu-id="a64c0-103">Elemento MSM (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="a64c0-103">MSM (WLANProfile) Element</span></span>

<span data-ttu-id="a64c0-104">L'elemento MSM (WLANProfile) contiene diverse impostazioni del modulo CSM (media Specific Module).</span><span class="sxs-lookup"><span data-stu-id="a64c0-104">The MSM (WLANProfile) element contains various media-specific module (MSM) settings.</span></span>

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

<span data-ttu-id="a64c0-105">L'elemento è definito dall'elemento [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a64c0-105">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="a64c0-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="a64c0-106">Child elements</span></span>



| <span data-ttu-id="a64c0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="a64c0-107">Element</span></span>                                                                            | <span data-ttu-id="a64c0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="a64c0-108">Type</span></span>                                                              | <span data-ttu-id="a64c0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a64c0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a64c0-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="a64c0-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="a64c0-111">Specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a64c0-112">**autenticazione**</span><span class="sxs-lookup"><span data-stu-id="a64c0-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="a64c0-113">Specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a64c0-114">**connettività**</span><span class="sxs-lookup"><span data-stu-id="a64c0-114">**connectivity**</span></span>](wlan-profileschema-connectivity-msm-element.md)                |                                                                   | <span data-ttu-id="a64c0-115">Contiene diverse impostazioni di connettività.</span><span class="sxs-lookup"><span data-stu-id="a64c0-115">Contains various connectivity settings.</span></span> <span data-ttu-id="a64c0-116">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-116">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a64c0-117">**crittografia**</span><span class="sxs-lookup"><span data-stu-id="a64c0-117">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="a64c0-118">Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="a64c0-118">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="a64c0-119">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="a64c0-119">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="a64c0-120">Specifica l'indice della chiave che deve essere utilizzato per crittografare il traffico wireless.</span><span class="sxs-lookup"><span data-stu-id="a64c0-120">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="a64c0-121">Viene usato solo quando il tipo di operazione è impostato su networkKey.</span><span class="sxs-lookup"><span data-stu-id="a64c0-121">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="a64c0-122">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="a64c0-122">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="a64c0-123">string</span><span class="sxs-lookup"><span data-stu-id="a64c0-123">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="a64c0-124">Contiene la chiave di rete o la passphrase.</span><span class="sxs-lookup"><span data-stu-id="a64c0-124">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a64c0-125">**keyType**</span><span class="sxs-lookup"><span data-stu-id="a64c0-125">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="a64c0-126">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="a64c0-126">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="a64c0-127">**phyType**</span><span class="sxs-lookup"><span data-stu-id="a64c0-127">**phyType**</span></span>](wlan-profileschema-phytype-connectivity-element.md)                 |                                                                   | <span data-ttu-id="a64c0-128">Specifica lo standard LAN wireless 802,11 usato sulla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="a64c0-128">Specifies the 802.11 wireless LAN standard used on the wireless LAN.</span></span> <span data-ttu-id="a64c0-129">Il valore "n" è supportato solo in Windows Vista con SP1 e versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-129">The value "n" is only supported on Windows Vista with SP1 and later versions of the operating system.</span></span><br/> <span data-ttu-id="a64c0-130">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-130">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="a64c0-131">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="a64c0-131">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="a64c0-132">Indica se verrà utilizzata la memorizzazione nella cache PMK.</span><span class="sxs-lookup"><span data-stu-id="a64c0-132">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="a64c0-133">Questo elemento è valido solo per le reti definite da WPA2.</span><span class="sxs-lookup"><span data-stu-id="a64c0-133">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="a64c0-134">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-134">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="a64c0-135">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="a64c0-135">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="a64c0-136">Specifica il numero di voci nella cache OMK nel client.</span><span class="sxs-lookup"><span data-stu-id="a64c0-136">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="a64c0-137">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="a64c0-137">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a64c0-138">Se la modalità PMKCache è abilitata e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.</span><span class="sxs-lookup"><span data-stu-id="a64c0-138">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="a64c0-139">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-139">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="a64c0-140">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="a64c0-140">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="a64c0-141">Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK.</span><span class="sxs-lookup"><span data-stu-id="a64c0-141">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="a64c0-142">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="a64c0-142">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="a64c0-143">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-143">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="a64c0-144">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="a64c0-144">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="a64c0-145">Determina se la pre-autenticazione verrà utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="a64c0-145">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="a64c0-146">La pre-autenticazione Abilita il roaming veloce sicuro WPA2.</span><span class="sxs-lookup"><span data-stu-id="a64c0-146">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="a64c0-147">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="a64c0-147">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a64c0-148">Se la modalità PMKCache è abilitata e questo elemento è assente, il valore predefinito è Disabled.</span><span class="sxs-lookup"><span data-stu-id="a64c0-148">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="a64c0-149">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-149">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="a64c0-150">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="a64c0-150">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="a64c0-151">Indica il numero di tentativi quando si esegue la preautenticazione ai punti di APs adiacenti.</span><span class="sxs-lookup"><span data-stu-id="a64c0-151">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="a64c0-152">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="a64c0-152">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="a64c0-153">Se la modalità PMKCache è abilitata e questo elemento è assente, il numero di tentativi predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="a64c0-153">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="a64c0-154">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a64c0-154">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="a64c0-155">**protetto**</span><span class="sxs-lookup"><span data-stu-id="a64c0-155">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="a64c0-156">boolean</span><span class="sxs-lookup"><span data-stu-id="a64c0-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a64c0-157">Indica se la chiave è crittografata.</span><span class="sxs-lookup"><span data-stu-id="a64c0-157">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="a64c0-158">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere FALSE.</span><span class="sxs-lookup"><span data-stu-id="a64c0-158">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of FALSE.</span></span><br/>                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="a64c0-159">**sicurezza**</span><span class="sxs-lookup"><span data-stu-id="a64c0-159">**security**</span></span>](wlan-profileschema-security-msm-element.md)                        |                                                                   | <span data-ttu-id="a64c0-160">Contiene diverse impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="a64c0-160">Contains various security settings.</span></span> <span data-ttu-id="a64c0-161">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-161">This element is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="a64c0-162">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="a64c0-162">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="a64c0-163">Contiene le informazioni sulla chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="a64c0-163">Contains the shared key information.</span></span> <span data-ttu-id="a64c0-164">Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.</span><span class="sxs-lookup"><span data-stu-id="a64c0-164">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="a64c0-165">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="a64c0-165">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="a64c0-166">boolean</span><span class="sxs-lookup"><span data-stu-id="a64c0-166">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="a64c0-167">Indica se viene utilizzato 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="a64c0-167">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="a64c0-168">Questo flag è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="a64c0-168">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="a64c0-169">Commenti</span><span class="sxs-lookup"><span data-stu-id="a64c0-169">Remarks</span></span>

<span data-ttu-id="a64c0-170">L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a64c0-170">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="a64c0-171">L'elemento [**Onex**](onexschema-onex-element.md) può essere inserito come elemento figlio dell'elemento [**Security (MSM)**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a64c0-171">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the [**security (MSM)**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="examples"></a><span data-ttu-id="a64c0-172">Esempio</span><span class="sxs-lookup"><span data-stu-id="a64c0-172">Examples</span></span>

<span data-ttu-id="a64c0-173">Per visualizzare i profili di esempio che usano l'elemento **MSM** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="a64c0-173">To view sample profiles that use the **MSM** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a64c0-174">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a64c0-174">Requirements</span></span>



| <span data-ttu-id="a64c0-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="a64c0-175">Requirement</span></span> | <span data-ttu-id="a64c0-176">Valore</span><span class="sxs-lookup"><span data-stu-id="a64c0-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="a64c0-177">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a64c0-177">Minimum supported client</span></span><br/> | <span data-ttu-id="a64c0-178">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="a64c0-178">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a64c0-179">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a64c0-179">Minimum supported server</span></span><br/> | <span data-ttu-id="a64c0-180">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a64c0-180">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="a64c0-181">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="a64c0-181">Redistributable</span></span><br/>          | <span data-ttu-id="a64c0-182">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="a64c0-182">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="a64c0-183">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a64c0-183">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64c0-184">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="a64c0-184">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="a64c0-185">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="a64c0-185">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a64c0-186">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a64c0-186">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="a64c0-187">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="a64c0-187">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a64c0-188">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="a64c0-188">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
