---
title: Metodo IMsTscAxEvents OnLeaveFullScreenMode
description: Chiamato quando il client lascia la modalità a schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL + ALT + INTERr).
ms.assetid: 95c5d427-b6e2-4a42-9816-b130ab533ac0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnLeaveFullScreenMode
- Metodo OnLeaveFullScreenMode Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnLeaveFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnLeaveFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4ee414f2dceba35a17ff86bce03c83d75aab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048507"
---
# <a name="imstscaxeventsonleavefullscreenmode-method"></a><span data-ttu-id="30e50-107">Metodo IMsTscAxEvents:: OnLeaveFullScreenMode</span><span class="sxs-lookup"><span data-stu-id="30e50-107">IMsTscAxEvents::OnLeaveFullScreenMode method</span></span>

<span data-ttu-id="30e50-108">Chiamato quando il client lascia la modalità a schermo intero.</span><span class="sxs-lookup"><span data-stu-id="30e50-108">Called when the client leaves full-screen mode.</span></span> <span data-ttu-id="30e50-109">Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).</span><span class="sxs-lookup"><span data-stu-id="30e50-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="30e50-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="30e50-110">Syntax</span></span>


```C++
void OnLeaveFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="30e50-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="30e50-111">Parameters</span></span>

<span data-ttu-id="30e50-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="30e50-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30e50-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="30e50-113">Return value</span></span>

<span data-ttu-id="30e50-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="30e50-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="30e50-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="30e50-115">Remarks</span></span>

<span data-ttu-id="30e50-116">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="30e50-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30e50-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="30e50-117">Requirements</span></span>



| <span data-ttu-id="30e50-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="30e50-118">Requirement</span></span> | <span data-ttu-id="30e50-119">Valore</span><span class="sxs-lookup"><span data-stu-id="30e50-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="30e50-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30e50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="30e50-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30e50-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="30e50-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="30e50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="30e50-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30e50-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="30e50-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="30e50-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="30e50-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30e50-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30e50-126">DLL</span><span class="sxs-lookup"><span data-stu-id="30e50-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30e50-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30e50-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="30e50-128">IID</span><span class="sxs-lookup"><span data-stu-id="30e50-128">IID</span></span><br/>                      | <span data-ttu-id="30e50-129">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="30e50-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="30e50-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="30e50-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30e50-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="30e50-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





