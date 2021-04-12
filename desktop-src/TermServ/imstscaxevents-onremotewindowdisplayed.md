---
title: Metodo IMsTscAxEvents OnRemoteWindowDisplayed
description: Chiamato quando viene visualizzata una finestra di RemoteApp.
ms.assetid: B1E83486-50CB-4CA4-BD01-2C72938335AF
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteWindowDisplayed
- Metodo OnRemoteWindowDisplayed Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteWindowDisplayed
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteWindowDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f03029f31e1ce2133c74c92c0d6d57f192e4d85f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400735"
---
# <a name="imstscaxeventsonremotewindowdisplayed-method"></a><span data-ttu-id="89863-106">Metodo IMsTscAxEvents:: OnRemoteWindowDisplayed</span><span class="sxs-lookup"><span data-stu-id="89863-106">IMsTscAxEvents::OnRemoteWindowDisplayed method</span></span>

<span data-ttu-id="89863-107">Chiamato quando viene visualizzata una finestra di RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="89863-107">Called when a RemoteApp window is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="89863-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="89863-108">Syntax</span></span>


```C++
void OnRemoteWindowDisplayed(
  [in] VARIANT_BOOL                   vbDisplayed,
  [in] HWND                           hwnd,
  [in] RemoteWindowDisplayedAttribute windowAttribute
);
```



## <a name="parameters"></a><span data-ttu-id="89863-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="89863-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89863-110">*vbDisplayed* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89863-110">*vbDisplayed* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89863-111">Tipo: **Variant \_ bool**</span><span class="sxs-lookup"><span data-stu-id="89863-111">Type: **VARIANT\_BOOL**</span></span>

<span data-ttu-id="89863-112">Indica se la finestra RemoteApp è visualizzata o nascosta.</span><span class="sxs-lookup"><span data-stu-id="89863-112">Indicates whether the RemoteApp window is displayed or hidden.</span></span>

</dd> <dt>

<span data-ttu-id="89863-113">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89863-113">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89863-114">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="89863-114">Type: **HWND**</span></span>

<span data-ttu-id="89863-115">Handle della finestra visualizzata.</span><span class="sxs-lookup"><span data-stu-id="89863-115">The handle of the window displayed.</span></span>

</dd> <dt>

<span data-ttu-id="89863-116">*windowAttribute* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89863-116">*windowAttribute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89863-117">Tipo: **[ **RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span><span class="sxs-lookup"><span data-stu-id="89863-117">Type: **[**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md)**</span></span>

<span data-ttu-id="89863-118">Valore dell'enumerazione [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) che specifica ulteriori informazioni sull'evento.</span><span class="sxs-lookup"><span data-stu-id="89863-118">A value of the [**RemoteWindowDisplayedAttribute**](remotewindowdisplayedattribute.md) enumeration that specifies more information about the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89863-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="89863-119">Return value</span></span>

<span data-ttu-id="89863-120">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="89863-120">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="89863-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="89863-121">Requirements</span></span>



| <span data-ttu-id="89863-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="89863-122">Requirement</span></span> | <span data-ttu-id="89863-123">Valore</span><span class="sxs-lookup"><span data-stu-id="89863-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="89863-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89863-124">Minimum supported client</span></span><br/> | <span data-ttu-id="89863-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="89863-125">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="89863-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="89863-126">Minimum supported server</span></span><br/> | <span data-ttu-id="89863-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89863-127">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="89863-128">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="89863-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="89863-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89863-129"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="89863-130">DLL</span><span class="sxs-lookup"><span data-stu-id="89863-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89863-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89863-131"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="89863-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="89863-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89863-133">**RemoteWindowDisplayedAttribute**</span><span class="sxs-lookup"><span data-stu-id="89863-133">**RemoteWindowDisplayedAttribute**</span></span>](remotewindowdisplayedattribute.md)
</dt> <dt>

[<span data-ttu-id="89863-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="89863-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





