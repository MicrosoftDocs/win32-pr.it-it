---
title: Controls. Previous, metodo
description: Il metodo precedente imposta l'elemento corrente sull'elemento precedente nella playlist.
ms.assetid: 09f83306-5e82-4384-ad28-38e406a401d8
keywords:
- Metodo precedente Media Player Windows
- Metodo precedente Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo precedente
topic_type:
- apiref
api_name:
- Controls.previous
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b8fcfacd93412f467e6ef1def5afa6305a6bc0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330003"
---
# <a name="controlsprevious-method"></a><span data-ttu-id="c99d4-106">Controls. Previous, metodo</span><span class="sxs-lookup"><span data-stu-id="c99d4-106">Controls.previous method</span></span>

<span data-ttu-id="c99d4-107">Il metodo **precedente** imposta l'elemento corrente sull'elemento precedente nella playlist.</span><span class="sxs-lookup"><span data-stu-id="c99d4-107">The **previous** method sets the current item to the previous item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="c99d4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c99d4-108">Syntax</span></span>


```JScript
Controls.previous()
```



## <a name="parameters"></a><span data-ttu-id="c99d4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c99d4-109">Parameters</span></span>

<span data-ttu-id="c99d4-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c99d4-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c99d4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c99d4-111">Return value</span></span>

<span data-ttu-id="c99d4-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="c99d4-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c99d4-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="c99d4-113">Remarks</span></span>

<span data-ttu-id="c99d4-114">Se la playlist si trova nella prima voce quando viene richiamato il **precedente** , l'ultima voce nella playlist diventerà quella corrente.</span><span class="sxs-lookup"><span data-stu-id="c99d4-114">If the playlist is on the first entry when **previous** is invoked, the last entry in the playlist will become the current one.</span></span>

## <a name="examples"></a><span data-ttu-id="c99d4-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="c99d4-115">Examples</span></span>

<span data-ttu-id="c99d4-116">Nell'esempio seguente viene creato un elemento BUTTON HTML che usa **Previous** per passare all'elemento precedente nella playlist corrente.</span><span class="sxs-lookup"><span data-stu-id="c99d4-116">The following example creates an HTML BUTTON element that uses **previous** to move to the preceding item in the current playlist.</span></span> <span data-ttu-id="c99d4-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="c99d4-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PREV"  NAME = "PREV"  VALUE = "|<<"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Previous'))

            /* Move to the preceding item in the playlist. */
            Player.controls.previous();
">

```



## <a name="requirements"></a><span data-ttu-id="c99d4-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c99d4-118">Requirements</span></span>



| <span data-ttu-id="c99d4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c99d4-119">Requirement</span></span> | <span data-ttu-id="c99d4-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c99d4-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c99d4-121">Versione</span><span class="sxs-lookup"><span data-stu-id="c99d4-121">Version</span></span><br/> | <span data-ttu-id="c99d4-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="c99d4-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c99d4-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c99d4-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c99d4-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c99d4-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c99d4-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c99d4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c99d4-126">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="c99d4-126">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="c99d4-127">**Controlli. Next**</span><span class="sxs-lookup"><span data-stu-id="c99d4-127">**Controls.next**</span></span>](controls-next.md)
</dt> <dt>

[<span data-ttu-id="c99d4-128">**Controls. Stop**</span><span class="sxs-lookup"><span data-stu-id="c99d4-128">**Controls.stop**</span></span>](controls-stop.md)
</dt> </dl>

 

 





