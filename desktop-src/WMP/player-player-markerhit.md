---
title: Evento Player. MarkerHit
description: L'evento MarkerHit si verifica quando viene raggiunto un marcatore. | Evento Player. MarkerHit
ms.assetid: c97aff61-6f06-4589-a75b-ac2af340cb1d
keywords:
- Media Player di Windows Event MarkerHit
- Windows Event MarkerHit Media Player, classe Player
- Classe Player Windows Media Player, evento MarkerHit
topic_type:
- apiref
api_name:
- Player.MarkerHit
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cce6b9ca7c103e9a9e9151a7ff0467a59786b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326309"
---
# <a name="playermarkerhit-event"></a><span data-ttu-id="e3a29-107">Evento Player. MarkerHit</span><span class="sxs-lookup"><span data-stu-id="e3a29-107">Player.MarkerHit event</span></span>

<span data-ttu-id="e3a29-108">L'evento **MarkerHit** si verifica quando viene raggiunto un marcatore.</span><span class="sxs-lookup"><span data-stu-id="e3a29-108">The **MarkerHit** event occurs when a marker is reached.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a29-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3a29-109">Syntax</span></span>


```JScript
Player.MarkerHit(
  MarkerNum
)
```



## <a name="parameters"></a><span data-ttu-id="e3a29-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e3a29-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3a29-111">*MarkerNum*</span><span class="sxs-lookup"><span data-stu-id="e3a29-111">*MarkerNum*</span></span> 
</dt> <dd>

<span data-ttu-id="e3a29-112">**Numero** (**Long**) che indica il numero del marcatore raggiunto.</span><span class="sxs-lookup"><span data-stu-id="e3a29-112">**Number** (**long**) indicating the number of the marker that was hit.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3a29-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e3a29-113">Return value</span></span>

<span data-ttu-id="e3a29-114">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="e3a29-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a29-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3a29-115">Remarks</span></span>

<span data-ttu-id="e3a29-116">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="e3a29-116">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="e3a29-117">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="e3a29-117">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a29-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3a29-118">Requirements</span></span>



| <span data-ttu-id="e3a29-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3a29-119">Requirement</span></span> | <span data-ttu-id="e3a29-120">Valore</span><span class="sxs-lookup"><span data-stu-id="e3a29-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a29-121">Versione</span><span class="sxs-lookup"><span data-stu-id="e3a29-121">Version</span></span><br/> | <span data-ttu-id="e3a29-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="e3a29-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e3a29-123">DLL</span><span class="sxs-lookup"><span data-stu-id="e3a29-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="e3a29-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3a29-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a29-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3a29-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a29-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="e3a29-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





