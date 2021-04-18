---
title: Player. stretchToFit
description: La proprietà stretchToFit specifica o recupera un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.
ms.assetid: 9ea02959-602e-4bac-a8aa-dce502d1bb54
keywords:
- Player. stretchToFit Windows Media Player
topic_type:
- apiref
api_name:
- Player.stretchToFit
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7b68042cf2a5bd0e7f718d1e19641edecdf548
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324824"
---
# <a name="playerstretchtofit"></a><span data-ttu-id="f9adc-104">Player. stretchToFit</span><span class="sxs-lookup"><span data-stu-id="f9adc-104">Player.stretchToFit</span></span>

<span data-ttu-id="f9adc-105">La proprietà **stretchToFit** specifica o recupera un valore che indica se il video visualizzato dal controllo Media Player di Windows viene ridimensionato automaticamente per adattarsi alla finestra video, quando la finestra video è più grande delle dimensioni dell'immagine video.</span><span class="sxs-lookup"><span data-stu-id="f9adc-105">The **stretchToFit** property specifies or retrieves a value indicating whether video displayed by the Windows Media Player control automatically sizes to fit the video window, when the video window is larger than the dimensions of the video image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9adc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9adc-106">Syntax</span></span>

<span data-ttu-id="f9adc-107">*Player*. **stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="f9adc-107">*player*.**stretchToFit**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f9adc-108">Valori possibili</span><span class="sxs-lookup"><span data-stu-id="f9adc-108">Possible Values</span></span>

<span data-ttu-id="f9adc-109">Questa proprietà è un **valore booleano** di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f9adc-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="f9adc-110">Valore</span><span class="sxs-lookup"><span data-stu-id="f9adc-110">Value</span></span> | <span data-ttu-id="f9adc-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9adc-111">Description</span></span>                                            |
|-------|--------------------------------------------------------|
| <span data-ttu-id="f9adc-112">true</span><span class="sxs-lookup"><span data-stu-id="f9adc-112">true</span></span>  | <span data-ttu-id="f9adc-113">Il video si estenderà per adattarsi alla finestra.</span><span class="sxs-lookup"><span data-stu-id="f9adc-113">The video will stretch to fit the window.</span></span>              |
| <span data-ttu-id="f9adc-114">false</span><span class="sxs-lookup"><span data-stu-id="f9adc-114">false</span></span> | <span data-ttu-id="f9adc-115">Valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="f9adc-115">Default.</span></span> <span data-ttu-id="f9adc-116">Il video non si adatta alla finestra.</span><span class="sxs-lookup"><span data-stu-id="f9adc-116">The video will not stretch to fit the window.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="f9adc-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f9adc-117">Remarks</span></span>

<span data-ttu-id="f9adc-118">Quando **stretchToFit** è impostato su true, il controllo Media Player Windows mantiene le proporzioni originali del video.</span><span class="sxs-lookup"><span data-stu-id="f9adc-118">When **stretchToFit** is set to true, the Windows Media Player control maintains the original aspect ratio of the video.</span></span> <span data-ttu-id="f9adc-119">Se le proporzioni del video non corrispondono alle proporzioni della finestra video, le aree della maschera nera possono essere visualizzate nella parte superiore e inferiore, o a sinistra e a destra, dell'immagine del video.</span><span class="sxs-lookup"><span data-stu-id="f9adc-119">If the aspect ratio of the video does not match the aspect ratio of the video window, black mask areas may appear on either the top and the bottom, or left and right, of the video image.</span></span>

<span data-ttu-id="f9adc-120">Questa proprietà si applica al controllo Windows Media Player solo se è incorporata in una pagina Web.</span><span class="sxs-lookup"><span data-stu-id="f9adc-120">This property applies to the Windows Media Player control only when embedded in a webpage.</span></span>

<span data-ttu-id="f9adc-121">**Windows Media Player 10 Mobile:** Questa proprietà non è supportata.</span><span class="sxs-lookup"><span data-stu-id="f9adc-121">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9adc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f9adc-122">Requirements</span></span>



| <span data-ttu-id="f9adc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f9adc-123">Requirement</span></span> | <span data-ttu-id="f9adc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f9adc-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f9adc-125">Versione</span><span class="sxs-lookup"><span data-stu-id="f9adc-125">Version</span></span><br/> | <span data-ttu-id="f9adc-126">Windows Media Player versione 7,1 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f9adc-126">Windows Media Player version 7.1 or later.</span></span><br/>                              |
| <span data-ttu-id="f9adc-127">DLL</span><span class="sxs-lookup"><span data-stu-id="f9adc-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="f9adc-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9adc-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9adc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9adc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9adc-130">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="f9adc-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





