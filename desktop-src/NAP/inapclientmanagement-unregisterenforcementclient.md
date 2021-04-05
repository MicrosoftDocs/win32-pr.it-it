---
title: Metodo INapClientManagement UnregisterEnforcementClient (NapManagement. h)
description: Annulla la registrazione di un client di imposizione con il sistema NAP.
ms.assetid: 549683de-7f2c-4da6-9616-862e0e99d21f
keywords:
- NAP metodo UnregisterEnforcementClient
- Metodo UnregisterEnforcementClient NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo UnregisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.UnregisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea318cf632ac00d54451b11428907c88159809df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120446"
---
# <a name="inapclientmanagementunregisterenforcementclient-method"></a><span data-ttu-id="08b00-106">Metodo INapClientManagement:: UnregisterEnforcementClient</span><span class="sxs-lookup"><span data-stu-id="08b00-106">INapClientManagement::UnregisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="08b00-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="08b00-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="08b00-108">Il metodo **UnregisterEnforcementClient** Annulla la registrazione di un client di imposizione con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="08b00-108">The **UnregisterEnforcementClient** method unregisters an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="08b00-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="08b00-109">Syntax</span></span>


```C++
HRESULT UnregisterEnforcementClient(
  [in] EnforcementEntityId id
);
```



## <a name="parameters"></a><span data-ttu-id="08b00-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="08b00-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b00-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08b00-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08b00-112">Valore [**EnforcementEntityId**](nap-datatypes.md) che identifica il client di imposizione di cui annullare la registrazione.</span><span class="sxs-lookup"><span data-stu-id="08b00-112">An [**EnforcementEntityId**](nap-datatypes.md) value that identifies the enforcement client to unregister.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b00-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="08b00-113">Return value</span></span>

<span data-ttu-id="08b00-114">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="08b00-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="08b00-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="08b00-115">Return code</span></span>                                                                                         | <span data-ttu-id="08b00-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="08b00-116">Description</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="08b00-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-117"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="08b00-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="08b00-118">Operation successful.</span></span><br/>                                               |
| <dl> <span data-ttu-id="08b00-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="08b00-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="08b00-120">Permissions error, access denied.</span></span><br/>                                   |
| <dl> <span data-ttu-id="08b00-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="08b00-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="08b00-122">System resource limit, could not perform the operation.</span></span><br/>             |
| <dl> <span data-ttu-id="08b00-123"><dt>**NAP \_ E \_ ancora \_ associato**</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-123"><dt>**NAP\_E\_STILL\_BOUND**</dt></span></span> </dl> | <span data-ttu-id="08b00-124">Impossibile annullare la registrazione del client di imposizione e rimanere associato.</span><span class="sxs-lookup"><span data-stu-id="08b00-124">The enforcement client could not be unregistered and remains bound.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="08b00-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="08b00-125">Requirements</span></span>



| <span data-ttu-id="08b00-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b00-126">Requirement</span></span> | <span data-ttu-id="08b00-127">Valore</span><span class="sxs-lookup"><span data-stu-id="08b00-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="08b00-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08b00-128">Minimum supported client</span></span><br/> | <span data-ttu-id="08b00-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="08b00-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="08b00-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="08b00-130">Minimum supported server</span></span><br/> | <span data-ttu-id="08b00-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="08b00-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="08b00-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="08b00-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="08b00-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="08b00-134">IDL</span><span class="sxs-lookup"><span data-stu-id="08b00-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="08b00-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="08b00-136">DLL</span><span class="sxs-lookup"><span data-stu-id="08b00-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b00-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b00-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="08b00-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="08b00-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08b00-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="08b00-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





