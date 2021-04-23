---
description: Questa proprietà invia un comando al dispositivo per cercare un time code. Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 0502d59a-0a9e-4192-af9f-1553cd13a69c
title: KSPROPERTY_EXTXPORT_TIMECODE_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6852dc44e6ef10eebb59721f16a276ac5d4306a3
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909439"
---
# <a name="ksproperty_extxport_timecode_search"></a><span data-ttu-id="cd89d-104">KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="cd89d-104">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span>

<span data-ttu-id="cd89d-105">Questa proprietà invia un comando al dispositivo per cercare un time code.</span><span class="sxs-lookup"><span data-stu-id="cd89d-105">This property sends a command to the device to search for a specified time code.</span></span> <span data-ttu-id="cd89d-106">Il driver di dispositivo UVC supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="cd89d-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="cd89d-107">Label</span><span class="sxs-lookup"><span data-stu-id="cd89d-107">Label</span></span> | <span data-ttu-id="cd89d-108">Valore</span><span class="sxs-lookup"><span data-stu-id="cd89d-108">Value</span></span> |
|-------------------|----------------------------------------|
| <span data-ttu-id="cd89d-109">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="cd89d-109">Property Set GUID</span></span> | <span data-ttu-id="cd89d-110">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="cd89d-110">PROPSETID\_EXT\_TRANSPORT</span></span>              |
| <span data-ttu-id="cd89d-111">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="cd89d-111">Property ID</span></span>       | <span data-ttu-id="cd89d-112">KSPROPERTY \_ EXTXPORT \_ TIMECODE \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="cd89d-112">KSPROPERTY\_EXTXPORT\_TIMECODE\_SEARCH</span></span> |
| <span data-ttu-id="cd89d-113">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="cd89d-113">Data Type</span></span>         | <span data-ttu-id="cd89d-114">**KSPROPERTY \_ Struttura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="cd89d-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="cd89d-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd89d-115">Remarks</span></span>

<span data-ttu-id="cd89d-116">Compilare il **membro Timecode** della struttura **KSPROPERTY \_ EXTXPORT \_ S** con il frame, il secondo, il minuto e l'ora desiderati.</span><span class="sxs-lookup"><span data-stu-id="cd89d-116">Fill in the **Timecode** member of the **KSPROPERTY\_EXTXPORT\_S** structure with the desired frame, second, minute, and hour.</span></span> <span data-ttu-id="cd89d-117">La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta in Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="cd89d-117">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="cd89d-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd89d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd89d-119">Set di proprietà Trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="cd89d-119">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



