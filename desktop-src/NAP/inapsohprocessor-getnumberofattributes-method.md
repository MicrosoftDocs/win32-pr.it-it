---
title: Metodo INapSoHProcessor GetNumberOfAttributes (NapProtocol. h)
description: Recupera il numero totale di attributi nel rapporto di integrità.
ms.assetid: ee0b1857-65a7-47bb-ae91-c939344a24d0
keywords:
- NAP metodo GetNumberOfAttributes
- Metodo GetNumberOfAttributes NAP, interfaccia INapSoHProcessor
- Interfaccia INapSoHProcessor NAP, metodo GetNumberOfAttributes
topic_type:
- apiref
api_name:
- INapSoHProcessor.GetNumberOfAttributes
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f1336362b44d49c71ce81b197f9f95b1a1b8fc9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517770"
---
# <a name="inapsohprocessorgetnumberofattributes-method"></a><span data-ttu-id="d573c-106">Metodo INapSoHProcessor:: GetNumberOfAttributes</span><span class="sxs-lookup"><span data-stu-id="d573c-106">INapSoHProcessor::GetNumberOfAttributes method</span></span>

> [!Note]  
> <span data-ttu-id="d573c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="d573c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d573c-108">Il metodo **INapSoHProcessor:: GetNumberOfAttributes** Recupera il numero totale di attributi nel rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="d573c-108">The **INapSoHProcessor::GetNumberOfAttributes** method retrieves the total number of attributes in the SoH.</span></span>

## <a name="syntax"></a><span data-ttu-id="d573c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d573c-109">Syntax</span></span>


```C++
HRESULT GetNumberOfAttributes(
  [out] UINT16 *attributeCount
);
```



## <a name="parameters"></a><span data-ttu-id="d573c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="d573c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d573c-111">*attributeCount* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d573c-111">*attributeCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d573c-112">Puntatore al conteggio degli attributi restituiti.</span><span class="sxs-lookup"><span data-stu-id="d573c-112">A pointer to the returned attribute count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d573c-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d573c-113">Return value</span></span>

<span data-ttu-id="d573c-114">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="d573c-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d573c-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d573c-115">Return code</span></span>                                                                                     | <span data-ttu-id="d573c-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d573c-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d573c-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d573c-118">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="d573c-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d573c-119"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d573c-120">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="d573c-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d573c-121"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d573c-122">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="d573c-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d573c-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d573c-123">Requirements</span></span>



| <span data-ttu-id="d573c-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="d573c-124">Requirement</span></span> | <span data-ttu-id="d573c-125">Valore</span><span class="sxs-lookup"><span data-stu-id="d573c-125">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d573c-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d573c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="d573c-127">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d573c-127">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d573c-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d573c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="d573c-129">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d573c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d573c-130">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d573c-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="d573c-131"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-131"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="d573c-132">IDL</span><span class="sxs-lookup"><span data-stu-id="d573c-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d573c-133"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-133"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="d573c-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d573c-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d573c-135"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d573c-135"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="d573c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d573c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d573c-137">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="d573c-137">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





