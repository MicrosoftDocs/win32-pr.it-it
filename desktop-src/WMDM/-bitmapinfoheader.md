---
title: Struttura _BITMAPINFOHEADER
description: La \_ struttura BITMAPINFOHEADER definisce il formato di un frame video.
ms.assetid: 394b8ded-81db-4ad3-8cf7-086f1e832771
keywords:
- Struttura di _BITMAPINFOHEADER Windows Media Gestione dispositivi
topic_type:
- apiref
api_name:
- _BITMAPINFOHEADER
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 481c80b6d209e0da8d00ef06d88392504bcae8e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331904"
---
# <a name="_bitmapinfoheader-structure"></a><span data-ttu-id="7b706-104">\_Struttura BITMAPINFOHEADER</span><span class="sxs-lookup"><span data-stu-id="7b706-104">\_BITMAPINFOHEADER structure</span></span>

<span data-ttu-id="7b706-105">La struttura **\_ BITMAPINFOHEADER** definisce il formato di un frame video.</span><span class="sxs-lookup"><span data-stu-id="7b706-105">The **\_BITMAPINFOHEADER** structure defines the format of a video frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b706-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b706-106">Syntax</span></span>


```C++
typedef struct _tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} _BITMAPINFOHEADER;
```



## <a name="members"></a><span data-ttu-id="7b706-107">Members</span><span class="sxs-lookup"><span data-stu-id="7b706-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b706-108">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="7b706-108">**biSize**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-109">Specifica il numero di byte necessari per la struttura.</span><span class="sxs-lookup"><span data-stu-id="7b706-109">Specifies the number of bytes required by the structure.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-110">**biWidth**</span><span class="sxs-lookup"><span data-stu-id="7b706-110">**biWidth**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-111">Specifica la larghezza della bitmap in pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-111">Specifies the width of the bitmap, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-112">**bialtezza**</span><span class="sxs-lookup"><span data-stu-id="7b706-112">**biHeight**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-113">Specifica l'altezza della bitmap in pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-113">Specifies the height of the bitmap, in pixels.</span></span> <span data-ttu-id="7b706-114">Se **biHeight** è positivo, la bitmap è un valore DIB bottom-up e la relativa origine è l'angolo inferiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="7b706-114">If **biHeight** is positive, the bitmap is a bottom-up DIB and its origin is the lower-left corner.</span></span> <span data-ttu-id="7b706-115">Se **biHeight** è negativo, la bitmap è un DIB dall'alto verso il basso e l'origine è l'angolo superiore sinistro.</span><span class="sxs-lookup"><span data-stu-id="7b706-115">If **biHeight** is negative, the bitmap is a top-down DIB and its origin is the upper-left corner.</span></span> <span data-ttu-id="7b706-116">Se **biHeight** è un valore negativo, a indicare una DIB dall'alto verso il basso, la **bicompressione** deve essere bi \_ RGB o bi \_ campi.</span><span class="sxs-lookup"><span data-stu-id="7b706-116">If **biHeight** is negative, indicating a top-down DIB, **biCompression** must be either BI\_RGB or BI\_BITFIELDS.</span></span> <span data-ttu-id="7b706-117">Non è possibile comprimere l'inizio dell'attività.</span><span class="sxs-lookup"><span data-stu-id="7b706-117">Top-down DIBs cannot be compressed.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-118">**Biplani**</span><span class="sxs-lookup"><span data-stu-id="7b706-118">**biPlanes**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-119">Specifica il numero di piani per il dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7b706-119">Specifies the number of planes for the target device.</span></span> <span data-ttu-id="7b706-120">Questo valore deve essere impostato su 1.</span><span class="sxs-lookup"><span data-stu-id="7b706-120">This value must be set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-121">**biBitCount**</span><span class="sxs-lookup"><span data-stu-id="7b706-121">**biBitCount**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-122">Specifica il numero di bit per pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-122">Specifies the number of bits per pixel.</span></span> <span data-ttu-id="7b706-123">Il membro **biBitCount** della struttura **BITMAPINFOHEADER** determina il numero di bit che definiscono ogni pixel e il numero massimo di colori nella bitmap.</span><span class="sxs-lookup"><span data-stu-id="7b706-123">The **biBitCount** member of the **BITMAPINFOHEADER** structure determines the number of bits that define each pixel and the maximum number of colors in the bitmap.</span></span> <span data-ttu-id="7b706-124">Questo membro deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b706-124">This member must be one of the following values.</span></span>



