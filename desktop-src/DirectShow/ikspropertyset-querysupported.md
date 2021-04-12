---
description: Il metodo QuerySupported determina se un oggetto supporta un set di proprietà specificato.
ms.assetid: eda0325c-dba4-4d9f-81e2-7fd67d5b9873
title: 'Metodo IKsPropertySet:: QuerySupported (KS. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.QuerySupported
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: a13c8523d45278ad403ee08d0822fb853b301520
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225397"
---
# <a name="ikspropertysetquerysupported-method"></a><span data-ttu-id="6401c-103">Metodo IKsPropertySet:: QuerySupported</span><span class="sxs-lookup"><span data-stu-id="6401c-103">IKsPropertySet::QuerySupported method</span></span>

<span data-ttu-id="6401c-104">Il `QuerySupported` metodo determina se un oggetto supporta un set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="6401c-104">The `QuerySupported` method determines whether an object supports a specified property set.</span></span>

## <a name="syntax"></a><span data-ttu-id="6401c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6401c-105">Syntax</span></span>


```C++
HRESULT QuerySupported(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [out] DWORD   *pTypeSupport
);
```



## <a name="parameters"></a><span data-ttu-id="6401c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6401c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6401c-107">*guidPropSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6401c-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6401c-108">GUID del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="6401c-108">Property set GUID.</span></span>

</dd> <dt>

<span data-ttu-id="6401c-109">*dwPropID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6401c-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6401c-110">Identificatore della proprietà all'interno del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="6401c-110">Identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="6401c-111">*pTypeSupport* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6401c-111">*pTypeSupport* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6401c-112">Puntatore a un valore in cui archiviare i flag che indicano il supporto fornito dal driver.</span><span class="sxs-lookup"><span data-stu-id="6401c-112">Pointer to a value in which to store flags indicating the support provided by the driver.</span></span> <span data-ttu-id="6401c-113">I flag supportati sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="6401c-113">Supported flags include the following.</span></span>



| <span data-ttu-id="6401c-114">Valore</span><span class="sxs-lookup"><span data-stu-id="6401c-114">Value</span></span>                    | <span data-ttu-id="6401c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6401c-115">Description</span></span>                                                                                            |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6401c-116">KSPROPERTY \_ supporto \_ Get</span><span class="sxs-lookup"><span data-stu-id="6401c-116">KSPROPERTY\_SUPPORT\_GET</span></span> | <span data-ttu-id="6401c-117">È possibile recuperare la proprietà chiamando il metodo [**IKsPropertySet:: Get**](ikspropertyset-get.md) .</span><span class="sxs-lookup"><span data-stu-id="6401c-117">You can retrieve the property by calling the [**IKsPropertySet::Get**](ikspropertyset-get.md) method.</span></span> |
| <span data-ttu-id="6401c-118">\_set di supporto KSPROPERTY \_</span><span class="sxs-lookup"><span data-stu-id="6401c-118">KSPROPERTY\_SUPPORT\_SET</span></span> | <span data-ttu-id="6401c-119">È possibile modificare la proprietà chiamando [**IKsPropertySet:: set**](ikspropertyset-set.md).</span><span class="sxs-lookup"><span data-stu-id="6401c-119">You can change the property by calling [**IKsPropertySet::Set**](ikspropertyset-set.md).</span></span>              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6401c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6401c-120">Return value</span></span>

<span data-ttu-id="6401c-121">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6401c-121">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6401c-122">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="6401c-122">Possible values include the following.</span></span>



| <span data-ttu-id="6401c-123">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="6401c-123">Return code</span></span>                                                                                              | <span data-ttu-id="6401c-124">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6401c-124">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6401c-125"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-125"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="6401c-126">Il set di proprietà e la combinazione di ID proprietà specificati sono supportati.</span><span class="sxs-lookup"><span data-stu-id="6401c-126">The specified property set and property ID combination is supported.</span></span><br/> |
| <dl> <span data-ttu-id="6401c-127"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-127"><dt>**E\_NOTIMPL**</dt></span></span> </dl>                | <span data-ttu-id="6401c-128">Il set di proprietà non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6401c-128">Property set is not supported.</span></span><br/>                                       |
| <dl> <span data-ttu-id="6401c-129"><dt>**\_ID Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-129"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="6401c-130">ID di proprietà non supportato per il set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="6401c-130">Property ID is not supported for the specified property set.</span></span><br/>         |
| <dl> <span data-ttu-id="6401c-131"><dt>**\_Set Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-131"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="6401c-132">Il set di proprietà non è supportato.</span><span class="sxs-lookup"><span data-stu-id="6401c-132">Property set is not supported.</span></span><br/>                                       |



 

## <a name="remarks"></a><span data-ttu-id="6401c-133">Commenti</span><span class="sxs-lookup"><span data-stu-id="6401c-133">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6401c-134">Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome.</span><span class="sxs-lookup"><span data-stu-id="6401c-134">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="6401c-135">Le due interfacce non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="6401c-135">The two interfaces are not compatible.</span></span> <span data-ttu-id="6401c-136">L'interfaccia **IKsControl** , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="6401c-136">The **IKsControl** interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="6401c-137">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="6401c-137">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="6401c-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6401c-138">Requirements</span></span>



| <span data-ttu-id="6401c-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="6401c-139">Requirement</span></span> | <span data-ttu-id="6401c-140">Valore</span><span class="sxs-lookup"><span data-stu-id="6401c-140">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6401c-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6401c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="6401c-142">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6401c-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                       |
| <span data-ttu-id="6401c-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6401c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="6401c-144">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6401c-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="6401c-145">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6401c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="6401c-146"><dt>KS. h; </dt> <dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-146"><dt>Ks.h; </dt> <dt>Ksproxy.h</dt></span></span> </dl> |
| <span data-ttu-id="6401c-147">Libreria</span><span class="sxs-lookup"><span data-stu-id="6401c-147">Library</span></span><br/>                  | <dl> <span data-ttu-id="6401c-148"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6401c-148"><dt>Strmiids.lib</dt></span></span> </dl>                                                          |



## <a name="see-also"></a><span data-ttu-id="6401c-149">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6401c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6401c-150">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="6401c-150">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="6401c-151">**Interfaccia IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="6401c-151">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="6401c-152">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="6401c-152">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




