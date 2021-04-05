---
title: Metodo INapEnforcementClientConnection SetIsolationInfo (NapEnforcementClient. h)
description: Viene usato da NapAgent per impostare le informazioni di isolamento del client.
ms.assetid: e92d8762-4ae9-40e5-a18e-7da757aa6f9e
keywords:
- NAP metodo SetIsolationInfo
- Metodo SetIsolationInfo NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c1cfd7ad227fec6942e0660769f52b3d4f12201
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740927"
---
# <a name="inapenforcementclientconnectionsetisolationinfo-method"></a><span data-ttu-id="7ccab-106">Metodo INapEnforcementClientConnection:: SetIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="7ccab-106">INapEnforcementClientConnection::SetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="7ccab-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="7ccab-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="7ccab-108">Il metodo **INapEnforcementClientConnection:: SetIsolationInfo** viene usato da napagent per impostare le informazioni di isolamento del client.</span><span class="sxs-lookup"><span data-stu-id="7ccab-108">The **INapEnforcementClientConnection::SetIsolationInfo** method is used by the NapAgent to set the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ccab-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ccab-109">Syntax</span></span>


```C++
HRESULT SetIsolationInfo(
  [in] const IsolationInfo *isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="7ccab-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ccab-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ccab-111">*isolationInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ccab-111">*isolationInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ccab-112">Puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di connettività del client.</span><span class="sxs-lookup"><span data-stu-id="7ccab-112">A pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ccab-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ccab-113">Return value</span></span>

<span data-ttu-id="7ccab-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="7ccab-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="7ccab-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ccab-115">Return code</span></span>                                                                                     | <span data-ttu-id="7ccab-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ccab-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ccab-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="7ccab-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="7ccab-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="7ccab-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="7ccab-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="7ccab-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="7ccab-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="7ccab-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="7ccab-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ccab-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ccab-123">Remarks</span></span>

<span data-ttu-id="7ccab-124">Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un SoHResponse e non devono essere impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7ccab-124">This information is set by NapAgent after processing an SoHResponse and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ccab-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ccab-125">Requirements</span></span>



| <span data-ttu-id="7ccab-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ccab-126">Requirement</span></span> | <span data-ttu-id="7ccab-127">Valore</span><span class="sxs-lookup"><span data-stu-id="7ccab-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ccab-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ccab-128">Minimum supported client</span></span><br/> | <span data-ttu-id="7ccab-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7ccab-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="7ccab-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ccab-130">Minimum supported server</span></span><br/> | <span data-ttu-id="7ccab-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7ccab-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="7ccab-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ccab-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ccab-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ccab-134">IDL</span><span class="sxs-lookup"><span data-stu-id="7ccab-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7ccab-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="7ccab-136">DLL</span><span class="sxs-lookup"><span data-stu-id="7ccab-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ccab-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ccab-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="7ccab-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ccab-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ccab-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="7ccab-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