| <span data-ttu-id="7b706-125">Valore</span><span class="sxs-lookup"><span data-stu-id="7b706-125">Value</span></span> | <span data-ttu-id="7b706-126">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b706-126">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b706-127">1</span><span class="sxs-lookup"><span data-stu-id="7b706-127">1</span></span>     | <span data-ttu-id="7b706-128">La bitmap è monocromatica e il membro bmiColors contiene due voci.</span><span class="sxs-lookup"><span data-stu-id="7b706-128">The bitmap is monochrome, and the bmiColors member contains two entries.</span></span> <span data-ttu-id="7b706-129">Ogni bit nella matrice bitmap rappresenta un pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-129">Each bit in the bitmap array represents a pixel.</span></span> <span data-ttu-id="7b706-130">Se il bit è chiaro, il pixel viene visualizzato con il colore della prima voce nella tabella bmiColors. Se viene impostato il bit, il pixel presenta il colore della seconda voce della tabella.</span><span class="sxs-lookup"><span data-stu-id="7b706-130">If the bit is clear, the pixel is displayed with the color of the first entry in the bmiColors table; if the bit is set, the pixel has the color of the second entry in the table.</span></span>                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7b706-131">2</span><span class="sxs-lookup"><span data-stu-id="7b706-131">2</span></span>     | <span data-ttu-id="7b706-132">La bitmap ha quattro valori di colore possibili.</span><span class="sxs-lookup"><span data-stu-id="7b706-132">The bitmap has four possible color values.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="7b706-133">4</span><span class="sxs-lookup"><span data-stu-id="7b706-133">4</span></span>     | <span data-ttu-id="7b706-134">La bitmap ha un massimo di 16 colori e il membro bmiColors contiene fino a 16 voci.</span><span class="sxs-lookup"><span data-stu-id="7b706-134">The bitmap has a maximum of 16 colors, and the bmiColors member contains up to 16 entries.</span></span> <span data-ttu-id="7b706-135">Ogni pixel della bitmap è rappresentato da un indice a 4 bit nella tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="7b706-135">Each pixel in the bitmap is represented by a 4-bit index into the color table.</span></span> <span data-ttu-id="7b706-136">Se, ad esempio, il primo byte nella bitmap è 0x1F, il byte rappresenta due pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-136">For example, if the first byte in the bitmap is 0x1F, the byte represents two pixels.</span></span> <span data-ttu-id="7b706-137">Il primo pixel contiene il colore nella seconda voce della tabella e il secondo pixel contiene il colore nella voce della tabella sedicesimo.</span><span class="sxs-lookup"><span data-stu-id="7b706-137">The first pixel contains the color in the second table entry, and the second pixel contains the color in the sixteenth table entry.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="7b706-138">8</span><span class="sxs-lookup"><span data-stu-id="7b706-138">8</span></span>     | <span data-ttu-id="7b706-139">La bitmap ha un massimo di 256 colori e il membro bmiColors contiene fino a 256 voci.</span><span class="sxs-lookup"><span data-stu-id="7b706-139">The bitmap has a maximum of 256 colors, and the bmiColors member contains up to 256 entries.</span></span> <span data-ttu-id="7b706-140">In questo caso, ogni byte della matrice rappresenta un singolo pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-140">In this case, each byte in the array represents a single pixel.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7b706-141">16</span><span class="sxs-lookup"><span data-stu-id="7b706-141">16</span></span>    | <span data-ttu-id="7b706-142">La bitmap ha un massimo di 2 ^ 16 colori.</span><span class="sxs-lookup"><span data-stu-id="7b706-142">The bitmap has a maximum of 2^16 colors.</span></span> <span data-ttu-id="7b706-143">Se il membro della bicompressione di BITMAPINFOHEADER è BI \_ RGB, il membro bmiColors è **null**.</span><span class="sxs-lookup"><span data-stu-id="7b706-143">If the biCompression member of the BITMAPINFOHEADER is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="7b706-144">Ogni parola nella matrice bitmap rappresenta un singolo pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-144">Each WORD in the bitmap array represents a single pixel.</span></span> <span data-ttu-id="7b706-145">Le intensità relative di rosso, verde e blu sono rappresentate da 5 bit per ogni componente colore.</span><span class="sxs-lookup"><span data-stu-id="7b706-145">The relative intensities of red, green, and blue are represented with 5 bits for each color component.</span></span> <span data-ttu-id="7b706-146">Il valore per il blu è nei 5 bit meno significativi, seguito da 5 bit ciascuno per il verde e il rosso.</span><span class="sxs-lookup"><span data-stu-id="7b706-146">The value for blue is in the least significant 5 bits, followed by 5 bits each for green and red.</span></span> <span data-ttu-id="7b706-147">Il bit più significativo non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7b706-147">The most significant bit is not used.</span></span> <span data-ttu-id="7b706-148">La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="7b706-148">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span> |
| <span data-ttu-id="7b706-149">24</span><span class="sxs-lookup"><span data-stu-id="7b706-149">24</span></span>    | <span data-ttu-id="7b706-150">La bitmap ha un massimo di 2 ^ 24 colori e il membro bmiColors è **null**.</span><span class="sxs-lookup"><span data-stu-id="7b706-150">The bitmap has a maximum of 2^24 colors, and the bmiColors member is **NULL**.</span></span> <span data-ttu-id="7b706-151">Ogni tripletta a 3 byte nella matrice di bitmap rappresenta le intensità relative rispettivamente di blu, verde e rosso per un pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-151">Each 3-byte triplet in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="7b706-152">La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="7b706-152">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="7b706-153">32</span><span class="sxs-lookup"><span data-stu-id="7b706-153">32</span></span>    | <span data-ttu-id="7b706-154">La bitmap ha un massimo di 2 ^ 32 colori.</span><span class="sxs-lookup"><span data-stu-id="7b706-154">The bitmap has a maximum of 2^32 colors.</span></span> <span data-ttu-id="7b706-155">Se il membro di biCompression è BI \_ RGB, il membro bmiColors è **null**.</span><span class="sxs-lookup"><span data-stu-id="7b706-155">If the biCompression member is BI\_RGB, the bmiColors member is **NULL**.</span></span> <span data-ttu-id="7b706-156">Ogni valore DWORD nella matrice di bitmap rappresenta le intensità relative di un pixel, rispettivamente blu, verde e rosso.</span><span class="sxs-lookup"><span data-stu-id="7b706-156">Each DWORD in the bitmap array represents the relative intensities of blue, green, and red, respectively, for a pixel.</span></span> <span data-ttu-id="7b706-157">Il byte elevato in ogni DWORD non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="7b706-157">The high byte in each DWORD is not used.</span></span> <span data-ttu-id="7b706-158">La tabella dei colori bmiColors viene utilizzata per l'ottimizzazione dei colori utilizzati nei dispositivi basati su tavolozza e deve contenere il numero di voci specificate dal membro biClrUsed.</span><span class="sxs-lookup"><span data-stu-id="7b706-158">The bmiColors color table is used for optimizing colors used on palette-based devices, and must contain the number of entries specified by the biClrUsed member.</span></span>                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="7b706-159">**bicompressione**</span><span class="sxs-lookup"><span data-stu-id="7b706-159">**biCompression**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-160">Specifica il tipo di compressione per una bitmap compressa dal basso verso l'alto.</span><span class="sxs-lookup"><span data-stu-id="7b706-160">Specifies the type of compression for a compressed bottom-up bitmap (top-down DIBs cannot be compressed).</span></span> <span data-ttu-id="7b706-161">Questo membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7b706-161">This member can be the one of the following values.</span></span>



