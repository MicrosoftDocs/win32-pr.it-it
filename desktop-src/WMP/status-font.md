---
title: Carattere stato
description: Carattere stato
ms.assetid: eba697e8-8be5-4692-b7b2-a52c5642022a
keywords:
- Interfacce di Windows Media Player Mobile, visualizzazione dello stato
- interfacce, visualizzazione stato
- informazioni di riferimento per Skins, status display
- visualizzazione dello stato in interfacce, tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5a773f3baaeda0eaa90dfe0702957b5b7888271
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955745"
---
# <a name="status-font"></a><span data-ttu-id="ddb57-107">Carattere stato</span><span class="sxs-lookup"><span data-stu-id="ddb57-107">Status Font</span></span>

<span data-ttu-id="ddb57-108">È necessario definire il tipo di carattere utilizzato dalla visualizzazione di stato che si desidera utilizzare.</span><span class="sxs-lookup"><span data-stu-id="ddb57-108">You must define the font used by the status display you wish to use.</span></span> <span data-ttu-id="ddb57-109">Il tipo di carattere è definito da tre valori, separati da virgole, che rappresentano la superficie, le dimensioni e il peso del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="ddb57-109">The font is defined by three values, separated by commas, representing the face, size, and weight of the font.</span></span>

<span data-ttu-id="ddb57-110">**Valori tipografici**</span><span class="sxs-lookup"><span data-stu-id="ddb57-110">**Typeface Values**</span></span>

<span data-ttu-id="ddb57-111">È possibile utilizzare qualsiasi nome tipografico se è probabile che sia installato nel computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ddb57-111">Any typeface name can be used if it is likely to be installed on the user's machine.</span></span> <span data-ttu-id="ddb57-112">Se un carattere tipografico non viene trovato nel computer, verrà selezionato un alternativo dal sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ddb57-112">If a typeface is not found on the machine, an alternate will be selected by the operating system.</span></span> <span data-ttu-id="ddb57-113">Nella tabella seguente vengono illustrati i caratteri tipografici di solito presenti nei dispositivi basati su Windows Mobile 2003.</span><span class="sxs-lookup"><span data-stu-id="ddb57-113">The following table shows the typefaces that are usually found on Windows Mobile 2003-based devices.</span></span>



| <span data-ttu-id="ddb57-114">Tipo di carattere</span><span class="sxs-lookup"><span data-stu-id="ddb57-114">Typeface</span></span>       | <span data-ttu-id="ddb57-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddb57-115">Description</span></span>              |
|----------------|--------------------------|
| <span data-ttu-id="ddb57-116">Tahoma</span><span class="sxs-lookup"><span data-stu-id="ddb57-116">Tahoma</span></span>         | <span data-ttu-id="ddb57-117">Carattere tipografico sans-serif.</span><span class="sxs-lookup"><span data-stu-id="ddb57-117">A sans-serif typeface.</span></span>   |
| <span data-ttu-id="ddb57-118">Console lucida</span><span class="sxs-lookup"><span data-stu-id="ddb57-118">Lucida Console</span></span> | <span data-ttu-id="ddb57-119">Carattere tipografico con Serif quadrato.</span><span class="sxs-lookup"><span data-stu-id="ddb57-119">A square-serif typeface.</span></span> |



 

<span data-ttu-id="ddb57-120">**Valori delle dimensioni**</span><span class="sxs-lookup"><span data-stu-id="ddb57-120">**Size Values**</span></span>

<span data-ttu-id="ddb57-121">Si tratta della dimensione del carattere tipografico nei punti.</span><span class="sxs-lookup"><span data-stu-id="ddb57-121">This is the size of the typeface in points.</span></span> <span data-ttu-id="ddb57-122">Qualsiasi valore intero positivo è valido, ma sono consigliati i numeri compresi tra 10 e 18.</span><span class="sxs-lookup"><span data-stu-id="ddb57-122">Any positive integer value is valid, though numbers between 10 and 18 are recommended.</span></span> <span data-ttu-id="ddb57-123">Le dimensioni minori di 10 potrebbero essere difficili da leggere e le dimensioni superiori a 18 potrebbero non lasciare spazio sufficiente per la visualizzazione di più lettere alla volta.</span><span class="sxs-lookup"><span data-stu-id="ddb57-123">Sizes smaller than 10 may be difficult to read, and sizes above 18 may not leave enough space to display more than a few letters at a time.</span></span>

<span data-ttu-id="ddb57-124">**Valori di peso**</span><span class="sxs-lookup"><span data-stu-id="ddb57-124">**Weight Values**</span></span>

<span data-ttu-id="ddb57-125">Gli unici valori consentiti sono riportati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ddb57-125">The only values allowed are shown in the following table.</span></span>



| <span data-ttu-id="ddb57-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ddb57-126">Value</span></span> | <span data-ttu-id="ddb57-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ddb57-127">Description</span></span> |
|-------|-------------|
| <span data-ttu-id="ddb57-128">B</span><span class="sxs-lookup"><span data-stu-id="ddb57-128">B</span></span>     | <span data-ttu-id="ddb57-129">Grassetto</span><span class="sxs-lookup"><span data-stu-id="ddb57-129">Bold</span></span>        |
| <span data-ttu-id="ddb57-130">N</span><span class="sxs-lookup"><span data-stu-id="ddb57-130">N</span></span>     | <span data-ttu-id="ddb57-131">Normale</span><span class="sxs-lookup"><span data-stu-id="ddb57-131">Normal</span></span>      |



 

## <a name="related-topics"></a><span data-ttu-id="ddb57-132">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ddb57-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddb57-133">**Stato**</span><span class="sxs-lookup"><span data-stu-id="ddb57-133">**Status**</span></span>](status.md)
</dt> </dl>

 

 




