---
title: Metodo Validate INapSoHConstructor (NapProtocol. h)
description: Verifica la validità del pacchetto SoH.
ms.assetid: 66338213-43c0-461a-a794-5f18d56bd505
keywords:
- Convalida NAP metodo
- Metodo Validate NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, metodo Validate
topic_type:
- apiref
api_name:
- INapSoHConstructor.Validate
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7db8a52d7986348e85c724171b6d417996c7315
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742607"
---
# <a name="inapsohconstructorvalidate-method"></a><span data-ttu-id="434ee-106">Metodo INapSoHConstructor:: Validate</span><span class="sxs-lookup"><span data-stu-id="434ee-106">INapSoHConstructor::Validate method</span></span>

> [!Note]  
> <span data-ttu-id="434ee-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="434ee-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="434ee-108">Il metodo **INapSoHConstructor:: Validate** controlla la validità del pacchetto SOH.</span><span class="sxs-lookup"><span data-stu-id="434ee-108">The **INapSoHConstructor::Validate** method checks the validity of the SoH packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="434ee-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="434ee-109">Syntax</span></span>


```C++
HRESULT Validate(
  [in] const SoH  *soh,
  [in]       BOOL isRequest
);
```



## <a name="parameters"></a><span data-ttu-id="434ee-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="434ee-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="434ee-111">rapporto di *integrità* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="434ee-111">*soh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434ee-112">Puntatore al pacchetto di rapporto di [**integrità**](/windows/win32/api/naptypes/ns-naptypes-soh) costruito.</span><span class="sxs-lookup"><span data-stu-id="434ee-112">A pointer to the constructed [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="434ee-113">*richiesta* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="434ee-113">*isRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="434ee-114">**Bool** che è **true** se il pacchetto è un [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) e **false** se è un **SoHResponse**.</span><span class="sxs-lookup"><span data-stu-id="434ee-114">A **BOOL** that is **TRUE** if the packet is an [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** if it is an **SoHResponse**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="434ee-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="434ee-115">Return value</span></span>

<span data-ttu-id="434ee-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="434ee-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="434ee-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="434ee-117">Return code</span></span>                                                                                            | <span data-ttu-id="434ee-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="434ee-118">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="434ee-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-119"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="434ee-120">Il pacchetto del rapporto di integrità è valido.</span><span class="sxs-lookup"><span data-stu-id="434ee-120">The SoH packet is valid.</span></span><br/>                                |
| <dl> <span data-ttu-id="434ee-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="434ee-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="434ee-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="434ee-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="434ee-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="434ee-124">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="434ee-125"><dt>**NAP \_ E \_ pacchetto non valido \_**</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-125"><dt>**NAP\_E\_INVALID\_PACKET**</dt></span></span> </dl> | <span data-ttu-id="434ee-126">Il pacchetto del rapporto di integrità non è valido.</span><span class="sxs-lookup"><span data-stu-id="434ee-126">The SoH packet is invalid.</span></span><br/>                              |



 

## <a name="requirements"></a><span data-ttu-id="434ee-127">Requisiti</span><span class="sxs-lookup"><span data-stu-id="434ee-127">Requirements</span></span>



| <span data-ttu-id="434ee-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="434ee-128">Requirement</span></span> | <span data-ttu-id="434ee-129">Valore</span><span class="sxs-lookup"><span data-stu-id="434ee-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="434ee-130">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="434ee-130">Minimum supported client</span></span><br/> | <span data-ttu-id="434ee-131">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="434ee-131">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="434ee-132">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="434ee-132">Minimum supported server</span></span><br/> | <span data-ttu-id="434ee-133">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="434ee-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="434ee-134">Intestazione</span><span class="sxs-lookup"><span data-stu-id="434ee-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="434ee-135"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-135"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="434ee-136">IDL</span><span class="sxs-lookup"><span data-stu-id="434ee-136">IDL</span></span><br/>                      | <dl> <span data-ttu-id="434ee-137"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-137"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="434ee-138">DLL</span><span class="sxs-lookup"><span data-stu-id="434ee-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="434ee-139"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="434ee-139"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="434ee-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="434ee-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="434ee-141">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="434ee-141">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





