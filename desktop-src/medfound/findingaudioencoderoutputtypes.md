---
description: Ricerca di tipi di output del codificatore audio
ms.assetid: cd47d45b-ea47-4dec-867e-d51145d7f084
title: Ricerca di tipi di output del codificatore audio (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5389274cca1178ebc0ae03e21f7a804f73a5db48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305379"
---
# <a name="finding-audio-encoder-output-types-microsoft-media-foundation"></a><span data-ttu-id="c680c-103">Ricerca di tipi di output del codificatore audio (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="c680c-103">Finding Audio Encoder Output Types (Microsoft Media Foundation)</span></span>

<span data-ttu-id="c680c-104">Poiché è necessario usare un formato di output del codificatore audio enumerato dal codificatore audio, è necessario disporre di un modo per trovare il formato più adatto alle proprie esigenze.</span><span class="sxs-lookup"><span data-stu-id="c680c-104">Because you must use an audio encoder output format that is enumerated by the audio encoder, you need to have a way of finding the format that is most suited to your needs.</span></span> <span data-ttu-id="c680c-105">Il numero di canali, i bit per campione e la frequenza di campionamento dell'output che si sceglie devono corrispondere ai valori per il contenuto compresso.</span><span class="sxs-lookup"><span data-stu-id="c680c-105">The number of channels, bits per sample, and sample rate of the output that you choose must match the values for the content that you compress.</span></span> <span data-ttu-id="c680c-106">Tuttavia, il codificatore può supportare diversi tipi all'interno di questi vincoli.</span><span class="sxs-lookup"><span data-stu-id="c680c-106">However, the encoder may support several types within these constraints.</span></span>

<span data-ttu-id="c680c-107">Il fattore decisivo per la scelta di un tipo è la velocità in bit del flusso codificato; si desidera trovare un tipo di supporto che corrisponda all'input e ha una velocità in bit più vicina possibile a un valore di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c680c-107">The deciding factor for choosing a type is the bit rate of the encoded stream; you want to find a media type that matches your input and has a bit rate that is as close as possible to a target value.</span></span> <span data-ttu-id="c680c-108">Se si enumerano i tipi di output VBR a passaggio singolo, è il valore di qualità che deciderà il tipo usato.</span><span class="sxs-lookup"><span data-stu-id="c680c-108">If you are enumerating one-pass VBR output types, it is the quality value that will decide the type you use.</span></span> <span data-ttu-id="c680c-109">Per ulteriori informazioni sui valori di qualità nei tipi di output enumerati, vedere [enumerazione di tipi audio per modalità di codifica specifiche](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="c680c-109">For more information about quality values in enumerated output types, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

> [!Note]  
>    <span data-ttu-id="c680c-110">Il codificatore audio enumera alcuni tipi che sono duplicati di altri tipi in quasi tutti i modi.</span><span class="sxs-lookup"><span data-stu-id="c680c-110">The audio encoder enumerates some types that are duplicates of other types in almost all ways.</span></span> <span data-ttu-id="c680c-111">Questi duplicati sono disponibili per i formati in cui il numero di pacchetti al secondo non soddisfa i requisiti per l'archiviazione nei file ASF se sincronizzati con il video.</span><span class="sxs-lookup"><span data-stu-id="c680c-111">These duplicates exist for formats where the number of packets per second does not meet the requirements for storage in ASF files when synchronized with video.</span></span> <span data-ttu-id="c680c-112">L'audio sincronizzato con video in un file ASF deve avere tre o più pacchetti al secondo per velocità in bit inferiori a 32000 e 5 o più pacchetti al secondo per velocità in bit maggiori o uguali a 32000.</span><span class="sxs-lookup"><span data-stu-id="c680c-112">Audio synchronized with video in an ASF file must have 3 or more packets per second for bit rates less than 32000, and 5 or more packets per second for bit rates greater than or equal to 32000.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="c680c-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c680c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c680c-114">Configurazione della codifica audio</span><span class="sxs-lookup"><span data-stu-id="c680c-114">Configuring Audio Encoding</span></span>](configuringaudioencoding.md)
</dt> <dt>

[<span data-ttu-id="c680c-115">Enumerazione dei tipi audio per modalità di codifica specifiche</span><span class="sxs-lookup"><span data-stu-id="c680c-115">Enumerating Audio Types for Specific Encoding Modes</span></span>](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> </dl>

 

 



