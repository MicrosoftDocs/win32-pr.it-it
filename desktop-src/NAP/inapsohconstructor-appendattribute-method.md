---
title: Metodo INapSoHConstructor AppendAttribute (NapProtocol. h)
description: Aggiunge un TLV alla fine del buffer del rapporto di integrità.
ms.assetid: 5706ceaa-757f-49d2-90e0-011415853875
keywords:
- NAP Metodo AppendAttribute
- Metodo AppendAttribute NAP, interfaccia INapSoHConstructor
- Interfaccia INapSoHConstructor NAP, Metodo AppendAttribute
topic_type:
- apiref
api_name:
- INapSoHConstructor.AppendAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc10fad9c775d324822700b77afed4e65a798db6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517709"
---
# <a name="inapsohconstructorappendattribute-method"></a><span data-ttu-id="ffb8c-106">Metodo INapSoHConstructor:: AppendAttribute</span><span class="sxs-lookup"><span data-stu-id="ffb8c-106">INapSoHConstructor::AppendAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="ffb8c-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ffb8c-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ffb8c-108">Il metodo **INapSoHConstructor:: AppendAttribute** aggiunge un TLV alla fine del buffer del rapporto di integrità.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-108">The **INapSoHConstructor::AppendAttribute** method adds a TLV to the end of the SoH buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffb8c-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffb8c-109">Syntax</span></span>


```C++
HRESULT AppendAttribute(
  [in]       SoHAttributeType  type,
  [in] const SoHAttributeValue *value
);
```



## <a name="parameters"></a><span data-ttu-id="ffb8c-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffb8c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffb8c-111">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ffb8c-111">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8c-112">Enumerazione [**SoHAttributeType**](sohattributetype-enum.md) che indica il tipo di attributo del nuovo TLV.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-112">A [**SoHAttributeType**](sohattributetype-enum.md) enumeration that indicates the attribute type of the new TLV.</span></span>

</dd> <dt>

<span data-ttu-id="ffb8c-113">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ffb8c-113">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffb8c-114">Puntatore a una struttura [**SoHAttributeValue**](sohattributevalue-union.md) contenente il valore per il nuovo TLV.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-114">A pointer to an [**SoHAttributeValue**](sohattributevalue-union.md) structure that contains the value for the new TLV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffb8c-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffb8c-115">Return value</span></span>

<span data-ttu-id="ffb8c-116">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ffb8c-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ffb8c-117">Return code</span></span>                                                                                     | <span data-ttu-id="ffb8c-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ffb8c-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ffb8c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ffb8c-120">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ffb8c-121"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ffb8c-122">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ffb8c-123"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ffb8c-124">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ffb8c-125">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffb8c-125">Remarks</span></span>

<span data-ttu-id="ffb8c-126">Non è necessario aggiungere [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV con questa funzione.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-126">The [**sohAttributeTypeSystemHealthId**](sohattributetype-enum.md) TLV must not be added using this function.</span></span> <span data-ttu-id="ffb8c-127">Viene aggiunto come primo TLV da [**INapSoHConstructor:: Initialize**](inapsohconstructor-initialize-method.md) ai pacchetti SOH appena costruiti.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-127">It is added as the first TLV by [**INapSoHConstructor::Initialize**](inapsohconstructor-initialize-method.md) to newly constructed SOH packets.</span></span>

<span data-ttu-id="ffb8c-128">Quando si aggiunge un attributo che verrà utilizzato dal sistema NAP, non deve essere crittografato o modificato in alcun modo.</span><span class="sxs-lookup"><span data-stu-id="ffb8c-128">When appending an attribute which will be consumed by the Nap System, it should not be encrypted or modified in any manner.</span></span> <span data-ttu-id="ffb8c-129">Se il HealthEntity richiede il controllo di crittografia/integrità (MACs) delle informazioni private, deve essere incluso solo nell'attributo [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) .</span><span class="sxs-lookup"><span data-stu-id="ffb8c-129">If the HealthEntity requires encryption/integrity checking (MACs) of private information, it should be included only in the [**sohAttributeTypeVendorSpecific**](sohattributetype-enum.md) attribute.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffb8c-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffb8c-130">Requirements</span></span>



| <span data-ttu-id="ffb8c-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffb8c-131">Requirement</span></span> | <span data-ttu-id="ffb8c-132">Valore</span><span class="sxs-lookup"><span data-stu-id="ffb8c-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ffb8c-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb8c-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ffb8c-134">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ffb8c-134">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ffb8c-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ffb8c-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ffb8c-136">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ffb8c-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ffb8c-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffb8c-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffb8c-138"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-138"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffb8c-139">IDL</span><span class="sxs-lookup"><span data-stu-id="ffb8c-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ffb8c-140"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-140"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="ffb8c-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ffb8c-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ffb8c-142"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffb8c-142"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ffb8c-143">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffb8c-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffb8c-144">**INapSoHConstructor**</span><span class="sxs-lookup"><span data-stu-id="ffb8c-144">**INapSoHConstructor**</span></span>](inapsohconstructor.md)
</dt> </dl>

 

 





