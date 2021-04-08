---
description: La \_ Proprietà DeviceDesc del dispositivo pkey \_ contiene la descrizione del dispositivo dell'endpoint, ad esempio &\# 0034; Speakers&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877189"
---
# <a name="pkey_device_devicedesc"></a><span data-ttu-id="b1799-103">\_DeviceDesc del dispositivo pkey \_</span><span class="sxs-lookup"><span data-stu-id="b1799-103">PKEY\_Device\_DeviceDesc</span></span>

<span data-ttu-id="b1799-104">La **proprietà \_ \_ DeviceDesc del dispositivo pkey** contiene la descrizione del dispositivo dell'endpoint (ad esempio, "Speakers").</span><span class="sxs-lookup"><span data-stu-id="b1799-104">The **PKEY\_Device\_DeviceDesc** property contains the device description of the endpoint device (for example, "Speakers").</span></span>

<span data-ttu-id="b1799-105">Il membro **VT** della struttura **PROPVARIANT** è impostato su VT \_ LPWSTR.</span><span class="sxs-lookup"><span data-stu-id="b1799-105">The **vt** member of the **PROPVARIANT** structure is set to VT\_LPWSTR.</span></span>

<span data-ttu-id="b1799-106">Il membro **pwszVal** della struttura **PROPVARIANT** punta a una stringa di caratteri wide con terminazione null che contiene la descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b1799-106">The **pwszVal** member of the **PROPVARIANT** structure points to a null-terminated, wide-character string that contains the device description.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1799-107">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b1799-107">Requirements</span></span>



| <span data-ttu-id="b1799-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1799-108">Requirement</span></span> | <span data-ttu-id="b1799-109">Valore</span><span class="sxs-lookup"><span data-stu-id="b1799-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1799-110">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1799-110">Minimum supported client</span></span><br/> | <span data-ttu-id="b1799-111">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b1799-111">Windows Vista \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b1799-112">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b1799-112">Minimum supported server</span></span><br/> | <span data-ttu-id="b1799-113">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b1799-113">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="b1799-114">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b1799-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1799-115"><dt>Functiondiscoverykeys \_ devpkey. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1799-115"><dt>Functiondiscoverykeys\_devpkey.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1799-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b1799-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1799-117">Proprietà audio principali</span><span class="sxs-lookup"><span data-stu-id="b1799-117">Core Audio Properties</span></span>](core-audio-properties.md)
</dt> <dt>

[<span data-ttu-id="b1799-118">Proprietà dispositivo</span><span class="sxs-lookup"><span data-stu-id="b1799-118">Device Properties</span></span>](device-properties.md)
</dt> </dl>

 

 




