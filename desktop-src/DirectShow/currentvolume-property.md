---
description: La proprietà CurrentVolume Recupera il numero di volume per la directory radice corrente.
ms.assetid: f8d06a30-d6d5-43b9-b838-741d781f8d01
title: Proprietà CurrentVolume
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7b91c394be620dfc3f00b8793222848131355f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303770"
---
# <a name="currentvolume-property"></a><span data-ttu-id="415b3-103">Proprietà CurrentVolume</span><span class="sxs-lookup"><span data-stu-id="415b3-103">CurrentVolume Property</span></span>

> [!Note]  
> <span data-ttu-id="415b3-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="415b3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="415b3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="415b3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="415b3-106">La `CurrentVolume` proprietà recupera il numero di volume per la directory radice corrente.</span><span class="sxs-lookup"><span data-stu-id="415b3-106">The `CurrentVolume` property retrieves the volume number for the current root directory.</span></span>

``` syntax
[ iCurVolume = ] MSWebDVD.CurrentVolume
```

## <a name="return-value"></a><span data-ttu-id="415b3-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="415b3-107">Return Value</span></span>

<span data-ttu-id="415b3-108">Restituisce un valore intero che rappresenta il volume DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="415b3-108">Returns an integer value representing the current DVD volume.</span></span> <span data-ttu-id="415b3-109">Se un disco fa parte di un set di più volumi, il valore intero deve essere maggiore di zero.</span><span class="sxs-lookup"><span data-stu-id="415b3-109">If a disc is part of a multi-volume set, then the integer value should be greater than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="415b3-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="415b3-110">Remarks</span></span>

<span data-ttu-id="415b3-111">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="415b3-111">This property is read-only with no default value.</span></span>

## <a name="see-also"></a><span data-ttu-id="415b3-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="415b3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415b3-113">**VolumesAvailable**</span><span class="sxs-lookup"><span data-stu-id="415b3-113">**VolumesAvailable**</span></span>](volumesavailable-property.md)
</dt> </dl>

 

 



