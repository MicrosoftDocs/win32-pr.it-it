---
title: Metodo INapEnforcementClientConnection GetSoHResponse (NapEnforcementClient. h)
description: Ottiene la SoH-Response ricevuta dal client di imposizione.
ms.assetid: fc0084a3-a668-435e-8390-f322941c5cd4
keywords:
- NAP metodo GetSoHResponse
- Metodo GetSoHResponse NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetSoHResponse
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetSoHResponse
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67be4d65135d6e4ce606a83eb08fdeed036cc62a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873557"
---
# <a name="inapenforcementclientconnectiongetsohresponse-method"></a><span data-ttu-id="3c975-106">Metodo INapEnforcementClientConnection:: GetSoHResponse</span><span class="sxs-lookup"><span data-stu-id="3c975-106">INapEnforcementClientConnection::GetSoHResponse method</span></span>

> [!Note]  
> <span data-ttu-id="3c975-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="3c975-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3c975-108">Il metodo **INapEnforcementClientConnection:: GetSoHResponse** ottiene la SoH-Response ricevuta dal client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="3c975-108">The **INapEnforcementClientConnection::GetSoHResponse** method gets the SoH-Response received by the enforcement client.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c975-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3c975-109">Syntax</span></span>


```C++
HRESULT GetSoHResponse(
  [out] NetworkSoHResponse **sohResponse
);
```



## <a name="parameters"></a><span data-ttu-id="3c975-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="3c975-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c975-111">*sohResponse* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3c975-111">*sohResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c975-112">Puntatore a un puntatore a una struttura [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opachi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3c975-112">A pointer to a pointer to a unique [**NetworkSoHResponse**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c975-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3c975-113">Return value</span></span>

<span data-ttu-id="3c975-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="3c975-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="3c975-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3c975-115">Return code</span></span>                                                                                     | <span data-ttu-id="3c975-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3c975-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="3c975-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="3c975-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="3c975-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="3c975-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="3c975-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="3c975-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="3c975-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="3c975-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="3c975-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3c975-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="3c975-123">Remarks</span></span>

<span data-ttu-id="3c975-124">Un pacchetto di dimensioni pari A zero byte è valido.</span><span class="sxs-lookup"><span data-stu-id="3c975-124">A zero-byte sized packet is valid.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c975-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3c975-125">Requirements</span></span>



| <span data-ttu-id="3c975-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="3c975-126">Requirement</span></span> | <span data-ttu-id="3c975-127">Valore</span><span class="sxs-lookup"><span data-stu-id="3c975-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c975-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c975-128">Minimum supported client</span></span><br/> | <span data-ttu-id="3c975-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c975-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="3c975-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3c975-130">Minimum supported server</span></span><br/> | <span data-ttu-id="3c975-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c975-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="3c975-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3c975-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c975-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="3c975-134">IDL</span><span class="sxs-lookup"><span data-stu-id="3c975-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3c975-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="3c975-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3c975-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c975-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c975-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="3c975-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3c975-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c975-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="3c975-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





