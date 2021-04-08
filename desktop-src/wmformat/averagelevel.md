---
title: AverageLevel
description: L'attributo AverageLevel contiene un valore di ampiezza a 16 bit che designa il livello di volume medio del contenuto audio.
ms.assetid: e6270ac8-5de3-4dee-824c-ba25fdd272c8
keywords:
- AverageLevel Windows Media Format
topic_type:
- apiref
api_name:
- AverageLevel
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 632379e42fa6c64e44018173b9d40340add4ee61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045715"
---
# <a name="averagelevel"></a><span data-ttu-id="a00be-104">AverageLevel</span><span class="sxs-lookup"><span data-stu-id="a00be-104">AverageLevel</span></span>

<span data-ttu-id="a00be-105">L'attributo **AverageLevel** contiene un valore di ampiezza a 16 bit che designa il livello di volume medio del contenuto audio.</span><span class="sxs-lookup"><span data-stu-id="a00be-105">The **AverageLevel** attribute contains a 16-bit amplitude value designating the average volume level of audio content.</span></span> <span data-ttu-id="a00be-106">Con [**PeakValue**](peakvalue.md), questo attributo viene usato per la normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="a00be-106">With [**PeakValue**](peakvalue.md), this attribute is used for normalization.</span></span> <span data-ttu-id="a00be-107">La normalizzazione è il processo di regolazione del livello di volume di riproduzione dei file audio, in modo che le parti più rumorose dei file vengano riavviate allo stesso livello e il volume medio per ognuno di essi sia lo stesso.</span><span class="sxs-lookup"><span data-stu-id="a00be-107">Normalization is the process of adjusting the playback volume level of audio files so that the loudest parts of files playback at the same level and the average volume for each is the same.</span></span>

## <a name="global-constant"></a><span data-ttu-id="a00be-108">Costante globale</span><span class="sxs-lookup"><span data-stu-id="a00be-108">Global Constant</span></span>

<span data-ttu-id="a00be-109">g \_ wszAverageLevel</span><span class="sxs-lookup"><span data-stu-id="a00be-109">g\_wszAverageLevel</span></span>

## <a name="data-type"></a><span data-ttu-id="a00be-110">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="a00be-110">Data Type</span></span>

<span data-ttu-id="a00be-111">**WMT \_ tipo \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a00be-111">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="a00be-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a00be-112">Remarks</span></span>

<span data-ttu-id="a00be-113">Questo attributo viene impostato dall'oggetto writer in base alle informazioni del codec.</span><span class="sxs-lookup"><span data-stu-id="a00be-113">This attribute is set by the writer object based on information from the codec.</span></span> <span data-ttu-id="a00be-114">Solo i flussi compressi con uno dei codec Windows Media Audio hanno un valore impostato automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a00be-114">Only streams compressed with one of the Windows Media Audio codecs have an automatically set value.</span></span>

<span data-ttu-id="a00be-115">**AverageLevel** non è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a00be-115">**AverageLevel** is not read-only.</span></span> <span data-ttu-id="a00be-116">Tuttavia, se il file verrà riprodotto dalla Media Player di Windows, è consigliabile non modificare questo valore.</span><span class="sxs-lookup"><span data-stu-id="a00be-116">However, if the file will be played by the Windows Media Player, you should not alter this value.</span></span> <span data-ttu-id="a00be-117">Windows Media Player usa questa operazione per normalizzare i livelli di file in una playlist.</span><span class="sxs-lookup"><span data-stu-id="a00be-117">The Windows Media Player uses this for normalizing the levels of files in a playlist.</span></span>

## <a name="see-also"></a><span data-ttu-id="a00be-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a00be-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00be-119">**Elenco degli attributi**</span><span class="sxs-lookup"><span data-stu-id="a00be-119">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




