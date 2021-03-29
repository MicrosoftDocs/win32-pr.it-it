---
description: Windows supporta formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel. La compressione riduce lo spazio di archiviazione su disco e memoria necessario per la bitmap.
ms.assetid: 14d14662-910a-4f3f-914e-6ccfc602c822
title: Compressione bitmap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38739f0e33f095b8eff567fc63b57db96b8cdc66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130854"
---
# <a name="bitmap-compression"></a><span data-ttu-id="f38a0-104">Compressione bitmap</span><span class="sxs-lookup"><span data-stu-id="f38a0-104">Bitmap Compression</span></span>

<span data-ttu-id="f38a0-105">Windows supporta formati per la compressione di bitmap che definiscono i colori con 8 o 4 bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="f38a0-105">Windows supports formats for compressing bitmaps that define their colors with 8 or 4 bits-per-pixel.</span></span> <span data-ttu-id="f38a0-106">La compressione riduce lo spazio di archiviazione su disco e memoria necessario per la bitmap.</span><span class="sxs-lookup"><span data-stu-id="f38a0-106">Compression reduces the disk and memory storage required for the bitmap.</span></span>

<span data-ttu-id="f38a0-107">Quando il membro di **compressione** della struttura dell'intestazione delle informazioni bitmap è bi \_ RLE8, viene usato un formato di codifica RLE (Run-Length Encoding) per comprimere una bitmap a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="f38a0-107">When the **Compression** member of the bitmap information header structure is BI\_RLE8, a run-length encoding (RLE) format is used to compress an 8-bit bitmap.</span></span> <span data-ttu-id="f38a0-108">Questo formato può essere compresso in modalità codificata o Absolute.</span><span class="sxs-lookup"><span data-stu-id="f38a0-108">This format can be compressed in encoded or absolute modes.</span></span> <span data-ttu-id="f38a0-109">Entrambe le modalità possono essere presenti in qualsiasi punto della stessa bitmap:</span><span class="sxs-lookup"><span data-stu-id="f38a0-109">Both modes can occur anywhere in the same bitmap:</span></span>

-   <span data-ttu-id="f38a0-110">La *modalità codificata* è costituita da due byte: il primo byte specifica il numero di pixel consecutivi da disegnare usando l'indice dei colori contenuto nel secondo byte.</span><span class="sxs-lookup"><span data-stu-id="f38a0-110">*Encoded mode* consists of two bytes: the first byte specifies the number of consecutive pixels to be drawn using the color index contained in the second byte.</span></span> <span data-ttu-id="f38a0-111">Inoltre, il primo byte della coppia può essere impostato su zero per indicare un carattere di escape che denota la fine di una riga, la fine di una bitmap o un Delta, a seconda del valore del secondo byte.</span><span class="sxs-lookup"><span data-stu-id="f38a0-111">In addition, the first byte of the pair can be set to zero to indicate an escape character that denotes the end of a line, the end of a bitmap, or a delta, depending on the value of the second byte.</span></span> <span data-ttu-id="f38a0-112">L'interpretazione dell'escape dipende dal valore del secondo byte della coppia, che può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="f38a0-112">The interpretation of the escape depends on the value of the second byte of the pair, which can be one of the following values.</span></span>



| <span data-ttu-id="f38a0-113">Valore</span><span class="sxs-lookup"><span data-stu-id="f38a0-113">Value</span></span> | <span data-ttu-id="f38a0-114">Significato</span><span class="sxs-lookup"><span data-stu-id="f38a0-114">Meaning</span></span>                                                                                                                                                     |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f38a0-115">0</span><span class="sxs-lookup"><span data-stu-id="f38a0-115">0</span></span>     | <span data-ttu-id="f38a0-116">Fine della riga.</span><span class="sxs-lookup"><span data-stu-id="f38a0-116">End of line.</span></span>                                                                                                                                                |
| <span data-ttu-id="f38a0-117">1</span><span class="sxs-lookup"><span data-stu-id="f38a0-117">1</span></span>     | <span data-ttu-id="f38a0-118">Fine della bitmap.</span><span class="sxs-lookup"><span data-stu-id="f38a0-118">End of bitmap.</span></span>                                                                                                                                              |
| <span data-ttu-id="f38a0-119">2</span><span class="sxs-lookup"><span data-stu-id="f38a0-119">2</span></span>     | <span data-ttu-id="f38a0-120">Delta.</span><span class="sxs-lookup"><span data-stu-id="f38a0-120">Delta.</span></span> <span data-ttu-id="f38a0-121">I 2 byte che seguono l'escape contengono valori senza segno che indicano gli offset orizzontali e verticali del pixel successivo dalla posizione corrente.</span><span class="sxs-lookup"><span data-stu-id="f38a0-121">The 2 bytes following the escape contain unsigned values indicating the horizontal and vertical offsets of the next pixel from the current position.</span></span> |



 

-   <span data-ttu-id="f38a0-122">In *modalità Absolute* il primo byte è zero e il secondo byte è un valore compreso nell'intervallo da 03h a FFH.</span><span class="sxs-lookup"><span data-stu-id="f38a0-122">In *absolute mode*, the first byte is zero and the second byte is a value in the range 03H through FFH.</span></span> <span data-ttu-id="f38a0-123">Il secondo byte rappresenta il numero di byte seguiti, ognuno dei quali contiene l'indice dei colori di un singolo pixel.</span><span class="sxs-lookup"><span data-stu-id="f38a0-123">The second byte represents the number of bytes that follow, each of which contains the color index of a single pixel.</span></span> <span data-ttu-id="f38a0-124">Quando il secondo byte è due o meno, l'escape ha lo stesso significato della modalità codificata.</span><span class="sxs-lookup"><span data-stu-id="f38a0-124">When the second byte is two or less, the escape has the same meaning as encoded mode.</span></span> <span data-ttu-id="f38a0-125">In modalità Absolute ogni esecuzione deve essere allineata al confine di una parola.</span><span class="sxs-lookup"><span data-stu-id="f38a0-125">In absolute mode, each run must be aligned on a word boundary.</span></span>

