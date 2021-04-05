---
title: Metodo INapEnforcementClientConnection SetSoHRequest (NapEnforcementClient. h)
description: Imposta la richiesta di rapporto di integrità.
ms.assetid: 87dbb982-a337-4644-a2fe-970bfdd6c140
keywords:
- NAP metodo SetSoHRequest
- Metodo SetSoHRequest NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetSoHRequest
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetSoHRequest
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92559d532e99bfa29d7f62fd29b279db20f2c0a3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740911"
---
# <a name="inapenforcementclientconnectionsetsohrequest-method"></a><span data-ttu-id="41377-106">Metodo INapEnforcementClientConnection:: SetSoHRequest</span><span class="sxs-lookup"><span data-stu-id="41377-106">INapEnforcementClientConnection::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="41377-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="41377-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="41377-108">Il metodo **INapEnforcementClientConnection:: SetSoHRequest** imposta la richiesta di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="41377-108">The **INapEnforcementClientConnection::SetSoHRequest** method sets the SoH-Request.</span></span>

## <a name="syntax"></a><span data-ttu-id="41377-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="41377-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in, unique] const NetworkSoHRequest *sohRequest
);
```



## <a name="parameters"></a><span data-ttu-id="41377-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="41377-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41377-111">*sohRequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="41377-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="41377-112">Puntatore a una struttura [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) univoca, ovvero un BLOB di dati opachi per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="41377-112">A pointer to a unique [**NetworkSoHRequest**](/windows/win32/api/naptypes/ns-naptypes-networksoh) structure, which is an opaque data blob to the enforcer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41377-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="41377-113">Return value</span></span>

<span data-ttu-id="41377-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="41377-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="41377-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="41377-115">Return code</span></span>                                                                                     | <span data-ttu-id="41377-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="41377-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="41377-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41377-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="41377-118">Il pacchetto del rapporto di integrità è valido.</span><span class="sxs-lookup"><span data-stu-id="41377-118">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="41377-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="41377-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="41377-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="41377-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="41377-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="41377-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="41377-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="41377-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="41377-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="41377-123">Remarks</span></span>

<span data-ttu-id="41377-124">Questa impostazione è impostata da NapAgent ed è sottoposta a query da Enforcer da inviare in transito.</span><span class="sxs-lookup"><span data-stu-id="41377-124">This is set by the NapAgent and queried by enforcers to send on the wire.</span></span>

<span data-ttu-id="41377-125">Il pacchetto di rapporto di integrità con lunghezza zero byte non è valido.</span><span class="sxs-lookup"><span data-stu-id="41377-125">A zero byte length SoH packet is invalid.</span></span>

## <a name="requirements"></a><span data-ttu-id="41377-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="41377-126">Requirements</span></span>



| <span data-ttu-id="41377-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="41377-127">Requirement</span></span> | <span data-ttu-id="41377-128">Valore</span><span class="sxs-lookup"><span data-stu-id="41377-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41377-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41377-129">Minimum supported client</span></span><br/> | <span data-ttu-id="41377-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="41377-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41377-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="41377-131">Minimum supported server</span></span><br/> | <span data-ttu-id="41377-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="41377-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41377-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="41377-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="41377-134"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="41377-134"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="41377-135">IDL</span><span class="sxs-lookup"><span data-stu-id="41377-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41377-136"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41377-136"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="41377-137">DLL</span><span class="sxs-lookup"><span data-stu-id="41377-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41377-138"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41377-138"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="41377-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="41377-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41377-140">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="41377-140">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





