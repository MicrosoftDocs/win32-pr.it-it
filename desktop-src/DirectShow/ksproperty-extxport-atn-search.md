---
description: Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4115c7ff1c4bc878b4ee80e284f11821c37909a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909448"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="4de40-104">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="4de40-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="4de40-105">Questa proprietà invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="4de40-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="4de40-106">Il driver di dispositivo UVC supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="4de40-106">The UVC device driver supports this property.</span></span>



| <span data-ttu-id="4de40-107">Label</span><span class="sxs-lookup"><span data-stu-id="4de40-107">Label</span></span> | <span data-ttu-id="4de40-108">Valore</span><span class="sxs-lookup"><span data-stu-id="4de40-108">Value</span></span> |
|-------------------|---------------------------------------|
| <span data-ttu-id="4de40-109">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="4de40-109">Property Set GUID</span></span> | <span data-ttu-id="4de40-110">PROPSETID \_ EXT \_ TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="4de40-110">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="4de40-111">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="4de40-111">Property ID</span></span>       | <span data-ttu-id="4de40-112">KSPROPERTY \_ EXTXPORT \_ ATN \_ SEARCH</span><span class="sxs-lookup"><span data-stu-id="4de40-112">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="4de40-113">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="4de40-113">Data Type</span></span>         | <span data-ttu-id="4de40-114">**KSPROPERTY \_ Struttura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="4de40-114">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4de40-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="4de40-115">Remarks</span></span>

<span data-ttu-id="4de40-116">Impostare il **membro dwAbsTrackNumber** della **struttura KSPROPERTY \_ EXTXPORT \_ S** sul valore seguente:</span><span class="sxs-lookup"><span data-stu-id="4de40-116">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="4de40-117">La specifica UVC non definisce il modo in cui il dispositivo usa il bit di continuità.</span><span class="sxs-lookup"><span data-stu-id="4de40-117">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="4de40-118">La **struttura KSPROPERTY \_ EXTXPORT \_ S** è descritta in Windows DDK.</span><span class="sxs-lookup"><span data-stu-id="4de40-118">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="4de40-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4de40-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4de40-120">Set di proprietà Trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="4de40-120">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



