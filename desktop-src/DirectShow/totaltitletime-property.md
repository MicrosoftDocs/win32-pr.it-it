---
description: La proprietà TotalTitleTime Recupera il tempo di riproduzione totale per il titolo corrente.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Proprietà TotalTitleTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882433"
---
# <a name="totaltitletime-property"></a><span data-ttu-id="84bac-103">Proprietà TotalTitleTime</span><span class="sxs-lookup"><span data-stu-id="84bac-103">TotalTitleTime Property</span></span>

> [!Note]  
> <span data-ttu-id="84bac-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="84bac-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="84bac-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="84bac-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="84bac-106">La `TotalTitleTime` proprietà recupera il tempo di riproduzione totale per il titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="84bac-106">The `TotalTitleTime` property retrieves the total playback time for the current title.</span></span>

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a><span data-ttu-id="84bac-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="84bac-107">Return Value</span></span>

<span data-ttu-id="84bac-108">Restituisce il tempo di riproduzione totale del titolo corrente sotto forma di stringa nel formato "HH: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="84bac-108">Returns the total playing time of the current title as a String in the format "hh:mm:ss:ff".</span></span>

## <a name="remarks"></a><span data-ttu-id="84bac-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="84bac-109">Remarks</span></span>

<span data-ttu-id="84bac-110">Questa proprietà è di sola lettura e non prevede alcun valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="84bac-110">This property is read-only with no default value.</span></span> <span data-ttu-id="84bac-111">La stringa restituita avrà una lunghezza di 11 caratteri nel formato "HH: mm: SS: FF" (hours, minutes, seconds, frames).</span><span class="sxs-lookup"><span data-stu-id="84bac-111">The returned string will be 11 characters long in the format "hh:mm:ss:ff" (hours, minutes, seconds, frames).</span></span>

## <a name="see-also"></a><span data-ttu-id="84bac-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="84bac-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84bac-113">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="84bac-113">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="84bac-114">**PlayAtTimeInTitle**</span><span class="sxs-lookup"><span data-stu-id="84bac-114">**PlayAtTimeInTitle**</span></span>](playattimeintitle-method.md)
</dt> </dl>

 

 



