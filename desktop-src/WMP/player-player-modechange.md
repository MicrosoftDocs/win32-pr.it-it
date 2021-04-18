---
title: Evento Player. ModeChange
description: L'evento ModeChange si verifica quando viene modificata una modalità di Windows Media Player. | Evento Player. ModeChange
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- Media Player di Windows Event ModeChange
- Windows Event ModeChange Media Player, classe Player
- Classe Player Windows Media Player, evento ModeChange
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb202672c7fce6705b8e86889c0ca44d7004a19e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325833"
---
# <a name="playermodechange-event"></a><span data-ttu-id="b15e4-107">Evento Player. ModeChange</span><span class="sxs-lookup"><span data-stu-id="b15e4-107">Player.ModeChange event</span></span>

<span data-ttu-id="b15e4-108">L'evento **ModeChange** si verifica quando viene modificata una modalità di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="b15e4-108">The **ModeChange** event occurs when a mode of Windows Media Player is changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="b15e4-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b15e4-109">Syntax</span></span>


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a><span data-ttu-id="b15e4-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b15e4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b15e4-111">*ModeName*</span><span class="sxs-lookup"><span data-stu-id="b15e4-111">*ModeName*</span></span> 
</dt> <dd>

<span data-ttu-id="b15e4-112">**Stringa** che indica la modalità che è stata modificata.</span><span class="sxs-lookup"><span data-stu-id="b15e4-112">**String** indicating the mode that was changed.</span></span> <span data-ttu-id="b15e4-113">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b15e4-113">Contains one of the following values.</span></span>



| <span data-ttu-id="b15e4-114">Valore</span><span class="sxs-lookup"><span data-stu-id="b15e4-114">Value</span></span>   | <span data-ttu-id="b15e4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b15e4-115">Description</span></span>                                         |
|---------|-----------------------------------------------------|
| <span data-ttu-id="b15e4-116">shuffle</span><span class="sxs-lookup"><span data-stu-id="b15e4-116">shuffle</span></span> | <span data-ttu-id="b15e4-117">Le tracce vengono riprodotte in ordine casuale.</span><span class="sxs-lookup"><span data-stu-id="b15e4-117">Tracks are played in random order.</span></span>                  |
| <span data-ttu-id="b15e4-118">loop</span><span class="sxs-lookup"><span data-stu-id="b15e4-118">loop</span></span>    | <span data-ttu-id="b15e4-119">L'intera sequenza di tracce viene riprodotta ripetutamente.</span><span class="sxs-lookup"><span data-stu-id="b15e4-119">The entire sequence of tracks is played repeatedly.</span></span> |



 

</dd> <dt>

<span data-ttu-id="b15e4-120">*NewValue*</span><span class="sxs-lookup"><span data-stu-id="b15e4-120">*NewValue*</span></span> 
</dt> <dd>

<span data-ttu-id="b15e4-121">**Valore booleano** che indica il nuovo stato della modalità specificata.</span><span class="sxs-lookup"><span data-stu-id="b15e4-121">**Boolean** indicating the new state of the specified mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b15e4-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b15e4-122">Return value</span></span>

<span data-ttu-id="b15e4-123">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="b15e4-123">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b15e4-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b15e4-124">Remarks</span></span>

<span data-ttu-id="b15e4-125">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="b15e4-125">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="b15e4-126">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="b15e4-126">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="b15e4-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b15e4-127">Requirements</span></span>



| <span data-ttu-id="b15e4-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="b15e4-128">Requirement</span></span> | <span data-ttu-id="b15e4-129">Valore</span><span class="sxs-lookup"><span data-stu-id="b15e4-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b15e4-130">Versione</span><span class="sxs-lookup"><span data-stu-id="b15e4-130">Version</span></span><br/> | <span data-ttu-id="b15e4-131">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="b15e4-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b15e4-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b15e4-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="b15e4-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b15e4-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b15e4-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b15e4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b15e4-135">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="b15e4-135">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="b15e4-136">**Settings. getMode**</span><span class="sxs-lookup"><span data-stu-id="b15e4-136">**Settings.getMode**</span></span>](settings-getmode.md)
</dt> <dt>

[<span data-ttu-id="b15e4-137">**Settings. semode**</span><span class="sxs-lookup"><span data-stu-id="b15e4-137">**Settings.setMode**</span></span>](settings-setmode.md)
</dt> </dl>

 

 





