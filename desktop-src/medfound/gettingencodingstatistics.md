---
description: Descrive le statistiche che è possibile recuperare da un codec Windows Media.
ms.assetid: 86c029af-e0fb-436a-b758-3f7d10c8bdeb
title: Recupero delle statistiche di codifica (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92fb298b35e9cd4114d1a5ba2f5badfad36c09c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749218"
---
# <a name="getting-encoding-statistics-microsoft-media-foundation"></a><span data-ttu-id="a322d-103">Recupero delle statistiche di codifica (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="a322d-103">Getting Encoding Statistics (Microsoft Media Foundation)</span></span>

<span data-ttu-id="a322d-104">Le informazioni su ciò che accade in una sessione di codifica sono in genere immediatamente disponibili sotto forma di codici di errore restituiti durante l'elaborazione degli esempi.</span><span class="sxs-lookup"><span data-stu-id="a322d-104">Information about what is happening in an encoding session is generally immediately available in the form of error codes returned when processing samples.</span></span> <span data-ttu-id="a322d-105">Tuttavia, esistono alcune statistiche che è possibile recuperare dal codec sui vari aspetti della codifica.</span><span class="sxs-lookup"><span data-stu-id="a322d-105">However, there are some statistics that you can retrieve from the codec about various encoding aspects.</span></span>

## <a name="video-frame-information"></a><span data-ttu-id="a322d-106">Informazioni sul frame video</span><span class="sxs-lookup"><span data-stu-id="a322d-106">Video Frame Information</span></span>

<span data-ttu-id="a322d-107">Alcune statistiche video che è possibile recuperare riguardano il numero di frame elaborati dal codificatore.</span><span class="sxs-lookup"><span data-stu-id="a322d-107">Some video statistics that you can retrieve deal with the number of frames processed by the encoder.</span></span> <span data-ttu-id="a322d-108">Sono disponibili tre proprietà del numero di frame che è possibile leggere dal codificatore video:</span><span class="sxs-lookup"><span data-stu-id="a322d-108">There are three frame number properties that you can read from the video encoder:</span></span>

-   <span data-ttu-id="a322d-109">[MFPKEY \_ TOTALFRAMES](mfpkey-totalframesproperty.md) è il numero di frame elaborati tramite il flusso di input di DMO.</span><span class="sxs-lookup"><span data-stu-id="a322d-109">[MFPKEY\_TOTALFRAMES](mfpkey-totalframesproperty.md) is the number of frames processed through the input stream of the DMO.</span></span>
-   <span data-ttu-id="a322d-110">[MFPKEY \_ CODEDFRAMES](mfpkey-codedframesproperty.md) è il numero di frame codificati.</span><span class="sxs-lookup"><span data-stu-id="a322d-110">[MFPKEY\_CODEDFRAMES](mfpkey-codedframesproperty.md) is the number of frames encoded.</span></span> <span data-ttu-id="a322d-111">Sottraendo questo valore dal numero totale di frame passati, è possibile determinare il numero di frame eliminati.</span><span class="sxs-lookup"><span data-stu-id="a322d-111">By subtracting this value from the total number of frames passed, you can determine how many frames were dropped.</span></span>
-   <span data-ttu-id="a322d-112">[MFPKEY \_ ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) è il numero di frame non codificati perché sono già stati inclusi contenuti duplicati.</span><span class="sxs-lookup"><span data-stu-id="a322d-112">[MFPKEY\_ZEROBYTEFRAMES](mfpkey-zerobyteframesproperty.md) is the number of frames not encoded because they duplicated content already included.</span></span> <span data-ttu-id="a322d-113">Questo valore non viene sottratto dal numero di fotogrammi codificati restituiti da DMO.</span><span class="sxs-lookup"><span data-stu-id="a322d-113">This value is not subtracted from the number of coded frames reported by the DMO.</span></span>

<span data-ttu-id="a322d-114">È possibile leggere le proprietà del fotogramma video in qualsiasi momento durante la codifica.</span><span class="sxs-lookup"><span data-stu-id="a322d-114">You can read video frame properties at any time during encoding.</span></span> <span data-ttu-id="a322d-115">Questo può essere utile per determinare se le impostazioni di codifica sono appropriate per il contenuto. Se c'è una grande differenza tra i frame totali e i frame codificati, il contenuto compresso potrebbe non soddisfare i requisiti di qualità.</span><span class="sxs-lookup"><span data-stu-id="a322d-115">This can be useful in determining if the encoding settings are appropriate for your content; if there is a large difference between total frames and coded frames, the compressed content might not meet your quality requirements.</span></span> <span data-ttu-id="a322d-116">È possibile leggere i valori finali dopo aver completato la codifica.</span><span class="sxs-lookup"><span data-stu-id="a322d-116">You can read the final values after you finish encoding.</span></span>

## <a name="vbr-buffer-statistics"></a><span data-ttu-id="a322d-117">Statistiche buffer VBR</span><span class="sxs-lookup"><span data-stu-id="a322d-117">VBR Buffer Statistics</span></span>

<span data-ttu-id="a322d-118">A seconda della modalità di codifica utilizzata, alcune o tutte le impostazioni del buffer possono essere determinate durante la codifica (ad esempio, la velocità in bit di VBR basata sulla qualità non è nota fino a quando non viene codificato il contenuto).</span><span class="sxs-lookup"><span data-stu-id="a322d-118">Depending upon the encoding mode used, some or all of the buffer settings may be determined during encoding (for example, the bit rate of quality based VBR is not known until the content is encoded).</span></span> <span data-ttu-id="a322d-119">Sono disponibili quattro proprietà del buffer VBR che è possibile ottenere usando il metodo **IPropertyBag:: Read** :</span><span class="sxs-lookup"><span data-stu-id="a322d-119">There are four VBR buffer properties that you can get using the **IPropertyBag::Read** method:</span></span>

-   <span data-ttu-id="a322d-120">[MFPKEY \_ RAVG](mfpkey-ravgproperty.md) è la velocità in bit media del contenuto VBR.</span><span class="sxs-lookup"><span data-stu-id="a322d-120">[MFPKEY\_RAVG](mfpkey-ravgproperty.md) is the average bit rate of the VBR content.</span></span>
-   <span data-ttu-id="a322d-121">[MFPKEY \_ BAVG](mfpkey-bavgproperty.md) è la finestra del buffer per la velocità in bit media.</span><span class="sxs-lookup"><span data-stu-id="a322d-121">[MFPKEY\_BAVG](mfpkey-bavgproperty.md) is the buffer window for the average bit rate.</span></span>
-   <span data-ttu-id="a322d-122">[MFPKEY \_ RMAX](mfpkey-rmaxproperty.md) è la velocità in bit massima del contenuto VBR.</span><span class="sxs-lookup"><span data-stu-id="a322d-122">[MFPKEY\_RMAX](mfpkey-rmaxproperty.md) is the peak bit rate of the VBR content.</span></span>
-   <span data-ttu-id="a322d-123">[MFPKEY \_ BMAX](mfpkey-bmaxproperty.md) è la finestra del buffer di picco.</span><span class="sxs-lookup"><span data-stu-id="a322d-123">[MFPKEY\_BMAX](mfpkey-bmaxproperty.md) is the peak buffer window.</span></span>

<span data-ttu-id="a322d-124">Dopo aver iniziato l'elaborazione degli esempi, è consigliabile non leggere alcuna proprietà VBR fino a quando non si termina la codifica del flusso.</span><span class="sxs-lookup"><span data-stu-id="a322d-124">After you begin processing samples, you should not read any of the VBR properties until you are finished encoding the stream.</span></span> <span data-ttu-id="a322d-125">In tal caso, il codificatore interpreta la richiesta come segnale del completamento della codifica.</span><span class="sxs-lookup"><span data-stu-id="a322d-125">If you do, the encoder interprets your request as a signal that the encoding is complete.</span></span> <span data-ttu-id="a322d-126">Il seguente esempio elaborato viene considerato come una nuova sessione di codifica.</span><span class="sxs-lookup"><span data-stu-id="a322d-126">The next sample that you process is treated as a new encoding session.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a322d-127">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="a322d-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a322d-128">Codec Windows Media</span><span class="sxs-lookup"><span data-stu-id="a322d-128">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



