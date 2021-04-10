---
title: Metodo INapEnforcementClientConnection GetConnectionId (NapEnforcementClient. h)
description: Viene utilizzato per ottenere l'ID di connessione univoco del client.
ms.assetid: bf744aa6-5786-473f-9508-db4ee0c75578
keywords:
- NAP metodo GetConnectionId
- Metodo GetConnectionId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetConnectionId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3ca16aea3c77ccf78359c3cdf5ab6461bc2219e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121602"
---
# <a name="inapenforcementclientconnectiongetconnectionid-method"></a><span data-ttu-id="159d8-106">Metodo INapEnforcementClientConnection:: GetConnectionId</span><span class="sxs-lookup"><span data-stu-id="159d8-106">INapEnforcementClientConnection::GetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="159d8-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="159d8-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="159d8-108">Il metodo **INapEnforcementClientConnection:: GetConnectionId** viene usato per ottenere l'ID di connessione univoco del client.</span><span class="sxs-lookup"><span data-stu-id="159d8-108">The **INapEnforcementClientConnection::GetConnectionId** method is used to get the unique connection ID of the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="159d8-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="159d8-109">Syntax</span></span>


```C++
HRESULT GetConnectionId(
  [out] ConnectionId **connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="159d8-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="159d8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159d8-111">*ConnectionId* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="159d8-111">*connectionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="159d8-112">Puntatore a un puntatore a un [**ConnectionId**](nap-datatypes.md) che identifica in modo univoco questa connessione.</span><span class="sxs-lookup"><span data-stu-id="159d8-112">A pointer to a pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies this connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159d8-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="159d8-113">Return value</span></span>

<span data-ttu-id="159d8-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="159d8-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="159d8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="159d8-115">Return code</span></span>                                                                                     | <span data-ttu-id="159d8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="159d8-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="159d8-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="159d8-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="159d8-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="159d8-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="159d8-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="159d8-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="159d8-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="159d8-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="159d8-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="159d8-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="159d8-123">Remarks</span></span>

<span data-ttu-id="159d8-124">L'ID connessione viene utilizzato principalmente a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="159d8-124">The connection ID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="159d8-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="159d8-125">Requirements</span></span>



| <span data-ttu-id="159d8-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="159d8-126">Requirement</span></span> | <span data-ttu-id="159d8-127">Valore</span><span class="sxs-lookup"><span data-stu-id="159d8-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="159d8-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159d8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="159d8-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="159d8-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="159d8-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="159d8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="159d8-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="159d8-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="159d8-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="159d8-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="159d8-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="159d8-134">IDL</span><span class="sxs-lookup"><span data-stu-id="159d8-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="159d8-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="159d8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="159d8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="159d8-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="159d8-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="159d8-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="159d8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159d8-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="159d8-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





