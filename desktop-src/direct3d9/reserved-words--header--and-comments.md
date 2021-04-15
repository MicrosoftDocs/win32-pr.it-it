---
description: La tabella seguente mostra quali parole sono riservate e non devono essere usate.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Parole riservate, intestazioni e commenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520889"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="ad5b9-103">Parole riservate, intestazioni e commenti</span><span class="sxs-lookup"><span data-stu-id="ad5b9-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="ad5b9-104">La tabella seguente mostra quali parole sono riservate e non devono essere usate.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="ad5b9-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="ad5b9-105">ARRAY</span></span>            | <span data-ttu-id="ad5b9-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="ad5b9-106">DWORD</span></span>    | <span data-ttu-id="ad5b9-107">UCHAR</span><span class="sxs-lookup"><span data-stu-id="ad5b9-107">UCHAR</span></span>     |
| <span data-ttu-id="ad5b9-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="ad5b9-108">BINARY</span></span>           | <span data-ttu-id="ad5b9-109">FLOAT</span><span class="sxs-lookup"><span data-stu-id="ad5b9-109">FLOAT</span></span>    | <span data-ttu-id="ad5b9-110">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="ad5b9-110">ULONGLONG</span></span> |
| <span data-ttu-id="ad5b9-111">risorsa BINARIa \_</span><span class="sxs-lookup"><span data-stu-id="ad5b9-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="ad5b9-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="ad5b9-112">SDWORD</span></span>   | <span data-ttu-id="ad5b9-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="ad5b9-113">UNICODE</span></span>   |
| <span data-ttu-id="ad5b9-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="ad5b9-114">CHAR</span></span>             | <span data-ttu-id="ad5b9-115">STRING</span><span class="sxs-lookup"><span data-stu-id="ad5b9-115">STRING</span></span>   | <span data-ttu-id="ad5b9-116">WORD</span><span class="sxs-lookup"><span data-stu-id="ad5b9-116">WORD</span></span>      |
| <span data-ttu-id="ad5b9-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="ad5b9-117">CSTRING</span></span>          | <span data-ttu-id="ad5b9-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="ad5b9-118">SWORD</span></span>    |           |
| <span data-ttu-id="ad5b9-119">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="ad5b9-119">DOUBLE</span></span>           | <span data-ttu-id="ad5b9-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="ad5b9-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="ad5b9-121">L'intestazione a lunghezza variabile è obbligatoria e deve trovarsi all'inizio del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="ad5b9-122">L'intestazione contiene i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-122">The header contains the following data.</span></span>



