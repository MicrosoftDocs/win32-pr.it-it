---
title: Metodo Controls. Play
description: Il metodo Play causa l'avvio della riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.
ms.assetid: 2218a13b-6294-45f5-bb6f-c5a1e433e0c6
keywords:
- Metodo di riproduzione Media Player Windows
- Metodo Play Media Player Windows, classe Controls
- Classe Controls Media Player Windows, metodo Play
topic_type:
- apiref
api_name:
- Controls.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea66f3bc4cf01d194dc44bcdf7b7cc838e1f3799
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331242"
---
# <a name="controlsplay-method"></a><span data-ttu-id="066d5-106">Metodo Controls. Play</span><span class="sxs-lookup"><span data-stu-id="066d5-106">Controls.play method</span></span>

<span data-ttu-id="066d5-107">Il metodo **Play** causa l'avvio della riproduzione dell'elemento multimediale corrente o riprende la riproduzione di un elemento sospeso.</span><span class="sxs-lookup"><span data-stu-id="066d5-107">The **play** method causes the current media item to start playing, or resumes play of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="066d5-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="066d5-108">Syntax</span></span>


```JScript
Controls.play()
```



## <a name="parameters"></a><span data-ttu-id="066d5-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="066d5-109">Parameters</span></span>

<span data-ttu-id="066d5-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="066d5-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="066d5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="066d5-111">Return value</span></span>

<span data-ttu-id="066d5-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="066d5-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="066d5-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="066d5-113">Remarks</span></span>

<span data-ttu-id="066d5-114">Se questo metodo viene chiamato durante l'avanzamento rapido o il riavvolgimento, il valore delle *Impostazioni*. **rate** è impostato su 1,0.</span><span class="sxs-lookup"><span data-stu-id="066d5-114">If this method is called while fast-forwarding or rewinding, the value of *Settings*.**rate** is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="066d5-115">Esempio</span><span class="sxs-lookup"><span data-stu-id="066d5-115">Examples</span></span>

<span data-ttu-id="066d5-116">Nell'esempio seguente viene creato un elemento BUTTON HTML che utilizza **Play** per riprodurre l'elemento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="066d5-116">The following example creates an HTML BUTTON element that uses **play** to play the current media item.</span></span> <span data-ttu-id="066d5-117">L'oggetto **Player** è stato creato con ID = "Player".</span><span class="sxs-lookup"><span data-stu-id="066d5-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<INPUT TYPE = "BUTTON"  ID = "PLAY"  NAME = "PLAY"  VALUE = "Play"
    onClick = "

        /* Check first to be sure the operation is valid. */
        if (Player.controls.isAvailable('Play'))

            /* Start playback. */
            Player.controls.play();
">

```



## <a name="requirements"></a><span data-ttu-id="066d5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="066d5-118">Requirements</span></span>



| <span data-ttu-id="066d5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="066d5-119">Requirement</span></span> | <span data-ttu-id="066d5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="066d5-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="066d5-121">Versione</span><span class="sxs-lookup"><span data-stu-id="066d5-121">Version</span></span><br/> | <span data-ttu-id="066d5-122">Windows Media Player versione 7,0 o successiva.</span><span class="sxs-lookup"><span data-stu-id="066d5-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="066d5-123">DLL</span><span class="sxs-lookup"><span data-stu-id="066d5-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="066d5-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="066d5-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="066d5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="066d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="066d5-126">**Oggetto Controls**</span><span class="sxs-lookup"><span data-stu-id="066d5-126">**Controls Object**</span></span>](controls-object.md)
</dt> </dl>

 

 





