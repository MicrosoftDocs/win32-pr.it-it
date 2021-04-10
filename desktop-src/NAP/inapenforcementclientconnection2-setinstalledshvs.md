---
title: Metodo INapEnforcementClientConnection2 SetInstalledShvs (NapEnforcementClient. h)
description: Utilizzato dall'agente NAP per impostare i validator di integrità di sistema installati (SHV) nel client.
ms.assetid: 38aa99b9-a15a-414d-91fc-128de8f5a654
keywords:
- NAP metodo SetInstalledShvs
- Metodo SetInstalledShvs NAP, interfaccia INapEnforcementClientConnection2
- Interfaccia INapEnforcementClientConnection2 NAP, metodo SetInstalledShvs
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection2.SetInstalledShvs
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6651cd5248094f82d9faa1862492f82648e94125
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121659"
---
# <a name="inapenforcementclientconnection2setinstalledshvs-method"></a><span data-ttu-id="36d4b-106">Metodo INapEnforcementClientConnection2:: SetInstalledShvs</span><span class="sxs-lookup"><span data-stu-id="36d4b-106">INapEnforcementClientConnection2::SetInstalledShvs method</span></span>

> [!Note]  
> <span data-ttu-id="36d4b-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="36d4b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="36d4b-108">Il metodo **SetInstalledShvs** viene utilizzato dall'agente NAP per impostare i validator di integrità del sistema installati (SHV) nel client.</span><span class="sxs-lookup"><span data-stu-id="36d4b-108">The **SetInstalledShvs** method is used by the NAP Agent to set the installed System Health Validators (SHVs) on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="36d4b-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="36d4b-109">Syntax</span></span>


```C++
HRESULT SetInstalledShvs(
  [in] SystemHealthEntityCount count,
  [in] SystemHealthEntityId    *ids
);
```



## <a name="parameters"></a><span data-ttu-id="36d4b-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="36d4b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36d4b-111">*numero* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="36d4b-111">*count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d4b-112">Valore [SystemHealthEntityCount](nap-datatypes.md) che specifica il numero di SHV da installare negli *ID*.</span><span class="sxs-lookup"><span data-stu-id="36d4b-112">A [SystemHealthEntityCount](nap-datatypes.md) value that specifies the number of SHVs to install in *ids*.</span></span>

</dd> <dt>

<span data-ttu-id="36d4b-113">*ID* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="36d4b-113">*ids* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="36d4b-114">Puntatore a un valore [SystemHealthEntityId](nap-datatypes.md) che contiene un elenco di ID di convalida integrità sistema da installare.</span><span class="sxs-lookup"><span data-stu-id="36d4b-114">A pointer to a [SystemHealthEntityId](nap-datatypes.md) value that contains a list of SHV IDs to install.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36d4b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="36d4b-115">Return value</span></span>

<span data-ttu-id="36d4b-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="36d4b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="36d4b-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="36d4b-117">Return code</span></span>                                                                                  | <span data-ttu-id="36d4b-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36d4b-118">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="36d4b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="36d4b-119"><dt>**S\_OK** </dt></span></span> </dl>        | <span data-ttu-id="36d4b-120">Il metodo è stato eseguito correttamente.</span><span class="sxs-lookup"><span data-stu-id="36d4b-120">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="36d4b-121"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="36d4b-121"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="36d4b-122">Il parametro *count* è 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="36d4b-122">The *count* parameter was 0 (zero).</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="36d4b-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="36d4b-123">Requirements</span></span>



| <span data-ttu-id="36d4b-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="36d4b-124">Requirement</span></span> | <span data-ttu-id="36d4b-125">Valore</span><span class="sxs-lookup"><span data-stu-id="36d4b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36d4b-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36d4b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="36d4b-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="36d4b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="36d4b-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="36d4b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="36d4b-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="36d4b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="36d4b-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="36d4b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="36d4b-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="36d4b-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="36d4b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="36d4b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="36d4b-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="36d4b-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="36d4b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="36d4b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36d4b-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36d4b-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="36d4b-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="36d4b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36d4b-137">**INapEnforcementClientConnection2**</span><span class="sxs-lookup"><span data-stu-id="36d4b-137">**INapEnforcementClientConnection2**</span></span>](inapenforcementclientconnection2.md)
</dt> </dl>

 

 





