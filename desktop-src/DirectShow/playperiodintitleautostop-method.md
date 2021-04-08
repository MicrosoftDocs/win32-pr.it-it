---
description: Il metodo PlayPeriodInTitleAutoStop avvia la riproduzione all'ora specificata nel titolo specificato fino all'ora di arresto specificata.
ms.assetid: 0c4df76d-3991-4a6c-a8e5-5fd713eeffc2
title: Metodo PlayPeriodInTitleAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d05899b66b7f1a11f8f5b177d311b9634a52595b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876373"
---
# <a name="playperiodintitleautostop-method"></a><span data-ttu-id="be810-103">Metodo PlayPeriodInTitleAutoStop</span><span class="sxs-lookup"><span data-stu-id="be810-103">PlayPeriodInTitleAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="be810-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="be810-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="be810-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="be810-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="be810-106">Il `PlayPeriodInTitleAutoStop` metodo avvia la riproduzione all'ora specificata nel titolo specificato fino all'ora di arresto specificata.</span><span class="sxs-lookup"><span data-stu-id="be810-106">The `PlayPeriodInTitleAutoStop` method starts playback at the specified time in the specified title until the specified stop time.</span></span>

``` syntax
MSWebDVD.PlayPeriodInTitleAutoStop(iTitle, sStartTime, sEndTime)
```

## <a name="parameters"></a><span data-ttu-id="be810-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="be810-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be810-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="be810-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="be810-109">Specifica il titolo come intero.</span><span class="sxs-lookup"><span data-stu-id="be810-109">Specifies the title as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="be810-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span><span class="sxs-lookup"><span data-stu-id="be810-110"><span id="sStartTime"></span><span id="sstarttime"></span><span id="SSTARTTIME"></span>*sStartTime*</span></span>
</dt> <dd>

<span data-ttu-id="be810-111">Specifica l'ora di inizio come stringa nel formato "HH: mm: SS: FF" (specifica di ore, minuti, secondi, frame).</span><span class="sxs-lookup"><span data-stu-id="be810-111">Specifies the start time as a string in "hh:mm:ss:ff" format (specifying hours, minutes, seconds, frames).</span></span>

</dd> <dt>

<span data-ttu-id="be810-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span><span class="sxs-lookup"><span data-stu-id="be810-112"><span id="sEndTime"></span><span id="sendtime"></span><span id="SENDTIME"></span>*sEndTime*</span></span>
</dt> <dd>

<span data-ttu-id="be810-113">Specifica l'ora di fine come stringa nel formato "HH: mm: SS: FF".</span><span class="sxs-lookup"><span data-stu-id="be810-113">Specifies the end time as a String in "hh:mm:ss:ff" format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be810-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="be810-114">Return Value</span></span>

<span data-ttu-id="be810-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="be810-115">No return value.</span></span>

## <a name="see-also"></a><span data-ttu-id="be810-116">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="be810-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be810-117">**PlayChaptersAutoStop**</span><span class="sxs-lookup"><span data-stu-id="be810-117">**PlayChaptersAutoStop**</span></span>](playchaptersautostop-method.md)
</dt> </dl>

 

 



