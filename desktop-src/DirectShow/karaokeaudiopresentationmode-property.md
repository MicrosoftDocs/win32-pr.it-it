---
description: La proprietà KaraokeAudioPresentationMode imposta o recupera la combinazione di altoparlanti a destra sinistra per i canali karaoke ausiliari.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Proprietà KaraokeAudioPresentationMode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303810"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="57418-103">Proprietà KaraokeAudioPresentationMode</span><span class="sxs-lookup"><span data-stu-id="57418-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="57418-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="57418-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="57418-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="57418-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="57418-106">La `KaraokeAudioPresentationMode` proprietà imposta o recupera la combinazione di altoparlanti a destra sinistra per i canali karaoke ausiliari.</span><span class="sxs-lookup"><span data-stu-id="57418-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="57418-107">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="57418-107">Return Value</span></span>

<span data-ttu-id="57418-108">Restituisce un valore integer contenente un set di flag di bit che indica il modo in cui i canali karaoke ausiliari vengono riprodottoti agli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="57418-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="57418-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="57418-109">Remarks</span></span>

<span data-ttu-id="57418-110">Questa proprietà è di lettura/scrittura e il valore predefinito è zero.</span><span class="sxs-lookup"><span data-stu-id="57418-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="57418-111">I canali audio sono in base zero, quindi i canali 0 e 1 rappresentano in genere i canali speaker destro e sinistro e i canali da 2 a 4 sono i tre canali karaoke ausiliari.</span><span class="sxs-lookup"><span data-stu-id="57418-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="57418-112">Quando l'oggetto MSWebDVD entra in modalità karaoke, disattiva automaticamente i canali 2 e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="57418-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="57418-113">Utilizzare operazioni **OR bit per bit** per impostare il bit appropriato in modo da inviare un canale ausiliario all'altoparlante sinistro, all'altoparlante destro, a entrambi gli altoparlanti (entrambi i bit) o a nessun altoparlante (entrambi BITS).</span><span class="sxs-lookup"><span data-stu-id="57418-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="57418-114">Questi bit sono tutti spenti per impostazione predefinita ogni volta che il navigatore DVD entra in modalità karaoke.</span><span class="sxs-lookup"><span data-stu-id="57418-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="57418-115">Il valore dei bit e la relativa azione corrispondente sono indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="57418-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="57418-116">Valore</span><span class="sxs-lookup"><span data-stu-id="57418-116">Value</span></span>  | <span data-ttu-id="57418-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57418-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="57418-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="57418-118">0x0004</span></span> | <span data-ttu-id="57418-119">Canale 2 downmix a sinistra</span><span class="sxs-lookup"><span data-stu-id="57418-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="57418-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="57418-120">0x0008</span></span> | <span data-ttu-id="57418-121">Downmix Channel 3 (altoparlante a sinistra)</span><span class="sxs-lookup"><span data-stu-id="57418-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="57418-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="57418-122">0x0010</span></span> | <span data-ttu-id="57418-123">Downmix Channel 4 (altoparlante a sinistra)</span><span class="sxs-lookup"><span data-stu-id="57418-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="57418-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="57418-124">0x0400</span></span> | <span data-ttu-id="57418-125">Downmix Channel 2 nell'altoparlante destro</span><span class="sxs-lookup"><span data-stu-id="57418-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="57418-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="57418-126">0x0800</span></span> | <span data-ttu-id="57418-127">Downmix Channel 3 nell'altoparlante destro</span><span class="sxs-lookup"><span data-stu-id="57418-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="57418-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="57418-128">0x1000</span></span> | <span data-ttu-id="57418-129">Downmix Channel 4 nell'altoparlante destro</span><span class="sxs-lookup"><span data-stu-id="57418-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



