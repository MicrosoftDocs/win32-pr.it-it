---
title: Evento Player. CdromMediaChange
description: L'evento CdromMediaChange si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD. | Evento Player. CdromMediaChange
ms.assetid: d31a791a-55e5-49ee-bfe5-7488277e3fda
keywords:
- Media Player di Windows Event CdromMediaChange
- Windows Event CdromMediaChange Media Player, classe Player
- Classe Player Windows Media Player, evento CdromMediaChange
topic_type:
- apiref
api_name:
- Player.CdromMediaChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c3125235d5f8d19963b85284e7dbe40c7af408d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327064"
---
# <a name="playercdrommediachange-event"></a><span data-ttu-id="07246-107">Evento Player. CdromMediaChange</span><span class="sxs-lookup"><span data-stu-id="07246-107">Player.CdromMediaChange event</span></span>

<span data-ttu-id="07246-108">L'evento **CdromMediaChange** si verifica quando si inserisce o si espelle un CD o un DVD da un'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="07246-108">The **CdromMediaChange** event occurs when a CD or DVD is inserted into or ejected from a CD or DVD drive.</span></span>

## <a name="syntax"></a><span data-ttu-id="07246-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07246-109">Syntax</span></span>


```JScript
Player.CdromMediaChange(
  CdromNum
)
```



## <a name="parameters"></a><span data-ttu-id="07246-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="07246-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07246-111">*CdromNum*</span><span class="sxs-lookup"><span data-stu-id="07246-111">*CdromNum*</span></span> 
</dt> <dd>

<span data-ttu-id="07246-112">**Numero** (**Long**) che specifica l'indice dell'unità CD o DVD.</span><span class="sxs-lookup"><span data-stu-id="07246-112">**Number** (**long**) specifying the index of the CD or DVD drive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07246-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07246-113">Return value</span></span>

<span data-ttu-id="07246-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="07246-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07246-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="07246-115">Remarks</span></span>

<span data-ttu-id="07246-116">L'indice dell'unità CD corrisponde all'indice di un oggetto **CDROM** in **cdromcollection**.</span><span class="sxs-lookup"><span data-stu-id="07246-116">The index of the CD drive corresponds to the index of a **Cdrom** object in the **CdromCollection**.</span></span>

<span data-ttu-id="07246-117">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="07246-117">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="07246-118">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="07246-118">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="07246-119">**Windows Media Player 10 Mobile:** Questo evento non è supportato.</span><span class="sxs-lookup"><span data-stu-id="07246-119">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="07246-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07246-120">Requirements</span></span>



| <span data-ttu-id="07246-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07246-121">Requirement</span></span> | <span data-ttu-id="07246-122">Valore</span><span class="sxs-lookup"><span data-stu-id="07246-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="07246-123">Versione</span><span class="sxs-lookup"><span data-stu-id="07246-123">Version</span></span><br/> | <span data-ttu-id="07246-124">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="07246-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="07246-125">DLL</span><span class="sxs-lookup"><span data-stu-id="07246-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="07246-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07246-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07246-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07246-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07246-128">**Oggetto cdrom**</span><span class="sxs-lookup"><span data-stu-id="07246-128">**Cdrom Object**</span></span>](cdrom-object.md)
</dt> <dt>

[<span data-ttu-id="07246-129">**Oggetto cdromcollection**</span><span class="sxs-lookup"><span data-stu-id="07246-129">**CdromCollection Object**</span></span>](cdromcollection-object.md)
</dt> <dt>

[<span data-ttu-id="07246-130">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="07246-130">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