| <span data-ttu-id="7b706-162">Valore</span><span class="sxs-lookup"><span data-stu-id="7b706-162">Value</span></span>         | <span data-ttu-id="7b706-163">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7b706-163">Description</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b706-164">\_RGB bi</span><span class="sxs-lookup"><span data-stu-id="7b706-164">BI\_RGB</span></span>       | <span data-ttu-id="7b706-165">Formato non compresso.</span><span class="sxs-lookup"><span data-stu-id="7b706-165">An uncompressed format.</span></span>                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="7b706-166">\_campi bi</span><span class="sxs-lookup"><span data-stu-id="7b706-166">BI\_BITFIELDS</span></span> | <span data-ttu-id="7b706-167">Specifica che la bitmap non è compressa e che la tabella dei colori è costituita da tre maschere colori DWORD che specificano rispettivamente i componenti rosso, verde e blu di ogni pixel.</span><span class="sxs-lookup"><span data-stu-id="7b706-167">Specifies that the bitmap is not compressed and that the color table consists of three DWORD color masks that specify the red, green, and blue components, respectively, of each pixel.</span></span> <span data-ttu-id="7b706-168">Questa operazione è valida se utilizzata con bitmap a 16 BPP e 32-BPP.</span><span class="sxs-lookup"><span data-stu-id="7b706-168">This is valid when used with 16-bpp and 32-bpp bitmaps.</span></span> <span data-ttu-id="7b706-169">Questo valore è valido in Microsoft Windows CE versione 2,0 e successive.</span><span class="sxs-lookup"><span data-stu-id="7b706-169">This value is valid in Microsoft Windows CE version 2.0 and later.</span></span> |



 

