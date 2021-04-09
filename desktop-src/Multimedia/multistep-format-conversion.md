---
title: Conversione del formato a più passaggi
description: Conversione del formato a più passaggi
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Gestione compressione audio (ACM), conversione dei dati
- ACM (Gestione compressione audio), conversione dei dati
- Esempi di ACM, conversione di dati
- conversione dei dati
- acmFormatSuggest (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955526"
---
# <a name="multistep-format-conversion"></a><span data-ttu-id="1c737-108">Conversione del formato a più passaggi</span><span class="sxs-lookup"><span data-stu-id="1c737-108">Multistep Format Conversion</span></span>

<span data-ttu-id="1c737-109">In alcuni casi l'ACM non è in grado di convertire i dati da un formato a un altro in un singolo passaggio.</span><span class="sxs-lookup"><span data-stu-id="1c737-109">Sometimes the ACM cannot convert data from one format to another in a single step.</span></span> <span data-ttu-id="1c737-110">Ad esempio, un'applicazione potrebbe dover convertire i dati stereo a 16 bit 44-kHz in mono ADPCM a 11 kHz.</span><span class="sxs-lookup"><span data-stu-id="1c737-110">For example, an application might need to convert 16-bit, 44-kHz stereo data to 11-kHz mono ADPCM.</span></span> <span data-ttu-id="1c737-111">Se il compressore o il decompressore non è in grado di eseguire direttamente questa conversione, l'applicazione potrebbe tentarla in due passaggi.</span><span class="sxs-lookup"><span data-stu-id="1c737-111">If the compressor or decompressor cannot do this conversion directly, the application might attempt it in two steps.</span></span> <span data-ttu-id="1c737-112">Ciò significa in genere eseguire una conversione tra due formati PCM, quindi un'altra conversione nel tipo di formato finale.</span><span class="sxs-lookup"><span data-stu-id="1c737-112">This usually means making one conversion between two PCM formats, then another conversion to the final format type.</span></span>

<span data-ttu-id="1c737-113">Per eseguire la conversione in due passaggi, usare la funzione [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) per trovare un formato PCM corrispondente al formato ADPCM.</span><span class="sxs-lookup"><span data-stu-id="1c737-113">To convert in two steps, use the [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) function to find a PCM format that matches the ADPCM format.</span></span> <span data-ttu-id="1c737-114">Usare quindi due flussi di conversione per eseguire la conversione.</span><span class="sxs-lookup"><span data-stu-id="1c737-114">Then use two conversion streams to perform the conversion.</span></span> <span data-ttu-id="1c737-115">Ad esempio, è possibile eseguire una conversione da PCM stereo a 16 bit, 44-kHz a 16 bit, 11 kHz mono, quindi eseguire la conversione da una mono a 11 kHz e da 11 kHz a 11 kHz mono ADPCM.</span><span class="sxs-lookup"><span data-stu-id="1c737-115">For example, perform one conversion from 16-bit, 44-kHz stereo PCM to 16-bit, 11-kHz mono, then convert from 16-bit, 11-kHz mono to 11-kHz mono ADPCM.</span></span>

<span data-ttu-id="1c737-116">La conversione a più passaggi si verifica anche quando il formato di origine o di destinazione non è PCM.</span><span class="sxs-lookup"><span data-stu-id="1c737-116">Multistep conversion also happens when either the source or the destination format is not PCM.</span></span> <span data-ttu-id="1c737-117">Se il formato di origine non è PCM, è necessario modificarlo in un formato PCM prima della conversione.</span><span class="sxs-lookup"><span data-stu-id="1c737-117">If the source format is not PCM, it should be changed to a PCM format before conversion.</span></span> <span data-ttu-id="1c737-118">Se il formato di destinazione non è PCM, l'origine deve essere convertita in un formato PCM intermedio e quindi convertita nel formato di destinazione finale.</span><span class="sxs-lookup"><span data-stu-id="1c737-118">If the destination format is not PCM, the source must be converted to an intermediate PCM format and then converted to the final destination format.</span></span>

<span data-ttu-id="1c737-119">Le conversioni più semplici si verificano quando i formati di origine e di destinazione sono entrambi formati PCM.</span><span class="sxs-lookup"><span data-stu-id="1c737-119">The most straightforward conversions occur when the source and destination formats are both PCM formats.</span></span> <span data-ttu-id="1c737-120">Quando il formato di origine o di destinazione non è PCM, la conversione potrebbe richiedere un passaggio aggiuntivo.</span><span class="sxs-lookup"><span data-stu-id="1c737-120">When either the source or destination format is not PCM, the conversion might require an additional step.</span></span> <span data-ttu-id="1c737-121">Se i formati di origine e di destinazione non sono PCM, la conversione richiede in genere più di un passaggio e, in alcuni casi, la conversione potrebbe non essere possibile.</span><span class="sxs-lookup"><span data-stu-id="1c737-121">If both source and destination formats are not PCM, the conversion will usually require more than one step, and, in some instances, conversion might not be possible.</span></span>

 

 




