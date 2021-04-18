---
description: Contiene diverse impostazioni di sicurezza.
ms.assetid: 1d912fb1-8fb4-4761-8991-5a50ffb0399e
title: Elemento Security (MSM) (LAN_policy) (WLAN)
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
ms.openlocfilehash: f6ea42a83d39c328db88e992555e5d593cc778b6
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2021
ms.locfileid: "106334003"
---
# <a name="security-msm-element-lan_policy-for-wlan"></a><span data-ttu-id="f30b0-103">Elemento Security (MSM) (LAN_policy) per WLAN</span><span class="sxs-lookup"><span data-stu-id="f30b0-103">Security (MSM) Element (LAN_policy) for WLAN</span></span>

<span data-ttu-id="f30b0-104">L'elemento Security (MSM) contiene diverse impostazioni di sicurezza.</span><span class="sxs-lookup"><span data-stu-id="f30b0-104">The security (MSM) element contains various security settings.</span></span>

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

<span data-ttu-id="f30b0-105">L'elemento è definito dall'elemento [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f30b0-105">The element is defined by the [**MSM**](wlan-profileschema-msm-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f30b0-106">Elementi figlio</span><span class="sxs-lookup"><span data-stu-id="f30b0-106">Child elements</span></span>



| <span data-ttu-id="f30b0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="f30b0-107">Element</span></span>                                                                            | <span data-ttu-id="f30b0-108">Tipo</span><span class="sxs-lookup"><span data-stu-id="f30b0-108">Type</span></span>                                                              | <span data-ttu-id="f30b0-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f30b0-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f30b0-110">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="f30b0-110">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)       |                                                                   | <span data-ttu-id="f30b0-111">Specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="f30b0-111">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f30b0-112">**autenticazione**</span><span class="sxs-lookup"><span data-stu-id="f30b0-112">**authentication**</span></span>](wlan-profileschema-authentication-authencryption-element.md) |                                                                   | <span data-ttu-id="f30b0-113">Specifica la coppia di autenticazione e crittografia da usare per questo profilo.</span><span class="sxs-lookup"><span data-stu-id="f30b0-113">Specifies the authentication and encryption pair to be used for this profile.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="f30b0-114">**crittografia**</span><span class="sxs-lookup"><span data-stu-id="f30b0-114">**encryption**</span></span>](wlan-profileschema-encryption-authencryption-element.md)         |                                                                   | <span data-ttu-id="f30b0-115">Imposta la crittografia dei dati da utilizzare per la connessione alla LAN wireless.</span><span class="sxs-lookup"><span data-stu-id="f30b0-115">Sets the data encryption to use to connect to the wireless LAN.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="f30b0-116">**keyIndex**</span><span class="sxs-lookup"><span data-stu-id="f30b0-116">**keyIndex**</span></span>](wlan-profileschema-keyindex-security-element.md)                   |                                                                   | <span data-ttu-id="f30b0-117">Specifica l'indice della chiave che deve essere utilizzato per crittografare il traffico wireless.</span><span class="sxs-lookup"><span data-stu-id="f30b0-117">Specifies which key index must be used to encrypt wireless traffic.</span></span> <span data-ttu-id="f30b0-118">Viene usato solo quando il tipo di operazione è impostato su networkKey.</span><span class="sxs-lookup"><span data-stu-id="f30b0-118">This is only used when keyType is set to networkKey.</span></span><br/>                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="f30b0-119">**keyMaterial**</span><span class="sxs-lookup"><span data-stu-id="f30b0-119">**keyMaterial**</span></span>](wlan-profileschema-keymaterial-sharedkey-element.md)            | [<span data-ttu-id="f30b0-120">string</span><span class="sxs-lookup"><span data-stu-id="f30b0-120">string</span></span>](/dotnet/api/system.string)   | <span data-ttu-id="f30b0-121">Contiene la chiave di rete o la passphrase.</span><span class="sxs-lookup"><span data-stu-id="f30b0-121">Contains the network key or passphrase.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f30b0-122">**keyType**</span><span class="sxs-lookup"><span data-stu-id="f30b0-122">**keyType**</span></span>](wlan-profileschema-keytype-sharedkey-element.md)                    |                                                                   | <span data-ttu-id="f30b0-123">Tipo di chiave.</span><span class="sxs-lookup"><span data-stu-id="f30b0-123">Type of key.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="f30b0-124">**PMKCacheMode**</span><span class="sxs-lookup"><span data-stu-id="f30b0-124">**PMKCacheMode**</span></span>](wlan-profileschema-pmkcachemode-security-element.md)           |                                                                   | <span data-ttu-id="f30b0-125">Indica se verrà utilizzata la memorizzazione nella cache PMK.</span><span class="sxs-lookup"><span data-stu-id="f30b0-125">Indicates whether PMK caching will be used.</span></span> <span data-ttu-id="f30b0-126">Questo elemento è valido solo per le reti definite da WPA2.</span><span class="sxs-lookup"><span data-stu-id="f30b0-126">This element is valid only for WPA2-defined networks.</span></span><br/> <span data-ttu-id="f30b0-127">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f30b0-127">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="f30b0-128">**PMKCacheSize**</span><span class="sxs-lookup"><span data-stu-id="f30b0-128">**PMKCacheSize**</span></span>](wlan-profileschema-pmkcachesize-security-element.md)           |                                                                   | <span data-ttu-id="f30b0-129">Specifica il numero di voci nella cache OMK nel client.</span><span class="sxs-lookup"><span data-stu-id="f30b0-129">Specifies the number of entries in the OMK cache on the client.</span></span> <span data-ttu-id="f30b0-130">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="f30b0-130">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="f30b0-131">Se la modalità PMKCache è abilitata e questo elemento è assente, per impostazione predefinita la dimensione della cache corrisponde a 128 voci.</span><span class="sxs-lookup"><span data-stu-id="f30b0-131">If PMKCache mode is enabled, and this element is absent, the size of the cache defaults to 128 entries.</span></span><br/> <span data-ttu-id="f30b0-132">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f30b0-132">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                   |
| [<span data-ttu-id="f30b0-133">**PMKCacheTTL**</span><span class="sxs-lookup"><span data-stu-id="f30b0-133">**PMKCacheTTL**</span></span>](wlan-profileschema-pmkcachettl-security-element.md)             |                                                                   | <span data-ttu-id="f30b0-134">Indica il periodo di tempo, in minuti, in cui verrà mantenuta una cache PMK.</span><span class="sxs-lookup"><span data-stu-id="f30b0-134">Indicates the length of time, in minutes, that a PMK cache will be kept.</span></span> <span data-ttu-id="f30b0-135">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="f30b0-135">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span><br/> <span data-ttu-id="f30b0-136">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f30b0-136">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="f30b0-137">**preAuthMode**</span><span class="sxs-lookup"><span data-stu-id="f30b0-137">**preAuthMode**</span></span>](wlan-profileschema-preauthmode-security-element.md)             |                                                                   | <span data-ttu-id="f30b0-138">Determina se la pre-autenticazione verrà utilizzata dal client.</span><span class="sxs-lookup"><span data-stu-id="f30b0-138">Determines if pre-authentication will be used by the client.</span></span> <span data-ttu-id="f30b0-139">La pre-autenticazione Abilita il roaming veloce sicuro WPA2.</span><span class="sxs-lookup"><span data-stu-id="f30b0-139">Pre-authentication enables WPA2 secure fast roaming.</span></span> <span data-ttu-id="f30b0-140">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="f30b0-140">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="f30b0-141">Se la modalità PMKCache è abilitata e questo elemento è assente, il valore predefinito è Disabled.</span><span class="sxs-lookup"><span data-stu-id="f30b0-141">If PMKCache mode is enabled, and this element is absent, the default value is disabled.</span></span><br/> <span data-ttu-id="f30b0-142">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f30b0-142">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/> |
| [<span data-ttu-id="f30b0-143">**preAuthThrottle**</span><span class="sxs-lookup"><span data-stu-id="f30b0-143">**preAuthThrottle**</span></span>](wlan-profileschema-preauththrottle-security-element.md)     |                                                                   | <span data-ttu-id="f30b0-144">Indica il numero di tentativi quando si esegue la preautenticazione ai punti di APs adiacenti.</span><span class="sxs-lookup"><span data-stu-id="f30b0-144">Indicates the number of tries when preauthenticating to neighboring APs.</span></span> <span data-ttu-id="f30b0-145">Questo elemento è valido solo per le reti definite da WPA2 con la modalità PMKCache impostata su Enabled.</span><span class="sxs-lookup"><span data-stu-id="f30b0-145">This element is valid only for WPA2-defined networks with PMKCache mode set to enabled.</span></span> <span data-ttu-id="f30b0-146">Se la modalità PMKCache è abilitata e questo elemento è assente, il numero di tentativi predefinito è 3.</span><span class="sxs-lookup"><span data-stu-id="f30b0-146">If PMKCache mode is enabled, and this element is absent, the number of tries defaults to 3.</span></span><br/> <span data-ttu-id="f30b0-147">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="f30b0-147">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span><br/>                                      |
| [<span data-ttu-id="f30b0-148">**protetto**</span><span class="sxs-lookup"><span data-stu-id="f30b0-148">**protected**</span></span>](wlan-profileschema-protected-sharedkey-element.md)                | [<span data-ttu-id="f30b0-149">boolean</span><span class="sxs-lookup"><span data-stu-id="f30b0-149">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f30b0-150">Indica se la chiave è crittografata.</span><span class="sxs-lookup"><span data-stu-id="f30b0-150">Indicates whether the key is encrypted.</span></span><br/> <span data-ttu-id="f30b0-151">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il valore di questo elemento deve essere **false**.</span><span class="sxs-lookup"><span data-stu-id="f30b0-151">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element must have a value of **FALSE**.</span></span><br/>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="f30b0-152">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="f30b0-152">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)                 |                                                                   | <span data-ttu-id="f30b0-153">Contiene le informazioni sulla chiave condivisa.</span><span class="sxs-lookup"><span data-stu-id="f30b0-153">Contains the shared key information.</span></span> <span data-ttu-id="f30b0-154">Questo elemento è obbligatorio solo se sono necessarie chiavi WEP o PSK per la coppia di autenticazione e crittografia.</span><span class="sxs-lookup"><span data-stu-id="f30b0-154">This element is only required if WEP or PSK keys are required for the authentication and encryption pair.</span></span><br/>                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="f30b0-155">**useOneX**</span><span class="sxs-lookup"><span data-stu-id="f30b0-155">**useOneX**</span></span>](wlan-profileschema-useonex-authencryption-element.md)               | [<span data-ttu-id="f30b0-156">boolean</span><span class="sxs-lookup"><span data-stu-id="f30b0-156">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="f30b0-157">Indica se viene utilizzato 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="f30b0-157">Indicates whether 802.1X is used.</span></span> <span data-ttu-id="f30b0-158">Questo flag è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="f30b0-158">This flag is optional.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



## <a name="remarks"></a><span data-ttu-id="f30b0-159">Commenti</span><span class="sxs-lookup"><span data-stu-id="f30b0-159">Remarks</span></span>

<span data-ttu-id="f30b0-160">L'elemento [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) può essere inserito come figlio dell'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f30b0-160">The [**FIPSMode**](wlan-profileschema-fipsmode-authencryption-element.md) element can be inserted as a child of the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span> <span data-ttu-id="f30b0-161">L'elemento [**Onex**](onexschema-onex-element.md) può essere inserito come elemento figlio dell'elemento **Security (MSM)** .</span><span class="sxs-lookup"><span data-stu-id="f30b0-161">The [**OneX**](onexschema-onex-element.md) element can be inserted as a child of the **security (MSM)** element.</span></span>

## <a name="examples"></a><span data-ttu-id="f30b0-162">Esempio</span><span class="sxs-lookup"><span data-stu-id="f30b0-162">Examples</span></span>

<span data-ttu-id="f30b0-163">Per visualizzare i profili di esempio che usano l'elemento **Security** , vedere esempi di profili [wireless](wireless-profile-samples.md).</span><span class="sxs-lookup"><span data-stu-id="f30b0-163">To view sample profiles that use the **security** element, see [Wireless Profile Samples](wireless-profile-samples.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f30b0-164">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f30b0-164">Requirements</span></span>



| <span data-ttu-id="f30b0-165">Requisito</span><span class="sxs-lookup"><span data-stu-id="f30b0-165">Requirement</span></span> | <span data-ttu-id="f30b0-166">Valore</span><span class="sxs-lookup"><span data-stu-id="f30b0-166">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="f30b0-167">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f30b0-167">Minimum supported client</span></span><br/> | <span data-ttu-id="f30b0-168">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="f30b0-168">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="f30b0-169">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f30b0-169">Minimum supported server</span></span><br/> | <span data-ttu-id="f30b0-170">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f30b0-170">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="f30b0-171">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="f30b0-171">Redistributable</span></span><br/>          | <span data-ttu-id="f30b0-172">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="f30b0-172">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="f30b0-173">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f30b0-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f30b0-174">Esempi di profili wireless</span><span class="sxs-lookup"><span data-stu-id="f30b0-174">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

<span data-ttu-id="f30b0-175">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="f30b0-175">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f30b0-176">**MSM**</span><span class="sxs-lookup"><span data-stu-id="f30b0-176">**MSM**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="f30b0-177">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="f30b0-177">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f30b0-178">**CSM (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="f30b0-178">**MSM (WLANProfile)**</span></span>](wlan-profileschema-msm-wlanprofile-element.md)
</dt> </dl>

 

 
