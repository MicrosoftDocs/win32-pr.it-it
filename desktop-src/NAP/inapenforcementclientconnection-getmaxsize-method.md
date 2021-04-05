---
title: Metodo INapEnforcementClientConnection GetMaxSize (NapEnforcementClient. h)
description: Ottiene la dimensione massima del pacchetto di rapporto di integrità per il client.
ms.assetid: 054bc783-db5d-4801-8984-6b8a131744a2
keywords:
- NAP metodo GetMaxSize
- Metodo GetMaxSize NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo GetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.GetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3d86cc71cd5da906146ab1577d58311d167d484
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740935"
---
# <a name="inapenforcementclientconnectiongetmaxsize-method"></a><span data-ttu-id="02cef-106">Metodo INapEnforcementClientConnection:: GetMaxSize</span><span class="sxs-lookup"><span data-stu-id="02cef-106">INapEnforcementClientConnection::GetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="02cef-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="02cef-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="02cef-108">Il metodo **INapEnforcementClientConnection:: GetMaxSize** ottiene la dimensione massima del pacchetto di rapporto di integrità per il client.</span><span class="sxs-lookup"><span data-stu-id="02cef-108">The **INapEnforcementClientConnection::GetMaxSize** method gets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="02cef-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02cef-109">Syntax</span></span>


```C++
HRESULT GetMaxSize(
  [out] ProtocolMaxSize *maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="02cef-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="02cef-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02cef-111">*MaxSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="02cef-111">*maxSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02cef-112">Puntatore a un [**ProtocolMaxSize**](nap-datatypes.md) che indica la dimensione massima, in byte, del pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="02cef-112">A pointer to a [**ProtocolMaxSize**](nap-datatypes.md) that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02cef-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02cef-113">Return value</span></span>

<span data-ttu-id="02cef-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="02cef-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="02cef-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="02cef-115">Return code</span></span>                                                                                     | <span data-ttu-id="02cef-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02cef-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="02cef-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="02cef-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="02cef-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="02cef-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="02cef-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="02cef-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="02cef-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="02cef-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="02cef-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="02cef-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="02cef-123">Requirements</span></span>



| <span data-ttu-id="02cef-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="02cef-124">Requirement</span></span> | <span data-ttu-id="02cef-125">Valore</span><span class="sxs-lookup"><span data-stu-id="02cef-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02cef-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02cef-126">Minimum supported client</span></span><br/> | <span data-ttu-id="02cef-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="02cef-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="02cef-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="02cef-128">Minimum supported server</span></span><br/> | <span data-ttu-id="02cef-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="02cef-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="02cef-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="02cef-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="02cef-131"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-131"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="02cef-132">IDL</span><span class="sxs-lookup"><span data-stu-id="02cef-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="02cef-133"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-133"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="02cef-134">DLL</span><span class="sxs-lookup"><span data-stu-id="02cef-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="02cef-135"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="02cef-135"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="02cef-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02cef-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02cef-137">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="02cef-137">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





