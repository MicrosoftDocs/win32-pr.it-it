---
description: Il metodo PlayAtTimeInTitle avvia la riproduzione all'ora specificata nel titolo specificato.
ms.assetid: 82726885-8393-409b-b8a1-29a8e9e9ac65
title: Metodo PlayAtTimeInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c40373b4327b6df5fc341ca392c223d464a70a8b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480597"
---
# <a name="playattimeintitle-method"></a><span data-ttu-id="63e99-103">Metodo PlayAtTimeInTitle</span><span class="sxs-lookup"><span data-stu-id="63e99-103">PlayAtTimeInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="63e99-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="63e99-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="63e99-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="63e99-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="63e99-106">Il `PlayAtTimeInTitle` metodo avvia la riproduzione all'ora specificata nel titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="63e99-106">The `PlayAtTimeInTitle` method starts playback at the specified time within the specified title.</span></span>

``` syntax
MSWebDVD.PlayAtTimeInTitle(sTime, iTitle)
```

## <a name="parameters"></a><span data-ttu-id="63e99-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="63e99-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63e99-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span><span class="sxs-lookup"><span data-stu-id="63e99-108"><span id="sTime"></span><span id="stime"></span><span id="STIME"></span>*sTime*</span></span>
</dt> <dd>

<span data-ttu-id="63e99-109">Specifica l'ora in cui iniziare la riproduzione sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="63e99-109">Specifies the time at which to start playback as a string.</span></span> <span data-ttu-id="63e99-110">Il formato della stringa deve essere "HH: mm: SS: FF" (specifica di ore, minuti, secondi, fotogrammi).</span><span class="sxs-lookup"><span data-stu-id="63e99-110">The string must be in the format "hh:mm:ss:ff" (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="63e99-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="63e99-111"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="63e99-112">Specifica l'indice del titolo come intero.</span><span class="sxs-lookup"><span data-stu-id="63e99-112">Specifies the index of the title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63e99-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63e99-113">Return Value</span></span>

<span data-ttu-id="63e99-114">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="63e99-114">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="63e99-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="63e99-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e99-116">**CurrentTitle**</span><span class="sxs-lookup"><span data-stu-id="63e99-116">**CurrentTitle**</span></span>](currenttitle-property.md)
</dt> <dt>

[<span data-ttu-id="63e99-117">**PlayAtTime**</span><span class="sxs-lookup"><span data-stu-id="63e99-117">**PlayAtTime**</span></span>](playattime-method.md)
</dt> <dt>

[<span data-ttu-id="63e99-118">**TitlesAvailable**</span><span class="sxs-lookup"><span data-stu-id="63e99-118">**TitlesAvailable**</span></span>](titlesavailable-property.md)
</dt> </dl>

 

 



