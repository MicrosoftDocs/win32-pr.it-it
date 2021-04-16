---
title: Metodo INapClientManagement GetRegisteredEnforcementClients (NapManagement. h)
description: Recupera le informazioni sui client di imposizione registrati.
ms.assetid: aae7c57c-a7fe-4cb2-94f6-53e501e38054
keywords:
- NAP metodo GetRegisteredEnforcementClients
- Metodo GetRegisteredEnforcementClients NAP, interfaccia INapClientManagement
- Interfaccia INapClientManagement NAP, metodo GetRegisteredEnforcementClients
topic_type:
- apiref
api_name:
- INapClientManagement.GetRegisteredEnforcementClients
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7767f96c9b5410b3de9cfef3695193c0d5572b2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477819"
---
# <a name="inapclientmanagementgetregisteredenforcementclients-method"></a><span data-ttu-id="14d93-106">Metodo INapClientManagement:: GetRegisteredEnforcementClients</span><span class="sxs-lookup"><span data-stu-id="14d93-106">INapClientManagement::GetRegisteredEnforcementClients method</span></span>

> [!Note]  
> <span data-ttu-id="14d93-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="14d93-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="14d93-108">Il metodo **GetRegisteredEnforcementClients** recupera le informazioni sui client di imposizione registrati.</span><span class="sxs-lookup"><span data-stu-id="14d93-108">The **GetRegisteredEnforcementClients** method retrieves information about the registered enforcement clients.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d93-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="14d93-109">Syntax</span></span>


```C++
HRESULT GetRegisteredEnforcementClients(
  [out] EnforcementEntityCount       *count,
  [out] NapComponentRegistrationInfo **enforcers
) const;
```



## <a name="parameters"></a><span data-ttu-id="14d93-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="14d93-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14d93-111">*numero* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="14d93-111">*count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14d93-112">Puntatore a un [**EnforcementEntityCount**](nap-datatypes.md) contenente il numero di client di imposizione registrati.</span><span class="sxs-lookup"><span data-stu-id="14d93-112">A pointer to a [**EnforcementEntityCount**](nap-datatypes.md) that contains the number of registered enforcement clients.</span></span>

</dd> <dt>

<span data-ttu-id="14d93-113">*imposizione* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="14d93-113">*enforcers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14d93-114">Puntatore a una matrice di strutture [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) che descrivono i client di imposizione registrati.</span><span class="sxs-lookup"><span data-stu-id="14d93-114">A pointer to an array of [**NapComponentRegistrationInfo**](/windows/win32/api/naptypes/ns-naptypes-napcomponentregistrationinfo) structures that describe the registered enforcement clients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14d93-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="14d93-115">Return value</span></span>

<span data-ttu-id="14d93-116">Il metodo restituisce un codice di stato HRESULT incluso ma non limitato a uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="14d93-116">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="14d93-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="14d93-117">Return code</span></span>                                                                                         | <span data-ttu-id="14d93-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14d93-118">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="14d93-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-119"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="14d93-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="14d93-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="14d93-121"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-121"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="14d93-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="14d93-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="14d93-123"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-123"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="14d93-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="14d93-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="14d93-125"><dt>**RPC \_ E \_ disconnessa**</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-125"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="14d93-126">NapAgent non è in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="14d93-126">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="requirements"></a><span data-ttu-id="14d93-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="14d93-127">Requirements</span></span>



| <span data-ttu-id="14d93-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="14d93-128">Requirement</span></span> | <span data-ttu-id="14d93-129">Valore</span><span class="sxs-lookup"><span data-stu-id="14d93-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="14d93-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14d93-130">Minimum supported client</span></span><br/> | <span data-ttu-id="14d93-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="14d93-131">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="14d93-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="14d93-132">Minimum supported server</span></span><br/> | <span data-ttu-id="14d93-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="14d93-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="14d93-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="14d93-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="14d93-135"><dt>NapManagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-135"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="14d93-136">IDL</span><span class="sxs-lookup"><span data-stu-id="14d93-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14d93-137"><dt>NapManagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-137"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="14d93-138">DLL</span><span class="sxs-lookup"><span data-stu-id="14d93-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14d93-139"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14d93-139"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="14d93-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="14d93-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14d93-141">**INapClientManagement**</span><span class="sxs-lookup"><span data-stu-id="14d93-141">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





