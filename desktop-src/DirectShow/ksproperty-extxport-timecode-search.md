---
description: Questa proprietà Invia un comando al dispositivo per cercare un codice temporale specificato. Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c52125f0c2e7ddd292cc1f93577a212d5c78a76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104048922"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="a1336-104">KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode</span><span class="sxs-lookup"><span data-stu-id="a1336-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="a1336-105">Questa proprietà Invia un comando al dispositivo per cercare un codice temporale specificato.</span><span class="sxs-lookup"><span data-stu-id="a1336-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="a1336-106">Il driver di dispositivo UVC supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="a1336-106">The UVC device driver supports this property.</span></span>



|                   |                                        |
|-------------------|----------------------------------------|
| <span data-ttu-id="a1336-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="a1336-107">Property Set GUID</span></span> | <span data-ttu-id="a1336-108">\_trasporto PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="a1336-108">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="a1336-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="a1336-109">Property ID</span></span>       | <span data-ttu-id="a1336-110">KSPROPERTY \_ EXTXPORT \_ - \_ ricerca timecode</span><span class="sxs-lookup"><span data-stu-id="a1336-110">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="a1336-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a1336-111">Data Type</span></span>         | <span data-ttu-id="a1336-112">**KSPROPERTY \_ Struttura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="a1336-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="a1336-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1336-113">Remarks</span></span>

<span data-ttu-id="a1336-114">Compilare il membro **timecode** della struttura **KSPROPERTY \_ EXTXPORT \_** con il frame, il secondo, il minuto e l'ora desiderati.</span><span class="sxs-lookup"><span data-stu-id="a1336-114">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="a1336-115">La struttura **KSPROPERTY \_ EXTXPORT \_ S** è descritta nel DDK di Windows.</span><span class="sxs-lookup"><span data-stu-id="a1336-115">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="a1336-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1336-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1336-117">Set di proprietà di trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="a1336-117">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



