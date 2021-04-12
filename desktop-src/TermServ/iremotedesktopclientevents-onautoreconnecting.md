---
title: Metodo IRemoteDesktopClientEvents OnAutoReconnecting
description: Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting
- Metodo OnAutoReconnecting Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519006"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a><span data-ttu-id="fb332-106">Metodo IRemoteDesktopClientEvents:: OnAutoReconnecting</span><span class="sxs-lookup"><span data-stu-id="fb332-106">IRemoteDesktopClientEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="fb332-107">Chiamato quando il controllo client tenta di ristabilire automaticamente una connessione a una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="fb332-107">Called when the client control attempts to automatically reestablish a connection to a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb332-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb332-108">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="fb332-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb332-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb332-110">*disconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-111">Motivo dell'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="fb332-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="fb332-112">*ExtendedDisconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-113">Informazioni estese per l'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="fb332-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="fb332-114">*disconnectErrorMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-115">Messaggio di errore per l'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="fb332-115">The error message for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="fb332-116">*NetworkAvailable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-116">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-117">Indica se la rete è disponibile.</span><span class="sxs-lookup"><span data-stu-id="fb332-117">Whether the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="fb332-118">*attemptCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-118">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-119">Il tentativo è.</span><span class="sxs-lookup"><span data-stu-id="fb332-119">Which attempt this is.</span></span>

</dd> <dt>

<span data-ttu-id="fb332-120">*maxAttemptCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fb332-120">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb332-121">Verrà eseguito il numero massimo di tentativi di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="fb332-121">The maximum number of reconnect attempts will be performed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb332-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb332-122">Return value</span></span>

<span data-ttu-id="fb332-123">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="fb332-123">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb332-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb332-124">Requirements</span></span>



| <span data-ttu-id="fb332-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb332-125">Requirement</span></span> | <span data-ttu-id="fb332-126">Valore</span><span class="sxs-lookup"><span data-stu-id="fb332-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb332-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb332-127">Minimum supported client</span></span><br/> | <span data-ttu-id="fb332-128">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fb332-128">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="fb332-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fb332-129">Minimum supported server</span></span><br/> | <span data-ttu-id="fb332-130">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fb332-130">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="fb332-131">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="fb332-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb332-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb332-132"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fb332-133">DLL</span><span class="sxs-lookup"><span data-stu-id="fb332-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb332-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb332-134"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="fb332-135">IID</span><span class="sxs-lookup"><span data-stu-id="fb332-135">IID</span></span><br/>                      | <span data-ttu-id="fb332-136">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="fb332-136">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fb332-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb332-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb332-138">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="fb332-138">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





