---
description: Indica se la modalità FIPS (Federal Information Processing Standards) è abilitata.
ms.assetid: 4c62c96c-82e7-4174-b833-95ee10b29344
title: Elemento FIPSMode (authEncryption)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FIPSMode
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 62a60670622084e3179e9720022c68ad5909ab4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752303"
---
# <a name="fipsmode-authencryption-element"></a><span data-ttu-id="3924f-103">Elemento FIPSMode (authEncryption)</span><span class="sxs-lookup"><span data-stu-id="3924f-103">FIPSMode (authEncryption) Element</span></span>

<span data-ttu-id="3924f-104">L'elemento **FIPSMode** (authEncryption) indica se la modalità FIPS (Federal Information Processing Standards) è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3924f-104">The **FIPSMode** (authEncryption) element indicates whether Federal Information Processing Standards (FIPS) mode is enabled.</span></span> <span data-ttu-id="3924f-105">Quando una connessione wireless funziona in modalità FIPS, il livello di sicurezza della connessione è conforme allo standard FIPS 140-2.</span><span class="sxs-lookup"><span data-stu-id="3924f-105">When a wireless connection is operating in FIPS mode, the security level of the connection complies with the FIPS 140-2 standard.</span></span> <span data-ttu-id="3924f-106">Per ulteriori informazioni su FIPS, vedere la [Home page di FIPS](https://www.itl.nist.gov/fipspubs/).</span><span class="sxs-lookup"><span data-stu-id="3924f-106">For more information about FIPS, see the [FIPS Home Page](https://www.itl.nist.gov/fipspubs/).</span></span>

<span data-ttu-id="3924f-107">Questo elemento è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="3924f-107">This element is optional.</span></span> <span data-ttu-id="3924f-108">Se questo elemento non viene specificato in un profilo, la modalità FIPS non è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3924f-108">If this element is not specified in a profile, then FIPS mode is not enabled.</span></span>

<span data-ttu-id="3924f-109">**FIPSMode** può essere impostato su true solo quando vengono soddisfatte le condizioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="3924f-109">**FIPSMode** can be set to TRUE only when the following conditions are met:</span></span>

-   <span data-ttu-id="3924f-110">L'elemento [**ConnectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) ha un valore `ESS` (ovvero la connessione è una connessione di infrastruttura).</span><span class="sxs-lookup"><span data-stu-id="3924f-110">The [**connectionType**](wlan-profileschema-connectiontype-wlanprofile-element.md) element has a value of `ESS` (that is, the connection is an infrastructure connection).</span></span>
-   <span data-ttu-id="3924f-111">Il valore dell'elemento [**Authentication**](wlan-profileschema-authentication-authencryption-element.md) è `WPA2` o `WPA2PSK` .</span><span class="sxs-lookup"><span data-stu-id="3924f-111">The [**authentication**](wlan-profileschema-authentication-authencryption-element.md) element has a value of `WPA2` or `WPA2PSK`.</span></span>
-   <span data-ttu-id="3924f-112">Il valore dell'elemento [**Encryption**](wlan-profileschema-encryption-authencryption-element.md) è `AES` .</span><span class="sxs-lookup"><span data-stu-id="3924f-112">The [**encryption**](wlan-profileschema-encryption-authencryption-element.md) element has a value of `AES`.</span></span>

<span data-ttu-id="3924f-113">A differenza della maggior parte degli elementi nello \_ schema del profilo WLAN, questo elemento si trova nello `https://www.microsoft.com/networking/WLAN/profile/v2` spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="3924f-113">Unlike most elements in the WLAN\_profile schema, this element is in the `https://www.microsoft.com/networking/WLAN/profile/v2` namespace.</span></span>

<span data-ttu-id="3924f-114">Il valore dell'elemento **FIPSMode** viene ignorato se il driver miniport per l'interfaccia wireless non supporta la modalità FIPS.</span><span class="sxs-lookup"><span data-stu-id="3924f-114">The value of the **FIPSMode** element is ignored if the miniport driver for the wireless interface does not support FIPS mode.</span></span>

<span data-ttu-id="3924f-115">**Windows XP con SP3 e l'API LAN wireless per Windows XP con SP2:** Questo elemento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="3924f-115">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span> <span data-ttu-id="3924f-116">Se **FIPSMode** è presente in un profilo, l'elemento viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="3924f-116">If **FIPSMode** is present in a profile, the element is ignored.</span></span>

``` syntax
<xs:element name="FIPSMode"
    type="boolean"
 />
```

<span data-ttu-id="3924f-117">L'elemento è definito dall'elemento [**authEncryption**](wlan-profileschema-authencryption-security-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3924f-117">The element is defined by the [**authEncryption**](wlan-profileschema-authencryption-security-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="3924f-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="3924f-118">Remarks</span></span>

<span data-ttu-id="3924f-119">Questo parametro può essere impostato dalla riga di comando tramite il comando **netsh wlan set profileparameter** .</span><span class="sxs-lookup"><span data-stu-id="3924f-119">This parameter can be set at the command line using the **netsh wlan set profileparameter** command.</span></span> <span data-ttu-id="3924f-120">Per ulteriori informazioni, vedere [comandi Netsh per WLAN (wireless local area network)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="3924f-120">For more information, see [Netsh Commands for Wireless Local Area Network (wlan)](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc755301(v=ws.10)).</span></span>

## <a name="examples"></a><span data-ttu-id="3924f-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="3924f-121">Examples</span></span>

<span data-ttu-id="3924f-122">Per visualizzare un profilo di esempio che usa l'elemento **FIPSMode** , vedere [esempio di profilo FIPS](fips-profile-sample.md).</span><span class="sxs-lookup"><span data-stu-id="3924f-122">To view a sample profile that uses the **FIPSMode** element, see [FIPS Profile Sample](fips-profile-sample.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3924f-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3924f-123">Requirements</span></span>



| <span data-ttu-id="3924f-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="3924f-124">Requirement</span></span> | <span data-ttu-id="3924f-125">Valore</span><span class="sxs-lookup"><span data-stu-id="3924f-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3924f-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3924f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3924f-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3924f-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3924f-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3924f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3924f-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3924f-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3924f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3924f-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="3924f-131">**Contesto di definizione dell'elemento nello schema**</span><span class="sxs-lookup"><span data-stu-id="3924f-131">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3924f-132">**authEncryption**</span><span class="sxs-lookup"><span data-stu-id="3924f-132">**authEncryption**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> <dt>

<span data-ttu-id="3924f-133">**Possibile elemento padre immediato nell'istanza dello schema**</span><span class="sxs-lookup"><span data-stu-id="3924f-133">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3924f-134">**authEncryption (sicurezza)**</span><span class="sxs-lookup"><span data-stu-id="3924f-134">**authEncryption (security)**</span></span>](wlan-profileschema-authencryption-security-element.md)
</dt> </dl>

 

 
