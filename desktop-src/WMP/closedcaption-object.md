---
title: Oggetto ClosedCaption
description: L'oggetto ClosedCaption fornisce un modo per includere le didascalie con una clip multimediale. Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).
ms.assetid: 5e192aa4-0ecd-4bda-8dad-1750039c7898
keywords:
- Media Player di Windows oggetto ClosedCaption
topic_type:
- apiref
api_name:
- ClosedCaption Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 85e53468e8d5cc2694555b9a05d8b207d1660618
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/06/2019
ms.locfileid: "104045959"
---
# <a name="closedcaption-object"></a><span data-ttu-id="8ec85-105">Oggetto ClosedCaption</span><span class="sxs-lookup"><span data-stu-id="8ec85-105">ClosedCaption Object</span></span>

<span data-ttu-id="8ec85-106">L'oggetto **ClosedCaption** fornisce un modo per includere le didascalie con una clip multimediale.</span><span class="sxs-lookup"><span data-stu-id="8ec85-106">The **ClosedCaption** object provides a way to include captions with a media clip.</span></span> <span data-ttu-id="8ec85-107">Il testo della didascalia si trova in un file di interscambio multimediale accessibile sincronizzato (SAMI).</span><span class="sxs-lookup"><span data-stu-id="8ec85-107">The captioning text is in a Synchronized Accessible Media Interchange (SAMI) file.</span></span>

<span data-ttu-id="8ec85-108">L'oggetto **ClosedCaption** supporta le proprietà seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ec85-108">The **ClosedCaption** object supports the following properties.</span></span>



| <span data-ttu-id="8ec85-109">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8ec85-109">Property</span></span>                                           | <span data-ttu-id="8ec85-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ec85-110">Description</span></span>                                                                                          |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec85-111">captioningID</span><span class="sxs-lookup"><span data-stu-id="8ec85-111">captioningID</span></span>](closedcaption-captioningid.md)     | <span data-ttu-id="8ec85-112">Specifica o Recupera il nome del frame o del controllo che visualizza la didascalia.</span><span class="sxs-lookup"><span data-stu-id="8ec85-112">Specifies or retrieves the name of the frame or control displaying the captioning.</span></span>                   |
| [<span data-ttu-id="8ec85-113">SAMIFileName</span><span class="sxs-lookup"><span data-stu-id="8ec85-113">SAMIFileName</span></span>](closedcaption-samifilename.md)     | <span data-ttu-id="8ec85-114">Specifica o Recupera il nome del file contenente le informazioni necessarie per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="8ec85-114">Specifies or retrieves the name of the file containing the information needed for closed captioning.</span></span> |
| [<span data-ttu-id="8ec85-115">SAMILang</span><span class="sxs-lookup"><span data-stu-id="8ec85-115">SAMILang</span></span>](closedcaption-samilang.md)             | <span data-ttu-id="8ec85-116">Specifica o recupera la lingua visualizzata per la didascalia chiusa.</span><span class="sxs-lookup"><span data-stu-id="8ec85-116">Specifies or retrieves the language displayed for closed captioning.</span></span>                                 |
| [<span data-ttu-id="8ec85-117">SAMILangCount</span><span class="sxs-lookup"><span data-stu-id="8ec85-117">SAMILangCount</span></span>](closedcaption-samilangcount.md)   | <span data-ttu-id="8ec85-118">Recupera il numero di lingue supportate dal file SAMI corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-118">Retrieves the number of languages supported by the current SAMI file.</span></span>                                |
| [<span data-ttu-id="8ec85-119">SAMIStyle</span><span class="sxs-lookup"><span data-stu-id="8ec85-119">SAMIStyle</span></span>](closedcaption-samistyle.md)           | <span data-ttu-id="8ec85-120">Specifica o recupera lo stile dei sottotitoli codificati.</span><span class="sxs-lookup"><span data-stu-id="8ec85-120">Specifies or retrieves the closed captioning style.</span></span>                                                  |
| [<span data-ttu-id="8ec85-121">SAMIStyleCount</span><span class="sxs-lookup"><span data-stu-id="8ec85-121">SAMIStyleCount</span></span>](closedcaption-samistylecount.md) | <span data-ttu-id="8ec85-122">Recupera il numero di stili supportati dal file SAMI corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-122">Retrieves the number of styles supported by the current SAMI file.</span></span>                                   |



 

<span data-ttu-id="8ec85-123">L'oggetto **ClosedCaption** supporta i metodi seguenti.</span><span class="sxs-lookup"><span data-stu-id="8ec85-123">The **ClosedCaption** object supports the following methods.</span></span>



| <span data-ttu-id="8ec85-124">Metodo</span><span class="sxs-lookup"><span data-stu-id="8ec85-124">Method</span></span>                                                 | <span data-ttu-id="8ec85-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8ec85-125">Description</span></span>                                                                              |
|--------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8ec85-126">getSAMILangID</span><span class="sxs-lookup"><span data-stu-id="8ec85-126">getSAMILangID</span></span>](closedcaption-getsamilangid.md)       | <span data-ttu-id="8ec85-127">Recupera l'identificatore delle impostazioni locali (LCID) di una lingua supportata dal file SAMI corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-127">Retrieves the locale identifier (LCID) of a language supported by the current SAMI file.</span></span> |
| [<span data-ttu-id="8ec85-128">getSAMILangName</span><span class="sxs-lookup"><span data-stu-id="8ec85-128">getSAMILangName</span></span>](closedcaption-getsamilangname.md)   | <span data-ttu-id="8ec85-129">Recupera il nome di una lingua supportata dal file SAMI corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-129">Retrieves the name of a language supported by the current SAMI file.</span></span>                     |
| [<span data-ttu-id="8ec85-130">getSAMIStyleName</span><span class="sxs-lookup"><span data-stu-id="8ec85-130">getSAMIStyleName</span></span>](closedcaption-getsamistylename.md) | <span data-ttu-id="8ec85-131">Recupera il nome di uno stile supportato dal file SAMI corrente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-131">Retrieves the name of a style supported by the current SAMI file.</span></span>                        |



 

<span data-ttu-id="8ec85-132">È possibile accedere all'oggetto **ClosedCaption** tramite la proprietà seguente.</span><span class="sxs-lookup"><span data-stu-id="8ec85-132">The **ClosedCaption** object is accessed through the following property.</span></span>



| <span data-ttu-id="8ec85-133">Oggetto</span><span class="sxs-lookup"><span data-stu-id="8ec85-133">Object</span></span>                      | <span data-ttu-id="8ec85-134">Proprietà</span><span class="sxs-lookup"><span data-stu-id="8ec85-134">Property</span></span>                                  |
|-----------------------------|-------------------------------------------|
| [<span data-ttu-id="8ec85-135">Player</span><span class="sxs-lookup"><span data-stu-id="8ec85-135">Player</span></span>](player-object.md) | [<span data-ttu-id="8ec85-136">closedCaption</span><span class="sxs-lookup"><span data-stu-id="8ec85-136">closedCaption</span></span>](player-closedcaption.md) |



 

## <a name="see-also"></a><span data-ttu-id="8ec85-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8ec85-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ec85-138">**Aggiunta di didascalie chiuse a file multimediali digitali**</span><span class="sxs-lookup"><span data-stu-id="8ec85-138">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="8ec85-139">**Riferimento del modello a oggetti per lo scripting**</span><span class="sxs-lookup"><span data-stu-id="8ec85-139">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




