---
title: Evento Player. DomainChange
description: L'evento DomainChange si verifica quando viene modificato il dominio DVD. | Evento Player. DomainChange
ms.assetid: 01965492-276e-4d30-99eb-767e0776b423
keywords:
- Media Player di Windows Event DomainChange
- Windows Event DomainChange Media Player, classe Player
- Classe Player Windows Media Player, evento DomainChange
topic_type:
- apiref
api_name:
- Player.DomainChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9637913451aa5bba937906130899c46e0bd34d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329303"
---
# <a name="playerdomainchange-event"></a><span data-ttu-id="95f8f-107">Evento Player. DomainChange</span><span class="sxs-lookup"><span data-stu-id="95f8f-107">Player.DomainChange event</span></span>

<span data-ttu-id="95f8f-108">L'evento **DomainChange** si verifica quando viene modificato il dominio DVD.</span><span class="sxs-lookup"><span data-stu-id="95f8f-108">The **DomainChange** event occurs when the DVD domain changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="95f8f-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="95f8f-109">Syntax</span></span>


```JScript
Player.DomainChange(
  strDomain
)
```



## <a name="parameters"></a><span data-ttu-id="95f8f-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="95f8f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95f8f-111">*strDomain*</span><span class="sxs-lookup"><span data-stu-id="95f8f-111">*strDomain*</span></span> 
</dt> <dd>

<span data-ttu-id="95f8f-112">**Stringa** che indica il nuovo dominio.</span><span class="sxs-lookup"><span data-stu-id="95f8f-112">**String** indicating the new domain.</span></span> <span data-ttu-id="95f8f-113">Contiene uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="95f8f-113">Contains one of the following values.</span></span>



| <span data-ttu-id="95f8f-114">string</span><span class="sxs-lookup"><span data-stu-id="95f8f-114">String</span></span>            | <span data-ttu-id="95f8f-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="95f8f-115">Description</span></span>                                                          |
|-------------------|----------------------------------------------------------------------|
| <span data-ttu-id="95f8f-116">FirstPlay</span><span class="sxs-lookup"><span data-stu-id="95f8f-116">firstplay</span></span>         | <span data-ttu-id="95f8f-117">Esecuzione dell'inizializzazione predefinita di un disco DVD.</span><span class="sxs-lookup"><span data-stu-id="95f8f-117">Performing default initialization of a DVD disc.</span></span>                     |
| <span data-ttu-id="95f8f-118">videoManagerMenu</span><span class="sxs-lookup"><span data-stu-id="95f8f-118">videoManagerMenu</span></span>  | <span data-ttu-id="95f8f-119">Visualizzazione dei menu per l'intero disco. Noto anche come menu radice o menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="95f8f-119">Displaying menus for whole disc. Also known as Root Menu or topMenu.</span></span> |
| <span data-ttu-id="95f8f-120">videoTitleSetMenu</span><span class="sxs-lookup"><span data-stu-id="95f8f-120">videoTitleSetMenu</span></span> | <span data-ttu-id="95f8f-121">Visualizzazione dei menu per il set di titoli corrente.</span><span class="sxs-lookup"><span data-stu-id="95f8f-121">Displaying menus for current title set.</span></span> <span data-ttu-id="95f8f-122">Noto anche come titleMenu.</span><span class="sxs-lookup"><span data-stu-id="95f8f-122">Also known as titleMenu.</span></span>     |
| <span data-ttu-id="95f8f-123">title</span><span class="sxs-lookup"><span data-stu-id="95f8f-123">title</span></span>             | <span data-ttu-id="95f8f-124">Visualizzazione del titolo corrente.</span><span class="sxs-lookup"><span data-stu-id="95f8f-124">Displaying the current title.</span></span>                                        |
| <span data-ttu-id="95f8f-125">stop</span><span class="sxs-lookup"><span data-stu-id="95f8f-125">stop</span></span>              | <span data-ttu-id="95f8f-126">Il navigatore DVD si trova nel dominio di arresto DVD.</span><span class="sxs-lookup"><span data-stu-id="95f8f-126">The DVD Navigator is in the DVD Stop domain.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95f8f-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="95f8f-127">Return value</span></span>

<span data-ttu-id="95f8f-128">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="95f8f-128">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="95f8f-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="95f8f-129">Remarks</span></span>

<span data-ttu-id="95f8f-130">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="95f8f-130">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="95f8f-131">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="95f8f-131">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="95f8f-132">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="95f8f-132">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="95f8f-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="95f8f-133">Requirements</span></span>



| <span data-ttu-id="95f8f-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="95f8f-134">Requirement</span></span> | <span data-ttu-id="95f8f-135">Valore</span><span class="sxs-lookup"><span data-stu-id="95f8f-135">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="95f8f-136">Versione</span><span class="sxs-lookup"><span data-stu-id="95f8f-136">Version</span></span><br/> | <span data-ttu-id="95f8f-137">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="95f8f-137">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="95f8f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="95f8f-138">DLL</span></span><br/>     | <dl> <span data-ttu-id="95f8f-139"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95f8f-139"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95f8f-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="95f8f-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95f8f-141">**Oggetto DVD**</span><span class="sxs-lookup"><span data-stu-id="95f8f-141">**DVD Object**</span></span>](dvd-object.md)
</dt> <dt>

[<span data-ttu-id="95f8f-142">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="95f8f-142">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





