---
title: Metodo INapEnforcementClientConnection SetPrivateData (NapEnforcementClient. h)
description: Viene usato da NapAgent per impostare i dati privati.
ms.assetid: 2559a612-8857-4e60-b5bc-dd8235ff69f9
keywords:
- NAP metodo SetPrivateData
- Metodo SetPrivateData NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetPrivateData
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetPrivateData
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3e73248e546b1f0e48438553877f0523bd30b56
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048156"
---
# <a name="inapenforcementclientconnectionsetprivatedata-method"></a><span data-ttu-id="5cafe-106">Metodo INapEnforcementClientConnection:: SetPrivateData</span><span class="sxs-lookup"><span data-stu-id="5cafe-106">INapEnforcementClientConnection::SetPrivateData method</span></span>

> [!Note]  
> <span data-ttu-id="5cafe-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="5cafe-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5cafe-108">Il metodo **INapEnforcementClientConnection:: SetPrivateData** viene usato da napagent per impostare i dati privati.</span><span class="sxs-lookup"><span data-stu-id="5cafe-108">The **INapEnforcementClientConnection::SetPrivateData** method is used by the NapAgent to set private data.</span></span>

## <a name="syntax"></a><span data-ttu-id="5cafe-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5cafe-109">Syntax</span></span>


```C++
HRESULT SetPrivateData(
  [in] const PrivateData *privateData
);
```



## <a name="parameters"></a><span data-ttu-id="5cafe-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="5cafe-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5cafe-111">*PrivateData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5cafe-111">*privateData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5cafe-112">Puntatore a un BLOB di dati [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) che può essere interpretato solo da napagent.</span><span class="sxs-lookup"><span data-stu-id="5cafe-112">A pointer to a [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) data blob that only the NapAgent can interpret.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5cafe-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5cafe-113">Return value</span></span>

<span data-ttu-id="5cafe-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="5cafe-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5cafe-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5cafe-115">Return code</span></span>                                                                                     | <span data-ttu-id="5cafe-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5cafe-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="5cafe-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="5cafe-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="5cafe-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="5cafe-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="5cafe-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="5cafe-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="5cafe-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="5cafe-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="5cafe-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5cafe-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5cafe-123">Requirements</span></span>



| <span data-ttu-id="5cafe-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5cafe-124">Requirement</span></span> | <span data-ttu-id="5cafe-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5cafe-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5cafe-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cafe-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5cafe-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5cafe-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5cafe-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5cafe-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5cafe-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5cafe-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5cafe-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5cafe-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5cafe-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="5cafe-132">IDL</span><span class="sxs-lookup"><span data-stu-id="5cafe-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5cafe-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="5cafe-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5cafe-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5cafe-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5cafe-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5cafe-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5cafe-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5cafe-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="5cafe-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





