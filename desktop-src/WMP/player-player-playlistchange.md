---
title: Evento Player. PlaylistChange
description: L'evento PlaylistChange si verifica quando viene modificata una playlist. | Evento Player. PlaylistChange
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- Media Player di Windows Event PlaylistChange
- Windows Event PlaylistChange Media Player, classe Player
- Classe Player Windows Media Player, evento PlaylistChange
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83d371818e8166b536543246eeecf0090509e62b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326460"
---
# <a name="playerplaylistchange-event"></a><span data-ttu-id="6bb72-107">Evento Player. PlaylistChange</span><span class="sxs-lookup"><span data-stu-id="6bb72-107">Player.PlaylistChange event</span></span>

<span data-ttu-id="6bb72-108">L'evento **PlaylistChange** si verifica quando viene modificata una playlist.</span><span class="sxs-lookup"><span data-stu-id="6bb72-108">The **PlaylistChange** event occurs when a playlist changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bb72-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6bb72-109">Syntax</span></span>


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a><span data-ttu-id="6bb72-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6bb72-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6bb72-111">*Playlist*</span><span class="sxs-lookup"><span data-stu-id="6bb72-111">*Playlist*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb72-112">Oggetto **playlist** che è stato modificato.</span><span class="sxs-lookup"><span data-stu-id="6bb72-112">**Playlist** object which changed.</span></span>

</dd> <dt>

<span data-ttu-id="6bb72-113">*change*</span><span class="sxs-lookup"><span data-stu-id="6bb72-113">*change*</span></span> 
</dt> <dd>

<span data-ttu-id="6bb72-114">**Numero** (**Long**) che indica il tipo di modifica apportata alla playlist.</span><span class="sxs-lookup"><span data-stu-id="6bb72-114">**Number** (**long**) indicating the type of change that occurred to the playlist.</span></span> <span data-ttu-id="6bb72-115">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="6bb72-115">Contains one of the following values.</span></span>



| <span data-ttu-id="6bb72-116">Number</span><span class="sxs-lookup"><span data-stu-id="6bb72-116">Number</span></span> | <span data-ttu-id="6bb72-117">Nome</span><span class="sxs-lookup"><span data-stu-id="6bb72-117">Name</span></span>          |
|--------|---------------|
| <span data-ttu-id="6bb72-118">0</span><span class="sxs-lookup"><span data-stu-id="6bb72-118">0</span></span>      | <span data-ttu-id="6bb72-119">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="6bb72-119">Unknown</span></span>       |
| <span data-ttu-id="6bb72-120">1</span><span class="sxs-lookup"><span data-stu-id="6bb72-120">1</span></span>      | <span data-ttu-id="6bb72-121">Cancella</span><span class="sxs-lookup"><span data-stu-id="6bb72-121">Clear</span></span>         |
| <span data-ttu-id="6bb72-122">2</span><span class="sxs-lookup"><span data-stu-id="6bb72-122">2</span></span>      | <span data-ttu-id="6bb72-123">InfoChange</span><span class="sxs-lookup"><span data-stu-id="6bb72-123">InfoChange</span></span>    |
| <span data-ttu-id="6bb72-124">3</span><span class="sxs-lookup"><span data-stu-id="6bb72-124">3</span></span>      | <span data-ttu-id="6bb72-125">Sposta</span><span class="sxs-lookup"><span data-stu-id="6bb72-125">Move</span></span>          |
| <span data-ttu-id="6bb72-126">4</span><span class="sxs-lookup"><span data-stu-id="6bb72-126">4</span></span>      | <span data-ttu-id="6bb72-127">Delete</span><span class="sxs-lookup"><span data-stu-id="6bb72-127">Delete</span></span>        |
| <span data-ttu-id="6bb72-128">5</span><span class="sxs-lookup"><span data-stu-id="6bb72-128">5</span></span>      | <span data-ttu-id="6bb72-129">Insert</span><span class="sxs-lookup"><span data-stu-id="6bb72-129">Insert</span></span>        |
| <span data-ttu-id="6bb72-130">6</span><span class="sxs-lookup"><span data-stu-id="6bb72-130">6</span></span>      | <span data-ttu-id="6bb72-131">Accoda</span><span class="sxs-lookup"><span data-stu-id="6bb72-131">Append</span></span>        |
| <span data-ttu-id="6bb72-132">7</span><span class="sxs-lookup"><span data-stu-id="6bb72-132">7</span></span>      | <span data-ttu-id="6bb72-133">Non supportato</span><span class="sxs-lookup"><span data-stu-id="6bb72-133">Not supported</span></span> |
| <span data-ttu-id="6bb72-134">8</span><span class="sxs-lookup"><span data-stu-id="6bb72-134">8</span></span>      | <span data-ttu-id="6bb72-135">NameChange</span><span class="sxs-lookup"><span data-stu-id="6bb72-135">NameChange</span></span>    |
| <span data-ttu-id="6bb72-136">9</span><span class="sxs-lookup"><span data-stu-id="6bb72-136">9</span></span>      | <span data-ttu-id="6bb72-137">Non supportate</span><span class="sxs-lookup"><span data-stu-id="6bb72-137">Not supported</span></span> |
| <span data-ttu-id="6bb72-138">10</span><span class="sxs-lookup"><span data-stu-id="6bb72-138">10</span></span>     | <span data-ttu-id="6bb72-139">Ordina</span><span class="sxs-lookup"><span data-stu-id="6bb72-139">Sort</span></span>          |



 

<span data-ttu-id="6bb72-140">È possibile derivare la costante di enumerazione di tipo C anteponendo il valore Name con "wmplc".</span><span class="sxs-lookup"><span data-stu-id="6bb72-140">The C-style enumeration constant can be derived by prefixing the name value with "wmplc".</span></span> <span data-ttu-id="6bb72-141">La costante per lo stato di spostamento, ad esempio, è **wmplcMove**.</span><span class="sxs-lookup"><span data-stu-id="6bb72-141">For example, the constant for the Move state is **wmplcMove**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6bb72-142">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6bb72-142">Return value</span></span>

<span data-ttu-id="6bb72-143">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6bb72-143">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bb72-144">Commenti</span><span class="sxs-lookup"><span data-stu-id="6bb72-144">Remarks</span></span>

<span data-ttu-id="6bb72-145">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="6bb72-145">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="6bb72-146">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="6bb72-146">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="6bb72-147">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6bb72-147">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bb72-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6bb72-148">Requirements</span></span>



| <span data-ttu-id="6bb72-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6bb72-149">Requirement</span></span> | <span data-ttu-id="6bb72-150">Valore</span><span class="sxs-lookup"><span data-stu-id="6bb72-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6bb72-151">Versione</span><span class="sxs-lookup"><span data-stu-id="6bb72-151">Version</span></span><br/> | <span data-ttu-id="6bb72-152">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="6bb72-152">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="6bb72-153">DLL</span><span class="sxs-lookup"><span data-stu-id="6bb72-153">DLL</span></span><br/>     | <dl> <span data-ttu-id="6bb72-154"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6bb72-154"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6bb72-155">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6bb72-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6bb72-156">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="6bb72-156">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





