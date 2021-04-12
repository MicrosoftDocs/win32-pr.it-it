---
description: Il metodo Get recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.
ms.assetid: f39862db-0659-4533-8cee-aee2f778e085
title: 'Metodo IKsPropertySet:: Get (ksproxy. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPropertySet.Get
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 9c4461e8c5886d84bcf3b7faa6675b749bc0c37d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481764"
---
# <a name="ikspropertysetget-method"></a><span data-ttu-id="86120-103">Metodo IKsPropertySet:: Get</span><span class="sxs-lookup"><span data-stu-id="86120-103">IKsPropertySet::Get method</span></span>

<span data-ttu-id="86120-104">Il metodo **Get** recupera una proprietà identificata da un GUID del set di proprietà e da un ID di proprietà.</span><span class="sxs-lookup"><span data-stu-id="86120-104">The **Get** method retrieves a property identified by a property set GUID and a property ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="86120-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="86120-105">Syntax</span></span>


```C++
HRESULT Get(
  [in]  REFGUID guidPropSet,
  [in]  DWORD   dwPropID,
  [in]  LPVOID  pInstanceData,
  [in]  DWORD   cbInstanceData,
  [out] LPVOID  pPropData,
  [in]  DWORD   cbPropData,
  [out] DWORD   *pcbReturned
);
```



## <a name="parameters"></a><span data-ttu-id="86120-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="86120-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="86120-107">*guidPropSet* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86120-107">*guidPropSet* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-108">GUID del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="86120-108">The GUID of the property set .</span></span>

</dd> <dt>

<span data-ttu-id="86120-109">*dwPropID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86120-109">*dwPropID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-110">Identificatore della proprietà all'interno del set di proprietà.</span><span class="sxs-lookup"><span data-stu-id="86120-110">The identifier of the property within the property set.</span></span>

</dd> <dt>

<span data-ttu-id="86120-111">*pInstanceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86120-111">*pInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-112">Puntatore a una matrice di byte che contiene i dati dell'istanza per la proprietà.</span><span class="sxs-lookup"><span data-stu-id="86120-112">A pointer to an array of bytes that contains instance data for the property.</span></span>

</dd> <dt>

<span data-ttu-id="86120-113">*cbInstanceData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86120-113">*cbInstanceData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-114">Dimensioni in byte della matrice specificata in *pInstanceData*.</span><span class="sxs-lookup"><span data-stu-id="86120-114">The size of the array given in *pInstanceData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="86120-115">*pPropData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86120-115">*pPropData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-116">Puntatore a una matrice di byte che riceve i dati della proprietà.</span><span class="sxs-lookup"><span data-stu-id="86120-116">A pointer to an array of bytes that receives the property data.</span></span>

</dd> <dt>

<span data-ttu-id="86120-117">*cbPropData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="86120-117">*cbPropData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-118">Dimensioni in byte della matrice specificata in *pPropData*.</span><span class="sxs-lookup"><span data-stu-id="86120-118">The size of the array given in *pPropData*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="86120-119">*pcbReturned* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="86120-119">*pcbReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="86120-120">Riceve il numero di byte che il metodo copia nella matrice *pPropData* .</span><span class="sxs-lookup"><span data-stu-id="86120-120">Receives the number of bytes the method copies to the *pPropData* array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="86120-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="86120-121">Return value</span></span>

<span data-ttu-id="86120-122">Restituisce un valore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="86120-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="86120-123">Di seguito sono indicati alcuni valori possibili.</span><span class="sxs-lookup"><span data-stu-id="86120-123">Possible values include the following.</span></span>



