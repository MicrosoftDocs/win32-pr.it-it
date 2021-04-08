---
description: Il metodo PlayForwards avvia la riproduzione dalla posizione corrente alla velocità specificata.
ms.assetid: 4f1a3e74-b343-413d-8df7-6c4bea39c62d
title: Metodo PlayForwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10d49d8d6d80613c4dd5b2b8a374002b37d9baa4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746794"
---
# <a name="playforwards-method"></a><span data-ttu-id="e1791-103">Metodo PlayForwards</span><span class="sxs-lookup"><span data-stu-id="e1791-103">PlayForwards Method</span></span>

> [!Note]  
> <span data-ttu-id="e1791-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="e1791-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e1791-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="e1791-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e1791-106">Il `PlayForwards` metodo inizia la riproduzione dalla posizione corrente alla velocità specificata.</span><span class="sxs-lookup"><span data-stu-id="e1791-106">The `PlayForwards` method starts forward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayForwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="e1791-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1791-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1791-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="e1791-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="e1791-109">Specifica la velocità di riproduzione come valore intero.</span><span class="sxs-lookup"><span data-stu-id="e1791-109">Specifies the speed at which to play as an Integer value.</span></span> <span data-ttu-id="e1791-110">Questo valore è un moltiplicatore: 1.0 è la velocità di riproduzione normale; 2,0 è una doppia velocità, 0,5 è la metà della velocità e così via.</span><span class="sxs-lookup"><span data-stu-id="e1791-110">This value is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="e1791-111">Quando **nSpeed** non è uguale a 1,0, l'audio viene disattivato e la sottoimmagine è disattivata.</span><span class="sxs-lookup"><span data-stu-id="e1791-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1791-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1791-112">Return Value</span></span>

<span data-ttu-id="e1791-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="e1791-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="e1791-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1791-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1791-115">**PlayBackwards**</span><span class="sxs-lookup"><span data-stu-id="e1791-115">**PlayBackwards**</span></span>](playbackwards-method.md)
</dt> </dl>

 

 



