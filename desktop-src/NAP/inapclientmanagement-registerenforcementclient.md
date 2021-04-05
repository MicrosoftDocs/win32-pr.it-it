---
title: Metodo INapClientManagement RegisterEnforcementClient (NapManagement. h)
description: Registra un client di imposizione con il sistema NAP.
ms.assetid: 26ea45ea-a366-4162-91dc-06bcd0261c56
keywords:
- NAP metodo RegisterEnforcementClient
- Metodo RegisterEnforcementClient NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo RegisterEnforcementClient
topic_type:
- apiref
api_name:
- INapClientManagement.RegisterEnforcementClient
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc8ed4b5fe5a97d60b764341f21f25628c3c3434
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120447"
---
# <a name="inapclientmanagementregisterenforcementclient-method"></a><span data-ttu-id="e8464-106">Metodo INapClientManagement:: RegisterEnforcementClient</span><span class="sxs-lookup"><span data-stu-id="e8464-106">INapClientManagement::RegisterEnforcementClient method</span></span>

> [!Note]  
> <span data-ttu-id="e8464-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="e8464-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e8464-108">Il metodo **RegisterEnforcementClient** registra un client di imposizione con il sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="e8464-108">The **RegisterEnforcementClient** method registers an enforcement client with the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8464-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e8464-109">Syntax</span></span>


```C++
HRESULT RegisterEnforcementClient(
  [in] const NapComponentRegistrationInfo *enforcer
);
```



## <a name="parameters"></a><span data-ttu-id="e8464-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="e8464-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8464-111">*applicazione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e8464-111">*enforcer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8464-112">Puntatore a una struttura di dati [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che contiene le informazioni di registrazione associate al client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="e8464-112">A pointer to a [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) data structure that contains the registration information that is associated with the enforcement client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8464-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e8464-113">Return value</span></span>

<span data-ttu-id="e8464-114">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="e8464-114">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="e8464-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e8464-115">Return code</span></span>                                                                                            | <span data-ttu-id="e8464-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8464-116">Description</span></span>                                                                       |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e8464-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-117"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="e8464-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="e8464-118">Operation successful.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="e8464-119"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-119"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>         | <span data-ttu-id="e8464-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="e8464-120">Permissions error, access denied.</span></span><br/>                                      |
| <dl> <span data-ttu-id="e8464-121"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="e8464-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e8464-122">System resource limit, could not perform the operation.</span></span><br/>                |
| <dl> <span data-ttu-id="e8464-123"><dt>**protezione accesso alla rete \_ E \_ ID in conflitto \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-123"><dt>**NAP\_E\_CONFLICTING\_ID**</dt></span></span> </dl> | <span data-ttu-id="e8464-124">Un agente di imposizione che usa l'identificatore specificato è già registrato.</span><span class="sxs-lookup"><span data-stu-id="e8464-124">An enforcement agent using the given identifier is already registered.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="e8464-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e8464-125">Requirements</span></span>



| <span data-ttu-id="e8464-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8464-126">Requirement</span></span> | <span data-ttu-id="e8464-127">Valore</span><span class="sxs-lookup"><span data-stu-id="e8464-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8464-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8464-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e8464-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e8464-129">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e8464-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e8464-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e8464-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e8464-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="e8464-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e8464-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8464-133"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-133"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="e8464-134">IDL</span><span class="sxs-lookup"><span data-stu-id="e8464-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8464-135"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-135"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="e8464-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e8464-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8464-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8464-137"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="e8464-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e8464-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8464-139">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="e8464-139">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





