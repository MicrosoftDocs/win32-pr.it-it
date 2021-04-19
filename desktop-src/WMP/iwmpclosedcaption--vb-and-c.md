---
title: Interfaccia IWMPClosedCaption (VB e C) (WMP. h)
description: Fornisce un modo per includere le didascalie con un file multimediale digitale. Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).
ms.assetid: 927f6fe4-5847-439e-9df0-19cc910d887d
keywords:
- Interfaccia IWMPClosedCaption (VB e C) Windows Media Player
- Interfaccia IWMPClosedCaption (VB e C) Windows Media Player, descritta
topic_type:
- apiref
api_name:
- IWMPClosedCaption (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ce3f697fc5c651a47f257a61bd9841987f54478
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328218"
---
# <a name="iwmpclosedcaption-vb-and-c-interface"></a><span data-ttu-id="2e33b-106">Interfaccia IWMPClosedCaption (VB e C#)</span><span class="sxs-lookup"><span data-stu-id="2e33b-106">IWMPClosedCaption (VB and C#) interface</span></span>

<span data-ttu-id="2e33b-107">Fornisce un modo per includere le didascalie con un file multimediale digitale.</span><span class="sxs-lookup"><span data-stu-id="2e33b-107">Provides a way to include captions with a digital media file.</span></span> <span data-ttu-id="2e33b-108">Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).</span><span class="sxs-lookup"><span data-stu-id="2e33b-108">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

## <a name="members"></a><span data-ttu-id="2e33b-109">Membri</span><span class="sxs-lookup"><span data-stu-id="2e33b-109">Members</span></span>

<span data-ttu-id="2e33b-110">L'interfaccia **IWMPClosedCaption (VB e C#)** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="2e33b-110">The **IWMPClosedCaption (VB and C#)** interface does not define any members.</span></span>

<span data-ttu-id="2e33b-111">L'interfaccia **IWMPClosedCaption** espone le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="2e33b-111">The **IWMPClosedCaption** interface exposes the following properties.</span></span>



| <span data-ttu-id="2e33b-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e33b-112">Property</span></span>                                                                             | <span data-ttu-id="2e33b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2e33b-113">Description</span></span>                                                                                |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2e33b-114">captioningId</span><span class="sxs-lookup"><span data-stu-id="2e33b-114">captioningId</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-captioningid--vb-and-c.md) | <span data-ttu-id="2e33b-115">Ottiene o imposta il nome dell'elemento HTML che visualizza la didascalia.</span><span class="sxs-lookup"><span data-stu-id="2e33b-115">Gets or sets the name of the HTML element displaying the captioning.</span></span>                       |
| [<span data-ttu-id="2e33b-116">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="2e33b-116">SAMIFileName</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samifilename--vb-and-c.md) | <span data-ttu-id="2e33b-117">Ottiene o imposta il nome del file contenente le informazioni necessarie per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="2e33b-117">Gets or sets the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="2e33b-118">SAMILang</span><span class="sxs-lookup"><span data-stu-id="2e33b-118">SAMILang</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)         | <span data-ttu-id="2e33b-119">Ottiene o imposta la lingua visualizzata per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="2e33b-119">Gets or sets the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="2e33b-120">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="2e33b-120">SAMIStyle</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samistyle--vb-and-c.md)       | <span data-ttu-id="2e33b-121">Ottiene o imposta lo stile dei sottotitoli codificati.</span><span class="sxs-lookup"><span data-stu-id="2e33b-121">Gets or sets the closed captioning style.</span></span>                                                  |



 

<span data-ttu-id="2e33b-122">Ottenere un'interfaccia **IWMPClosedCaption** usando la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="2e33b-122">Get an **IWMPClosedCaption** interface by using the following property.</span></span>



| <span data-ttu-id="2e33b-123">Oggetto</span><span class="sxs-lookup"><span data-stu-id="2e33b-123">Object</span></span>                                                            | <span data-ttu-id="2e33b-124">Proprietà</span><span class="sxs-lookup"><span data-stu-id="2e33b-124">Property</span></span>                                                                   |
|-------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="2e33b-125">AxWindowsMediaPlayer</span><span class="sxs-lookup"><span data-stu-id="2e33b-125">AxWindowsMediaPlayer</span></span>](axwindowsmediaplayer-object--vb-and-c.md) | [<span data-ttu-id="2e33b-126">closedCaption</span><span class="sxs-lookup"><span data-stu-id="2e33b-126">closedCaption</span></span>](axwmplib-axwindowsmediaplayer-closedcaption--vb-and-c.md) |



 

## <a name="requirements"></a><span data-ttu-id="2e33b-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2e33b-127">Requirements</span></span>



| <span data-ttu-id="2e33b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e33b-128">Requirement</span></span> | <span data-ttu-id="2e33b-129">Valore</span><span class="sxs-lookup"><span data-stu-id="2e33b-129">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e33b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2e33b-130">Header</span></span><br/> | <dl> <span data-ttu-id="2e33b-131"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e33b-131"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e33b-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2e33b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e33b-133">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="2e33b-133">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="2e33b-134">**Interfacce per Visual Basic .NET e C #**</span><span class="sxs-lookup"><span data-stu-id="2e33b-134">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="2e33b-135">**Interfaccia IWMPClosedCaption2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="2e33b-135">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