| <span data-ttu-id="ad5b9-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad5b9-123">Type</span></span>           | <span data-ttu-id="ad5b9-124">Necessario</span><span class="sxs-lookup"><span data-stu-id="ad5b9-124">Required</span></span> | <span data-ttu-id="ad5b9-125">Dimensioni (in byte)</span><span class="sxs-lookup"><span data-stu-id="ad5b9-125">Size (in bytes)</span></span> | <span data-ttu-id="ad5b9-126">Valore</span><span class="sxs-lookup"><span data-stu-id="ad5b9-126">Value</span></span> | <span data-ttu-id="ad5b9-127">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad5b9-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="ad5b9-128">Numero magico</span><span class="sxs-lookup"><span data-stu-id="ad5b9-128">Magic Number</span></span>   | <span data-ttu-id="ad5b9-129">x</span><span class="sxs-lookup"><span data-stu-id="ad5b9-129">x</span></span>        | <span data-ttu-id="ad5b9-130">4</span><span class="sxs-lookup"><span data-stu-id="ad5b9-130">4</span></span>               | <span data-ttu-id="ad5b9-131">XOF</span><span class="sxs-lookup"><span data-stu-id="ad5b9-131">xof</span></span>   |                              |
| <span data-ttu-id="ad5b9-132">Numero di versione</span><span class="sxs-lookup"><span data-stu-id="ad5b9-132">Version Number</span></span> | <span data-ttu-id="ad5b9-133">x</span><span class="sxs-lookup"><span data-stu-id="ad5b9-133">x</span></span>        | <span data-ttu-id="ad5b9-134">2</span><span class="sxs-lookup"><span data-stu-id="ad5b9-134">2</span></span>               | <span data-ttu-id="ad5b9-135">03</span><span class="sxs-lookup"><span data-stu-id="ad5b9-135">03</span></span>    | <span data-ttu-id="ad5b9-136">Versione principale 3</span><span class="sxs-lookup"><span data-stu-id="ad5b9-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="ad5b9-137">03</span><span class="sxs-lookup"><span data-stu-id="ad5b9-137">03</span></span>    | <span data-ttu-id="ad5b9-138">Versione secondaria 3</span><span class="sxs-lookup"><span data-stu-id="ad5b9-138">Minor version 3</span></span>              |
| <span data-ttu-id="ad5b9-139">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="ad5b9-139">Format Type</span></span>    | <span data-ttu-id="ad5b9-140">x</span><span class="sxs-lookup"><span data-stu-id="ad5b9-140">x</span></span>        | <span data-ttu-id="ad5b9-141">4</span><span class="sxs-lookup"><span data-stu-id="ad5b9-141">4</span></span>               | <span data-ttu-id="ad5b9-142">txt</span><span class="sxs-lookup"><span data-stu-id="ad5b9-142">txt</span></span>   | <span data-ttu-id="ad5b9-143">File di testo</span><span class="sxs-lookup"><span data-stu-id="ad5b9-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="ad5b9-144">bin</span><span class="sxs-lookup"><span data-stu-id="ad5b9-144">bin</span></span>   | <span data-ttu-id="ad5b9-145">File binario</span><span class="sxs-lookup"><span data-stu-id="ad5b9-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="ad5b9-146">tzip</span><span class="sxs-lookup"><span data-stu-id="ad5b9-146">tzip</span></span>  | <span data-ttu-id="ad5b9-147">File di testo compresso MSZip</span><span class="sxs-lookup"><span data-stu-id="ad5b9-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="ad5b9-148">bzip</span><span class="sxs-lookup"><span data-stu-id="ad5b9-148">bzip</span></span>  | <span data-ttu-id="ad5b9-149">File binario compresso MSZip</span><span class="sxs-lookup"><span data-stu-id="ad5b9-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="ad5b9-150">Dimensioni float</span><span class="sxs-lookup"><span data-stu-id="ad5b9-150">Float Size</span></span>     | <span data-ttu-id="ad5b9-151">x</span><span class="sxs-lookup"><span data-stu-id="ad5b9-151">x</span></span>        | <span data-ttu-id="ad5b9-152">0064</span><span class="sxs-lookup"><span data-stu-id="ad5b9-152">0064</span></span>            |       | <span data-ttu-id="ad5b9-153">float a 64 bit</span><span class="sxs-lookup"><span data-stu-id="ad5b9-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="ad5b9-154">x</span><span class="sxs-lookup"><span data-stu-id="ad5b9-154">x</span></span>        | <span data-ttu-id="ad5b9-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="ad5b9-155">"0032"</span></span>          |       | <span data-ttu-id="ad5b9-156">float a 32 bit</span><span class="sxs-lookup"><span data-stu-id="ad5b9-156">32-bit floats</span></span>                |



 

<span data-ttu-id="ad5b9-157">I valori nella tabella sono delimitati da virgolette per richiamare l'attenzione sul numero di caratteri in ogni valore.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="ad5b9-158">Quelli con 4 byte contengono quattro caratteri, quelli con 2 byte contengono due caratteri.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="ad5b9-159">I commenti sono applicabili solo ai file di testo.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="ad5b9-160">I commenti possono essere presenti in qualsiasi punto del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="ad5b9-161">Un commento inizia con le barre doppie (//) di tipo C++ o con un segno di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="ad5b9-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="ad5b9-162">Il commento viene eseguito alla nuova riga successiva.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-162">The comment runs to the next new line.</span></span> <span data-ttu-id="ad5b9-163">Nell'esempio seguente vengono illustrati i commenti validi.</span><span class="sxs-lookup"><span data-stu-id="ad5b9-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="ad5b9-164">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ad5b9-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ad5b9-165">Codifica testo</span><span class="sxs-lookup"><span data-stu-id="ad5b9-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



