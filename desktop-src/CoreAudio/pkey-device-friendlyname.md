---
description: La \_ Proprietà Device \_ FriendlyName di pkey contiene il nome descrittivo del dispositivo endpoint (ad esempio, &\# 0034; Altoparlanti (scheda audio XYZ) &\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877181"
---
# <a name="pkey_device_friendlyname"></a><span data-ttu-id="f42c1-103">PKEY \_ Device \_ FriendlyName</span><span class="sxs-lookup"><span data-stu-id="f42c1-103">PKEY\_Device\_FriendlyName</span></span>

<span data-ttu-id="f42c1-104">La **proprietà \_ Device \_ FriendlyName di pkey** contiene il nome descrittivo del dispositivo endpoint (ad esempio, "Speakers (scheda audio XYZ)").</span><span class="sxs-lookup"><span data-stu-id="f42c1-104">The **PKEY\_Device\_FriendlyName** property contains the friendly name of the endpoint device (for example, "Speakers (XYZ Audio Adapter)").</span></span>

<span data-ttu-id="f42c1-105">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="f42c1-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="f42c1-106">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene il nome descrittivo del dispositivo endpoint.</span><span class="sxs-lookup"><span data-stu-id="f42c1-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the friendly name of the endpoint device.</span></span>

## <a name="requirements"></a><span data-ttu-id="f42c1-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f42c1-107">Requirements</span></span>



| <span data-ttu-id="f42c1-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="f42c1-108">Requirement</span></span> | <span data-ttu-id="f42c1-109">Valore</span><span class="sxs-lookup"><span data-stu-id="f42c1-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f42c1-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42c1-110">Minimum supported client</span></span><br/> | <span data-ttu-id="f42c1-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f42c1-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f42c1-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f42c1-112">Minimum supported server</span></span><br/> | <span data-ttu-id="f42c1-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f42c1-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="f42c1-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f42c1-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="f42c1-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="f42c1-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f42c1-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f42c1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f42c1-117">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="f42c1-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="f42c1-118">Proprietà dispositivo</span><span class="sxs-lookup"><span data-stu-id="f42c1-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




