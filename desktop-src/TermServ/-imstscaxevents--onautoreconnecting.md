---
title: Metodo IMsTscAxEvents OnAutoReconnecting
description: Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto). | Metodo IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnAutoReconnecting
- Metodo OnAutoReconnecting Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353486"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a><span data-ttu-id="2cdd3-107">Metodo IMsTscAxEvents:: OnAutoReconnecting</span><span class="sxs-lookup"><span data-stu-id="2cdd3-107">IMsTscAxEvents::OnAutoReconnecting method</span></span>

<span data-ttu-id="2cdd3-108">Chiamato quando un client è in fase di riconnessione automatica di una sessione con un server di host sessione Desktop remoto (host sessione Desktop remoto).</span><span class="sxs-lookup"><span data-stu-id="2cdd3-108">Called when a client is in the process of automatically reconnecting a session with a Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cdd3-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2cdd3-109">Syntax</span></span>


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a><span data-ttu-id="2cdd3-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="2cdd3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2cdd3-111">*disconnectReason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cdd3-111">*disconnectReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdd3-112">Codice che descrive il motivo dell'ultima disconnessione della sessione.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-112">Code describing the reason for the last session disconnection.</span></span>

</dd> <dt>

<span data-ttu-id="2cdd3-113">*attemptCount* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2cdd3-113">*attemptCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdd3-114">Numero di tentativi effettuati nel processo di riconnessione automatica corrente.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-114">Number of attempts that have been made in the current automatic reconnection process.</span></span> <span data-ttu-id="2cdd3-115">Questo conteggio viene incrementato di uno per ogni tentativo eseguito.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-115">This count increases by one for each attempt made.</span></span>

</dd> <dt>

<span data-ttu-id="2cdd3-116">*pArcContinueStatus* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2cdd3-116">*pArcContinueStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2cdd3-117">Puntatore a un codice restituito che specifica lo stato del processo di riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-117">Pointer to a returned code specifying the state of the automatic reconnection process.</span></span> <span data-ttu-id="2cdd3-118">Questo codice può essere reimpostato per modificare lo stato del processo di riconnessione automatica corrente.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-118">This code can be reset to change the state of the current automatic reconnection process.</span></span>

<span data-ttu-id="2cdd3-119">Per ulteriori informazioni sulla reimpostazione del codice, fare riferimento alla sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-119">For more information about resetting this code, refer to the Remarks section.</span></span>

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span data-ttu-id="2cdd3-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic \* \* \* \* (0)</span><span class="sxs-lookup"><span data-stu-id="2cdd3-120"><span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>\*\*\*\*autoReconnectContinueAutomatic\*\*\*\* (0)</span></span>


</dt> <dd>

<span data-ttu-id="2cdd3-121">Il processo di riconnessione si verifica automaticamente.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-121">The reconnection process is occurring automatically.</span></span> <span data-ttu-id="2cdd3-122">Si tratta del valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-122">This is the default value.</span></span>

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span data-ttu-id="2cdd3-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop \* \* \* \* (1)</span><span class="sxs-lookup"><span data-stu-id="2cdd3-123"><span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>\*\*\*\*autoReconnectContinueStop\*\*\*\* (1)</span></span>


</dt> <dd>

<span data-ttu-id="2cdd3-124">Il processo di riconnessione è stato arrestato.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-124">The reconnection process has been stopped.</span></span>

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span data-ttu-id="2cdd3-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual \* \* \* \* (2)</span><span class="sxs-lookup"><span data-stu-id="2cdd3-125"><span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>\*\*\*\*autoReconnectContinueManual\*\*\*\* (2)</span></span>


</dt> <dd>

<span data-ttu-id="2cdd3-126">Il processo di riconnessione è in corso manualmente.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-126">The reconnection process is occurring manually.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2cdd3-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2cdd3-127">Return value</span></span>

<span data-ttu-id="2cdd3-128">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-128">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cdd3-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="2cdd3-129">Remarks</span></span>

<span data-ttu-id="2cdd3-130">Implementare questo metodo nel sink di evento per ricevere una notifica che indica che il controllo sta ristabiliscendo una connessione con un server Host sessione Desktop remoto.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-130">Implement this method in your event sink to receive notification that the control is reestablishing a connection with an RD Session Host server.</span></span>

