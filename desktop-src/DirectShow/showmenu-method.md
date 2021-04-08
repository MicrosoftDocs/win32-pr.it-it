---
description: Il metodo ShowMenu Visualizza il menu specificato sullo schermo.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Metodo ShowMenu
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746786"
---
# <a name="showmenu-method"></a><span data-ttu-id="bdf21-103">Metodo ShowMenu</span><span class="sxs-lookup"><span data-stu-id="bdf21-103">ShowMenu Method</span></span>

> [!Note]  
> <span data-ttu-id="bdf21-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bdf21-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="bdf21-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="bdf21-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="bdf21-106">Il `ShowMenu` Metodo Visualizza il menu specificato sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="bdf21-106">The `ShowMenu` method displays the specified menu on the screen.</span></span>

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a><span data-ttu-id="bdf21-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdf21-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf21-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span><span class="sxs-lookup"><span data-stu-id="bdf21-108"><span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*</span></span>
</dt> <dd>

<span data-ttu-id="bdf21-109">Specifica l'ID del menu come intero.</span><span class="sxs-lookup"><span data-stu-id="bdf21-109">Specifies the menu ID as an Integer.</span></span>



| <span data-ttu-id="bdf21-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bdf21-110">Value</span></span> | <span data-ttu-id="bdf21-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdf21-111">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="bdf21-112">2</span><span class="sxs-lookup"><span data-stu-id="bdf21-112">2</span></span>     | <span data-ttu-id="bdf21-113">Titolo (inizio)</span><span class="sxs-lookup"><span data-stu-id="bdf21-113">Title (Top)</span></span> |
| <span data-ttu-id="bdf21-114">3</span><span class="sxs-lookup"><span data-stu-id="bdf21-114">3</span></span>     | <span data-ttu-id="bdf21-115">Radice</span><span class="sxs-lookup"><span data-stu-id="bdf21-115">Root</span></span>        |
| <span data-ttu-id="bdf21-116">4</span><span class="sxs-lookup"><span data-stu-id="bdf21-116">4</span></span>     | <span data-ttu-id="bdf21-117">Sottoimmagine</span><span class="sxs-lookup"><span data-stu-id="bdf21-117">Subpicture</span></span>  |
| <span data-ttu-id="bdf21-118">5</span><span class="sxs-lookup"><span data-stu-id="bdf21-118">5</span></span>     | <span data-ttu-id="bdf21-119">Audio</span><span class="sxs-lookup"><span data-stu-id="bdf21-119">Audio</span></span>       |
| <span data-ttu-id="bdf21-120">6</span><span class="sxs-lookup"><span data-stu-id="bdf21-120">6</span></span>     | <span data-ttu-id="bdf21-121">Angle</span><span class="sxs-lookup"><span data-stu-id="bdf21-121">Angle</span></span>       |
| <span data-ttu-id="bdf21-122">7</span><span class="sxs-lookup"><span data-stu-id="bdf21-122">7</span></span>     | <span data-ttu-id="bdf21-123">Capitolo</span><span class="sxs-lookup"><span data-stu-id="bdf21-123">Chapter</span></span>     |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf21-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdf21-124">Return Value</span></span>

<span data-ttu-id="bdf21-125">Nessun valore restituito.</span><span class="sxs-lookup"><span data-stu-id="bdf21-125">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf21-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdf21-126">Remarks</span></span>

<span data-ttu-id="bdf21-127">I nomi dei menu DVD possono avere un po' di confusione.</span><span class="sxs-lookup"><span data-stu-id="bdf21-127">DVD menu names can be somewhat confusing.</span></span> <span data-ttu-id="bdf21-128">Il menu titolo è un altro nome per il menu di gestione video, il menu principale per l'intero disco; Elenca in genere tutti i set di titoli video disponibili sul disco. Il menu radice è il menu per un set di titoli video, che può contenere un titolo o un gruppo di titoli.</span><span class="sxs-lookup"><span data-stu-id="bdf21-128">The title menu is another name for the Video Manager Menu, the main menu for the entire disc; it generally lists all the video title sets available on the disc. The root menu is the menu for one video title set, which can contain one title or a group of titles.</span></span> <span data-ttu-id="bdf21-129">Tutti i titoli di un set di titoli condividono lo stesso menu di immagine, audio e angolo.</span><span class="sxs-lookup"><span data-stu-id="bdf21-129">All the titles in a title set share the same Subpicture, Audio, and Angle menus.</span></span>

 

 