</dd> <dt>

<span data-ttu-id="7b706-170">**biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="7b706-170">**biSizeImage**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-171">Specifica la dimensione, in byte, dell'immagine.</span><span class="sxs-lookup"><span data-stu-id="7b706-171">Specifies the size of the image, in bytes.</span></span> <span data-ttu-id="7b706-172">Questo valore può essere impostato su zero per le \_ bitmap RGB bi.</span><span class="sxs-lookup"><span data-stu-id="7b706-172">This may be set to zero for BI\_RGB bitmaps.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-173">**biXPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="7b706-173">**biXPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-174">Specifica la risoluzione orizzontale in pixel per contatore del dispositivo di destinazione per la bitmap.</span><span class="sxs-lookup"><span data-stu-id="7b706-174">Specifies the horizontal resolution, in pixels per meter, of the target device for the bitmap.</span></span> <span data-ttu-id="7b706-175">Un'applicazione può usare questo valore per selezionare una bitmap da un gruppo di risorse che corrisponde meglio alle caratteristiche del dispositivo corrente.</span><span class="sxs-lookup"><span data-stu-id="7b706-175">An application can use this value to select a bitmap from a resource group that best matches the characteristics of the current device.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-176">**biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="7b706-176">**biYPelsPerMeter**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-177">Specifica la risoluzione verticale, in pixel per contatore, del dispositivo di destinazione per la bitmap.</span><span class="sxs-lookup"><span data-stu-id="7b706-177">Specifies the vertical resolution, in pixels per meter, of the target device for the bitmap.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-178">**biClrUsed**</span><span class="sxs-lookup"><span data-stu-id="7b706-178">**biClrUsed**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-179">Specifica il numero di indici di colori nella tabella dei colori che vengono effettivamente utilizzati dalla bitmap.</span><span class="sxs-lookup"><span data-stu-id="7b706-179">Specifies the number of color indexes in the color table that are actually used by the bitmap.</span></span> <span data-ttu-id="7b706-180">Se questo valore è zero, la bitmap usa il numero massimo di colori corrispondente al valore del membro **biBitCount** per la modalità di compressione specificata da **biCompression**.</span><span class="sxs-lookup"><span data-stu-id="7b706-180">If this value is zero, the bitmap uses the maximum number of colors corresponding to the value of the **biBitCount** member for the compression mode specified by **biCompression**.</span></span>

