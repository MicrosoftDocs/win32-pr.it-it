---
title: Player. Close (metodo)
description: Il metodo Close rilascia le risorse di Windows Media Player.
ms.assetid: 15bd5a05-dbfa-4bea-90c2-afd9f69631e0
keywords:
- Chiudi metodo Windows Media Player
- Metodo Close Media Player Windows, classe Player
- Classe Player Windows Media Player, metodo Close
topic_type:
- apiref
api_name:
- Player.close
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: debc2667c42da92b3a2639e0f14c767d2b5b0651
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329714"
---
# <a name="playerclose-method"></a><span data-ttu-id="f17c7-106">Player. Close (metodo)</span><span class="sxs-lookup"><span data-stu-id="f17c7-106">Player.close method</span></span>

<span data-ttu-id="f17c7-107">Il metodo **Close** rilascia le risorse di Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f17c7-107">The **close** method releases Windows Media Player resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="f17c7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f17c7-108">Syntax</span></span>


```JScript
Player.close()
```



## <a name="parameters"></a><span data-ttu-id="f17c7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f17c7-109">Parameters</span></span>

<span data-ttu-id="f17c7-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f17c7-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f17c7-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f17c7-111">Return value</span></span>

<span data-ttu-id="f17c7-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f17c7-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f17c7-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f17c7-113">Remarks</span></span>

<span data-ttu-id="f17c7-114">Questo metodo chiude il file multimediale digitale corrente, non Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="f17c7-114">This method closes the current digital media file, not Windows Media Player itself.</span></span>

## <a name="examples"></a><span data-ttu-id="f17c7-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="f17c7-115">Examples</span></span>

<span data-ttu-id="f17c7-116">Nell'esempio seguente viene creato un elemento BUTTON HTML che, quando selezionato, interrompe la riproduzione in Windows Media Player e rilascia le risorse in uso.</span><span class="sxs-lookup"><span data-stu-id="f17c7-116">The following example creates an HTML BUTTON element that, when clicked, stops playback in Windows Media Player and releases the resources in use.</span></span> <span data-ttu-id="f17c7-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="f17c7-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT  TYPE = "BUTTON"  ID = "CLOSEIT"  VALUE = "Close it"  onClick = "

        /* Close the Player object. */
        Player.close();
">

```



## <a name="requirements"></a><span data-ttu-id="f17c7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f17c7-118">Requirements</span></span>



| <span data-ttu-id="f17c7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="f17c7-119">Requirement</span></span> | <span data-ttu-id="f17c7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="f17c7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f17c7-121">Versione</span><span class="sxs-lookup"><span data-stu-id="f17c7-121">Version</span></span><br/> | <span data-ttu-id="f17c7-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="f17c7-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f17c7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f17c7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="f17c7-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f17c7-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f17c7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f17c7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f17c7-126">**Oggetto Player**</span><span class="sxs-lookup"><span data-stu-id="f17c7-126">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





