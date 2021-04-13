---
description: Deprecato. L'oggetto PenInputPanel è stato sostituito dal pannello di input di testo (TIP). Si verifica in seguito alla modifica dell'oggetto PenInputPanel tra layout.
ms.assetid: 21d38406-7ed9-4741-a092-ed3a369dc0dc
title: Evento PenInputPanel. PanelChanged (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d6ff0f415e12131221a8dad1c0775a347ef96cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347871"
---
# <a name="peninputpanelpanelchanged-event"></a><span data-ttu-id="88981-104">PenInputPanel. PanelChanged, evento</span><span class="sxs-lookup"><span data-stu-id="88981-104">PenInputPanel.PanelChanged event</span></span>

<span data-ttu-id="88981-105">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="88981-105">Deprecated.</span></span> <span data-ttu-id="88981-106">L'oggetto [**PenInputPanel**](peninputpanel-class.md) è stato sostituito dal [Pannello di input di testo (tip)](text-input-panel-reference.md).</span><span class="sxs-lookup"><span data-stu-id="88981-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="88981-107">Si verifica in seguito alla modifica dell'oggetto [**PenInputPanel**](peninputpanel-class.md) tra layout.</span><span class="sxs-lookup"><span data-stu-id="88981-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object changes between layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="88981-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="88981-108">Syntax</span></span>


```C++
HRESULT PanelChanged(
  [in] PanelType NewPanelType
);
```



## <a name="parameters"></a><span data-ttu-id="88981-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="88981-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88981-110">*NewPanelType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="88981-110">*NewPanelType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88981-111">Nuovo tipo di pannello usato per l'input all'interno dell'oggetto [**PenInputPanel**](peninputpanel-class.md) , dopo l'attivazione dell'evento **PanelChanged** .</span><span class="sxs-lookup"><span data-stu-id="88981-111">The new panel type used for input within the [**PenInputPanel**](peninputpanel-class.md) object, after the **PanelChanged** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88981-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="88981-112">Return value</span></span>

<span data-ttu-id="88981-113">Se l'evento ha esito positivo, viene restituito **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="88981-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="88981-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88981-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="88981-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="88981-115">Remarks</span></span>

<span data-ttu-id="88981-116">Quando si crea un oggetto [**PenInputPanel**](peninputpanel-class.md) , la [**grafia**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) è il **PanelType** predefinito.</span><span class="sxs-lookup"><span data-stu-id="88981-116">When creating a [**PenInputPanel**](peninputpanel-class.md) object, [**Handwriting**](/windows/win32/api/peninputpanel/ne-peninputpanel-paneltype) is the default **PanelType**.</span></span> <span data-ttu-id="88981-117">Se si modifica il pannello impostando la proprietà [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) prima che il pannello input penna diventi attivo per la prima volta, si verifica un evento **PanelChanged** .</span><span class="sxs-lookup"><span data-stu-id="88981-117">If you change the panel by setting the [**CurrentPanel**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_currentpanel) property before the pen input panel becomes active for the first time, a **PanelChanged** event occurs.</span></span>

<span data-ttu-id="88981-118">L'evento **PanelChanged** non viene generato quando l'utente cambia tra i pad di scrittura riga e boxed.</span><span class="sxs-lookup"><span data-stu-id="88981-118">The **PanelChanged** event is not raised when the user changes between Lined and Boxed writing pads.</span></span>

## <a name="requirements"></a><span data-ttu-id="88981-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="88981-119">Requirements</span></span>



| <span data-ttu-id="88981-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="88981-120">Requirement</span></span> | <span data-ttu-id="88981-121">Valore</span><span class="sxs-lookup"><span data-stu-id="88981-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88981-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88981-122">Minimum supported client</span></span><br/> | <span data-ttu-id="88981-123">Solo app desktop Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="88981-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="88981-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="88981-124">Minimum supported server</span></span><br/> | <span data-ttu-id="88981-125">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="88981-125">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="88981-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="88981-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="88981-127"><dt>Msinkaut. h (richiede anche Msinkaut \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="88981-127"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="88981-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="88981-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="88981-129"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="88981-129"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="88981-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="88981-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88981-131">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="88981-131">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 
