---
title: Porting di chiamate del buffer di accumulo
description: È necessario allocare il buffer di accumulo richiedendo il formato pixel appropriato con la funzione OpenGL auxInitDisplayMode o ChoosePixelFormat.
ms.assetid: 523728ce-4aae-4247-a3dc-23864231cad1
keywords:
- Porting di IRIS GL, buffer di accumulo
- porting da IRIS GL, buffer di accumulo
- porting in OpenGL da IRIS GL, buffer di accumulo
- Porting OpenGL da IRIS GL, buffer di accumulo
- buffer di accumulo OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca91cb3ba35535ba2470297070dffc932a1c33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104222082"
---
# <a name="porting-accumulation-buffer-calls"></a><span data-ttu-id="9a335-108">Porting di chiamate del buffer di accumulo</span><span class="sxs-lookup"><span data-stu-id="9a335-108">Porting Accumulation Buffer Calls</span></span>

<span data-ttu-id="9a335-109">È necessario allocare il buffer di accumulo richiedendo il formato pixel appropriato con la funzione OpenGL **auxInitDisplayMode** o [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) .</span><span class="sxs-lookup"><span data-stu-id="9a335-109">You must allocate your accumulation buffer by requesting the appropriate pixel format with the OpenGL **auxInitDisplayMode** or [**ChoosePixelFormat**](/windows/desktop/api/wingdi/nf-wingdi-choosepixelformat) function.</span></span> <span data-ttu-id="9a335-110">La tabella seguente elenca le funzioni di IRIS GL che interessano il buffer di accumulo e le relative funzioni OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9a335-110">The following table lists IRIS GL functions that affect the accumulation buffer and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="9a335-111">Funzione IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9a335-111">IRIS GL function</span></span>       | <span data-ttu-id="9a335-112">OpenGL (funzione)</span><span class="sxs-lookup"><span data-stu-id="9a335-112">OpenGL function</span></span>                                       | <span data-ttu-id="9a335-113">Significato</span><span class="sxs-lookup"><span data-stu-id="9a335-113">Meaning</span></span>                                                                       |
|------------------------|-------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="9a335-114">**acsize**</span><span class="sxs-lookup"><span data-stu-id="9a335-114">**acsize**</span></span>             | <span data-ttu-id="9a335-115">**auxInitDisplayMode** o **ChoosePixelFormat**</span><span class="sxs-lookup"><span data-stu-id="9a335-115">**auxInitDisplayMode** or **ChoosePixelFormat**</span></span>       | <span data-ttu-id="9a335-116">Specifica il numero di bitplane per ogni componente colore nel buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="9a335-116">Specifies number of bitplanes per color component in the accumulation buffer.</span></span> |
| <span data-ttu-id="9a335-117">**acbuf**</span><span class="sxs-lookup"><span data-stu-id="9a335-117">**acbuf**</span></span>              | [<span data-ttu-id="9a335-118">**glAccum**</span><span class="sxs-lookup"><span data-stu-id="9a335-118">**glAccum**</span></span>](glaccum.md)                            | <span data-ttu-id="9a335-119">Opera sul buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="9a335-119">Operates on the accumulation buffer.</span></span>                                          |
|                        | [<span data-ttu-id="9a335-120">**glClearAccum**</span><span class="sxs-lookup"><span data-stu-id="9a335-120">**glClearAccum**</span></span>](glclearaccum.md)                  | <span data-ttu-id="9a335-121">Imposta i valori cancellati per il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="9a335-121">Sets clear values for accumulation buffer.</span></span>                                    |
| <span data-ttu-id="9a335-122">**acbuf**( \_ Clear AC)</span><span class="sxs-lookup"><span data-stu-id="9a335-122">**acbuf**( AC\_CLEAR )</span></span> | <span data-ttu-id="9a335-123">[**glClear**](glclear.md) ( \_ bit del buffer di accut GL \_ \_ )</span><span class="sxs-lookup"><span data-stu-id="9a335-123">[**glClear**](glclear.md) ( GL\_ACCUM\_BUFFER\_BIT )</span></span> | <span data-ttu-id="9a335-124">Cancella il buffer di accumulo.</span><span class="sxs-lookup"><span data-stu-id="9a335-124">Clears the accumulation buffer.</span></span>                                               |



 

<span data-ttu-id="9a335-125">La tabella seguente elenca i parametri **acbuf** di Iris GL insieme ai parametri [**glAccum**](glaccum.md) OpenGL equivalenti.</span><span class="sxs-lookup"><span data-stu-id="9a335-125">The following table lists the IRIS GL **acbuf** parameters along with the equivalent OpenGL [**glAccum**](glaccum.md) parameters.</span></span>



| <span data-ttu-id="9a335-126">Parametro di IRIS GL</span><span class="sxs-lookup"><span data-stu-id="9a335-126">IRIS GL parameter</span></span>     | <span data-ttu-id="9a335-127">Parametro OpenGL</span><span class="sxs-lookup"><span data-stu-id="9a335-127">OpenGL parameter</span></span> |
|-----------------------|------------------|
| <span data-ttu-id="9a335-128">\_accumulo AC</span><span class="sxs-lookup"><span data-stu-id="9a335-128">AC\_ACCUMULATE</span></span>        | <span data-ttu-id="9a335-129">\_Accue GL</span><span class="sxs-lookup"><span data-stu-id="9a335-129">GL\_ACCUM</span></span>        |
| <span data-ttu-id="9a335-130">\_ \_ accumulo Clear AC</span><span class="sxs-lookup"><span data-stu-id="9a335-130">AC\_CLEAR\_ACCUMULATE</span></span> | <span data-ttu-id="9a335-131">\_carico GL</span><span class="sxs-lookup"><span data-stu-id="9a335-131">GL\_LOAD</span></span>         |
| <span data-ttu-id="9a335-132">\_ritorno AC</span><span class="sxs-lookup"><span data-stu-id="9a335-132">AC\_RETURN</span></span>            | <span data-ttu-id="9a335-133">\_return GL</span><span class="sxs-lookup"><span data-stu-id="9a335-133">GL\_RETURN</span></span>       |
| <span data-ttu-id="9a335-134">\_mult AC</span><span class="sxs-lookup"><span data-stu-id="9a335-134">AC\_MULT</span></span>              | <span data-ttu-id="9a335-135">\_mult</span><span class="sxs-lookup"><span data-stu-id="9a335-135">GL\_MULT</span></span>         |
| <span data-ttu-id="9a335-136">\_aggiunta CA</span><span class="sxs-lookup"><span data-stu-id="9a335-136">AC\_ADD</span></span>               | <span data-ttu-id="9a335-137">Aggiunta di GL \_</span><span class="sxs-lookup"><span data-stu-id="9a335-137">GL\_ADD</span></span>          |



 

 

 