</dd> <dt>

<span data-ttu-id="7b706-181">**biClrImportant**</span><span class="sxs-lookup"><span data-stu-id="7b706-181">**biClrImportant**</span></span>
</dt> <dd>

<span data-ttu-id="7b706-182">Specifica il numero di indici di colore necessari per visualizzare la bitmap.</span><span class="sxs-lookup"><span data-stu-id="7b706-182">Specifies the number of color indexes required for displaying the bitmap.</span></span> <span data-ttu-id="7b706-183">Se questo valore è zero, tutti i colori sono obbligatori.</span><span class="sxs-lookup"><span data-stu-id="7b706-183">If this value is zero, all colors are required.</span></span>

<span data-ttu-id="7b706-184">Se biClrUsed è diverso da zero e il membro biBitCount è inferiore a 16, il membro biClrUsed specifica il numero effettivo di colori a cui il motore di grafica o il driver di dispositivo accede.</span><span class="sxs-lookup"><span data-stu-id="7b706-184">If biClrUsed is nonzero and the biBitCount member is less than 16, the biClrUsed member specifies the actual number of colors the graphics engine or device driver accesses.</span></span> <span data-ttu-id="7b706-185">Se biBitCount è maggiore o uguale a 16, il membro biClrUsed specifica la dimensione della tabella dei colori utilizzata per ottimizzare le prestazioni delle tavolozze dei colori di sistema.</span><span class="sxs-lookup"><span data-stu-id="7b706-185">If biBitCount is 16 or greater, the biClrUsed member specifies the size of the color table used to optimize performance of the system color palettes.</span></span> <span data-ttu-id="7b706-186">Se biBitCount è uguale a 16 o 32, la tavolozza dei colori ottimale inizia immediatamente dopo le tre maschere DWORD.</span><span class="sxs-lookup"><span data-stu-id="7b706-186">If biBitCount equals 16 or 32, the optimal color palette starts immediately following the three DWORD masks.</span></span>

<span data-ttu-id="7b706-187">Se la bitmap è una bitmap compressa, ovvero una bitmap in cui la matrice bitmap segue immediatamente la \_ struttura BITMAPINFOHEADER e a cui fa riferimento un solo puntatore, il membro biClrUsed deve essere pari a zero o alla dimensione effettiva della tabella dei colori.</span><span class="sxs-lookup"><span data-stu-id="7b706-187">If the bitmap is a packed bitmap (a bitmap in which the bitmap array immediately follows the \_BITMAPINFOHEADER structure and is referenced by a single pointer), the biClrUsed member must be either zero or the actual size of the color table.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7b706-188">Commenti</span><span class="sxs-lookup"><span data-stu-id="7b706-188">Remarks</span></span>

<span data-ttu-id="7b706-189">Questa struttura è contenuta all'interno di una struttura **\_ VIDEOINFOHEADER** .</span><span class="sxs-lookup"><span data-stu-id="7b706-189">This structure is contained within a **\_VIDEOINFOHEADER** structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b706-190">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b706-190">Requirements</span></span>



| <span data-ttu-id="7b706-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b706-191">Requirement</span></span> | <span data-ttu-id="7b706-192">Valore</span><span class="sxs-lookup"><span data-stu-id="7b706-192">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b706-193">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b706-193">Header</span></span><br/> | <dl> <span data-ttu-id="7b706-194"><dt>WMDM. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7b706-194"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7b706-195">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7b706-195">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7b706-196">**Strutture**</span><span class="sxs-lookup"><span data-stu-id="7b706-196">**Structures**</span></span>](structures.md)
</dt> <dt>

[<span data-ttu-id="7b706-197">**\_VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="7b706-197">**\_VIDEOINFOHEADER**</span></span>](-videoinfoheader.md)
</dt> </dl>

 

 





