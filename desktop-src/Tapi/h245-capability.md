---
description: L' \_ enumerazione della funzionalità h245 descrive il supporto del formato audio e video.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumerazione H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332823"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="a378e-103">\_Enumerazione della funzionalità h245</span><span class="sxs-lookup"><span data-stu-id="a378e-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="a378e-104">\[**H245 \_ La funzionalità** non è disponibile per l'utilizzo in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a378e-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="a378e-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="a378e-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="a378e-106">L'enumerazione della **\_ funzionalità h245** descrive il supporto del formato audio e video.</span><span class="sxs-lookup"><span data-stu-id="a378e-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="a378e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a378e-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="a378e-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="a378e-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="a378e-109"><span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 HC**</span><span class="sxs-lookup"><span data-stu-id="a378e-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="a378e-110">Il protocollo audio G. 711 è supportato.</span><span class="sxs-lookup"><span data-stu-id="a378e-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="a378e-111"><span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 HC**</span><span class="sxs-lookup"><span data-stu-id="a378e-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="a378e-112">Il protocollo audio G. 723 è supportato.</span><span class="sxs-lookup"><span data-stu-id="a378e-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="a378e-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF HC**</span><span class="sxs-lookup"><span data-stu-id="a378e-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="a378e-114">Il protocollo video H. 263 è supportato.</span><span class="sxs-lookup"><span data-stu-id="a378e-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="a378e-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF HC**</span><span class="sxs-lookup"><span data-stu-id="a378e-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="a378e-116">Il protocollo video H. 263 è supportato.</span><span class="sxs-lookup"><span data-stu-id="a378e-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a378e-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a378e-117">Requirements</span></span>



| <span data-ttu-id="a378e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a378e-118">Requirement</span></span> | <span data-ttu-id="a378e-119">Valore</span><span class="sxs-lookup"><span data-stu-id="a378e-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a378e-120">Versione TAPI</span><span class="sxs-lookup"><span data-stu-id="a378e-120">TAPI version</span></span><br/> | <span data-ttu-id="a378e-121">Richiede TAPI 3,0 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="a378e-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="a378e-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a378e-122">Header</span></span><br/>       | <dl> <span data-ttu-id="a378e-123"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="a378e-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a378e-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a378e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a378e-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="a378e-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




