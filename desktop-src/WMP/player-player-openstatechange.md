---
title: Evento Player. OpenStateChange
description: L'evento OpenStateChange si verifica in seguito alla modifica del valore della proprietà openState. | Evento Player. OpenStateChange
ms.assetid: b6b840ab-72c7-4150-a259-1e7d8afcec81
keywords:
- Media Player di Windows Event OpenStateChange
- Windows Event OpenStateChange Media Player, classe Player
- Classe Player Windows Media Player, evento OpenStateChange
topic_type:
- apiref
api_name:
- Player.OpenStateChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 020a25a811623b9f7d7dd8f316c470cada6a142b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326463"
---
# <a name="playeropenstatechange-event"></a><span data-ttu-id="dde45-107">Evento Player. OpenStateChange</span><span class="sxs-lookup"><span data-stu-id="dde45-107">Player.OpenStateChange event</span></span>

<span data-ttu-id="dde45-108">L'evento **OpenStateChange** si verifica in seguito alla modifica del valore della proprietà **openState** .</span><span class="sxs-lookup"><span data-stu-id="dde45-108">The **OpenStateChange** event occurs when the **openState** property changes value.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde45-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dde45-109">Syntax</span></span>


```JScript
Player.OpenStateChange(
  NewState
)
```



## <a name="parameters"></a><span data-ttu-id="dde45-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="dde45-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde45-111">*NewState*</span><span class="sxs-lookup"><span data-stu-id="dde45-111">*NewState*</span></span> 
</dt> <dd>

<span data-ttu-id="dde45-112">**Numero** (**Long**) che specifica il nuovo stato aperto.</span><span class="sxs-lookup"><span data-stu-id="dde45-112">**Number** (**long**) specifying the new open state.</span></span> <span data-ttu-id="dde45-113">Per una tabella di valori, vedere [openState](player-openstate.md) .</span><span class="sxs-lookup"><span data-stu-id="dde45-113">See [openState](player-openstate.md) for a table of values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde45-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dde45-114">Return value</span></span>

<span data-ttu-id="dde45-115">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="dde45-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dde45-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="dde45-116">Remarks</span></span>

<span data-ttu-id="dde45-117">Windows Media Player può passare attraverso diversi stati aperti mentre tenta di aprire un file di rete, ad esempio l'individuazione del server, la connessione al server e infine l'apertura del file.</span><span class="sxs-lookup"><span data-stu-id="dde45-117">Windows Media Player can go through several open states while it attempts to open a network file, such as locating the server, connecting to the server, and finally opening the file.</span></span> <span data-ttu-id="dde45-118">Questo evento verrà generato ogni volta che viene modificato lo stato di apertura.</span><span class="sxs-lookup"><span data-stu-id="dde45-118">This event will be fired each time the open state changes.</span></span>

<span data-ttu-id="dde45-119">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="dde45-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="dde45-120">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="dde45-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="dde45-121">Non è garantito che gli Stati di Windows Media Player vengano eseguiti in un ordine particolare.</span><span class="sxs-lookup"><span data-stu-id="dde45-121">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="dde45-122">Inoltre, non tutti gli Stati si verificano necessariamente durante una sequenza di eventi.</span><span class="sxs-lookup"><span data-stu-id="dde45-122">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="dde45-123">Non è necessario scrivere codice che si basa sull'ordine di stato.</span><span class="sxs-lookup"><span data-stu-id="dde45-123">You should not write code that relies upon state order.</span></span>

## <a name="requirements"></a><span data-ttu-id="dde45-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dde45-124">Requirements</span></span>



| <span data-ttu-id="dde45-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="dde45-125">Requirement</span></span> | <span data-ttu-id="dde45-126">Valore</span><span class="sxs-lookup"><span data-stu-id="dde45-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dde45-127">Versione</span><span class="sxs-lookup"><span data-stu-id="dde45-127">Version</span></span><br/> | <span data-ttu-id="dde45-128">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="dde45-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="dde45-129">DLL</span><span class="sxs-lookup"><span data-stu-id="dde45-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="dde45-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dde45-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dde45-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dde45-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dde45-132">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="dde45-132">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="dde45-133">**Player. openState**</span><span class="sxs-lookup"><span data-stu-id="dde45-133">**Player.openState**</span></span>](player-openstate.md)
</dt> </dl>

 

 





