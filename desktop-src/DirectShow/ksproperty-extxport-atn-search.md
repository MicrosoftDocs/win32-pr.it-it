---
description: Questa proprietà Invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN). Il driver di dispositivo UVC supporta questa proprietà.
ms.assetid: 209e0aa3-d7a3-4b5c-ae5a-5063a3804a9d
title: KSPROPERTY_EXTXPORT_ATN_SEARCH
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc8ff454386c444ed6b55bfbeede60196a75127c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303711"
---
# <a name="ksproperty_extxport_atn_search"></a><span data-ttu-id="f0712-104">\_ricerca KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="f0712-104">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>

<span data-ttu-id="f0712-105">Questa proprietà Invia un comando al dispositivo per cercare un numero di traccia assoluto (ATN).</span><span class="sxs-lookup"><span data-stu-id="f0712-105">This property sends a command to the device to search for an absolute track number (ATN).</span></span> <span data-ttu-id="f0712-106">Il driver di dispositivo UVC supporta questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="f0712-106">The UVC device driver supports this property.</span></span>



|                   |                                       |
|-------------------|---------------------------------------|
| <span data-ttu-id="f0712-107">GUID set di proprietà</span><span class="sxs-lookup"><span data-stu-id="f0712-107">Property Set GUID</span></span> | <span data-ttu-id="f0712-108">\_trasporto PROPSETID ext \_</span><span class="sxs-lookup"><span data-stu-id="f0712-108">PROPSETID\_EXT\_TRANSPORT</span></span>             |
| <span data-ttu-id="f0712-109">ID proprietà</span><span class="sxs-lookup"><span data-stu-id="f0712-109">Property ID</span></span>       | <span data-ttu-id="f0712-110">\_ricerca KSPROPERTY EXTXPORT \_ ATN \_</span><span class="sxs-lookup"><span data-stu-id="f0712-110">KSPROPERTY\_EXTXPORT\_ATN\_SEARCH</span></span>     |
| <span data-ttu-id="f0712-111">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="f0712-111">Data Type</span></span>         | <span data-ttu-id="f0712-112">**KSPROPERTY \_ Struttura EXTXPORT \_ S**</span><span class="sxs-lookup"><span data-stu-id="f0712-112">**KSPROPERTY\_EXTXPORT\_S** structure</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f0712-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f0712-113">Remarks</span></span>

<span data-ttu-id="f0712-114">Impostare il membro **dwAbsTrackNumber** della struttura **KSPROPERTY \_ EXTXPORT \_ S** sul valore seguente:</span><span class="sxs-lookup"><span data-stu-id="f0712-114">Set the **dwAbsTrackNumber** member of the **KSPROPERTY\_EXTXPORT\_S** structure to the following value:</span></span>


```
(absolute track number << 1) + continuity bit
```



<span data-ttu-id="f0712-115">La specifica UVC non definisce il modo in cui il dispositivo usa il bit di continuità.</span><span class="sxs-lookup"><span data-stu-id="f0712-115">The UVC specification does not define how the device uses the continuity bit.</span></span> <span data-ttu-id="f0712-116">La struttura **KSPROPERTY \_ EXTXPORT \_ S** è descritta nel DDK di Windows.</span><span class="sxs-lookup"><span data-stu-id="f0712-116">The **KSPROPERTY\_EXTXPORT\_S** structure is described in the Windows DDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="f0712-117">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f0712-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0712-118">Set di proprietà di trasporto dispositivo esterno</span><span class="sxs-lookup"><span data-stu-id="f0712-118">External Device Transport Property Set</span></span>](external-device-transport-property-set.md)
</dt> </dl>

 

 



