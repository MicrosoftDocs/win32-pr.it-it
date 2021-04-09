---
description: L'evento ShowMenu viene inviato quando il disco Abilita o Disabilita la visualizzazione di un menu.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965713"
---
# <a name="showmenu"></a><span data-ttu-id="ef815-103">ShowMenu</span><span class="sxs-lookup"><span data-stu-id="ef815-103">ShowMenu</span></span>

> [!Note]  
> <span data-ttu-id="ef815-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="ef815-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="ef815-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="ef815-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="ef815-106">L' `ShowMenu` evento viene inviato quando il disco Abilita o Disabilita la visualizzazione di un menu.</span><span class="sxs-lookup"><span data-stu-id="ef815-106">The `ShowMenu` event is sent when the disc enables or disables the showing of a menu.</span></span>

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a><span data-ttu-id="ef815-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef815-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef815-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span><span class="sxs-lookup"><span data-stu-id="ef815-108"><span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*</span></span>
</dt> <dd>

<span data-ttu-id="ef815-109">Specifica quale menu è stato abilitato o disabilitato come valore numerico.</span><span class="sxs-lookup"><span data-stu-id="ef815-109">Specifies which menu has been enabled or disabled as a Number value.</span></span>



| <span data-ttu-id="ef815-110">Valore</span><span class="sxs-lookup"><span data-stu-id="ef815-110">Value</span></span> | <span data-ttu-id="ef815-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ef815-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ef815-112">2</span><span class="sxs-lookup"><span data-stu-id="ef815-112">2</span></span>     | <span data-ttu-id="ef815-113">Titolo</span><span class="sxs-lookup"><span data-stu-id="ef815-113">Title</span></span>       |
| <span data-ttu-id="ef815-114">3</span><span class="sxs-lookup"><span data-stu-id="ef815-114">3</span></span>     | <span data-ttu-id="ef815-115">Radice</span><span class="sxs-lookup"><span data-stu-id="ef815-115">Root</span></span>        |
| <span data-ttu-id="ef815-116">4</span><span class="sxs-lookup"><span data-stu-id="ef815-116">4</span></span>     | <span data-ttu-id="ef815-117">Sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="ef815-117">Subpicture</span></span>  |
| <span data-ttu-id="ef815-118">5</span><span class="sxs-lookup"><span data-stu-id="ef815-118">5</span></span>     | <span data-ttu-id="ef815-119">Audio</span><span class="sxs-lookup"><span data-stu-id="ef815-119">Audio</span></span>       |
| <span data-ttu-id="ef815-120">6</span><span class="sxs-lookup"><span data-stu-id="ef815-120">6</span></span>     | <span data-ttu-id="ef815-121">Angle</span><span class="sxs-lookup"><span data-stu-id="ef815-121">Angle</span></span>       |
| <span data-ttu-id="ef815-122">7</span><span class="sxs-lookup"><span data-stu-id="ef815-122">7</span></span>     | <span data-ttu-id="ef815-123">Capitolo</span><span class="sxs-lookup"><span data-stu-id="ef815-123">Chapter</span></span>     |



 

</dd> <dt>

<span data-ttu-id="ef815-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="ef815-124"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="ef815-125">Specifica se l'operazione è abilitata o disabilitata come valore booleano.</span><span class="sxs-lookup"><span data-stu-id="ef815-125">Specifies whether the operation is enabled or disabled as a Boolean.</span></span>

</dd> </dl>

 

 