<span data-ttu-id="2cdd3-131">Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueAutomatic**, questo metodo funziona in modalità puramente consultivo.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-131">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueAutomatic**, this method functions in a purely advisory mode.</span></span> <span data-ttu-id="2cdd3-132">I contenitori possono restare in ascolto di questo evento per le notifiche che il processo di riconnessione automatica sta procedendo.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-132">Containers can listen to this event for notifications that the automatic reconnection process is proceeding.</span></span> <span data-ttu-id="2cdd3-133">Il controllo tenterà automaticamente di ristabilire una connessione in base ai propri tempi interni e ai conteggi dei tentativi.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-133">The control will automatically keep trying to re-establish a connection based on its own internal timing and attempt counts.</span></span> <span data-ttu-id="2cdd3-134">Questo metodo viene chiamato durante ogni tentativo di riconnessione automatica per notificare il contenitore.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-134">This method is called during each automatic reconnection attempt in order to notify the container.</span></span>

<span data-ttu-id="2cdd3-135">Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueStop**, il tentativo di riconnessione automatica corrente verrà interrotto, una notifica di disconnessione verrà inviata al contenitore e non verranno rilasciate altre notifiche automatiche di riconnessione.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-135">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueStop**, the current automatic reconnection attempt will be terminated, a disconnect notification will be sent to the container, and no further automatic reconnect notifications will be issued.</span></span>

> [!Note]  
> <span data-ttu-id="2cdd3-136">Usare la proprietà [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) per abilitare o disabilitare la riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-136">Use the [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) property to enable or disable automatic reconnection.</span></span>

 

<span data-ttu-id="2cdd3-137">Quando lo stato del processo di riconnessione automatica viene modificato impostando il valore del parametro *pArcContinueStatus* su **autoReconnectContinueManual**, il contenitore controllerà manualmente il processo di riconnessione automatica chiamando [**Connect**](imstscax-connect.md) per attivare un tentativo di connessione o [**disconnettersi**](imstscax-disconnect.md) per annullare il processo di riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-137">When the state of the automatic reconnection process is changed by setting the value of the *pArcContinueStatus* parameter to **autoReconnectContinueManual**, the container will manually control the automatic reconnection process by calling [**Connect**](imstscax-connect.md) to trigger a connection attempt or [**Disconnect**](imstscax-disconnect.md) to cancel the automatic reconnection process.</span></span> <span data-ttu-id="2cdd3-138">Una volta impostato su questo valore, il controllo smette di eseguire tentativi di riconnessione automatici e diventa il criterio del contenitore per effettuare **chiamate di connessione per** attivare i tentativi di riconnessione automatici.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-138">Once set to this value, the control will stop making automatic reconnection attempts and it becomes the policy of the container to make **Connect** calls to trigger automatic reconnection attempts.</span></span> <span data-ttu-id="2cdd3-139">Questa operazione viene eseguita quando il contenitore fornisce un comportamento personalizzato dell'interfaccia utente per la riconnessione automatica, ad esempio il riavvio di una connessione RAS o VPN eliminata prima del processo di riconnessione automatica.</span><span class="sxs-lookup"><span data-stu-id="2cdd3-139">This is done when the container provides customized UI behavior for automatic reconnection, such as restarting a dropped RAS or VPN connection before the automatic reconnection process.</span></span>

<span data-ttu-id="2cdd3-140">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="2cdd3-140">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2cdd3-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2cdd3-141">Requirements</span></span>



| <span data-ttu-id="2cdd3-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="2cdd3-142">Requirement</span></span> | <span data-ttu-id="2cdd3-143">Valore</span><span class="sxs-lookup"><span data-stu-id="2cdd3-143">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdd3-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cdd3-144">Minimum supported client</span></span><br/> | <span data-ttu-id="2cdd3-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2cdd3-145">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="2cdd3-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2cdd3-146">Minimum supported server</span></span><br/> | <span data-ttu-id="2cdd3-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2cdd3-147">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="2cdd3-148">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="2cdd3-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="2cdd3-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cdd3-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="2cdd3-150">DLL</span><span class="sxs-lookup"><span data-stu-id="2cdd3-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2cdd3-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2cdd3-151"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cdd3-152">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2cdd3-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cdd3-153">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="2cdd3-153">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





