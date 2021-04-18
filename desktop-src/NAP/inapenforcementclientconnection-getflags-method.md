---
title: Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
description: Viene usato per distinguere le risposte per la prima volta da risposte dovute a SoHRequests memorizzate nella cache dalle forze di esecuzione. | Metodo GetFlags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: e8399615-5190-46f7-a3bf-3070de548953
keywords:
- Metodo GetFlags NAP
- Metodo GetFlags NAP, interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, Metodo GetFlags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a35e183b5d4f606d21f4afce8cca68135732a35c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321310"
---
# <a name="inapenforcementclientconnectiongetflags-method"></a><span data-ttu-id="875e4-107">Metodo INapEnforcementClientConnection:: GetFlags</span><span class="sxs-lookup"><span data-stu-id="875e4-107">INapEnforcementClientConnection::GetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="875e4-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="875e4-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="875e4-109">Il metodo **INapEnforcementClientConnection:: GetFlags** viene usato per distinguere le risposte per la prima volta da risposte dovute alla memorizzazione nella cache di SoHRequests da parte degli Enforcer.</span><span class="sxs-lookup"><span data-stu-id="875e4-109">The **INapEnforcementClientConnection::GetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="875e4-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="875e4-110">Syntax</span></span>


```C++
HRESULT GetFlags(
  [out] UINT8 *flags
);
```



## <a name="parameters"></a><span data-ttu-id="875e4-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="875e4-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="875e4-112">*flag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="875e4-112">*flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="875e4-113">Puntatore a un flag che determina se [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) è dovuto a un **SoHRequest** memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="875e4-113">A pointer to a flag that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="875e4-114">Se *Flags* ha un valore [**freshSoHRequest**](nap-type-constants.md), si tratta di una nuova richiesta; in caso contrario, è una richiesta memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="875e4-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="875e4-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="875e4-115">Return value</span></span>

<span data-ttu-id="875e4-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="875e4-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="875e4-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="875e4-117">Return code</span></span>                                                                                     | <span data-ttu-id="875e4-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="875e4-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="875e4-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="875e4-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="875e4-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="875e4-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="875e4-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="875e4-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="875e4-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="875e4-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="875e4-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="875e4-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="875e4-125">Requirements</span></span>



| <span data-ttu-id="875e4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="875e4-126">Requirement</span></span> | <span data-ttu-id="875e4-127">Valore</span><span class="sxs-lookup"><span data-stu-id="875e4-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="875e4-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="875e4-128">Minimum supported client</span></span><br/> | <span data-ttu-id="875e4-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="875e4-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="875e4-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="875e4-130">Minimum supported server</span></span><br/> | <span data-ttu-id="875e4-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="875e4-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="875e4-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="875e4-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="875e4-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="875e4-134">IDL</span><span class="sxs-lookup"><span data-stu-id="875e4-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="875e4-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="875e4-136">DLL</span><span class="sxs-lookup"><span data-stu-id="875e4-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="875e4-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="875e4-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="875e4-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="875e4-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="875e4-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="875e4-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





