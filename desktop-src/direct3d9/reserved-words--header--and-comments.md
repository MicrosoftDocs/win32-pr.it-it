---
description: La tabella seguente mostra quali parole sono riservate e non devono essere usate.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Parole riservate, intestazione e commenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343656"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="46ca7-103">Parole riservate, intestazione e commenti</span><span class="sxs-lookup"><span data-stu-id="46ca7-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="46ca7-104">La tabella seguente mostra quali parole sono riservate e non devono essere usate.</span><span class="sxs-lookup"><span data-stu-id="46ca7-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="46ca7-105">Parole riservate</span><span class="sxs-lookup"><span data-stu-id="46ca7-105">Reserved Words</span></span> | <span data-ttu-id="46ca7-106">Parole riservate</span><span class="sxs-lookup"><span data-stu-id="46ca7-106">Reserved Words</span></span> | <span data-ttu-id="46ca7-107">Parole riservate</span><span class="sxs-lookup"><span data-stu-id="46ca7-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="46ca7-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="46ca7-108">ARRAY</span></span>            | <span data-ttu-id="46ca7-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="46ca7-109">DWORD</span></span>    | <span data-ttu-id="46ca7-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="46ca7-110">UCHAR</span></span>     |
| <span data-ttu-id="46ca7-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="46ca7-111">BINARY</span></span>           | <span data-ttu-id="46ca7-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="46ca7-112">FLOAT</span></span>    | <span data-ttu-id="46ca7-113">Ulonglong</span><span class="sxs-lookup"><span data-stu-id="46ca7-113">ULONGLONG</span></span> |
| <span data-ttu-id="46ca7-114">RISORSA \_ BINARIA</span><span class="sxs-lookup"><span data-stu-id="46ca7-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="46ca7-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="46ca7-115">SDWORD</span></span>   | <span data-ttu-id="46ca7-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="46ca7-116">UNICODE</span></span>   |
| <span data-ttu-id="46ca7-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="46ca7-117">CHAR</span></span>             | <span data-ttu-id="46ca7-118">STRING</span><span class="sxs-lookup"><span data-stu-id="46ca7-118">STRING</span></span>   | <span data-ttu-id="46ca7-119">WORD</span><span class="sxs-lookup"><span data-stu-id="46ca7-119">WORD</span></span>      |
| <span data-ttu-id="46ca7-120">Cstring</span><span class="sxs-lookup"><span data-stu-id="46ca7-120">CSTRING</span></span>          | <span data-ttu-id="46ca7-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="46ca7-121">SWORD</span></span>    |           |
| <span data-ttu-id="46ca7-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="46ca7-122">DOUBLE</span></span>           | <span data-ttu-id="46ca7-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="46ca7-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="46ca7-124">L'intestazione a lunghezza variabile è obbligatoria e deve essere all'inizio del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="46ca7-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="46ca7-125">L'intestazione contiene i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="46ca7-125">The header contains the following data.</span></span>



