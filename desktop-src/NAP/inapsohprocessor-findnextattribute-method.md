---
title: Metodo INapSoHProcessor FindNextAttribute (NapProtocol. h)
description: Trova il percorso (indice) dell'attributo successivo del tipo indicato da SoHAttributeType.
ms.assetid: 0ff94a32-ece8-4a89-9ee9-93c5e14dfb6c
keywords:
- NAP metodo FindNextAttribute
- Metodo FindNextAttribute NAP, interfaccia INapSoHProcessor
- Interfaccia INapSoHProcessor NAP, metodo FindNextAttribute
topic_type:
- apiref
api_name:
- INapSoHProcessor.FindNextAttribute
api_location:
- qutil.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1a270e36f8254ed5dbfcd9776cf013f9d10d4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740223"
---
# <a name="inapsohprocessorfindnextattribute-method"></a><span data-ttu-id="ba391-106">Metodo INapSoHProcessor:: FindNextAttribute</span><span class="sxs-lookup"><span data-stu-id="ba391-106">INapSoHProcessor::FindNextAttribute method</span></span>

> [!Note]  
> <span data-ttu-id="ba391-107">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="ba391-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ba391-108">Il metodo **INapSoHProcessor:: FindNextAttribute** trova il percorso (indice) dell'attributo successivo del tipo indicato da *SoHAttributeType*.</span><span class="sxs-lookup"><span data-stu-id="ba391-108">The **INapSoHProcessor::FindNextAttribute** method finds the location (index) of the next attribute of the type indicated by *SoHAttributeType*.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba391-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ba391-109">Syntax</span></span>


```C++
HRESULT FindNextAttribute(
  [in]  UINT16           fromLocation,
  [in]  SoHAttributeType type,
  [out] UINT16           *attributeLocation
);
```



## <a name="parameters"></a><span data-ttu-id="ba391-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ba391-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba391-111">*fromLocation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ba391-111">*fromLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba391-112">Posizione iniziale (indice) nel pacchetto del rapporto di integrità (SoH) per iniziare la ricerca degli attributi.</span><span class="sxs-lookup"><span data-stu-id="ba391-112">The starting location (index) in the Statement of Health (SoH) packet to begin the attribute search.</span></span> <span data-ttu-id="ba391-113">Questo valore deve essere compreso nell'intervallo da 0 a (**numAttrib** -1) in cui **numAttrib** viene recuperato utilizzando [**INapSoHProcessor:: GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span><span class="sxs-lookup"><span data-stu-id="ba391-113">This value must be in the range of 0 to (**numAttrib** - 1) where **numAttrib** is retrieved using [**INapSoHProcessor::GetNumberOfAttributes**](inapsohprocessor-getnumberofattributes-method.md).</span></span>

> [!Note]  
> <span data-ttu-id="ba391-114">Il pacchetto di rapporto di integrità utilizza gli indici degli attributi in base 0.</span><span class="sxs-lookup"><span data-stu-id="ba391-114">The SoH packet uses 0-based attribute indices.</span></span>

 

</dd> <dt>

<span data-ttu-id="ba391-115">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ba391-115">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba391-116">Struttura [**SoHAttributeType**](sohattributetype-enum.md) che contiene il tipo di attributo da individuare.</span><span class="sxs-lookup"><span data-stu-id="ba391-116">An [**SoHAttributeType**](sohattributetype-enum.md) structure that contains the attribute type to locate.</span></span>

</dd> <dt>

<span data-ttu-id="ba391-117">*attributeLocation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ba391-117">*attributeLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba391-118">Puntatore che contiene il percorso (indice) nel pacchetto SoH del primo attributo di tipo *SoHAttributeType* dall'indice *fromLocation*.</span><span class="sxs-lookup"><span data-stu-id="ba391-118">A pointer that contains the location (index) in the SoH packet of the first attribute of type *SoHAttributeType* from the index *fromLocation*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba391-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ba391-119">Return value</span></span>

<span data-ttu-id="ba391-120">È possibile che vengano restituiti anche altri codici di errore specifici di COM.</span><span class="sxs-lookup"><span data-stu-id="ba391-120">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ba391-121">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ba391-121">Return code</span></span>                                                                                            | <span data-ttu-id="ba391-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ba391-122">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ba391-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-123"><dt>**S\_OK** </dt></span></span> </dl>                  | <span data-ttu-id="ba391-124">Operazione riuscita.</span><span class="sxs-lookup"><span data-stu-id="ba391-124">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ba391-125"><dt>**E \_ ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-125"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>        | <span data-ttu-id="ba391-126">Errore delle autorizzazioni, accesso negato.</span><span class="sxs-lookup"><span data-stu-id="ba391-126">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ba391-127"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-127"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>         | <span data-ttu-id="ba391-128">Limite di risorse di sistema. Impossibile eseguire l'operazione.</span><span class="sxs-lookup"><span data-stu-id="ba391-128">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="ba391-129"><dt>**FILE di errore \_ \_ non \_ trovato**</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-129"><dt>**ERROR\_FILE\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="ba391-130">Attributo non trovato.</span><span class="sxs-lookup"><span data-stu-id="ba391-130">Attribute not found.</span></span><br/>                                    |



 

## <a name="remarks"></a><span data-ttu-id="ba391-131">Commenti</span><span class="sxs-lookup"><span data-stu-id="ba391-131">Remarks</span></span>

<span data-ttu-id="ba391-132">Il metodo **FindNextAttribute** cerca gli attributi di tipo *SoHAttributeType* dall'indice specificato da *fromLocation* e versioni successive fino a quando non viene trovata una corrispondenza.</span><span class="sxs-lookup"><span data-stu-id="ba391-132">The **FindNextAttribute** method searches for attributes of type *SoHAttributeType* from the index specified by *fromLocation* and higher until a match is found.</span></span> <span data-ttu-id="ba391-133">Se non viene trovata alcuna corrispondenza, viene restituito il **file di errore \_ \_ non \_ trovato** .</span><span class="sxs-lookup"><span data-stu-id="ba391-133">If no match is found, **ERROR\_FILE\_NOT\_FOUND** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba391-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ba391-134">Requirements</span></span>



| <span data-ttu-id="ba391-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba391-135">Requirement</span></span> | <span data-ttu-id="ba391-136">Valore</span><span class="sxs-lookup"><span data-stu-id="ba391-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba391-137">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba391-137">Minimum supported client</span></span><br/> | <span data-ttu-id="ba391-138">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba391-138">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ba391-139">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ba391-139">Minimum supported server</span></span><br/> | <span data-ttu-id="ba391-140">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba391-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="ba391-141">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ba391-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba391-142"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-142"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba391-143">IDL</span><span class="sxs-lookup"><span data-stu-id="ba391-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ba391-144"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-144"><dt>NapProtocol.idl</dt></span></span> </dl> |
| <span data-ttu-id="ba391-145">DLL</span><span class="sxs-lookup"><span data-stu-id="ba391-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba391-146"><dt>Qutil.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba391-146"><dt>Qutil.dll</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="ba391-147">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ba391-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba391-148">**INapSoHProcessor**</span><span class="sxs-lookup"><span data-stu-id="ba391-148">**INapSoHProcessor**</span></span>](inapsohprocessor.md)
</dt> </dl>

 

 





