---
title: Metodo disconnected IRemoteDesktopClientEvents
description: Chiamato quando il controllo client è stato disconnesso da una sessione remota.
ms.assetid: EA26B530-0AA8-49D6-8E3C-E53179FC5104
ms.tgt_platform: multiple
keywords:
- Metodo disconnected Servizi Desktop remoto
- Metodo disconnected Servizi Desktop remoto, interfaccia IRemoteDesktopClientEvents
- Interfaccia IRemoteDesktopClientEvents Servizi Desktop remoto, metodo disconnected
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bd59b03fe9cb23309d53773289291c8a791935a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742383"
---
# <a name="iremotedesktopclienteventsondisconnected-method"></a><span data-ttu-id="1701d-106">Metodo IRemoteDesktopClientEvents:: disconnected</span><span class="sxs-lookup"><span data-stu-id="1701d-106">IRemoteDesktopClientEvents::OnDisconnected method</span></span>

<span data-ttu-id="1701d-107">Chiamato quando il controllo client è stato disconnesso da una sessione remota.</span><span class="sxs-lookup"><span data-stu-id="1701d-107">Called when the client control has been disconnected from a remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="1701d-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1701d-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long disconnectReason,
  [in] long ExtendedDisconnectReason,
  [in] BSTR disconnectErrorMessage
);
```



## <a name="parameters"></a><span data-ttu-id="1701d-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="1701d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1701d-110">*disconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1701d-110">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1701d-111">Motivo dell'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="1701d-111">The reason for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="1701d-112">*ExtendedDisconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1701d-112">*ExtendedDisconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1701d-113">Informazioni estese per l'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="1701d-113">Extended information for the disconnect event.</span></span>

</dd> <dt>

<span data-ttu-id="1701d-114">*disconnectErrorMessage* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1701d-114">*disconnectErrorMessage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1701d-115">Messaggio di errore per l'evento di disconnessione.</span><span class="sxs-lookup"><span data-stu-id="1701d-115">The error message for the disconnect event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1701d-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1701d-116">Return value</span></span>

<span data-ttu-id="1701d-117">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="1701d-117">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1701d-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1701d-118">Requirements</span></span>



| <span data-ttu-id="1701d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1701d-119">Requirement</span></span> | <span data-ttu-id="1701d-120">Valore</span><span class="sxs-lookup"><span data-stu-id="1701d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1701d-121">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1701d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1701d-122">Windows 8</span><span class="sxs-lookup"><span data-stu-id="1701d-122">Windows 8</span></span><br/>                                                                           |
| <span data-ttu-id="1701d-123">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1701d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1701d-124">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="1701d-124">Windows Server 2012</span></span><br/>                                                                 |
| <span data-ttu-id="1701d-125">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="1701d-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="1701d-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1701d-126"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1701d-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1701d-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1701d-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1701d-128"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="1701d-129">IID</span><span class="sxs-lookup"><span data-stu-id="1701d-129">IID</span></span><br/>                      | <span data-ttu-id="1701d-130">DIID \_ IRemoteDesktopClientEvents è definito come 079863B7-6D47-4105-8BFE-0CDCB360E67D</span><span class="sxs-lookup"><span data-stu-id="1701d-130">DIID\_IRemoteDesktopClientEvents is defined as 079863B7-6D47-4105-8BFE-0CDCB360E67D</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1701d-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1701d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1701d-132">**IRemoteDesktopClientEvents**</span><span class="sxs-lookup"><span data-stu-id="1701d-132">**IRemoteDesktopClientEvents**</span></span>](iremotedesktopclientevents.md)
</dt> </dl>

 

 





