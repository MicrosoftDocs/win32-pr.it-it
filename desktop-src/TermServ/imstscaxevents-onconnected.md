---
title: Metodo OnConnected IMsTscAxEvents
description: Chiamato quando il controllo client è in fase di creazione di una connessione con un server Host sessione Desktop remoto (host sessione Desktop remoto).
ms.assetid: 9c26d112-c070-4870-93d5-2fcc84a1331f
ms.tgt_platform: multiple
keywords:
- Metodo OnConnected Servizi Desktop remoto
- Metodo OnConnected Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, Metodo OnConnected
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnConnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d83a6a14f58a0704f0a3110532ad8cf8c0d7dc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741322"
---
# <a name="imstscaxeventsonconnected-method"></a><span data-ttu-id="f2aad-106">Metodo IMsTscAxEvents:: OnConnected</span><span class="sxs-lookup"><span data-stu-id="f2aad-106">IMsTscAxEvents::OnConnected method</span></span>

<span data-ttu-id="f2aad-107">Chiamato quando il controllo client è in fase di creazione di una connessione con un server Host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="f2aad-107">Called when the client control is in the process of establishing a connection with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2aad-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f2aad-108">Syntax</span></span>


```C++
void OnConnected();
```



## <a name="parameters"></a><span data-ttu-id="f2aad-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f2aad-109">Parameters</span></span>

<span data-ttu-id="f2aad-110">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="f2aad-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f2aad-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f2aad-111">Return value</span></span>

<span data-ttu-id="f2aad-112">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="f2aad-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2aad-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="f2aad-113">Remarks</span></span>

<span data-ttu-id="f2aad-114">Implementare questo metodo nel sink di evento per ricevere una notifica che il controllo ha stabilito una connessione con un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="f2aad-114">Implement this method in your event sink to receive notification that the control has established a connection with an RD Session Host server.</span></span>

<span data-ttu-id="f2aad-115">Per ulteriori informazioni sulla chiamata a questo metodo, vedere l'evento [**IMsTscAxEvents:: OnLoginComplete**](imstscaxevents-onlogincomplete.md) .</span><span class="sxs-lookup"><span data-stu-id="f2aad-115">Refer to the [**IMsTscAxEvents::OnLoginComplete**](imstscaxevents-onlogincomplete.md) event for more information on calling this method.</span></span>

<span data-ttu-id="f2aad-116">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="f2aad-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2aad-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f2aad-117">Requirements</span></span>



| <span data-ttu-id="f2aad-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2aad-118">Requirement</span></span> | <span data-ttu-id="f2aad-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f2aad-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2aad-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2aad-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f2aad-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f2aad-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f2aad-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f2aad-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f2aad-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f2aad-123">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f2aad-124">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="f2aad-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="f2aad-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2aad-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2aad-126">DLL</span><span class="sxs-lookup"><span data-stu-id="f2aad-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2aad-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2aad-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2aad-128">IID</span><span class="sxs-lookup"><span data-stu-id="f2aad-128">IID</span></span><br/>                      | <span data-ttu-id="f2aad-129">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="f2aad-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="f2aad-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f2aad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2aad-131">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="f2aad-131">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





