---
title: Metodo IMsTscAxEvents OnFocusReleased
description: Chiamato quando viene premuta la combinazione di tasti di attivazione della versione. Questo evento, ad esempio, viene chiamato quando l'utente preme CTRL + ALT + freccia sinistra o la combinazione di tasti CTRL + ALT + freccia destra.
ms.assetid: f5d755b0-4b8f-4d62-8dc4-f6b63e3819e5
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnFocusReleased
- Metodo OnFocusReleased Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnFocusReleased
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFocusReleased
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eff03f95d4ebbb068bccbfd9f68a930c00f0b00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301879"
---
# <a name="imstscaxeventsonfocusreleased-method"></a><span data-ttu-id="93c5f-107">Metodo IMsTscAxEvents:: OnFocusReleased</span><span class="sxs-lookup"><span data-stu-id="93c5f-107">IMsTscAxEvents::OnFocusReleased method</span></span>

<span data-ttu-id="93c5f-108">Chiamato quando viene premuta la combinazione di tasti di attivazione della versione.</span><span class="sxs-lookup"><span data-stu-id="93c5f-108">Called when the release focus key combination is pressed.</span></span> <span data-ttu-id="93c5f-109">Questo evento, ad esempio, viene chiamato quando l'utente preme CTRL + ALT + freccia sinistra o la combinazione di tasti CTRL + ALT + freccia destra.</span><span class="sxs-lookup"><span data-stu-id="93c5f-109">For example, this event is called when the user presses the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination.</span></span>

<span data-ttu-id="93c5f-110">Questo evento consente al contenitore di controlli ActiveX di prendere il controllo dal controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="93c5f-110">This event enables the ActiveX control container to take away control from the ActiveX control.</span></span> <span data-ttu-id="93c5f-111">Questo, ad esempio, è utile in uno scenario in cui non è presente un mouse e le combinazioni di tasti speciali, ad esempio ALT + TAB, vengono reindirizzate al server.</span><span class="sxs-lookup"><span data-stu-id="93c5f-111">For example, this is useful in a scenario where you do not have a mouse, and special key combinations such as ALT+TAB are being redirected to the server.</span></span> <span data-ttu-id="93c5f-112">In questo caso, non è possibile riportare lo stato attivo alla tastiera sul desktop locale.</span><span class="sxs-lookup"><span data-stu-id="93c5f-112">In this case, you do not have a way to return the keyboard focus back to the local desktop.</span></span> <span data-ttu-id="93c5f-113">Tuttavia, con la combinazione di tasti CTRL + ALT + freccia sinistra o CTRL + ALT + freccia destra, il contenitore ActiveX può restare in ascolto di questo evento e rispondere spostando lo stato attivo dal controllo ActiveX.</span><span class="sxs-lookup"><span data-stu-id="93c5f-113">However, with the CTRL+ALT+LEFT ARROW or the CTRL+ALT+RIGHT ARROW key combination, the ActiveX container can listen for this event and respond by taking focus away from the ActiveX control.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c5f-114">Sintassi</span><span class="sxs-lookup"><span data-stu-id="93c5f-114">Syntax</span></span>


```C++
void OnFocusReleased(
  [in] INT iDirection
);
```



## <a name="parameters"></a><span data-ttu-id="93c5f-115">Parametri</span><span class="sxs-lookup"><span data-stu-id="93c5f-115">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93c5f-116">*iDirection* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93c5f-116">*iDirection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93c5f-117">Il parametro direction di 1 (CTRL + ALT + freccia destra) o 1 (CTRL + ALT + freccia sinistra).</span><span class="sxs-lookup"><span data-stu-id="93c5f-117">The direction parameter of 1 (CTRL+ALT+RIGHT ARROW) or  1 (CTRL+ALT+LEFT ARROW).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93c5f-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="93c5f-118">Return value</span></span>

<span data-ttu-id="93c5f-119">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="93c5f-119">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="93c5f-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="93c5f-120">Remarks</span></span>

<span data-ttu-id="93c5f-121">Questo evento è disponibile quando nel client viene usato Connessione Desktop remoto 6,0.</span><span class="sxs-lookup"><span data-stu-id="93c5f-121">This event is available when Remote Desktop Connection 6.0 is used on the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="93c5f-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="93c5f-122">Requirements</span></span>



| <span data-ttu-id="93c5f-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c5f-123">Requirement</span></span> | <span data-ttu-id="93c5f-124">Valore</span><span class="sxs-lookup"><span data-stu-id="93c5f-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="93c5f-125">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c5f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="93c5f-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93c5f-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="93c5f-127">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="93c5f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="93c5f-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93c5f-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="93c5f-129">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="93c5f-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="93c5f-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c5f-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="93c5f-131">DLL</span><span class="sxs-lookup"><span data-stu-id="93c5f-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c5f-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93c5f-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="93c5f-133">IID</span><span class="sxs-lookup"><span data-stu-id="93c5f-133">IID</span></span><br/>                      | <span data-ttu-id="93c5f-134">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="93c5f-134">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="93c5f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="93c5f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93c5f-136">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="93c5f-136">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





