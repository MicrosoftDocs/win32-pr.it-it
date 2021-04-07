---
title: Metodo INapEnforcementClientConnection GetCorrelationId (NapEnforcementClient. h)
description: Ottiene l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.
ms.assetid: f59880d4-5de6-4163-ae01-1095ff52bf38
keywords:
- NAP metodo GetCorrelationId
- Metodo GetCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82572cc499a61d453a70c47391e48f2004dca24d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104048759"
---
# <a name="inapenforcementclientconnectiongetcorrelationid-method"></a><span data-ttu-id="cb487-106">Metodo INapEnforcementClientConnection:: GetCorrelationId</span><span class="sxs-lookup"><span data-stu-id="cb487-106">INapEnforcementClientConnection::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="cb487-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="cb487-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="cb487-108">Il metodo **INapEnforcementClientConnection:: GetCorrelationId** Ottiene l'ID usato per correlare le richieste e le risposte a rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="cb487-108">The **INapEnforcementClientConnection::GetCorrelationId** method gets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb487-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cb487-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="cb487-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="cb487-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb487-111">ID correlazione  \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cb487-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cb487-112">Struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoca che identifica questo scambio di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="cb487-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb487-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cb487-113">Return value</span></span>

<span data-ttu-id="cb487-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="cb487-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="cb487-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="cb487-115">Return code</span></span>                                                                                     | <span data-ttu-id="cb487-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb487-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="cb487-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="cb487-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="cb487-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="cb487-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="cb487-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="cb487-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="cb487-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="cb487-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="cb487-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cb487-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="cb487-123">Remarks</span></span>

<span data-ttu-id="cb487-124">L'ID di correlazione viene impostato da NapAgent e in base all'ID connessione.</span><span class="sxs-lookup"><span data-stu-id="cb487-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="cb487-125">Questo ID viene usato per correlare le richieste e le risposte, ovvero descrive in modo univoco uno scambio di rapporto di integrità e contiene sempre l'ID del set di integrità più recente per l'oggetto connessione.</span><span class="sxs-lookup"><span data-stu-id="cb487-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="cb487-126">Quando viene ricevuta una SoH-Response, il NapAgent garantisce prima di tutto gli ID corrispondenti; in caso contrario, viene restituito un errore e l'applicazione deve eliminare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="cb487-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="cb487-127">Per ulteriori informazioni, vedere [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="cb487-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb487-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cb487-128">Requirements</span></span>



| <span data-ttu-id="cb487-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb487-129">Requirement</span></span> | <span data-ttu-id="cb487-130">Valore</span><span class="sxs-lookup"><span data-stu-id="cb487-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb487-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb487-131">Minimum supported client</span></span><br/> | <span data-ttu-id="cb487-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cb487-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="cb487-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="cb487-133">Minimum supported server</span></span><br/> | <span data-ttu-id="cb487-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cb487-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="cb487-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cb487-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb487-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="cb487-137">IDL</span><span class="sxs-lookup"><span data-stu-id="cb487-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="cb487-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="cb487-139">DLL</span><span class="sxs-lookup"><span data-stu-id="cb487-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb487-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb487-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="cb487-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cb487-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb487-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="cb487-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





