---
description: Il metodo GetKaraokeChannelAssignment recupera un valore che indica la modalità di assegnazione dei canali karaoke agli altoparlanti.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Metodo GetKaraokeChannelAssignment
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103877105"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="53c4c-103">Metodo GetKaraokeChannelAssignment</span><span class="sxs-lookup"><span data-stu-id="53c4c-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="53c4c-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="53c4c-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="53c4c-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="53c4c-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="53c4c-106">Il `GetKaraokeChannelAssignment` metodo recupera un valore che indica la modalità di assegnazione dei canali karaoke ai relatori.</span><span class="sxs-lookup"><span data-stu-id="53c4c-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="53c4c-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="53c4c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53c4c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="53c4c-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="53c4c-109">Specifica il flusso audio come intero.</span><span class="sxs-lookup"><span data-stu-id="53c4c-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53c4c-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="53c4c-110">Return Value</span></span>

<span data-ttu-id="53c4c-111">Restituisce un Integer che indica l'assegnazione del altoparlante per il flusso specificato.</span><span class="sxs-lookup"><span data-stu-id="53c4c-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="53c4c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="53c4c-112">Return code</span></span> | <span data-ttu-id="53c4c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="53c4c-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="53c4c-114">2</span><span class="sxs-lookup"><span data-stu-id="53c4c-114">2</span></span>           | <span data-ttu-id="53c4c-115">Il flusso viene assegnato agli altoparlanti sinistro e destro.</span><span class="sxs-lookup"><span data-stu-id="53c4c-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="53c4c-116">3</span><span class="sxs-lookup"><span data-stu-id="53c4c-116">3</span></span>           | <span data-ttu-id="53c4c-117">Il flusso viene assegnato agli altoparlanti sinistro, destro e intermedio.</span><span class="sxs-lookup"><span data-stu-id="53c4c-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="53c4c-118">4</span><span class="sxs-lookup"><span data-stu-id="53c4c-118">4</span></span>           | <span data-ttu-id="53c4c-119">Il flusso viene assegnato ai relatori Left, Right e AUDIO1.</span><span class="sxs-lookup"><span data-stu-id="53c4c-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="53c4c-120">5</span><span class="sxs-lookup"><span data-stu-id="53c4c-120">5</span></span>           | <span data-ttu-id="53c4c-121">Il flusso viene assegnato agli altoparlanti a sinistra, a destra, al centro e a AUDIO1.</span><span class="sxs-lookup"><span data-stu-id="53c4c-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="53c4c-122">6</span><span class="sxs-lookup"><span data-stu-id="53c4c-122">6</span></span>           | <span data-ttu-id="53c4c-123">Il flusso viene assegnato ai relatori Left, Right e AUDIO2.</span><span class="sxs-lookup"><span data-stu-id="53c4c-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="53c4c-124">7</span><span class="sxs-lookup"><span data-stu-id="53c4c-124">7</span></span>           | <span data-ttu-id="53c4c-125">Il flusso viene assegnato agli altoparlanti a sinistra, a destra, al centro e a AUDIO2.</span><span class="sxs-lookup"><span data-stu-id="53c4c-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="53c4c-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="53c4c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c4c-127">**KaraokeAudioPresentationMode**</span><span class="sxs-lookup"><span data-stu-id="53c4c-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



