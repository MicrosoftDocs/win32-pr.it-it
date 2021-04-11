---
description: Codici FOURCC
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: Codici FOURCC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123567"
---
# <a name="fourcc-codes"></a><span data-ttu-id="5a4c7-103">Codici FOURCC</span><span class="sxs-lookup"><span data-stu-id="5a4c7-103">FOURCC Codes</span></span>

<span data-ttu-id="5a4c7-104">A molti formati multimediali digitali sono assegnati codici FOURCC.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="5a4c7-105">Un codice FOURCC è un Unsigned Integer a 32 bit creato concatenando quattro caratteri ASCII.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="5a4c7-106">Ad esempio, il codice FOURCC per YUY2 video è' YUY2'.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="5a4c7-107">Per i formati video compressi e i formati video non RGB (ad esempio YUV), il membro di **bicompressione** della struttura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) deve essere impostato sul codice FourCC.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="5a4c7-108">Sono disponibili diverse macro C/C++ che semplificano la dichiarazione di valori FOURCC nel codice sorgente.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="5a4c7-109">La macro **MAKEFOURCC** , ad esempio, è dichiarata in mmsystem. h e la macro **FCC** è dichiarata in Aviriff. h.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="5a4c7-110">Utilizzarli come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="5a4c7-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="5a4c7-111">È anche possibile dichiarare direttamente un codice FOURCC come valore letterale stringa semplicemente invertendo l'ordine dei caratteri.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="5a4c7-112">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="5a4c7-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="5a4c7-113">Invertire l'ordine è necessario perché il sistema operativo Microsoft Windows utilizza un'architettura little-endian.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="5a4c7-114">' Y ' = 0x59,' U ' = 0x55 è 2' = 0x32, quindi ' 2YUY ' è 0x32595559.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="5a4c7-115">Conversione di codici FOURCC in GUID di sottotipo</span><span class="sxs-lookup"><span data-stu-id="5a4c7-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="5a4c7-116">Un intervallo di 2 \* guid 32 è riservato per rappresentare FourCC.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="5a4c7-117">Questi GUID sono tutti il formato in `XXXXXXXX-0000-0010-8000-00AA00389B71` cui `XXXXXXXX` è il codice FourCC.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="5a4c7-118">Pertanto, il GUID del sottotipo per YUY2 è `32595559-0000-0010-8000-00AA00389B71` .</span><span class="sxs-lookup"><span data-stu-id="5a4c7-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="5a4c7-119">Molti di questi GUID sono già definiti nel file di intestazione UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="5a4c7-120">Ad esempio, il sottotipo YUY2 è definito come MEDIASUBTYPE \_ YUY2.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="5a4c7-121">La libreria di classi base DirectShow fornisce anche una classe helper, [**FOURCCMap**](fourccmap.md), che può essere usata per convertire i codici FourCC in valori GUID.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="5a4c7-122">Il costruttore **FOURCCMap** accetta un codice FourCC come parametro di input.</span><span class="sxs-lookup"><span data-stu-id="5a4c7-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="5a4c7-123">È quindi possibile eseguire il cast dell'oggetto **FOURCCMap** al GUID corrispondente:</span><span class="sxs-lookup"><span data-stu-id="5a4c7-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="5a4c7-124">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="5a4c7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a4c7-125">**Sottotipi audio**</span><span class="sxs-lookup"><span data-stu-id="5a4c7-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="5a4c7-126">Sottotipi video</span><span class="sxs-lookup"><span data-stu-id="5a4c7-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="5a4c7-127">Uso dei codec</span><span class="sxs-lookup"><span data-stu-id="5a4c7-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



