---
title: Metodo INapEnforcementClientConnection GetStringCorrelationId (NapEnforcementClient. h)
description: Ottiene la versione in formato stringa dell'ID utilizzato per correlare le richieste e le risposte.
ms.assetid: d744fa4e-5e30-429e-810d-7326047bb3f8
keywords:
- NAP metodo GetStringCorrelationId
- Metodo GetStringCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetStringCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetStringCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6a01ca16bffb627f4ca5be38ef547980951c0ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517578"
---
# <a name="inapenforcementclientconnectiongetstringcorrelationid-method"></a><span data-ttu-id="a1cdd-106">Metodo INapEnforcementClientConnection:: GetStringCorrelationId</span><span class="sxs-lookup"><span data-stu-id="a1cdd-106">INapEnforcementClientConnection::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="a1cdd-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="a1cdd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a1cdd-108">Il metodo **INapEnforcementClientConnection:: GetStringCorrelationId** ottiene la versione in formato stringa dell'ID usato per correlare le richieste e le risposte.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-108">The **INapEnforcementClientConnection::GetStringCorrelationId** method gets the string version of the ID used to correlate requests and responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1cdd-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1cdd-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] CountedString **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="a1cdd-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1cdd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1cdd-111">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a1cdd-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a1cdd-112">Puntatore a una struttura [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) che contiene la versione in formato stringa dell'oggetto [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid)della connessione.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-112">A pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the string version of the connection's [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1cdd-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1cdd-113">Return value</span></span>

<span data-ttu-id="a1cdd-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a1cdd-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a1cdd-115">Return code</span></span>                                                                                     | <span data-ttu-id="a1cdd-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1cdd-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1cdd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="a1cdd-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="a1cdd-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="a1cdd-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="a1cdd-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="a1cdd-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="a1cdd-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a1cdd-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1cdd-123">Requirements</span></span>



| <span data-ttu-id="a1cdd-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1cdd-124">Requirement</span></span> | <span data-ttu-id="a1cdd-125">Valore</span><span class="sxs-lookup"><span data-stu-id="a1cdd-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1cdd-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1cdd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="a1cdd-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a1cdd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a1cdd-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1cdd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="a1cdd-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a1cdd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a1cdd-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1cdd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1cdd-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="a1cdd-132">IDL</span><span class="sxs-lookup"><span data-stu-id="a1cdd-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a1cdd-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="a1cdd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a1cdd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1cdd-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1cdd-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a1cdd-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1cdd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1cdd-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="a1cdd-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