| <span data-ttu-id="46ca7-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="46ca7-126">Type</span></span>           | <span data-ttu-id="46ca7-127">Necessario</span><span class="sxs-lookup"><span data-stu-id="46ca7-127">Required</span></span> | <span data-ttu-id="46ca7-128">Dimensioni (in byte)</span><span class="sxs-lookup"><span data-stu-id="46ca7-128">Size (in bytes)</span></span> | <span data-ttu-id="46ca7-129">Valore</span><span class="sxs-lookup"><span data-stu-id="46ca7-129">Value</span></span> | <span data-ttu-id="46ca7-130">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46ca7-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="46ca7-131">Numero magico</span><span class="sxs-lookup"><span data-stu-id="46ca7-131">Magic Number</span></span>   | <span data-ttu-id="46ca7-132">x</span><span class="sxs-lookup"><span data-stu-id="46ca7-132">x</span></span>        | <span data-ttu-id="46ca7-133">4</span><span class="sxs-lookup"><span data-stu-id="46ca7-133">4</span></span>               | <span data-ttu-id="46ca7-134">Xof</span><span class="sxs-lookup"><span data-stu-id="46ca7-134">xof</span></span>   |                              |
| <span data-ttu-id="46ca7-135">Numero di versione</span><span class="sxs-lookup"><span data-stu-id="46ca7-135">Version Number</span></span> | <span data-ttu-id="46ca7-136">x</span><span class="sxs-lookup"><span data-stu-id="46ca7-136">x</span></span>        | <span data-ttu-id="46ca7-137">2</span><span class="sxs-lookup"><span data-stu-id="46ca7-137">2</span></span>               | <span data-ttu-id="46ca7-138">03</span><span class="sxs-lookup"><span data-stu-id="46ca7-138">03</span></span>    | <span data-ttu-id="46ca7-139">Versione principale 3</span><span class="sxs-lookup"><span data-stu-id="46ca7-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="46ca7-140">03</span><span class="sxs-lookup"><span data-stu-id="46ca7-140">03</span></span>    | <span data-ttu-id="46ca7-141">Versione secondaria 3</span><span class="sxs-lookup"><span data-stu-id="46ca7-141">Minor version 3</span></span>              |
| <span data-ttu-id="46ca7-142">Tipo di formato</span><span class="sxs-lookup"><span data-stu-id="46ca7-142">Format Type</span></span>    | <span data-ttu-id="46ca7-143">x</span><span class="sxs-lookup"><span data-stu-id="46ca7-143">x</span></span>        | <span data-ttu-id="46ca7-144">4</span><span class="sxs-lookup"><span data-stu-id="46ca7-144">4</span></span>               | <span data-ttu-id="46ca7-145">txt</span><span class="sxs-lookup"><span data-stu-id="46ca7-145">txt</span></span>   | <span data-ttu-id="46ca7-146">File di testo</span><span class="sxs-lookup"><span data-stu-id="46ca7-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="46ca7-147">bin</span><span class="sxs-lookup"><span data-stu-id="46ca7-147">bin</span></span>   | <span data-ttu-id="46ca7-148">File binario</span><span class="sxs-lookup"><span data-stu-id="46ca7-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="46ca7-149">tzip</span><span class="sxs-lookup"><span data-stu-id="46ca7-149">tzip</span></span>  | <span data-ttu-id="46ca7-150">File di testo compresso MSZip</span><span class="sxs-lookup"><span data-stu-id="46ca7-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="46ca7-151">bzip</span><span class="sxs-lookup"><span data-stu-id="46ca7-151">bzip</span></span>  | <span data-ttu-id="46ca7-152">File binario compresso MSZip</span><span class="sxs-lookup"><span data-stu-id="46ca7-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="46ca7-153">Dimensioni float</span><span class="sxs-lookup"><span data-stu-id="46ca7-153">Float Size</span></span>     | <span data-ttu-id="46ca7-154">x</span><span class="sxs-lookup"><span data-stu-id="46ca7-154">x</span></span>        | <span data-ttu-id="46ca7-155">0064</span><span class="sxs-lookup"><span data-stu-id="46ca7-155">0064</span></span>            |       | <span data-ttu-id="46ca7-156">Float a 64 bit</span><span class="sxs-lookup"><span data-stu-id="46ca7-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="46ca7-157">x</span><span class="sxs-lookup"><span data-stu-id="46ca7-157">x</span></span>        | <span data-ttu-id="46ca7-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="46ca7-158">"0032"</span></span>          |       | <span data-ttu-id="46ca7-159">Float a 32 bit</span><span class="sxs-lookup"><span data-stu-id="46ca7-159">32-bit floats</span></span>                |



 

<span data-ttu-id="46ca7-160">I valori nella tabella sono delimitati da virgolette per richiamare l'attenzione sul numero di caratteri in ogni valore.</span><span class="sxs-lookup"><span data-stu-id="46ca7-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="46ca7-161">Quelli con 4 byte contengono quattro caratteri, quelli con 2 byte contengono due caratteri.</span><span class="sxs-lookup"><span data-stu-id="46ca7-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="46ca7-162">I commenti sono applicabili solo nei file di testo.</span><span class="sxs-lookup"><span data-stu-id="46ca7-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="46ca7-163">I commenti possono essere presenti in qualsiasi punto del flusso di dati.</span><span class="sxs-lookup"><span data-stu-id="46ca7-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="46ca7-164">Un commento inizia con una doppia barra (//) in stile C++ o con un segno di cancelletto ( \# ).</span><span class="sxs-lookup"><span data-stu-id="46ca7-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="46ca7-165">Il commento viene eseguito alla nuova riga successiva.</span><span class="sxs-lookup"><span data-stu-id="46ca7-165">The comment runs to the next new line.</span></span> <span data-ttu-id="46ca7-166">L'esempio seguente mostra i commenti validi.</span><span class="sxs-lookup"><span data-stu-id="46ca7-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="46ca7-167">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="46ca7-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="46ca7-168">Codifica testo</span><span class="sxs-lookup"><span data-stu-id="46ca7-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



