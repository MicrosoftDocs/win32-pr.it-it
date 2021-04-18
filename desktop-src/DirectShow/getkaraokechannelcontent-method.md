---
description: Il metodo GetKaraokeChannelContent recupera un valore che indica il tipo di contenuto nel canale Karaoke specificato nel flusso specificato.
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: Metodo GetKaraokeChannelContent
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304004"
---
# <a name="getkaraokechannelcontent-method"></a><span data-ttu-id="49ea5-103">Metodo GetKaraokeChannelContent</span><span class="sxs-lookup"><span data-stu-id="49ea5-103">GetKaraokeChannelContent Method</span></span>

> [!Note]  
> <span data-ttu-id="49ea5-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="49ea5-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="49ea5-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="49ea5-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="49ea5-106">Il `GetKaraokeChannelContent` metodo recupera un valore che indica il tipo di contenuto nel canale Karaoke specificato nel flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="49ea5-106">The `GetKaraokeChannelContent` method retrieves a value that indicates the type of content in the specified karaoke channel in the specified stream.</span></span>

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a><span data-ttu-id="49ea5-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="49ea5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49ea5-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="49ea5-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-109">Specifica il flusso audio come intero.</span><span class="sxs-lookup"><span data-stu-id="49ea5-109">Specifies the audio stream as an Integer.</span></span>

</dd> <dt>

<span data-ttu-id="49ea5-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span><span class="sxs-lookup"><span data-stu-id="49ea5-110"><span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*</span></span>
</dt> <dd>

<span data-ttu-id="49ea5-111">Specifica il canale come intero.</span><span class="sxs-lookup"><span data-stu-id="49ea5-111">Specifies the channel as an Integer.</span></span> <span data-ttu-id="49ea5-112">I valori possibili per ogni canale sono:</span><span class="sxs-lookup"><span data-stu-id="49ea5-112">The possible values for each channel are:</span></span>



| <span data-ttu-id="49ea5-113">Valore</span><span class="sxs-lookup"><span data-stu-id="49ea5-113">Value</span></span>  | <span data-ttu-id="49ea5-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49ea5-114">Description</span></span>    |
|--------|----------------|
| <span data-ttu-id="49ea5-115">0x0001</span><span class="sxs-lookup"><span data-stu-id="49ea5-115">0x0001</span></span> | <span data-ttu-id="49ea5-116">Guida vocale 1</span><span class="sxs-lookup"><span data-stu-id="49ea5-116">Guide Vocal 1</span></span>  |
| <span data-ttu-id="49ea5-117">0x0002</span><span class="sxs-lookup"><span data-stu-id="49ea5-117">0x0002</span></span> | <span data-ttu-id="49ea5-118">Guida vocale 2</span><span class="sxs-lookup"><span data-stu-id="49ea5-118">Guide Vocal 2</span></span>  |
| <span data-ttu-id="49ea5-119">0x0004</span><span class="sxs-lookup"><span data-stu-id="49ea5-119">0x0004</span></span> | <span data-ttu-id="49ea5-120">Guida melodia 1</span><span class="sxs-lookup"><span data-stu-id="49ea5-120">Guide Melody 1</span></span> |
| <span data-ttu-id="49ea5-121">0x0008</span><span class="sxs-lookup"><span data-stu-id="49ea5-121">0x0008</span></span> | <span data-ttu-id="49ea5-122">Guida melodia 2</span><span class="sxs-lookup"><span data-stu-id="49ea5-122">Guide Melody 2</span></span> |
| <span data-ttu-id="49ea5-123">0x0010</span><span class="sxs-lookup"><span data-stu-id="49ea5-123">0x0010</span></span> | <span data-ttu-id="49ea5-124">Guida melodia A</span><span class="sxs-lookup"><span data-stu-id="49ea5-124">Guide Melody A</span></span> |
| <span data-ttu-id="49ea5-125">0x0020</span><span class="sxs-lookup"><span data-stu-id="49ea5-125">0x0020</span></span> | <span data-ttu-id="49ea5-126">Guida melodia B</span><span class="sxs-lookup"><span data-stu-id="49ea5-126">Guide Melody B</span></span> |
| <span data-ttu-id="49ea5-127">0x0040</span><span class="sxs-lookup"><span data-stu-id="49ea5-127">0x0040</span></span> | <span data-ttu-id="49ea5-128">Effetto audio A</span><span class="sxs-lookup"><span data-stu-id="49ea5-128">Sound Effect A</span></span> |
| <span data-ttu-id="49ea5-129">0x0080</span><span class="sxs-lookup"><span data-stu-id="49ea5-129">0x0080</span></span> | <span data-ttu-id="49ea5-130">Effetto audio B</span><span class="sxs-lookup"><span data-stu-id="49ea5-130">Sound Effect B</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49ea5-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="49ea5-131">Return Value</span></span>

<span data-ttu-id="49ea5-132">Restituisce un valore intero i cui singoli bit specificano il contenuto del canale Karaoke.</span><span class="sxs-lookup"><span data-stu-id="49ea5-132">Returns an integer value whose individual bits specify the contents of the karaoke channel.</span></span>

## <a name="remarks"></a><span data-ttu-id="49ea5-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="49ea5-133">Remarks</span></span>

<span data-ttu-id="49ea5-134">La numerazione del canale audio DVD è in base zero, quindi i canali 2, 3 e 4 sono i canali karaoke ausiliari.</span><span class="sxs-lookup"><span data-stu-id="49ea5-134">DVD audio channel numbering is zero-based, so channels 2, 3, and 4 are the auxiliary karaoke channels.</span></span> <span data-ttu-id="49ea5-135">Dopo la restituzione del metodo, eseguire un'operazione AND bit per bit su *IContent* per determinare il contenuto di ogni canale.</span><span class="sxs-lookup"><span data-stu-id="49ea5-135">After the method returns, perform a bitwise AND operation on *iContent* to determine the contents of each channel.</span></span> <span data-ttu-id="49ea5-136">Poiché un singolo canale potrebbe avere più di un tipo di contenuto registrato, è necessario verificare tutti i valori possibili anche dopo che è stata trovata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="49ea5-136">Because a single channel might have more than one type of content recorded on it, you should test for all the possible values even after a match is found.</span></span>

<span data-ttu-id="49ea5-137">Quando l'utente conosce il contenuto di ogni canale, deve essere in grado di regolare il volume o di attivare o disattivare i singoli canali in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="49ea5-137">After the user knows the contents of each channel, he or she must be able to adjust the volume or turn the individual channels on or off as needed.</span></span> <span data-ttu-id="49ea5-138">Implementare questa funzionalità nell'applicazione usando la proprietà [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="49ea5-138">Implement this functionality in your application by using the [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) property.</span></span>

> [!Note]  
> <span data-ttu-id="49ea5-139">Per riprodurre i dischi Karaoke, il decodificatore audio nel sistema dell'utente deve essere compatibile con l'implementazione del karaoke DirectShow 8.</span><span class="sxs-lookup"><span data-stu-id="49ea5-139">To play karaoke discs, the audio decoder on the user's system must be compatible with the DirectShow 8 karaoke implementation.</span></span>

 

 

 



