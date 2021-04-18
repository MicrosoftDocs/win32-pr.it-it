---
title: Evento Player. errore MediaError
description: L'evento errore MediaError si verifica quando l'oggetto multimediale presenta una condizione di errore.
ms.assetid: b2e0176a-cc52-4f59-8894-440f426a1b6e
keywords:
- Media Player di Windows Event errore MediaError
- Windows Event errore MediaError Media Player, classe Player
- Classe Player Windows Media Player, evento errore MediaError
topic_type:
- apiref
api_name:
- Player.MediaError
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec8c22825f4aa720efa85275ce520eb81f082fd9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329918"
---
# <a name="playermediaerror-event"></a><span data-ttu-id="c30aa-106">Evento Player. errore MediaError</span><span class="sxs-lookup"><span data-stu-id="c30aa-106">Player.MediaError event</span></span>

<span data-ttu-id="c30aa-107">L'evento **errore MediaError** si verifica quando l'oggetto **multimediale** presenta una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="c30aa-107">The **MediaError** event occurs when the **Media** object has an error condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="c30aa-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c30aa-108">Syntax</span></span>


```JScript
Player.MediaError(
  pMediaObject
)
```



## <a name="parameters"></a><span data-ttu-id="c30aa-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c30aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c30aa-110">*pMediaObject*</span><span class="sxs-lookup"><span data-stu-id="c30aa-110">*pMediaObject*</span></span> 
</dt> <dd>

<span data-ttu-id="c30aa-111">Oggetto **multimediale** con una condizione di errore.</span><span class="sxs-lookup"><span data-stu-id="c30aa-111">**Media** object that has an error condition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c30aa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c30aa-112">Return value</span></span>

<span data-ttu-id="c30aa-113">Questo evento non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c30aa-113">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c30aa-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="c30aa-114">Remarks</span></span>

<span data-ttu-id="c30aa-115">Il valore dei parametri evento viene specificato da Windows Media Player ed è possibile accedervi o passarli a un metodo in un file JScript importato usando il nome del parametro specificato.</span><span class="sxs-lookup"><span data-stu-id="c30aa-115">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="c30aa-116">Questo nome di parametro deve essere digitato esattamente come illustrato, incluse le maiuscole.</span><span class="sxs-lookup"><span data-stu-id="c30aa-116">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="c30aa-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c30aa-117">Requirements</span></span>



| <span data-ttu-id="c30aa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c30aa-118">Requirement</span></span> | <span data-ttu-id="c30aa-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c30aa-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c30aa-120">Versione</span><span class="sxs-lookup"><span data-stu-id="c30aa-120">Version</span></span><br/> | <span data-ttu-id="c30aa-121">Windows Media Player per Windows XP o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="c30aa-121">Windows Media Player for Windows XP or later.</span></span><br/>                           |
| <span data-ttu-id="c30aa-122">DLL</span><span class="sxs-lookup"><span data-stu-id="c30aa-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="c30aa-123"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c30aa-123"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c30aa-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c30aa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30aa-125">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="c30aa-125">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





