---
title: Metodo seflags INapEnforcementClientConnection (NapEnforcementClient. h)
description: Viene usato per distinguere le risposte per la prima volta da risposte dovute a SoHRequests memorizzate nella cache dalle forze di esecuzione. | Metodo seflags INapEnforcementClientConnection (NapEnforcementClient. h)
ms.assetid: 2f35bcdf-662c-431f-a39e-a7c758f35603
keywords:
- Metodo seflags NAP
- Metodo seflags NAP, interfaccia INapEnforcementClientConnection
- Interfaccia NAP di INapEnforcementClientConnection, metodo seflags
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetFlags
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7489997fb97f0e97c5a72d23646af8ae92272628
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321650"
---
# <a name="inapenforcementclientconnectionsetflags-method"></a><span data-ttu-id="25adf-107">Metodo INapEnforcementClientConnection:: seflags</span><span class="sxs-lookup"><span data-stu-id="25adf-107">INapEnforcementClientConnection::SetFlags method</span></span>

> [!Note]  
> <span data-ttu-id="25adf-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="25adf-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="25adf-109">Il metodo **INapEnforcementClientConnection:: Seflags** viene usato per distinguere le risposte per la prima volta da risposte dovute alla memorizzazione nella cache di SoHRequests da parte degli Enforcer.</span><span class="sxs-lookup"><span data-stu-id="25adf-109">The **INapEnforcementClientConnection::SetFlags** method is used to differentiate first-time responses from responses due to SoHRequests cached by the enforcers.</span></span>

## <a name="syntax"></a><span data-ttu-id="25adf-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="25adf-110">Syntax</span></span>


```C++
HRESULT SetFlags(
  [in] UINT8 flags
);
```



## <a name="parameters"></a><span data-ttu-id="25adf-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="25adf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25adf-112">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25adf-112">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25adf-113">Flag che determinano se il [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) è dovuto a un **SoHRequest** memorizzato nella cache.</span><span class="sxs-lookup"><span data-stu-id="25adf-113">Flags that determines if the [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) is due to a cached **SoHRequest**.</span></span> <span data-ttu-id="25adf-114">Se *Flags* ha un valore [**freshSoHRequest**](nap-type-constants.md), si tratta di una nuova richiesta; in caso contrario, è una richiesta memorizzata nella cache.</span><span class="sxs-lookup"><span data-stu-id="25adf-114">If *flags* has a value of [**freshSoHRequest**](nap-type-constants.md), it is a new request; otherwise it is a cached request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25adf-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="25adf-115">Return value</span></span>

<span data-ttu-id="25adf-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="25adf-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="25adf-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="25adf-117">Return code</span></span>                                                                                     | <span data-ttu-id="25adf-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="25adf-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="25adf-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="25adf-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="25adf-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="25adf-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="25adf-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="25adf-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="25adf-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="25adf-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="25adf-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25adf-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="25adf-125">Remarks</span></span>

<span data-ttu-id="25adf-126">Questo valore viene impostato da NapAgent.</span><span class="sxs-lookup"><span data-stu-id="25adf-126">This value is set by the NapAgent.</span></span>

## <a name="requirements"></a><span data-ttu-id="25adf-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="25adf-127">Requirements</span></span>



| <span data-ttu-id="25adf-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="25adf-128">Requirement</span></span> | <span data-ttu-id="25adf-129">Valore</span><span class="sxs-lookup"><span data-stu-id="25adf-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25adf-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25adf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="25adf-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="25adf-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="25adf-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="25adf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="25adf-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="25adf-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="25adf-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="25adf-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="25adf-135"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-135"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="25adf-136">IDL</span><span class="sxs-lookup"><span data-stu-id="25adf-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25adf-137"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-137"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="25adf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="25adf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25adf-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25adf-139"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="25adf-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="25adf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25adf-141">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="25adf-141">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





