---
title: Metodo INapEnforcementClientConnection SetMaxSize (NapEnforcementClient. h)
description: Imposta la dimensione massima del pacchetto di rapporto di integrità per il client.
ms.assetid: 30d3747d-bcf8-41b3-b0af-29f20d48417b
keywords:
- NAP metodo SetMaxSize
- Metodo SetMaxSize NAP, interfaccia INapEnforcementClientConnection
- Interfaccia INapEnforcementClientConnection NAP, metodo SetMaxSize
topic_type:
- apiref
api_name:
- INapEnforcementClientConnection.SetMaxSize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b10d7bc1a023371683f17bb3e6e12cd578fa964
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400488"
---
# <a name="inapenforcementclientconnectionsetmaxsize-method"></a><span data-ttu-id="68ebf-106">Metodo INapEnforcementClientConnection:: SetMaxSize</span><span class="sxs-lookup"><span data-stu-id="68ebf-106">INapEnforcementClientConnection::SetMaxSize method</span></span>

> [!Note]  
> <span data-ttu-id="68ebf-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="68ebf-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="68ebf-108">Il metodo **INapEnforcementClientConnection:: SetMaxSize** imposta la dimensione massima del pacchetto di rapporto di integrità per il client.</span><span class="sxs-lookup"><span data-stu-id="68ebf-108">The **INapEnforcementClientConnection::SetMaxSize** method sets the maximum size of the SoH packet for this client.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ebf-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68ebf-109">Syntax</span></span>


```C++
HRESULT SetMaxSize(
  [in] ProtocolMaxSize maxSize
);
```



## <a name="parameters"></a><span data-ttu-id="68ebf-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="68ebf-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68ebf-111">*MaxSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68ebf-111">*maxSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68ebf-112">Struttura [**ProtocolMaxSize**](nap-datatypes.md) che indica la dimensione massima, in byte, del pacchetto di rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="68ebf-112">A [**ProtocolMaxSize**](nap-datatypes.md) structure that indicates the maximum size, in bytes, of the SoH packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68ebf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68ebf-113">Return value</span></span>

<span data-ttu-id="68ebf-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="68ebf-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="68ebf-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="68ebf-115">Return code</span></span>                                                                                     | <span data-ttu-id="68ebf-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68ebf-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="68ebf-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="68ebf-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="68ebf-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="68ebf-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="68ebf-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="68ebf-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="68ebf-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="68ebf-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="68ebf-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="68ebf-123">Commenti</span><span class="sxs-lookup"><span data-stu-id="68ebf-123">Remarks</span></span>

<span data-ttu-id="68ebf-124">Questo valore viene impostato dal client di imposizione.</span><span class="sxs-lookup"><span data-stu-id="68ebf-124">This value is set by the enforcement client.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ebf-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68ebf-125">Requirements</span></span>



| <span data-ttu-id="68ebf-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="68ebf-126">Requirement</span></span> | <span data-ttu-id="68ebf-127">Valore</span><span class="sxs-lookup"><span data-stu-id="68ebf-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68ebf-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68ebf-128">Minimum supported client</span></span><br/> | <span data-ttu-id="68ebf-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="68ebf-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="68ebf-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="68ebf-130">Minimum supported server</span></span><br/> | <span data-ttu-id="68ebf-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="68ebf-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="68ebf-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68ebf-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="68ebf-133"><dt>NapEnforcementClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-133"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="68ebf-134">IDL</span><span class="sxs-lookup"><span data-stu-id="68ebf-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="68ebf-135"><dt>NapEnforcementClient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-135"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |
| <span data-ttu-id="68ebf-136">DLL</span><span class="sxs-lookup"><span data-stu-id="68ebf-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68ebf-137"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ebf-137"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="68ebf-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68ebf-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ebf-139">**INapEnforcementClientConnection**</span><span class="sxs-lookup"><span data-stu-id="68ebf-139">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





