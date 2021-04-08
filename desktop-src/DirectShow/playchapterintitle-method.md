---
description: Il metodo PlayChapterInTitle riproduce il capitolo specificato nel titolo specificato.
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: Metodo PlayChapterInTitle
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875905"
---
# <a name="playchapterintitle-method"></a><span data-ttu-id="fe328-103">Metodo PlayChapterInTitle</span><span class="sxs-lookup"><span data-stu-id="fe328-103">PlayChapterInTitle Method</span></span>

> [!Note]  
> <span data-ttu-id="fe328-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="fe328-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fe328-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="fe328-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fe328-106">Il `PlayChapterInTitle` metodo riproduce il capitolo specificato nel titolo specificato.</span><span class="sxs-lookup"><span data-stu-id="fe328-106">The `PlayChapterInTitle` method plays the specified chapter in the specified title.</span></span>

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a><span data-ttu-id="fe328-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="fe328-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe328-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span><span class="sxs-lookup"><span data-stu-id="fe328-108"><span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*</span></span>
</dt> <dd>

<span data-ttu-id="fe328-109">Specifica il titolo come valore intero.</span><span class="sxs-lookup"><span data-stu-id="fe328-109">Specifies the title as an Integer value.</span></span>

</dd> <dt>

<span data-ttu-id="fe328-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="fe328-110"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="fe328-111">Specifica il capitolo come valore intero.</span><span class="sxs-lookup"><span data-stu-id="fe328-111">Specifies the chapter as an Integer value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe328-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fe328-112">Return Value</span></span>

<span data-ttu-id="fe328-113">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="fe328-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe328-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="fe328-114">Remarks</span></span>

<span data-ttu-id="fe328-115">Questo metodo avvia la riproduzione nel capitolo specificato e continua la riproduzione a tempo indefinito.</span><span class="sxs-lookup"><span data-stu-id="fe328-115">This method starts playback at the specified chapter and then continues playing indefinitely.</span></span> <span data-ttu-id="fe328-116">Per riprodurre solo un determinato capitolo, usare [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="fe328-116">If you want to play only a particular chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

 

 



