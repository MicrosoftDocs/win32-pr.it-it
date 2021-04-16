---
description: Il metodo PlayChaptersAutoStop avvia la riproduzione nel capitolo specificato nel titolo specificato e per il numero di capitoli specificati.
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: Metodo PlayChaptersAutoStop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225380"
---
# <a name="playchaptersautostop-method"></a><span data-ttu-id="ad9b0-103">Metodo PlayChaptersAutoStop</span><span class="sxs-lookup"><span data-stu-id="ad9b0-103">PlayChaptersAutoStop Method</span></span>

> [!Note]  
> <span data-ttu-id="ad9b0-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ad9b0-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ad9b0-106">Il `PlayChaptersAutoStop` metodo avvia la riproduzione in corrispondenza del capitolo specificato nel titolo specificato e per il numero di capitoli specificati.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-106">The `PlayChaptersAutoStop` method starts playback at the specified chapter in the specified title and for the number of chapters specified.</span></span>

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a><span data-ttu-id="ad9b0-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad9b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad9b0-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="ad9b0-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="ad9b0-109">Specifica il titolo come valore intero.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b0-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="ad9b0-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="ad9b0-111">Specifica il capitolo iniziale come valore intero.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-111">Specifies the start chapter as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="ad9b0-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span><span class="sxs-lookup"><span data-stu-id="ad9b0-112"><span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*</span></span>
</dt> <dd>

<span data-ttu-id="ad9b0-113">Specifica il numero di capitoli da riprodurre come valore intero.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-113">Specifies the number of chapters to play as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad9b0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad9b0-114">Return Value</span></span>

<span data-ttu-id="ad9b0-115">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad9b0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad9b0-116">Remarks</span></span>

<span data-ttu-id="ad9b0-117">Quando l'ultimo capitolo è stato riprodotto, questo metodo fa in modo che un [**\_ capitolo del DVD \_ \_ EC**](ec-dvd-chapter-autostop.md) venga inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ad9b0-117">When the last chapter has played, this method causes an [**EC\_DVD\_CHAPTER\_AUTOSTOP**](ec-dvd-chapter-autostop.md) event notification to be sent to the application.</span></span>

 

 



