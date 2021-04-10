---
title: Metodo Initialize INapSoHProcessor (NapProtocol. h)
description: Inizializza il pacchetto del protocollo e il sistema di elaborazione del rapporto di integrità. Questo metodo deve essere chiamato una sola volta.
ms.assetid: 4fccc847-3c4d-4fc5-935d-28fb2964a9be
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSoHProcessor
- Interfaccia NAP di INapSoHProcessor, metodo Initialize
topic_type:
- apiref
api_name:
- INapSoHProcessor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ff3a32bb213caf19964ccea8175a43e5016f08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964220"
---
# <a name="inapsohprocessorinitialize-method"></a><span data-ttu-id="6dd3f-107">Metodo INapSoHProcessor:: Initialize</span><span class="sxs-lookup"><span data-stu-id="6dd3f-107">INapSoHProcessor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="6dd3f-108">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="6dd3f-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6dd3f-109">Il metodo **INapSoHProcessor:: Initialize** Inizializza il pacchetto del protocollo e il sistema di elaborazione del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-109">The **INapSoHProcessor::Initialize** method initializes the protocol packet and SoH processor system.</span></span> <span data-ttu-id="6dd3f-110">Questo metodo deve essere chiamato una sola volta.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-110">This method must be called exactly once.</span></span>

## <a name="syntax"></a><span data-ttu-id="6dd3f-111">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6dd3f-111">Syntax</span></span>


```C++
HRESULT Initialize(
  [in]  const SoH                  *soh,
  [in]        BOOL                 isRequest,
  [out]       SystemHealthEntityId *id
);
```



## <a name="parameters"></a><span data-ttu-id="6dd3f-112">Parametri</span><span class="sxs-lookup"><span data-stu-id="6dd3f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dd3f-113">rapporto di *integrità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dd3f-113">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd3f-114">Puntatore al pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) da elaborare.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-114">A pointer to the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet to be processed.</span></span>

</dd> <dt>

<span data-ttu-id="6dd3f-115">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6dd3f-115">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd3f-116">**Bool** che è **true** se il pacchetto è un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-116">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> <dt>

<span data-ttu-id="6dd3f-117">*ID* in \[ uscita\]</span><span class="sxs-lookup"><span data-stu-id="6dd3f-117">*id* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6dd3f-118">Un [SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA o del servizio di convalida dell'integrità di sistema che ha creato il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-118">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that constructed the packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dd3f-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6dd3f-119">Return value</span></span>

<span data-ttu-id="6dd3f-120">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6dd3f-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6dd3f-121">Return code</span></span>                                                                                            | <span data-ttu-id="6dd3f-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6dd3f-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="6dd3f-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="6dd3f-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="6dd3f-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="6dd3f-126">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="6dd3f-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="6dd3f-128">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="6dd3f-129"><dt>**NAP \_ E \_ pacchetto non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-129"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="6dd3f-130">Il pacchetto del rapporto di integrità non è valido.</span><span class="sxs-lookup"><span data-stu-id="6dd3f-130">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="6dd3f-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6dd3f-131">Requirements</span></span>



| <span data-ttu-id="6dd3f-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dd3f-132">Requirement</span></span> | <span data-ttu-id="6dd3f-133">Valore</span><span class="sxs-lookup"><span data-stu-id="6dd3f-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dd3f-134">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dd3f-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6dd3f-135">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6dd3f-135">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6dd3f-136">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6dd3f-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6dd3f-137">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6dd3f-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6dd3f-138">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6dd3f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dd3f-139"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-139"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="6dd3f-140">IDL</span><span class="sxs-lookup"><span data-stu-id="6dd3f-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6dd3f-141"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-141"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="6dd3f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6dd3f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6dd3f-143"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6dd3f-143"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="6dd3f-144">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6dd3f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6dd3f-145">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="6dd3f-145">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





