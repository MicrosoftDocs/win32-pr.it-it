---
description: Contiene una chiave di rete o una passphrase.
ms.assetid: d2ed407e-5eaa-477b-8c4d-a47795048e0b
title: Elemento portamateriali (sharedKey)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyMaterial
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 59f3fc25fda5f4bf4221417636ac25ab7d0f9a15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231725"
---
# <a name="keymaterial-sharedkey-element"></a><span data-ttu-id="fcc18-103">Elemento portamateriali (sharedKey)</span><span class="sxs-lookup"><span data-stu-id="fcc18-103">keyMaterial (sharedKey) Element</span></span>

<span data-ttu-id="fcc18-104">L'elemento sharedKey contiene una chiave di rete o una passphrase.</span><span class="sxs-lookup"><span data-stu-id="fcc18-104">The keyMaterial (sharedKey) element contains a network key or passphrase.</span></span> <span data-ttu-id="fcc18-105">Se il valore dell'elemento [**protected**](wlan-profileschema-protected-sharedkey-element.md) è true, il materiale della chiave verrà crittografato. in caso contrario, il materiale della chiave non è crittografato.</span><span class="sxs-lookup"><span data-stu-id="fcc18-105">If the [**protected**](wlan-profileschema-protected-sharedkey-element.md) element has a value of TRUE, then this key material is encrypted; otherwise, the key material is unencrypted.</span></span> <span data-ttu-id="fcc18-106">Il materiale della chiave crittografata è espresso in formato esadecimale.</span><span class="sxs-lookup"><span data-stu-id="fcc18-106">Encrypted key material is expressed in hexadecimal form.</span></span>

``` syntax
<xs:element name="keyMaterial"
    type="string"
 />
```

