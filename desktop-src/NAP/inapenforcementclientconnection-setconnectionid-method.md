---
title: Metodo INapEnforcementClientConnection SetConnectionId (NapEnforcementClient. h)
description: Viene utilizzato per impostare l'ID univoco della connessione e deve essere impostato dal client di imposizione non appena viene creata la connessione.
ms.assetid: 69d1a891-bc86-4c8a-b614-ebcdaa4a9057
keywords:
- NAP metodo SetConnectionId
- Metodo SetConnectionId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetConnectionId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetConnectionId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa9749be304170ec7706b637429f577e77411ac5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964007"
---
# <a name="inapenforcementclientconnectionsetconnectionid-method"></a><span data-ttu-id="b75f1-106">Metodo INapEnforcementClientConnection:: SetConnectionId</span><span class="sxs-lookup"><span data-stu-id="b75f1-106">INapEnforcementClientConnection::SetConnectionId method</span></span>

> [!Note]  
> <span data-ttu-id="b75f1-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="b75f1-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b75f1-108">Il metodo **INapEnforcementClientConnection:: SetConnectionId** viene usato per impostare l'ID univoco della connessione e deve essere impostato dal client di imposizione non appena viene creata la connessione.</span><span class="sxs-lookup"><span data-stu-id="b75f1-108">The **INapEnforcementClientConnection::SetConnectionId** method is used to set the unique ID of the connection and must be set by the enforcement client as soon as the connection is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75f1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b75f1-109">Syntax</span></span>


```C++
HRESULT SetConnectionId(
  [in] const ConnectionId *connectionId
);
```



## <a name="parameters"></a><span data-ttu-id="b75f1-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="b75f1-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b75f1-111">*ConnectionId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b75f1-111">*connectionId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b75f1-112">Puntatore a un [**ConnectionId**](nap-datatypes.md) che identifica in modo univoco una connessione.</span><span class="sxs-lookup"><span data-stu-id="b75f1-112">A pointer to a [**ConnectionId**](nap-datatypes.md) that uniquely identifies a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b75f1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b75f1-113">Return value</span></span>

<span data-ttu-id="b75f1-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="b75f1-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="b75f1-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="b75f1-115">Return code</span></span>                                                                                     | <span data-ttu-id="b75f1-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b75f1-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b75f1-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="b75f1-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="b75f1-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="b75f1-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="b75f1-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="b75f1-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b75f1-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="b75f1-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="b75f1-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b75f1-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="b75f1-123">Remarks</span></span>

<span data-ttu-id="b75f1-124">Questo ConnectionID viene usato principalmente a scopo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="b75f1-124">This ConnectionID is primarily used for logging purposes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75f1-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b75f1-125">Requirements</span></span>



| <span data-ttu-id="b75f1-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b75f1-126">Requirement</span></span> | <span data-ttu-id="b75f1-127">Valore</span><span class="sxs-lookup"><span data-stu-id="b75f1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b75f1-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b75f1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b75f1-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b75f1-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b75f1-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b75f1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b75f1-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b75f1-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b75f1-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b75f1-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b75f1-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="b75f1-134">IDL</span><span class="sxs-lookup"><span data-stu-id="b75f1-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b75f1-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="b75f1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="b75f1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b75f1-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b75f1-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="b75f1-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b75f1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75f1-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="b75f1-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





