---
title: Metodo INapEnforcementClientConnection SetCorrelationId (NapEnforcementClient. h)
description: Imposta l'ID usato per correlare le richieste di rapporto di integrità e le risposte a rapporto di integrità.
ms.assetid: 8f9d5bde-95b1-4566-84ee-31c6ed5e8986
keywords:
- NAP metodo SetCorrelationId
- Metodo SetCorrelationId NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetCorrelationId
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetCorrelationId
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c99576b8302f7fcf949f132cf110a5ac5f675ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517577"
---
# <a name="inapenforcementclientconnectionsetcorrelationid-method"></a><span data-ttu-id="886e2-106">Metodo INapEnforcementClientConnection:: SetCorrelationId</span><span class="sxs-lookup"><span data-stu-id="886e2-106">INapEnforcementClientConnection::SetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="886e2-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="886e2-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="886e2-108">Il metodo **INapEnforcementClientConnection:: SetCorrelationId** imposta l'ID usato per correlare le richieste e le risposte a rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="886e2-108">The **INapEnforcementClientConnection::SetCorrelationId** method sets the ID used to correlate SoH-requests and SoH-responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="886e2-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="886e2-109">Syntax</span></span>


```C++
HRESULT SetCorrelationId(
  [in] CorrelationId correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="886e2-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="886e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="886e2-111">ID correlazione  \[ in\]</span><span class="sxs-lookup"><span data-stu-id="886e2-111">*correlationId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="886e2-112">Struttura [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) univoca che identifica uno scambio di rapporto di integrità specifico.</span><span class="sxs-lookup"><span data-stu-id="886e2-112">A unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) structure that identifies a specific SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="886e2-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="886e2-113">Return value</span></span>

<span data-ttu-id="886e2-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="886e2-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="886e2-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="886e2-115">Return code</span></span>                                                                                     | <span data-ttu-id="886e2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="886e2-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="886e2-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="886e2-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="886e2-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="886e2-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="886e2-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="886e2-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="886e2-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="886e2-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="886e2-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="886e2-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="886e2-123">Remarks</span></span>

<span data-ttu-id="886e2-124">L'ID di correlazione viene impostato da NapAgent e in base all'ID connessione.</span><span class="sxs-lookup"><span data-stu-id="886e2-124">The correlation-id is set by the NapAgent and based on the connection-id.</span></span>

<span data-ttu-id="886e2-125">Questo ID viene usato per correlare le richieste e le risposte, ovvero descrive in modo univoco uno scambio di rapporto di integrità e contiene sempre l'ID del set di integrità più recente per l'oggetto connessione.</span><span class="sxs-lookup"><span data-stu-id="886e2-125">This id is used to correlate requests and responses, i.e. it uniquely describes an SoH exchange and always contains the id of the most recent SoH set on the connection object.</span></span>

<span data-ttu-id="886e2-126">Quando viene ricevuta una SoH-Response, il NapAgent garantisce prima di tutto gli ID corrispondenti; in caso contrario, viene restituito un errore e l'applicazione deve eliminare il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="886e2-126">When an SoH-Response is received, the NapAgent first ensures the IDs match; if not, an error is returned and the enforcer must drop the packet.</span></span> <span data-ttu-id="886e2-127">Per ulteriori informazioni, vedere [**INapEnforcementClientBinding::P rocesssohresponse**](inapenforcementclientbinding-processsohresponse-method.md) .</span><span class="sxs-lookup"><span data-stu-id="886e2-127">See [**INapEnforcementClientBinding::ProcessSoHResponse**](inapenforcementclientbinding-processsohresponse-method.md) for more details.</span></span>

## <a name="requirements"></a><span data-ttu-id="886e2-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="886e2-128">Requirements</span></span>



| <span data-ttu-id="886e2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="886e2-129">Requirement</span></span> | <span data-ttu-id="886e2-130">Valore</span><span class="sxs-lookup"><span data-stu-id="886e2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="886e2-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="886e2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="886e2-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="886e2-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="886e2-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="886e2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="886e2-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="886e2-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="886e2-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="886e2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="886e2-136"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-136"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="886e2-137">IDL</span><span class="sxs-lookup"><span data-stu-id="886e2-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="886e2-138"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-138"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="886e2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="886e2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="886e2-140"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="886e2-140"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="886e2-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="886e2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="886e2-142">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="886e2-142">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





