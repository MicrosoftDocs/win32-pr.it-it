---
title: Metodo IMsTscAxEvents OnAutoReconnecting2
description: Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto). | Metodo IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting2
- Metodo OnAutoReconnecting2 Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321769"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a><span data-ttu-id="aee63-107">Metodo IMsTscAxEvents:: OnAutoReconnecting2</span><span class="sxs-lookup"><span data-stu-id="aee63-107">IMsTscAxEvents::OnAutoReconnecting2 method</span></span>

<span data-ttu-id="aee63-108">Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="aee63-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="aee63-109">Si tratta di una versione migliorata del metodo [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .</span><span class="sxs-lookup"><span data-stu-id="aee63-109">This is an enhanced version of the [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee63-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aee63-110">Syntax</span></span>


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a><span data-ttu-id="aee63-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="aee63-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee63-112">*disconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee63-112">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee63-113">Codice che descrive il motivo dell'ultima disconnessione della sessione.</span><span class="sxs-lookup"><span data-stu-id="aee63-113">Code that describes the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="aee63-114">*NetworkAvailable* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee63-114">*networkAvailable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee63-115">Specifica se la rete è disponibile.</span><span class="sxs-lookup"><span data-stu-id="aee63-115">Specifies if the network is available.</span></span>

</dd> <dt>

<span data-ttu-id="aee63-116">*attemptCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee63-116">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee63-117">Numero di tentativi effettuati nel processo di riconnessione automatica corrente.</span><span class="sxs-lookup"><span data-stu-id="aee63-117">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="aee63-118">Questo conteggio viene incrementato di uno per ogni tentativo eseguito.</span><span class="sxs-lookup"><span data-stu-id="aee63-118">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="aee63-119">*maxAttemptCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee63-119">*maxAttemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee63-120">Numero massimo di tentativi che verranno eseguiti nel processo di riconnessione automatica corrente.</span><span class="sxs-lookup"><span data-stu-id="aee63-120">The maximum number of attempts that will be made in the current automatic reconnection process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee63-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aee63-121">Return value</span></span>

<span data-ttu-id="aee63-122">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="aee63-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="aee63-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee63-123">Requirements</span></span>



| <span data-ttu-id="aee63-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee63-124">Requirement</span></span> | <span data-ttu-id="aee63-125">Valore</span><span class="sxs-lookup"><span data-stu-id="aee63-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="aee63-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee63-126">Minimum supported client</span></span><br/> | <span data-ttu-id="aee63-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="aee63-127">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="aee63-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aee63-128">Minimum supported server</span></span><br/> | <span data-ttu-id="aee63-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="aee63-129">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="aee63-130">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="aee63-130">Type library</span></span><br/>             | <dl> <span data-ttu-id="aee63-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee63-131"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="aee63-132">DLL</span><span class="sxs-lookup"><span data-stu-id="aee63-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aee63-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aee63-133"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee63-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aee63-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee63-135">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="aee63-135">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





