---
description: Il metodo Play riproduce il titolo del DVD corrente.
ms.assetid: fe9dc266-5b12-479d-85cb-50cc6bb9d580
title: Metodo Play (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f62323c9c86be476a35977dadf554bbfca3bca91
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521297"
---
# <a name="play-method-directshow"></a><span data-ttu-id="b07d3-103">Metodo Play (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="b07d3-103">Play Method (DirectShow)</span></span>

> [!Note]  
> <span data-ttu-id="b07d3-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b07d3-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="b07d3-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="b07d3-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="b07d3-106">Il `Play` metodo riproduce il titolo del DVD corrente.</span><span class="sxs-lookup"><span data-stu-id="b07d3-106">The `Play` method plays the current DVD title.</span></span>

``` syntax
MSWebDVD.Play()
```

## <a name="return-value"></a><span data-ttu-id="b07d3-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b07d3-107">Return Value</span></span>

<span data-ttu-id="b07d3-108">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="b07d3-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b07d3-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="b07d3-109">Remarks</span></span>

<span data-ttu-id="b07d3-110">Se la riproduzione viene sospesa o arrestata e [**EnableResetOnStop**](enableresetonstop-property.md) è true, la chiamata di **Play** riprende la riproduzione alla velocità normale nella posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="b07d3-110">If playback is paused or stopped and [**EnableResetOnStop**](enableresetonstop-property.md) is true, then calling **Play** will resume playback at normal speed at the current location.</span></span> <span data-ttu-id="b07d3-111">Se la riproduzione viene interrotta e **EnableResetOnStop** è false, la chiamata a **Play** provocherà la riproduzione del disco all'inizio del primo titolo.</span><span class="sxs-lookup"><span data-stu-id="b07d3-111">If playback is stopped and **EnableResetOnStop** is false, then calling **Play** will cause the disc to start playing at the beginning of the first title.</span></span>

## <a name="see-also"></a><span data-ttu-id="b07d3-112">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b07d3-112">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b07d3-113">**Riprendi**</span><span class="sxs-lookup"><span data-stu-id="b07d3-113">**Resume**</span></span>](resume-method.md)
</dt> </dl>

 

 



