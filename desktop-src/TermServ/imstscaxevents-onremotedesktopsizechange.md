---
title: Metodo IMsTscAxEvents OnRemoteDesktopSizeChange
description: Chiamato per indicare che la dimensione del controllo client sul desktop remoto è cambiata in risposta a un'operazione di controllo client.
ms.assetid: 6d27aec0-7249-4aac-8755-186815b50be7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnRemoteDesktopSizeChange
- Metodo OnRemoteDesktopSizeChange Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnRemoteDesktopSizeChange
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnRemoteDesktopSizeChange
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6aee74049ea726b4e2686a028359afe01d2d7632
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518052"
---
# <a name="imstscaxeventsonremotedesktopsizechange-method"></a><span data-ttu-id="e8cc0-106">Metodo IMsTscAxEvents:: OnRemoteDesktopSizeChange</span><span class="sxs-lookup"><span data-stu-id="e8cc0-106">IMsTscAxEvents::OnRemoteDesktopSizeChange method</span></span>

<span data-ttu-id="e8cc0-107">Chiamato per indicare che la dimensione del controllo client sul desktop remoto è cambiata in risposta a un'operazione di controllo client.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-107">Called to indicate that the size of the client control on the remote desktop has changed in response to a client control operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8cc0-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8cc0-108">Syntax</span></span>


```C++
void OnRemoteDesktopSizeChange(
  [in] long width,
  [in] long height
);
```



## <a name="parameters"></a><span data-ttu-id="e8cc0-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8cc0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8cc0-110">*larghezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8cc0-110">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8cc0-111">Larghezza, in pixel, del desktop remoto ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-111">Width, in pixels, of the resized remote desktop.</span></span>

</dd> <dt>

<span data-ttu-id="e8cc0-112">*altezza* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8cc0-112">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8cc0-113">Altezza, in pixel, del desktop remoto ridimensionato.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-113">Height, in pixels, of the resized remote desktop.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8cc0-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8cc0-114">Return value</span></span>

<span data-ttu-id="e8cc0-115">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8cc0-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="e8cc0-116">Remarks</span></span>

<span data-ttu-id="e8cc0-117">Questo evento consente al contenitore di determinare se deve essere ridimensionato in risposta a un'operazione di controllo client, il che potrebbe comportare una dimensione del desktop visualizzabile più grande.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-117">This event allows the container to determine if it must resize itself in response to a client control operation, which could result in a larger viewable desktop size.</span></span> <span data-ttu-id="e8cc0-118">Si noti che il controllo regola automaticamente le barre di scorrimento per le nuove dimensioni della sessione.</span><span class="sxs-lookup"><span data-stu-id="e8cc0-118">Note that the control will automatically adjust scroll bars for the new session size.</span></span>

<span data-ttu-id="e8cc0-119">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="e8cc0-119">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e8cc0-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8cc0-120">Requirements</span></span>



| <span data-ttu-id="e8cc0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8cc0-121">Requirement</span></span> | <span data-ttu-id="e8cc0-122">Valore</span><span class="sxs-lookup"><span data-stu-id="e8cc0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e8cc0-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8cc0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e8cc0-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8cc0-124">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="e8cc0-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8cc0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e8cc0-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8cc0-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="e8cc0-127">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="e8cc0-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8cc0-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8cc0-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8cc0-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e8cc0-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8cc0-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8cc0-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="e8cc0-131">IID</span><span class="sxs-lookup"><span data-stu-id="e8cc0-131">IID</span></span><br/>                      | <span data-ttu-id="e8cc0-132">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="e8cc0-132">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e8cc0-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8cc0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8cc0-134">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="e8cc0-134">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





