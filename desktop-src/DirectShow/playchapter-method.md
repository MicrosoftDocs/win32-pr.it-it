---
description: Il metodo PlayChapter avvia la riproduzione dal capitolo specificato all'interno del titolo corrente.
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: Metodo PlayChapter
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303704"
---
# <a name="playchapter-method"></a><span data-ttu-id="ac6fb-103">Metodo PlayChapter</span><span class="sxs-lookup"><span data-stu-id="ac6fb-103">PlayChapter Method</span></span>

> [!Note]  
> <span data-ttu-id="ac6fb-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ac6fb-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ac6fb-106">Il `PlayChapter` metodo avvia la riproduzione dal capitolo specificato all'interno del titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-106">The `PlayChapter` method starts playback from the specified chapter within the current title.</span></span>

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a><span data-ttu-id="ac6fb-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ac6fb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac6fb-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span><span class="sxs-lookup"><span data-stu-id="ac6fb-108"><span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*</span></span>
</dt> <dd>

<span data-ttu-id="ac6fb-109">Specifica l'indice del capitolo nel titolo corrente come intero.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-109">Specifies the chapter index in the current title as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac6fb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ac6fb-110">Return Value</span></span>

<span data-ttu-id="ac6fb-111">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac6fb-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="ac6fb-112">Remarks</span></span>

<span data-ttu-id="ac6fb-113">Quando viene raggiunta la fine del capitolo specificato, questo metodo continua a riprodurre i capitoli successivi, se presenti.</span><span class="sxs-lookup"><span data-stu-id="ac6fb-113">When the end of the specified chapter is reached, this method continues playing subsequent chapters, if any exist.</span></span> <span data-ttu-id="ac6fb-114">Se si desidera riprodurre solo un capitolo specificato, utilizzare [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span><span class="sxs-lookup"><span data-stu-id="ac6fb-114">If you want to play only a specified chapter, use [**PlayChaptersAutoStop**](playchaptersautostop-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac6fb-115">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ac6fb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac6fb-116">**PlayChapterInTitle**</span><span class="sxs-lookup"><span data-stu-id="ac6fb-116">**PlayChapterInTitle**</span></span>](playchapterintitle-method.md)
</dt> </dl>

 

 



