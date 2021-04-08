---
title: Metodo IMsTscAxEvents OnFatalError
description: Chiamato quando il controllo client rileva un errore irreversibile.
ms.assetid: 13a5eb2e-d847-4561-b30b-3f23a0579b4d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo OnFatalError
- Metodo OnFatalError Servizi Desktop remoto, interfaccia IMsTscAxEvents
- Interfaccia IMsTscAxEvents Servizi Desktop remoto, metodo OnFatalError
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnFatalError
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73402ac178bcb2ac3dc03c0adda092d3b49f6ba3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103874077"
---
# <a name="imstscaxeventsonfatalerror-method"></a><span data-ttu-id="68a55-106">Metodo IMsTscAxEvents:: OnFatalError</span><span class="sxs-lookup"><span data-stu-id="68a55-106">IMsTscAxEvents::OnFatalError method</span></span>

<span data-ttu-id="68a55-107">Chiamato quando il controllo client rileva un errore irreversibile.</span><span class="sxs-lookup"><span data-stu-id="68a55-107">Called when the client control encounters a fatal error.</span></span>

## <a name="syntax"></a><span data-ttu-id="68a55-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68a55-108">Syntax</span></span>


```C++
void OnFatalError(
  [in] long errorCode
);
```



## <a name="parameters"></a><span data-ttu-id="68a55-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="68a55-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68a55-110">Codice errore  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68a55-110">*errorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68a55-111">Indica il codice di errore.</span><span class="sxs-lookup"><span data-stu-id="68a55-111">Indicates the error code.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="68a55-112"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="68a55-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-113">Si è verificato un errore sconosciuto.</span><span class="sxs-lookup"><span data-stu-id="68a55-113">An unknown error has occurred.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="68a55-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="68a55-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-115">Codice di errore interno 1.</span><span class="sxs-lookup"><span data-stu-id="68a55-115">Internal error code 1.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="68a55-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="68a55-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-117">Si è verificato un errore di memoria insufficiente.</span><span class="sxs-lookup"><span data-stu-id="68a55-117">An out-of-memory error has occurred.</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="68a55-118"><span id="3"></span>**3**</span><span class="sxs-lookup"><span data-stu-id="68a55-118"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-119">Si è verificato un errore di creazione della finestra.</span><span class="sxs-lookup"><span data-stu-id="68a55-119">A window-creation error has occurred.</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="68a55-120"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="68a55-120"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-121">Codice di errore interno 2.</span><span class="sxs-lookup"><span data-stu-id="68a55-121">Internal error code 2.</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="68a55-122"><span id="5"></span>**5**</span><span class="sxs-lookup"><span data-stu-id="68a55-122"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-123">Codice di errore interno 3.</span><span class="sxs-lookup"><span data-stu-id="68a55-123">Internal error code 3.</span></span> <span data-ttu-id="68a55-124">Lo stato non è valido.</span><span class="sxs-lookup"><span data-stu-id="68a55-124">This is not a valid state.</span></span>

</dd> <dt>

<span id="6"></span>

<span data-ttu-id="68a55-125"><span id="6"></span>**6**</span><span class="sxs-lookup"><span data-stu-id="68a55-125"><span id="6"></span>**6**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-126">Codice di errore interno 4.</span><span class="sxs-lookup"><span data-stu-id="68a55-126">Internal error code 4.</span></span>

</dd> <dt>

<span id="7"></span>

<span data-ttu-id="68a55-127"><span id="7"></span>**7**</span><span class="sxs-lookup"><span data-stu-id="68a55-127"><span id="7"></span>**7**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-128">Si è verificato un errore irreversibile durante la connessione client.</span><span class="sxs-lookup"><span data-stu-id="68a55-128">An unrecoverable error has occurred during client connection.</span></span>

</dd> <dt>

<span id="100"></span>

<span data-ttu-id="68a55-129"><span id="100"></span>**100**</span><span class="sxs-lookup"><span data-stu-id="68a55-129"><span id="100"></span>**100**</span></span>


</dt> <dd>

<span data-ttu-id="68a55-130">Errore di inizializzazione Winsock.</span><span class="sxs-lookup"><span data-stu-id="68a55-130">Winsock initialization error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68a55-131">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68a55-131">Return value</span></span>

<span data-ttu-id="68a55-132">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="68a55-132">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="68a55-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="68a55-133">Remarks</span></span>

<span data-ttu-id="68a55-134">In risposta a questo evento, il contenitore Visualizza un messaggio di errore e si arresta.</span><span class="sxs-lookup"><span data-stu-id="68a55-134">In response to this event, the container displays an error message and shuts down.</span></span>

<span data-ttu-id="68a55-135">Per ulteriori informazioni su Connessione Web Desktop remoto, vedere [requisiti per connessione Web Desktop remoto](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="68a55-135">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="68a55-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68a55-136">Requirements</span></span>



| <span data-ttu-id="68a55-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="68a55-137">Requirement</span></span> | <span data-ttu-id="68a55-138">Valore</span><span class="sxs-lookup"><span data-stu-id="68a55-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68a55-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68a55-139">Minimum supported client</span></span><br/> | <span data-ttu-id="68a55-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68a55-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68a55-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68a55-141">Minimum supported server</span></span><br/> | <span data-ttu-id="68a55-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68a55-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68a55-143">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="68a55-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="68a55-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a55-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68a55-145">DLL</span><span class="sxs-lookup"><span data-stu-id="68a55-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68a55-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68a55-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68a55-147">IID</span><span class="sxs-lookup"><span data-stu-id="68a55-147">IID</span></span><br/>                      | <span data-ttu-id="68a55-148">IMsTscAxEvents è definito come 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="68a55-148">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="68a55-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68a55-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68a55-150">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="68a55-150">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





