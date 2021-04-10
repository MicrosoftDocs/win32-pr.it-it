---
title: Metodo INapClientManagement GetRegisteredSystemHealthAgents (NapManagement. h)
description: Recupera le informazioni sul SHAs registrato.
ms.assetid: c38d2d23-62d4-49f0-81a3-52394866f0c4
keywords:
- NAP metodo GetRegisteredSystemHealthAgents
- Metodo GetRegisteredSystemHealthAgents NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetRegisteredSystemHealthAgents
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredSystemHealthAgents
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4852e2d4c1ffa08b1a7ea7b3d8395c1b116cca6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964522"
---
# <a name="inapclientmanagementgetregisteredsystemhealthagents-method"></a><span data-ttu-id="269db-106">Metodo INapClientManagement:: GetRegisteredSystemHealthAgents</span><span class="sxs-lookup"><span data-stu-id="269db-106">INapClientManagement::GetRegisteredSystemHealthAgents method</span></span>

> [!Note]  
> <span data-ttu-id="269db-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="269db-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="269db-108">Il metodo **GetRegisteredSystemHealthAgents** recupera le informazioni relative al Shas registrato.</span><span class="sxs-lookup"><span data-stu-id="269db-108">The **GetRegisteredSystemHealthAgents** method retrieves information about the registered SHAs.</span></span>

## <a name="syntax"></a><span data-ttu-id="269db-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="269db-109">Syntax</span></span>


```C++
HRESULT GetRegisteredSystemHealthAgents(
  [out] SystemHealthEntityCount      *count,
  [out] NapComponentRegistrationInfo **agents
) const;
```



## <a name="parameters"></a><span data-ttu-id="269db-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="269db-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="269db-111">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="269db-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="269db-112">Puntatore a un [**SystemHealthEntityCount**](nap-datatypes.md) che descrive il numero di Shas registrati.</span><span class="sxs-lookup"><span data-stu-id="269db-112">A pointer to a [**SystemHealthEntityCount**](nap-datatypes.md) that describes the number of registered SHAs.</span></span>

</dd> <dt>

<span data-ttu-id="269db-113">*agenti* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="269db-113">*agents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="269db-114">Puntatore a una matrice di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono il Shas registrato.</span><span class="sxs-lookup"><span data-stu-id="269db-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered SHAs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="269db-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="269db-115">Return value</span></span>

<span data-ttu-id="269db-116">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="269db-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="269db-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="269db-117">Return code</span></span>                                                                                         | <span data-ttu-id="269db-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="269db-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="269db-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="269db-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="269db-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="269db-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="269db-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="269db-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="269db-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="269db-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="269db-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="269db-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="269db-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="269db-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="269db-125"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="269db-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="269db-126">NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="269db-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="269db-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="269db-127">Requirements</span></span>



| <span data-ttu-id="269db-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="269db-128">Requirement</span></span> | <span data-ttu-id="269db-129">Valore</span><span class="sxs-lookup"><span data-stu-id="269db-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="269db-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="269db-130">Minimum supported client</span></span><br/> | <span data-ttu-id="269db-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="269db-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="269db-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="269db-132">Minimum supported server</span></span><br/> | <span data-ttu-id="269db-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="269db-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="269db-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="269db-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="269db-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="269db-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="269db-136">IDL</span><span class="sxs-lookup"><span data-stu-id="269db-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="269db-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="269db-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="269db-138">DLL</span><span class="sxs-lookup"><span data-stu-id="269db-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="269db-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="269db-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="269db-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="269db-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="269db-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="269db-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





