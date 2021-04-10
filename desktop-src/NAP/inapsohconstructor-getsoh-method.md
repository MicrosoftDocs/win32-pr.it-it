---
title: Metodo INapSoHConstructor GetSoH (NapProtocol. h)
description: Recupera il pacchetto SoHRequest o SoHResponse costruito.
ms.assetid: 402c72fd-9e23-453a-8c95-57615295e056
keywords:
- NAP metodo GetSoH
- Metodo GetSoH NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, metodo GetSoH
topic_type:
- apiref
api_name:
- INapSoHConstructor.GetSoH
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 066257aadf0ed14816efec06936d4b070087159f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119643"
---
# <a name="inapsohconstructorgetsoh-method"></a><span data-ttu-id="c9a4c-106">Metodo INapSoHConstructor:: GetSoH</span><span class="sxs-lookup"><span data-stu-id="c9a4c-106">INapSoHConstructor::GetSoH method</span></span>

> [!Note]  
> <span data-ttu-id="c9a4c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="c9a4c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c9a4c-108">Il metodo **INapSoHConstructor:: GetSoH** Recupera il pacchetto SoHRequest o SoHResponse costruito.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-108">The **INapSoHConstructor::GetSoH** method retrieves the constructed SoHRequest or SoHResponse packet.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9a4c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c9a4c-109">Syntax</span></span>


```C++
HRESULT GetSoH(
  [out] SoH **soh
);
```



## <a name="parameters"></a><span data-ttu-id="c9a4c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="c9a4c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9a4c-111">rapporto di *integrità* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c9a4c-111">*soh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9a4c-112">Puntatore a un puntatore al pacchetto [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) o **SoHResponse** costruito.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-112">A pointer to a pointer to the constructed [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) or **SoHResponse** packet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9a4c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c9a4c-113">Return value</span></span>

<span data-ttu-id="c9a4c-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c9a4c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c9a4c-115">Return code</span></span>                                                                                     | <span data-ttu-id="c9a4c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9a4c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c9a4c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c9a4c-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-118">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="c9a4c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c9a4c-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c9a4c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c9a4c-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="c9a4c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9a4c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c9a4c-123">Requirements</span></span>



| <span data-ttu-id="c9a4c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9a4c-124">Requirement</span></span> | <span data-ttu-id="c9a4c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="c9a4c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9a4c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a4c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c9a4c-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c9a4c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c9a4c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c9a4c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c9a4c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c9a4c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c9a4c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c9a4c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9a4c-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="c9a4c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c9a4c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c9a4c-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="c9a4c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c9a4c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9a4c-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9a4c-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="c9a4c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c9a4c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9a4c-137">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="c9a4c-137">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





