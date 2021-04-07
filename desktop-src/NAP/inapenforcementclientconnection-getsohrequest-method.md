---
title: Metodo INapEnforcementClientConnection GetSoHRequest (NapEnforcementClient. h)
description: Ottiene la richiesta di rapporto di integrità corrente.
ms.assetid: 21397a0d-ef18-494e-9c5a-43d7f6216a67
keywords:
- NAP metodo GetSoHRequest
- Metodo GetSoHRequest NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6115e607f810aef67911ec7d7800d35207368e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964008"
---
# <a name="inapenforcementclientconnectiongetsohrequest-method"></a><span data-ttu-id="54e38-106">Metodo INapEnforcementClientConnection:: GetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="54e38-106">INapEnforcementClientConnection::GetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="54e38-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="54e38-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="54e38-108">Il metodo **INapEnforcementClientConnection:: GetSoHRequest** ottiene la richiesta di rapporto di integrità corrente.</span><span class="sxs-lookup"><span data-stu-id="54e38-108">The **INapEnforcementClientConnection::GetSoHRequest** method gets the current SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="54e38-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="54e38-109">Syntax</span></span>


```C++
HRESULT GetSoHRequest(
  [out] NetworkSoHRequest **sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="54e38-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="54e38-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54e38-111">*sohRequest* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="54e38-111">*sohRequest* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54e38-112">Puntatore a un puntatore a una struttura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) , che rappresenta un BLOB di dati opachi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="54e38-112">A pointer to a pointer to a [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54e38-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="54e38-113">Return value</span></span>

<span data-ttu-id="54e38-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="54e38-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="54e38-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="54e38-115">Return code</span></span>                                                                                     | <span data-ttu-id="54e38-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54e38-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="54e38-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="54e38-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="54e38-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="54e38-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="54e38-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="54e38-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="54e38-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="54e38-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="54e38-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="54e38-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="54e38-123">Remarks</span></span>

<span data-ttu-id="54e38-124">Questa impostazione è impostata da NapAgent ed è sottoposta a query da Enforcer da inviare in transito.</span><span class="sxs-lookup"><span data-stu-id="54e38-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="54e38-125">Il pacchetto di rapporto di integrità con lunghezza zero byte non è valido.</span><span class="sxs-lookup"><span data-stu-id="54e38-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="54e38-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="54e38-126">Requirements</span></span>



| <span data-ttu-id="54e38-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="54e38-127">Requirement</span></span> | <span data-ttu-id="54e38-128">Valore</span><span class="sxs-lookup"><span data-stu-id="54e38-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54e38-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e38-129">Minimum supported client</span></span><br/> | <span data-ttu-id="54e38-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="54e38-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54e38-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="54e38-131">Minimum supported server</span></span><br/> | <span data-ttu-id="54e38-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="54e38-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="54e38-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="54e38-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="54e38-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="54e38-135">IDL</span><span class="sxs-lookup"><span data-stu-id="54e38-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54e38-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="54e38-137">DLL</span><span class="sxs-lookup"><span data-stu-id="54e38-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54e38-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54e38-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="54e38-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="54e38-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54e38-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="54e38-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