<span data-ttu-id="f38a0-126">Nell'esempio seguente vengono illustrati i valori esadecimali di una bitmap compressa a 8 bit:</span><span class="sxs-lookup"><span data-stu-id="f38a0-126">The following example shows the hexadecimal values of an 8-bit compressed bitmap:</span></span>


```C++
[03 04] [05 06] [00 03 45 56 67] [02 78] [00 02 05 01] 
[02 78] [00 00] [09 1E] [00 01] 
```



<span data-ttu-id="f38a0-127">La bitmap si espande come segue (i valori a due cifre rappresentano un indice dei colori per un singolo pixel):</span><span class="sxs-lookup"><span data-stu-id="f38a0-127">The bitmap expands as follows (two-digit values represent a color index for a single pixel):</span></span>


```C++
04 04 04 
06 06 06 06 06 
45 56 67 
78 78 
move current position 5 right and 1 down 
78 78 
end of line 
1E 1E 1E 1E 1E 1E 1E 1E 1E 
end of RLE bitmap 
```



<span data-ttu-id="f38a0-128">Quando il membro di **compressione** è bi \_ RLE4, la bitmap viene compressa usando un formato di codifica di lunghezza di esecuzione per una bitmap a 4 bit, che usa anche le modalità codificata e assoluta:</span><span class="sxs-lookup"><span data-stu-id="f38a0-128">When the **Compression** member is BI\_RLE4, the bitmap is compressed by using a run-length encoding format for a 4-bit bitmap, which also uses encoded and absolute modes:</span></span>

-   <span data-ttu-id="f38a0-129">In modalità codificata, il primo byte della coppia contiene il numero di pixel da disegnare usando gli indici dei colori nel secondo byte.</span><span class="sxs-lookup"><span data-stu-id="f38a0-129">In encoded mode, the first byte of the pair contains the number of pixels to be drawn using the color indexes in the second byte.</span></span> <span data-ttu-id="f38a0-130">Il secondo byte contiene due indici di colore, uno nei 4 bit di ordine superiore e uno nei 4 bit di ordine inferiore.</span><span class="sxs-lookup"><span data-stu-id="f38a0-130">The second byte contains two color indexes, one in its high-order 4 bits and one in its low-order 4 bits.</span></span> <span data-ttu-id="f38a0-131">Il primo dei pixel viene disegnato usando il colore specificato dai 4 bit più significativi, il secondo viene disegnato usando il colore nei 4 bit di ordine inferiore, il terzo viene disegnato usando il colore nei 4 bit più significativi e così via, fino a quando non vengono disegnati tutti i pixel specificati dal primo byte.</span><span class="sxs-lookup"><span data-stu-id="f38a0-131">The first of the pixels is drawn using the color specified by the high-order 4 bits, the second is drawn using the color in the low-order 4 bits, the third is drawn using the color in the high-order 4 bits, and so on, until all the pixels specified by the first byte have been drawn.</span></span>
-   <span data-ttu-id="f38a0-132">In modalità Absolute il primo byte è zero.</span><span class="sxs-lookup"><span data-stu-id="f38a0-132">In absolute mode, the first byte is zero.</span></span> <span data-ttu-id="f38a0-133">Il secondo byte contiene il numero di indici di colore che seguono.</span><span class="sxs-lookup"><span data-stu-id="f38a0-133">The second byte contains the number of color indexes that follow.</span></span> <span data-ttu-id="f38a0-134">I byte successivi contengono indici di colore nei 4 bit di ordine superiore e inferiore, un indice dei colori per ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="f38a0-134">Subsequent bytes contain color indexes in their high- and low-order 4 bits, one color index for each pixel.</span></span> <span data-ttu-id="f38a0-135">In modalità Absolute ogni esecuzione deve essere allineata al confine di una parola.</span><span class="sxs-lookup"><span data-stu-id="f38a0-135">In absolute mode, each run must be aligned on a word boundary.</span></span> <span data-ttu-id="f38a0-136">I caratteri di escape end-of-line, end-of-bitmap e Delta descritti per BI \_ RLE8 si applicano anche alla \_ compressione RLE4 di BI.</span><span class="sxs-lookup"><span data-stu-id="f38a0-136">The end-of-line, end-of-bitmap, and delta escapes described for BI\_RLE8 also apply to BI\_RLE4 compression.</span></span>

<span data-ttu-id="f38a0-137">Nell'esempio seguente vengono illustrati i valori esadecimali di una bitmap compressa a 4 bit:</span><span class="sxs-lookup"><span data-stu-id="f38a0-137">The following example shows the hexadecimal values of a 4-bit compressed bitmap:</span></span>


```C++
03 04 05 06 00 06 45 56 67 00 04 78 00 02 05 01 
04 78 00 00 09 1E 00 01 
```



<span data-ttu-id="f38a0-138">La bitmap si espande come segue (i valori a una sola cifra rappresentano un indice dei colori per un singolo pixel):</span><span class="sxs-lookup"><span data-stu-id="f38a0-138">The bitmap expands as follows (single-digit values represent a color index for a single pixel):</span></span>


```C++
0 4 0 
0 6 0 6 0 
4 5 5 6 6 7 
7 8 7 8 
move current position 5 right and 1 down 
7 8 7 8 
end of line 
1 E 1 E 1 E 1 E 1 
end of RLE bitmap 
```



 

 



