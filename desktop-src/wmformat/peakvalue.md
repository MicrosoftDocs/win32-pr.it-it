---
title: PeakValue
description: L'attributo PeakValue contiene un valore di ampiezza a 16 bit che designa il livello di picco del volume del contenuto audio.
ms.assetid: 885f6d4c-661a-4681-96b6-c1a282c8bf18
keywords:
- PeakValue Windows Media Format
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37ef933ec1b10555aa4c88a24261313abb261163
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299135"
---
# <a name="peakvalue"></a><span data-ttu-id="6ddc4-104">PeakValue</span><span class="sxs-lookup"><span data-stu-id="6ddc4-104">PeakValue</span></span>

<span data-ttu-id="6ddc4-105">L'attributo **PeakValue** contiene un valore di ampiezza a 16 bit che designa il livello di picco del volume del contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-105">The **PeakValue** attribute contains contains a 16-bit amplitude value designating the peak volume level of audio content.</span></span> <span data-ttu-id="6ddc4-106">Con [**AverageLevel**](averagelevel.md), questo attributo viene usato per la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-106">With [**AverageLevel**](averagelevel.md), this attribute is used for normalization.</span></span> <span data-ttu-id="6ddc4-107">La normalizzazione è il processo di regolazione del livello di volume di riproduzione dei file audio, in modo che le parti più rumorose dei file vengano riavviate allo stesso livello e il volume medio per ognuno di essi sia lo stesso.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same..</span></span>

## <a name="global-constant"></a><span data-ttu-id="6ddc4-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="6ddc4-108">Global Constant</span></span>

<span data-ttu-id="6ddc4-109">g \_ wszPeakValue</span><span class="sxs-lookup"><span data-stu-id="6ddc4-109">g\_wszPeakValue</span></span>

## <a name="data-type"></a><span data-ttu-id="6ddc4-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="6ddc4-110">Data Type</span></span>

<span data-ttu-id="6ddc4-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="6ddc4-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="6ddc4-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="6ddc4-112">Remarks</span></span>

<span data-ttu-id="6ddc4-113">Questo attributo viene impostato dall'oggetto writer in base alle informazioni del codec.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="6ddc4-114">Solo i flussi compressi con uno dei codec Windows Media Audio hanno un valore impostato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="6ddc4-115">**PeakValue** non è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-115">**PeakValue** is not read-only.</span></span> <span data-ttu-id="6ddc4-116">Tuttavia, se il file verrà riprodotto dalla Media Player di Windows, è consigliabile non modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="6ddc4-117">Windows Media Player usa questa operazione per normalizzare i livelli di file in una playlist.</span><span class="sxs-lookup"><span data-stu-id="6ddc4-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="6ddc4-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6ddc4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ddc4-119">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="6ddc4-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




