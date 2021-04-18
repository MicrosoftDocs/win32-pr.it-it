---
description: Il metodo GetValue recupera un valore PROPVARIANT specificato da una chiave.
ms.assetid: 927844f5-8f57-4596-ae0d-c67b8011ca87
title: 'Metodo IPortableDeviceValues:: GetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 6ab5ec24e67d5259eec86c6a33d32766a5426b38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325811"
---
# <a name="iportabledevicevaluesgetvalue-method"></a><span data-ttu-id="116aa-103">Metodo IPortableDeviceValues:: GetValue</span><span class="sxs-lookup"><span data-stu-id="116aa-103">IPortableDeviceValues::GetValue method</span></span>

<span data-ttu-id="116aa-104">Il metodo **GetValue** recupera un valore **PROPVARIANT** specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="116aa-104">The **GetValue** method retrieves a **PROPVARIANT** value specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="116aa-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="116aa-105">Syntax</span></span>


```C++
HRESULT GetValue(
  [in]  REFPROPERTYKEY key,
  [out] PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="116aa-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="116aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="116aa-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="116aa-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="116aa-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="116aa-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="116aa-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="116aa-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="116aa-110">Puntatore al valore **PROPVARIANT** recuperato.</span><span class="sxs-lookup"><span data-stu-id="116aa-110">Pointer to the retrieved **PROPVARIANT** value.</span></span> <span data-ttu-id="116aa-111">Il chiamante deve rilasciare la memoria chiamando **PropVariantClear** al termine di tale operazione.</span><span class="sxs-lookup"><span data-stu-id="116aa-111">The caller must release the memory by calling **PropVariantClear** when done with it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="116aa-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="116aa-112">Return value</span></span>

<span data-ttu-id="116aa-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="116aa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="116aa-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="116aa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="116aa-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="116aa-115">Return code</span></span>                                                                                                            | <span data-ttu-id="116aa-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="116aa-116">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="116aa-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="116aa-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="116aa-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="116aa-118">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="116aa-119"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="116aa-119"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="116aa-120">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="116aa-120">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="116aa-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="116aa-121">Remarks</span></span>

<span data-ttu-id="116aa-122">Quando VARTYPE for *pValue* è VT \_ vector o VT \_ Ui1, il recupero di un buffer di dimensioni **null** o zero non è supportato.</span><span class="sxs-lookup"><span data-stu-id="116aa-122">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="116aa-123">Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="116aa-123">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="116aa-124">Questo metodo può essere utilizzato per recuperare un valore di qualsiasi tipo dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="116aa-124">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="116aa-125">Tuttavia, se si conosce il tipo di valore in anticipo, utilizzare uno dei metodi di recupero specializzati di questa interfaccia per evitare il sovraccarico dell'utilizzo diretto dei valori PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="116aa-125">However, if you know the value type in advance, use one of the specialized retrieval methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="116aa-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="116aa-126">Requirements</span></span>



| <span data-ttu-id="116aa-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="116aa-127">Requirement</span></span> | <span data-ttu-id="116aa-128">Valore</span><span class="sxs-lookup"><span data-stu-id="116aa-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="116aa-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="116aa-129">Header</span></span><br/>  | <dl> <span data-ttu-id="116aa-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="116aa-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="116aa-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="116aa-131">Library</span></span><br/> | <dl> <span data-ttu-id="116aa-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="116aa-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="116aa-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="116aa-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="116aa-134">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="116aa-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="116aa-135">**IPortableDeviceValues:: RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="116aa-135">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> <dt>

[<span data-ttu-id="116aa-136">**IPortableDeviceValues:: SetValue**</span><span class="sxs-lookup"><span data-stu-id="116aa-136">**IPortableDeviceValues::SetValue**</span></span>](iportabledevicevalues-setvalue.md)
</dt> </dl>

 

 




