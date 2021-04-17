---
description: Il metodo set imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.
ms.assetid: 78f506dc-7fb4-446d-863e-cffee9da5280
title: 'Metodo IKsPropertySet:: set (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Set
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: b233cea7e131919d94b00afeb5a6e2ea3703c738
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401201"
---
# <a name="ikspropertysetset-method"></a><span data-ttu-id="06fe7-103">Metodo IKsPropertySet:: set</span><span class="sxs-lookup"><span data-stu-id="06fe7-103">IKsPropertySet::Set method</span></span>

<span data-ttu-id="06fe7-104">Il `Set` metodo imposta una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06fe7-104">The `Set` method sets a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="06fe7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="06fe7-105">Syntax</span></span>


```C++
HRESULT Set(
  [in] REFGUID guidPropSet,
  [in] DWORD   dwPropID,
  [in] LPVOID  pInstanceData,
  [in] DWORD   cbInstanceData,
  [in] LPVOID  pPropData,
  [in] DWORD   cbPropData
);
```



## <a name="parameters"></a><span data-ttu-id="06fe7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="06fe7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06fe7-107">*guidPropSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-108">GUID del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06fe7-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="06fe7-109">*dwPropID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-110">Identificatore della proprietà all'interno del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="06fe7-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="06fe7-111">*pInstanceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-112">Puntatore a un buffer che contiene i dati dell'istanza per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="06fe7-112">Pointer to a buffer that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="06fe7-113">*cbInstanceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-114">Dimensioni del buffer *pInstanceData* in byte.</span><span class="sxs-lookup"><span data-stu-id="06fe7-114">Size of the *pInstanceData* buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="06fe7-115">*pPropData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-115">*pPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-116">Puntatore a un buffer che contiene il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="06fe7-116">Pointer to a buffer that contains the value of the property.</span></span>

</dd> <dt>

<span data-ttu-id="06fe7-117">*cbPropData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06fe7-118">Sise del buffer *pPropData* , in byte.</span><span class="sxs-lookup"><span data-stu-id="06fe7-118">Sise of the *pPropData* buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06fe7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="06fe7-119">Return value</span></span>

<span data-ttu-id="06fe7-120">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="06fe7-120">Returns an **HRESULT** value.</span></span> <span data-ttu-id="06fe7-121">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="06fe7-121">Possible values include the following.</span></span>



| <span data-ttu-id="06fe7-122">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="06fe7-122">Return code</span></span>                                                                                              | <span data-ttu-id="06fe7-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06fe7-123">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="06fe7-124"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="06fe7-124"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="06fe7-125">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="06fe7-125">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="06fe7-126"><dt>**\_Set Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="06fe7-126"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="06fe7-127">Il set di proprietà non è supportato.</span><span class="sxs-lookup"><span data-stu-id="06fe7-127">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="06fe7-128"><dt>**\_ID Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="06fe7-128"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="06fe7-129">ID di proprietà non supportato per il set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="06fe7-129">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="06fe7-130">Commenti</span><span class="sxs-lookup"><span data-stu-id="06fe7-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="06fe7-131">Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome.</span><span class="sxs-lookup"><span data-stu-id="06fe7-131">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="06fe7-132">Le due interfacce non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="06fe7-132">The two interfaces are not compatible.</span></span> <span data-ttu-id="06fe7-133">L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="06fe7-133">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="06fe7-134">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="06fe7-134">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="06fe7-135">Requisiti</span><span class="sxs-lookup"><span data-stu-id="06fe7-135">Requirements</span></span>



| <span data-ttu-id="06fe7-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="06fe7-136">Requirement</span></span> | <span data-ttu-id="06fe7-137">Valore</span><span class="sxs-lookup"><span data-stu-id="06fe7-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06fe7-138">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fe7-138">Minimum supported client</span></span><br/> | <span data-ttu-id="06fe7-139">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="06fe7-140">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="06fe7-140">Minimum supported server</span></span><br/> | <span data-ttu-id="06fe7-141">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="06fe7-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="06fe7-142">Intestazione</span><span class="sxs-lookup"><span data-stu-id="06fe7-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="06fe7-143"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="06fe7-143"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="06fe7-144">Libreria</span><span class="sxs-lookup"><span data-stu-id="06fe7-144">Library</span></span><br/>                  | <dl> <span data-ttu-id="06fe7-145"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06fe7-145"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06fe7-146">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="06fe7-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06fe7-147">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="06fe7-147">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="06fe7-148">**Interfaccia IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="06fe7-148">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="06fe7-149">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="06fe7-149">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




