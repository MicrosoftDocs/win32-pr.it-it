---
title: Metodo INapClientManagement UnregisterSystemHealthAgent (NapManagement. h)
description: Annulla la registrazione di un SHA con il sistema NAP.
ms.assetid: c3ad6f2a-c39a-4590-8487-24c802433845
keywords:
- NAP metodo UnregisterSystemHealthAgent
- Metodo UnregisterSystemHealthAgent NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo UnregisterSystemHealthAgent
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterSystemHealthAgent
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbff7af1c279090d12883d2a4e06ee9bcc364438
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302022"
---
# <a name="inapclientmanagementunregistersystemhealthagent-method"></a><span data-ttu-id="15616-106">Metodo INapClientManagement:: UnregisterSystemHealthAgent</span><span class="sxs-lookup"><span data-stu-id="15616-106">INapClientManagement::UnregisterSystemHealthAgent method</span></span>

> [!Note]  
> <span data-ttu-id="15616-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="15616-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="15616-108">Il metodo **UnregisterSystemHealthAgent** Annulla la registrazione di un Sha con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="15616-108">The **UnregisterSystemHealthAgent** method unregisters an SHA with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="15616-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15616-109">Syntax</span></span>


```C++
HRESULT UnregisterSystemHealthAgent(
  [in] SystemHealthEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="15616-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="15616-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15616-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15616-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15616-112">[**SystemHealthEntityId**](nap-datatypes.md) che identifica l'agente integrità sistema di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="15616-112">A [**SystemHealthEntityId**](nap-datatypes.md) that identifies the System Health Agent to be unregistered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15616-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15616-113">Return value</span></span>

<span data-ttu-id="15616-114">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="15616-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="15616-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="15616-115">Return code</span></span>                                                                                         | <span data-ttu-id="15616-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="15616-116">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="15616-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="15616-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="15616-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="15616-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="15616-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="15616-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="15616-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="15616-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="15616-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="15616-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="15616-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="15616-122">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="15616-123"><dt>**NAP \_ E \_ ancora \_ associato**</dt></span><span class="sxs-lookup"><span data-stu-id="15616-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="15616-124">SHA rimane associato e non è possibile annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="15616-124">The SHA remains bound and could not be unregistered.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="15616-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15616-125">Requirements</span></span>



| <span data-ttu-id="15616-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="15616-126">Requirement</span></span> | <span data-ttu-id="15616-127">Valore</span><span class="sxs-lookup"><span data-stu-id="15616-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="15616-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15616-128">Minimum supported client</span></span><br/> | <span data-ttu-id="15616-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="15616-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="15616-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="15616-130">Minimum supported server</span></span><br/> | <span data-ttu-id="15616-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="15616-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="15616-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15616-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="15616-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="15616-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="15616-134">IDL</span><span class="sxs-lookup"><span data-stu-id="15616-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="15616-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="15616-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="15616-136">DLL</span><span class="sxs-lookup"><span data-stu-id="15616-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15616-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15616-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="15616-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15616-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15616-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="15616-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





