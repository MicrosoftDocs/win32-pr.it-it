---
title: Metodo INapEnforcementClientConnection GetIsolationInfo (NapEnforcementClient. h)
description: Viene usato per ottenere le informazioni di isolamento del client.
ms.assetid: 33040554-dcbe-4563-b047-fc7e28bac55c
keywords:
- NAP metodo GetIsolationInfo
- Metodo GetIsolationInfo NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetIsolationInfo
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 890f7268801fda77a9794ed21c4d36e78a52dd5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964962"
---
# <a name="inapenforcementclientconnectiongetisolationinfo-method"></a><span data-ttu-id="cca15-106">Metodo INapEnforcementClientConnection:: GetIsolationInfo</span><span class="sxs-lookup"><span data-stu-id="cca15-106">INapEnforcementClientConnection::GetIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="cca15-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="cca15-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cca15-108">Il metodo **INapEnforcementClientConnection:: GetIsolationInfo** viene usato per ottenere le informazioni di isolamento del client.</span><span class="sxs-lookup"><span data-stu-id="cca15-108">The **INapEnforcementClientConnection::GetIsolationInfo** method is used get the isolation information of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca15-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cca15-109">Syntax</span></span>


```C++
HRESULT GetIsolationInfo(
  [out] IsolationInfo **isolationInfo
);
```



## <a name="parameters"></a><span data-ttu-id="cca15-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cca15-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca15-111">*isolationInfo* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cca15-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cca15-112">Puntatore a un puntatore a una struttura [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) che contiene lo stato di connettività del client.</span><span class="sxs-lookup"><span data-stu-id="cca15-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the connectivity state of the client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca15-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cca15-113">Return value</span></span>

<span data-ttu-id="cca15-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="cca15-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cca15-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cca15-115">Return code</span></span>                                                                                     | <span data-ttu-id="cca15-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cca15-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cca15-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cca15-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="cca15-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cca15-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cca15-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="cca15-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cca15-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cca15-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cca15-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cca15-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="cca15-123">Remarks</span></span>

<span data-ttu-id="cca15-124">Queste informazioni vengono impostate da NapAgent dopo l'elaborazione di un [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) e non devono essere impostate dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cca15-124">This information is set by the NapAgent after processing a [**SoHResponse**](/windows/win32/api/naptypes/ns-naptypes-soh) and must not be set by the enforcer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cca15-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cca15-125">Requirements</span></span>



| <span data-ttu-id="cca15-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="cca15-126">Requirement</span></span> | <span data-ttu-id="cca15-127">Valore</span><span class="sxs-lookup"><span data-stu-id="cca15-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca15-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca15-128">Minimum supported client</span></span><br/> | <span data-ttu-id="cca15-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cca15-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cca15-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cca15-130">Minimum supported server</span></span><br/> | <span data-ttu-id="cca15-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cca15-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cca15-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cca15-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="cca15-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cca15-134">IDL</span><span class="sxs-lookup"><span data-stu-id="cca15-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cca15-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="cca15-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cca15-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cca15-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cca15-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cca15-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cca15-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca15-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="cca15-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





