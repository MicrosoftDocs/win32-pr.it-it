---
description: Filtro decodificatore CC
ms.assetid: 57ef75f6-411c-4b1f-b0dc-ac293ebc0b9c
title: Filtro decodificatore CC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93995207e4f1a397db28f743d1f972b871b0553
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103965540"
---
# <a name="cc-decoder-filter"></a><span data-ttu-id="79533-103">Filtro decodificatore CC</span><span class="sxs-lookup"><span data-stu-id="79533-103">CC Decoder Filter</span></span>

> [!IMPORTANT]
> <span data-ttu-id="79533-104">Questo componente è stato rimosso da Windows Vista e dai sistemi operativi successivi.</span><span class="sxs-lookup"><span data-stu-id="79533-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="79533-105">È disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="79533-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

 

<span data-ttu-id="79533-106">Il decodificatore CC VBI è un filtro della classe del flusso in modalità kernel.</span><span class="sxs-lookup"><span data-stu-id="79533-106">The CC VBI Decoder is a kernel-mode stream class filter.</span></span> <span data-ttu-id="79533-107">Viene visualizzato in GraphEdit sotto la categoria "WDM Streaming VBI codecs".</span><span class="sxs-lookup"><span data-stu-id="79533-107">It appears in GraphEdit under the "WDM Streaming VBI Codecs" category.</span></span> <span data-ttu-id="79533-108">Accetta le forme d'onda di esempio fornite da un filtro di acquisizione e recapita i dati decodificati per la didascalia al [decodificatore della riga 21](line-21-decoder-filter.md) e/o alle applicazioni interessate.</span><span class="sxs-lookup"><span data-stu-id="79533-108">It accepts sample waveforms delivered by a capture filter and delivers decoded closed-captioning data to the [Line 21 Decoder](line-21-decoder-filter.md) and/or to interested applications.</span></span>

<span data-ttu-id="79533-109">Questo filtro ha due pin di input, VBI e HWCC.</span><span class="sxs-lookup"><span data-stu-id="79533-109">This filter has two input pins, VBI and HWCC.</span></span> <span data-ttu-id="79533-110">Il pin VBI viene usato per i dati VBI non elaborati e il pin HWCC viene usato quando la decodifica VBI viene eseguita nell'hardware dal filtro di acquisizione.</span><span class="sxs-lookup"><span data-stu-id="79533-110">The VBI pin is used for raw VBI data, and the HWCC pin is used when the VBI decoding is performed in hardware by the capture filter.</span></span> <span data-ttu-id="79533-111">Quando i dati vengono ricevuti sul pin HWCC, il decodificatore CC funziona in modalità "pass-through" e invia i dati direttamente al decodificatore della riga 21 senza elaborarli in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="79533-111">When the data is received on the HWCC pin, the CC Decoder operates in "pass-through" mode, and sends the data directly to the Line 21 Decoder without processing it in any way.</span></span> <span data-ttu-id="79533-112">Se il filtro di acquisizione espone un pin HWCC, deve essere connesso direttamente al pin corrispondente sul decoder CC.</span><span class="sxs-lookup"><span data-stu-id="79533-112">If the capture filter exposes an HWCC pin, it must be connected directly to the corresponding pin on the CC Decoder.</span></span> <span data-ttu-id="79533-113">La categoria pin è **PINNAME \_ video \_ CC \_ Capture**.</span><span class="sxs-lookup"><span data-stu-id="79533-113">The pin category is **PINNAME\_VIDEO\_CC\_CAPTURE**.</span></span>

<span data-ttu-id="79533-114">Il decodificatore CC dispone di un massimo di otto pin di output, ognuno dei quali può selezionare le proprie righe e sottoflussi.</span><span class="sxs-lookup"><span data-stu-id="79533-114">The CC Decoder has up to eight output pins, each of which can select their own lines and substreams.</span></span> <span data-ttu-id="79533-115">Il primo pin di output è connesso al decodificatore line-21.</span><span class="sxs-lookup"><span data-stu-id="79533-115">The first output pin is connected to the Line-21 Decoder.</span></span>

<span data-ttu-id="79533-116">Il filtro del decodificatore CC viene visualizzato nella categoria di filtro "WDM Streaming VBI codecs" (**am \_ KSCATEGORY \_ VBICODEC**).</span><span class="sxs-lookup"><span data-stu-id="79533-116">The CC Decoder filter appears in the "WDM Streaming VBI Codecs" filter category (**AM\_KSCATEGORY\_VBICODEC**).</span></span>

<span data-ttu-id="79533-117">Poiché si tratta di un filtro in modalità kernel, le applicazioni non possono crearlo direttamente tramite **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="79533-117">Because this is a kernel-mode filter, applications cannot create it directly using **CoCreateInstance**.</span></span> <span data-ttu-id="79533-118">Usare invece l' [enumeratore di dispositivo di sistema](system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="79533-118">Instead, use the [System Device Enumerator](system-device-enumerator.md).</span></span> <span data-ttu-id="79533-119">Per ulteriori informazioni, vedere [creazione di filtri Kernel-Mode](creating-kernel-mode-filters.md).</span><span class="sxs-lookup"><span data-stu-id="79533-119">For more information, see [Creating Kernel-Mode Filters](creating-kernel-mode-filters.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79533-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="79533-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79533-121">Filtri DirectShow</span><span class="sxs-lookup"><span data-stu-id="79533-121">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="79533-122">Visualizzazione di didascalie chiuse</span><span class="sxs-lookup"><span data-stu-id="79533-122">Viewing Closed Captions</span></span>](viewing-closed-captions.md)
</dt> </dl>

 

 



