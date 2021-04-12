---
description: Il metodo PlayBackwards avvia la riproduzione precedente dalla posizione corrente alla velocità specificata.
ms.assetid: 7f8421e7-f835-4a10-a9c9-0e43de159e4f
title: Metodo PlayBackwards
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b396c3829569d3f3ad25f0c0e8718dfd23f268
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480596"
---
# <a name="playbackwards-method"></a><span data-ttu-id="21826-103">Metodo PlayBackwards</span><span class="sxs-lookup"><span data-stu-id="21826-103">PlayBackwards Method</span></span>

> [!Note]  
> <span data-ttu-id="21826-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="21826-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="21826-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="21826-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="21826-106">Il `PlayBackwards` metodo avvia la riproduzione precedente dalla posizione corrente alla velocità specificata.</span><span class="sxs-lookup"><span data-stu-id="21826-106">The `PlayBackwards` method starts backward playback from the current location at the specified speed.</span></span>

``` syntax
MSWebDVD.PlayBackwards(nSpeed)
```

## <a name="parameters"></a><span data-ttu-id="21826-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="21826-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21826-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span><span class="sxs-lookup"><span data-stu-id="21826-108"><span id="nSpeed"></span><span id="nspeed"></span><span id="NSPEED"></span>*nSpeed*</span></span>
</dt> <dd>

<span data-ttu-id="21826-109">Specifica la velocità di riproduzione sotto forma di numero.</span><span class="sxs-lookup"><span data-stu-id="21826-109">Specifies the speed at which to play as a number.</span></span> <span data-ttu-id="21826-110">Questo numero è un moltiplicatore: 1.0 è la velocità di riproduzione normale; 2,0 è una doppia velocità, 0,5 è la metà della velocità e così via.</span><span class="sxs-lookup"><span data-stu-id="21826-110">This number is a multiplier—1.0 is normal playback speed; 2.0 is double speed, 0.5 is half speed, and so on.</span></span> <span data-ttu-id="21826-111">Quando **nSpeed** non è uguale a 1,0, l'audio viene disattivato e la sottoimmagine è disattivata.</span><span class="sxs-lookup"><span data-stu-id="21826-111">When **nSpeed** does not equal 1.0, audio is muted and the subpicture is turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21826-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21826-112">Return Value</span></span>

<span data-ttu-id="21826-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="21826-113">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="21826-114">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21826-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21826-115">**PlayForwards**</span><span class="sxs-lookup"><span data-stu-id="21826-115">**PlayForwards**</span></span>](playforwards-method.md)
</dt> </dl>

 

 



