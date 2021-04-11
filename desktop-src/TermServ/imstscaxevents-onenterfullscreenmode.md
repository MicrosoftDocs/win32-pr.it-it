---
title: Metodo IMsTscAxEvents OnEnterFullScreenMode
description: Chiamato quando il client entra in modalità schermo intero. Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di scelta rapida per la modalità schermo intero (CTRL + ALT + INTERr).
ms.assetid: dc772492-59a2-4403-8b9a-0aff1801aa6f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnEnterFullScreenMode
- Metodo OnEnterFullScreenMode Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnEnterFullScreenMode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnEnterFullScreenMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 226054fc7b1371bb088deb70ec9e87ea5a340b07
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964420"
---
# <a name="imstscaxeventsonenterfullscreenmode-method"></a><span data-ttu-id="fec01-107">Metodo IMsTscAxEvents:: OnEnterFullScreenMode</span><span class="sxs-lookup"><span data-stu-id="fec01-107">IMsTscAxEvents::OnEnterFullScreenMode method</span></span>

<span data-ttu-id="fec01-108">Chiamato quando il client entra in modalità schermo intero.</span><span class="sxs-lookup"><span data-stu-id="fec01-108">Called when the client enters full-screen mode.</span></span> <span data-ttu-id="fec01-109">Questo evento, ad esempio, viene chiamato quando l'utente preme la combinazione di tasti di [scelta rapida](terminal-services-shortcut-keys.md) per la modalità schermo intero (CTRL + ALT + INTERR).</span><span class="sxs-lookup"><span data-stu-id="fec01-109">For example, this event is called when the user presses the full-screen mode [shortcut key](terminal-services-shortcut-keys.md) combination (CTRL+ALT+BREAK).</span></span>

## <a name="syntax"></a><span data-ttu-id="fec01-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fec01-110">Syntax</span></span>


```C++
void OnEnterFullScreenMode();
```



## <a name="parameters"></a><span data-ttu-id="fec01-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="fec01-111">Parameters</span></span>

<span data-ttu-id="fec01-112">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="fec01-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fec01-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fec01-113">Return value</span></span>

<span data-ttu-id="fec01-114">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fec01-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fec01-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="fec01-115">Remarks</span></span>

<span data-ttu-id="fec01-116">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="fec01-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fec01-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fec01-117">Requirements</span></span>



| <span data-ttu-id="fec01-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="fec01-118">Requirement</span></span> | <span data-ttu-id="fec01-119">Valore</span><span class="sxs-lookup"><span data-stu-id="fec01-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fec01-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec01-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fec01-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fec01-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="fec01-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fec01-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fec01-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fec01-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="fec01-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fec01-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="fec01-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec01-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fec01-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fec01-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fec01-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fec01-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fec01-128">IID</span><span class="sxs-lookup"><span data-stu-id="fec01-128">IID</span></span><br/>                      | <span data-ttu-id="fec01-129">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="fec01-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="fec01-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fec01-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fec01-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="fec01-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





