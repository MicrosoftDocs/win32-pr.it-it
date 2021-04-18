---
title: Carattere Marquee
description: Carattere Marquee
ms.assetid: 037dce92-761a-4249-aca4-7d995cb15e7f
keywords:
- Interfacce di Windows Media Player Mobile, Marquees
- interfacce, Marquee
- riferimento per Skin, Marquees
- Marquees in Skins, fonts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9b912fdaa91c84b4b6ec38fcd6716f7f4b3102c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298967"
---
# <a name="marquee-font"></a><span data-ttu-id="0328a-107">Carattere Marquee</span><span class="sxs-lookup"><span data-stu-id="0328a-107">Marquee Font</span></span>

<span data-ttu-id="0328a-108">È necessario definire il tipo di carattere usato dalla casella di visualizzazione Marquee che si vuole usare.</span><span class="sxs-lookup"><span data-stu-id="0328a-108">You must define the font used by the marquee display box you wish to use.</span></span> <span data-ttu-id="0328a-109">Il tipo di carattere è definito da tre valori, separati da virgole, che rappresentano la superficie, le dimensioni e il peso del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="0328a-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="0328a-110">**Valori tipografici**</span><span class="sxs-lookup"><span data-stu-id="0328a-110">**Typeface Values**</span></span>

<span data-ttu-id="0328a-111">È possibile utilizzare qualsiasi nome tipografico se è probabile che sia installato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0328a-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="0328a-112">Se un carattere tipografico non viene trovato nel computer, verrà selezionato un alternativo dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="0328a-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="0328a-113">Nella tabella seguente vengono illustrati i caratteri tipografici di solito presenti nei dispositivi basati su Windows Mobile 2003.</span><span class="sxs-lookup"><span data-stu-id="0328a-113">The following table shows typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="0328a-114">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="0328a-114">Typeface</span></span>       | <span data-ttu-id="0328a-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0328a-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="0328a-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="0328a-116">Tahoma</span></span>         | <span data-ttu-id="0328a-117">Carattere tipografico sans-serif.</span><span class="sxs-lookup"><span data-stu-id="0328a-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="0328a-118">Console lucida</span><span class="sxs-lookup"><span data-stu-id="0328a-118">Lucida Console</span></span> | <span data-ttu-id="0328a-119">Carattere tipografico con Serif quadrato.</span><span class="sxs-lookup"><span data-stu-id="0328a-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="0328a-120">**Valori delle dimensioni**</span><span class="sxs-lookup"><span data-stu-id="0328a-120">**Size Values**</span></span>

<span data-ttu-id="0328a-121">Si tratta della dimensione del carattere tipografico nei punti.</span><span class="sxs-lookup"><span data-stu-id="0328a-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="0328a-122">Qualsiasi valore intero positivo è valido, ma sono consigliati i numeri compresi tra 10 e 18.</span><span class="sxs-lookup"><span data-stu-id="0328a-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="0328a-123">Le dimensioni minori di 10 potrebbero essere difficili da leggere e le dimensioni superiori a 18 potrebbero non dare spazio sufficiente per la visualizzazione di più lettere alla volta.</span><span class="sxs-lookup"><span data-stu-id="0328a-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not give you enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="0328a-124">**Valori di peso**</span><span class="sxs-lookup"><span data-stu-id="0328a-124">**Weight Values**</span></span>

<span data-ttu-id="0328a-125">Gli unici valori consentiti sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="0328a-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="0328a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="0328a-126">Value</span></span> | <span data-ttu-id="0328a-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0328a-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="0328a-128">B</span><span class="sxs-lookup"><span data-stu-id="0328a-128">B</span></span>     | <span data-ttu-id="0328a-129">Grassetto</span><span class="sxs-lookup"><span data-stu-id="0328a-129">Bold</span></span>        |
| <span data-ttu-id="0328a-130">N</span><span class="sxs-lookup"><span data-stu-id="0328a-130">N</span></span>     | <span data-ttu-id="0328a-131">Normale</span><span class="sxs-lookup"><span data-stu-id="0328a-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="0328a-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="0328a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0328a-133">**Testo scorrevole**</span><span class="sxs-lookup"><span data-stu-id="0328a-133">**Marquee**</span></span>](marquee.md)
</dt> </dl>

 

 




