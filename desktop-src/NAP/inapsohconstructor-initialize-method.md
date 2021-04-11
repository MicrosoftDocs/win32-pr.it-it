---
title: Metodo Initialize INapSoHConstructor (NapProtocol. h)
description: Inizializza un pacchetto di protocollo di rapporto di integrità nel sistema NAP.
ms.assetid: 1678b677-c8c8-465c-a412-9b929e39bbac
keywords:
- Metodo di inizializzazione NAP
- Metodo Initialize NAP, interfaccia INapSoHConstructor
- Interfaccia NAP di INapSoHConstructor, metodo Initialize
topic_type:
- apiref
api_name:
- INapSoHConstructor.Initialize
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab8d6b27547be6e7c7e9abb59f7edb7b49e716e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964147"
---
# <a name="inapsohconstructorinitialize-method"></a><span data-ttu-id="8921d-106">Metodo INapSoHConstructor:: Initialize</span><span class="sxs-lookup"><span data-stu-id="8921d-106">INapSoHConstructor::Initialize method</span></span>

> [!Note]  
> <span data-ttu-id="8921d-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="8921d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="8921d-108">Il metodo **INapSoHConstructor:: Initialize** Inizializza un pacchetto di protocollo di rapporto di integrità nel sistema NAP.</span><span class="sxs-lookup"><span data-stu-id="8921d-108">The **INapSoHConstructor::Initialize** method initializes a SoH protocol packet in the NAP system.</span></span>

## <a name="syntax"></a><span data-ttu-id="8921d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8921d-109">Syntax</span></span>


```C++
HRESULT Initialize(
  [in] SystemHealthEntityId id,
  [in] BOOL                 isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="8921d-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="8921d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8921d-111">*ID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8921d-111">*id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8921d-112">[SystemHealthEntityId](nap-datatypes.md) univoco che contiene l'ID dell'SHA o del servizio di convalida dell'integrità di sistema che costruisce il pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8921d-112">A unique [SystemHealthEntityId](nap-datatypes.md) that contains the ID of the SHA or SHV that is constructing the packet.</span></span>

</dd> <dt>

<span data-ttu-id="8921d-113">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8921d-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8921d-114">**Bool** che è **true** se il pacchetto deve essere un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="8921d-114">A **BOOL** that is **TRUE** if the packet is to be an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is to be an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8921d-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8921d-115">Return value</span></span>

<span data-ttu-id="8921d-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="8921d-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="8921d-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8921d-117">Return code</span></span>                                                                                     | <span data-ttu-id="8921d-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8921d-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="8921d-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="8921d-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="8921d-120">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="8921d-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="8921d-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="8921d-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="8921d-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="8921d-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="8921d-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8921d-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="8921d-125">Remarks</span></span>

<span data-ttu-id="8921d-126">Questo metodo deve essere chiamato una sola volta per ogni pacchetto.</span><span class="sxs-lookup"><span data-stu-id="8921d-126">This method must be called exactly once per packet.</span></span>

<span data-ttu-id="8921d-127">Il [SystemHealthEntityId](nap-datatypes.md) specificato in *ID* è il primo TLV nel pacchetto SOH appena costruito e ha il tipo di attributo [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span><span class="sxs-lookup"><span data-stu-id="8921d-127">The [SystemHealthEntityId](nap-datatypes.md) specified in *id*, is the first TLV in the newly constructed SOH packet and has the attribute type [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8921d-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8921d-128">Requirements</span></span>



| <span data-ttu-id="8921d-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8921d-129">Requirement</span></span> | <span data-ttu-id="8921d-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8921d-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="8921d-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8921d-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8921d-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8921d-132">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8921d-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8921d-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8921d-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8921d-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="8921d-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8921d-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8921d-136"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-136"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="8921d-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8921d-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8921d-138"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-138"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="8921d-139">DLL</span><span class="sxs-lookup"><span data-stu-id="8921d-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8921d-140"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8921d-140"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="8921d-141">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8921d-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8921d-142">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="8921d-142">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