| <span data-ttu-id="86120-124">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="86120-124">Return code</span></span>                                                                                              | <span data-ttu-id="86120-125">Descrizione</span><span class="sxs-lookup"><span data-stu-id="86120-125">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="86120-126"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="86120-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="86120-127">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="86120-127">Success.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="86120-128"><dt>**\_Set Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="86120-128"><dt>**E\_PROP\_SET\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="86120-129">Il set di proprietà non è supportato.</span><span class="sxs-lookup"><span data-stu-id="86120-129">The property set is not supported.</span></span><br/>                               |
| <dl> <span data-ttu-id="86120-130"><dt>**\_ID Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="86120-130"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl>  | <span data-ttu-id="86120-131">ID di proprietà non supportato per il set di proprietà specificato.</span><span class="sxs-lookup"><span data-stu-id="86120-131">The property ID is not supported for the specified property set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86120-132">Commenti</span><span class="sxs-lookup"><span data-stu-id="86120-132">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="86120-133">Nel file di intestazione DSOUND. h esiste un'altra interfaccia con questo nome.</span><span class="sxs-lookup"><span data-stu-id="86120-133">Another interface by this name exists in the dsound.h header file.</span></span> <span data-ttu-id="86120-134">Le due interfacce non sono compatibili.</span><span class="sxs-lookup"><span data-stu-id="86120-134">The two interfaces are not compatible.</span></span> <span data-ttu-id="86120-135">L'interfaccia [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) , documentata in DirectShow DDK, è ora l'interfaccia consigliata per passare i set di proprietà tra i driver WDM e i componenti in modalità utente.</span><span class="sxs-lookup"><span data-stu-id="86120-135">The [IKsControl](/windows-hardware/drivers/ddi/ksproxy/nn-ksproxy-ikscontrol) interface, documented in the DirectShow DDK, is now the recommended interface for passing property sets between WDM drivers and user mode components.</span></span>

 

<span data-ttu-id="86120-136">Per recuperare una proprietà, allocare un buffer che verrà compilato da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="86120-136">To retrieve a property, allocate a buffer which this method will then fill in.</span></span> <span data-ttu-id="86120-137">Per determinare le dimensioni del buffer necessarie, specificare **null** per *pPropData* e zero (0) per *cbPropData*.</span><span class="sxs-lookup"><span data-stu-id="86120-137">To determine the necessary buffer size, specify **NULL** for *pPropData* and zero (0) for *cbPropData*.</span></span> <span data-ttu-id="86120-138">Questo metodo restituisce le dimensioni del buffer necessarie in *pcbReturned*.</span><span class="sxs-lookup"><span data-stu-id="86120-138">This method returns the necessary buffer size in *pcbReturned*.</span></span>

<span data-ttu-id="86120-139">Prima di ksproxy. h, è necessario includere KS. h.</span><span class="sxs-lookup"><span data-stu-id="86120-139">You must include Ks.h before Ksproxy.h.</span></span>

## <a name="examples"></a><span data-ttu-id="86120-140">Esempio</span><span class="sxs-lookup"><span data-stu-id="86120-140">Examples</span></span>

<span data-ttu-id="86120-141">Nell'esempio seguente viene eseguita una query su un PIN per la relativa categoria pin, recuperando la proprietà di **\_ \_ categoria AMPROPERTY pin** .</span><span class="sxs-lookup"><span data-stu-id="86120-141">The following example queries a pin for its pin category, by retrieving the **AMPROPERTY\_PIN\_CATEGORY** property.</span></span> <span data-ttu-id="86120-142">(Vedere [impostare la proprietà pin](pin-property-set.md)).</span><span class="sxs-lookup"><span data-stu-id="86120-142">(See [Pin Property Set](pin-property-set.md).)</span></span>


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="86120-143">Requisiti</span><span class="sxs-lookup"><span data-stu-id="86120-143">Requirements</span></span>



| <span data-ttu-id="86120-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="86120-144">Requirement</span></span> | <span data-ttu-id="86120-145">Valore</span><span class="sxs-lookup"><span data-stu-id="86120-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="86120-146">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86120-146">Minimum supported client</span></span><br/> | <span data-ttu-id="86120-147">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86120-147">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="86120-148">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="86120-148">Minimum supported server</span></span><br/> | <span data-ttu-id="86120-149">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="86120-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="86120-150">Intestazione</span><span class="sxs-lookup"><span data-stu-id="86120-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="86120-151"><dt>Ksproxy. h</dt></span><span class="sxs-lookup"><span data-stu-id="86120-151"><dt>Ksproxy.h</dt></span></span> </dl>    |
| <span data-ttu-id="86120-152">Libreria</span><span class="sxs-lookup"><span data-stu-id="86120-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="86120-153"><dt>Strmiids. lib</dt></span><span class="sxs-lookup"><span data-stu-id="86120-153"><dt>Strmiids.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="86120-154">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="86120-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86120-155">Codici di errore e di esito positivo</span><span class="sxs-lookup"><span data-stu-id="86120-155">Error and Success Codes</span></span>](error-and-success-codes.md)
</dt> <dt>

[<span data-ttu-id="86120-156">**Interfaccia IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="86120-156">**IKsPropertySet Interface**</span></span>](ikspropertyset.md)
</dt> <dt>

[<span data-ttu-id="86120-157">Set di proprietà</span><span class="sxs-lookup"><span data-stu-id="86120-157">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 