<span data-ttu-id="fcc18-107">L'elemento è definito dall'elemento [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc18-107">The element is defined by the [**sharedKey**](wlan-profileschema-sharedkey-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="fcc18-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="fcc18-108">Remarks</span></span>

<span data-ttu-id="fcc18-109">L'intervallo di valori validi per l'elemento del materiale di crittografia varia in base al tipo di autenticazione e crittografia utilizzato, come specificato dagli elementi [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) e [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) .</span><span class="sxs-lookup"><span data-stu-id="fcc18-109">The range of valid values for the keyMaterial element varies by the type of authentication and encryption used, as specified by the [**authentication**](wlan-profileschema-authentication-authencryption-element.md) and [**encryption**](wlan-profileschema-encryption-authencryption-element.md) elements.</span></span> <span data-ttu-id="fcc18-110">Varia anche in base al [**tipo di tipo**](wlan-profileschema-keytype-sharedkey-element.md).</span><span class="sxs-lookup"><span data-stu-id="fcc18-110">It also varies by [**keyType**](wlan-profileschema-keytype-sharedkey-element.md).</span></span>

<span data-ttu-id="fcc18-111">Nella tabella seguente vengono illustrati i valori validi del **materiale** per alcune coppie di autenticazione e di crittografia.</span><span class="sxs-lookup"><span data-stu-id="fcc18-111">The following table shows valid **keyMaterial** values for some authentication and encryption pairs.</span></span>



| <span data-ttu-id="fcc18-112">valore di [**autenticazione**](wlan-profileschema-authentication-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="fcc18-112">[**authentication**](wlan-profileschema-authentication-authencryption-element.md) value</span></span> | <span data-ttu-id="fcc18-113">valore di [**crittografia**](wlan-profileschema-encryption-authencryption-element.md)</span><span class="sxs-lookup"><span data-stu-id="fcc18-113">[**encryption**](wlan-profileschema-encryption-authencryption-element.md) value</span></span> | <span data-ttu-id="fcc18-114">valore di [**tipo di tipo**](wlan-profileschema-keytype-sharedkey-element.md)</span><span class="sxs-lookup"><span data-stu-id="fcc18-114">[**keyType**](wlan-profileschema-keytype-sharedkey-element.md) value</span></span> | <span data-ttu-id="fcc18-115">Valori validi per il **materiale** consentiti</span><span class="sxs-lookup"><span data-stu-id="fcc18-115">Valid **keyMaterial** values</span></span>                                                                                                                                                                   |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fcc18-116">aperto o condiviso</span><span class="sxs-lookup"><span data-stu-id="fcc18-116">open or shared</span></span>                                                                           | <span data-ttu-id="fcc18-117">WEP</span><span class="sxs-lookup"><span data-stu-id="fcc18-117">WEP</span></span>                                                                              | <span data-ttu-id="fcc18-118">networkKey</span><span class="sxs-lookup"><span data-stu-id="fcc18-118">networkKey</span></span>                                                            | <span data-ttu-id="fcc18-119">Questo elemento contiene una chiave WEP di 5 o 13 caratteri ANSI oppure di 10 o 26 caratteri esadecimali.</span><span class="sxs-lookup"><span data-stu-id="fcc18-119">This element contains a WEP key of 5 or 13 ANSI characters, or of 10 or 26 hexadecimal characters.</span></span>                                                                                             |
| <span data-ttu-id="fcc18-120">WPAPSK o WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="fcc18-120">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="fcc18-121">TKIP o AES</span><span class="sxs-lookup"><span data-stu-id="fcc18-121">TKIP or AES</span></span>                                                                      | <span data-ttu-id="fcc18-122">passPhrase</span><span class="sxs-lookup"><span data-stu-id="fcc18-122">passPhrase</span></span>                                                            | <span data-ttu-id="fcc18-123">Questo elemento contiene una passphrase da 8 a 63 caratteri ASCII, ovvero da 8 a 63 caratteri ANSI nell'intervallo da 32 a 126.</span><span class="sxs-lookup"><span data-stu-id="fcc18-123">This element contains a passphrase of 8 to 63 ASCII characters, that is, 8 to 63 ANSI characters in the range of 32 to 126.</span></span> <span data-ttu-id="fcc18-124">I valori di chiave devono essere conformi ai requisiti specificati da 802.11 i.</span><span class="sxs-lookup"><span data-stu-id="fcc18-124">Key values must comply with the requirements specified by 802.11i.</span></span> |
| <span data-ttu-id="fcc18-125">WPAPSK o WPA2PSK</span><span class="sxs-lookup"><span data-stu-id="fcc18-125">WPAPSK or WPA2PSK</span></span>                                                                        | <span data-ttu-id="fcc18-126">TKIP o AES</span><span class="sxs-lookup"><span data-stu-id="fcc18-126">TKIP or AES</span></span>                                                                      | <span data-ttu-id="fcc18-127">networkKey</span><span class="sxs-lookup"><span data-stu-id="fcc18-127">networkKey</span></span>                                                            | <span data-ttu-id="fcc18-128">Questo elemento contiene una chiave di 64 caratteri esadecimali.</span><span class="sxs-lookup"><span data-stu-id="fcc18-128">This element contains a key of 64 hexadecimal characters.</span></span>                                                                                                                                      |



 

<span data-ttu-id="fcc18-129">È possibile immettere caratteri Unicode in cui vengono specificati i caratteri ANSI o ASCII.</span><span class="sxs-lookup"><span data-stu-id="fcc18-129">Unicode characters may be entered where ANSI or ASCII characters are specified above.</span></span> <span data-ttu-id="fcc18-130">Tuttavia, se non è possibile eseguire il mapping dei caratteri Unicode specificati ai caratteri ANSI o ASCII, il materiale della chiave fornito viene rifiutato.</span><span class="sxs-lookup"><span data-stu-id="fcc18-130">However, if the supplied Unicode characters cannot be mapped to ANSI or ASCII characters, then the supplied key material is rejected.</span></span>

<span data-ttu-id="fcc18-131">Il materiale della chiave restituito da [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) è sempre crittografato.</span><span class="sxs-lookup"><span data-stu-id="fcc18-131">Key material returned by [**WlanGetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetprofile) is always encrypted.</span></span> <span data-ttu-id="fcc18-132">Inoltre, se il materiale della chiave non crittografata viene passato a [**WLanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), il materiale della chiave viene crittografato automaticamente prima di essere archiviato nell'archivio profili.</span><span class="sxs-lookup"><span data-stu-id="fcc18-132">Also, if unencrypted key material is passed to [**WlanSetProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetprofile), the key material is automatically encrypted before it is stored in the profile store.</span></span>

<span data-ttu-id="fcc18-133">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Il materiale della chiave non viene mai crittografato.</span><span class="sxs-lookup"><span data-stu-id="fcc18-133">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** The key material is never encrypted.</span></span>

<span data-ttu-id="fcc18-134">Se il processo viene eseguito nel contesto dell'account LocalSystem, è possibile decrittografare il materiale della chiave chiamando [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span><span class="sxs-lookup"><span data-stu-id="fcc18-134">If your process runs in the context of the LocalSystem account, then you can unencrypt key material by calling [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata).</span></span>

## <a name="examples"></a><span data-ttu-id="fcc18-135">Esempio</span><span class="sxs-lookup"><span data-stu-id="fcc18-135">Examples</span></span>

<span data-ttu-id="fcc18-136">Per visualizzare i profili di esempio che usano l'elemento **codematerial** , vedere esempio di profilo [non broadcast](non-broadcast-profile-sample.md), esempio di [profilo WPA-Personal](wpa-personal-profile-sample.md)e [esempio di profilo WPA2-Personal](wpa2-personal-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="fcc18-136">To view sample profiles that use the **keyMaterial** element, see [Non-Broadcast Profile Sample](non-broadcast-profile-sample.md), [WPA-Personal Profile Sample](wpa-personal-profile-sample.md), and [WPA2-Personal Profile Sample](wpa2-personal-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fcc18-137">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fcc18-137">Requirements</span></span>



| <span data-ttu-id="fcc18-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcc18-138">Requirement</span></span> | <span data-ttu-id="fcc18-139">Valore</span><span class="sxs-lookup"><span data-stu-id="fcc18-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="fcc18-140">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcc18-140">Minimum supported client</span></span><br/> | <span data-ttu-id="fcc18-141">Windows Vista, Windows XP con \[ solo app desktop SP3\]</span><span class="sxs-lookup"><span data-stu-id="fcc18-141">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fcc18-142">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fcc18-142">Minimum supported server</span></span><br/> | <span data-ttu-id="fcc18-143">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fcc18-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="fcc18-144">Componente ridistribuibile</span><span class="sxs-lookup"><span data-stu-id="fcc18-144">Redistributable</span></span><br/>          | <span data-ttu-id="fcc18-145">API LAN wireless per Windows XP con SP2</span><span class="sxs-lookup"><span data-stu-id="fcc18-145">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="fcc18-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fcc18-146">See also</span></span>

<dl> <dt>

<span data-ttu-id="fcc18-147">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="fcc18-147">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc18-148">**sharedKey**</span><span class="sxs-lookup"><span data-stu-id="fcc18-148">**sharedKey**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> <dt>

<span data-ttu-id="fcc18-149">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="fcc18-149">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fcc18-150">**sharedKey (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="fcc18-150">**sharedKey (security)**</span></span>](wlan-profileschema-sharedkey-security-element.md)
</dt> </dl>

 

 
