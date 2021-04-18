---
description: Il metodo SetValue aggiunge un nuovo valore PROPVARIANT o ne sovrascrive uno esistente.
ms.assetid: 69630a21-79e9-4c96-8ed7-9a41ebb991cd
title: 'Metodo IPortableDeviceValues:: SetValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 4c2ba6c5b6f015e5961356ff8e246605bfeddd31
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326846"
---
# <a name="iportabledevicevaluessetvalue-method"></a><span data-ttu-id="3cb48-103">Metodo IPortableDeviceValues:: SetValue</span><span class="sxs-lookup"><span data-stu-id="3cb48-103">IPortableDeviceValues::SetValue method</span></span>

<span data-ttu-id="3cb48-104">Il **Metodo SetValue aggiunge** un nuovo valore **PROPVARIANT** o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="3cb48-104">The **SetValue** method adds a new **PROPVARIANT** value or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="3cb48-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3cb48-105">Syntax</span></span>


```C++
HRESULT SetValue(
  [in]       REFPROPERTYKEY key,
  [in] const PROPVARIANT    *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3cb48-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3cb48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3cb48-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3cb48-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb48-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="3cb48-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="3cb48-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3cb48-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3cb48-110">Oggetto **PROPVARIANT** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="3cb48-110">A **PROPVARIANT** that specifies the new value.</span></span> <span data-ttu-id="3cb48-111">L'SDK copia il valore, in modo che il chiamante possa rilasciare la variabile locale chiamando **PropVariantClear** dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="3cb48-111">The SDK copies the value, so the caller can release the local variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3cb48-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3cb48-112">Return value</span></span>

<span data-ttu-id="3cb48-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3cb48-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3cb48-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3cb48-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3cb48-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3cb48-115">Return code</span></span>                                                                          | <span data-ttu-id="3cb48-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3cb48-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3cb48-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3cb48-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3cb48-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3cb48-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3cb48-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="3cb48-119">Remarks</span></span>

<span data-ttu-id="3cb48-120">Quando VARTYPE per *pValue* è VT \_ vector o VT \_ Ui1, non è supportata l'impostazione di un buffer di dimensioni **null** o zero.</span><span class="sxs-lookup"><span data-stu-id="3cb48-120">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="3cb48-121">Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="3cb48-121">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="3cb48-122">Questo metodo può essere utilizzato per recuperare un valore di qualsiasi tipo dalla raccolta.</span><span class="sxs-lookup"><span data-stu-id="3cb48-122">This method can be used to retrieve a value of any type from the collection.</span></span> <span data-ttu-id="3cb48-123">Tuttavia, se si conosce il tipo di valore in anticipo, utilizzare uno dei metodi **set** specializzati di questa interfaccia per evitare il sovraccarico dell'utilizzo diretto dei valori PROPVARIANT.</span><span class="sxs-lookup"><span data-stu-id="3cb48-123">However, if you know the value type in advance, use one of the specialized **Set...** methods of this interface to avoid the overhead of working with PROPVARIANT values directly.</span></span>

<span data-ttu-id="3cb48-124">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="3cb48-124">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="3cb48-125">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="3cb48-125">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="3cb48-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3cb48-126">Requirements</span></span>



| <span data-ttu-id="3cb48-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3cb48-127">Requirement</span></span> | <span data-ttu-id="3cb48-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3cb48-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3cb48-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3cb48-129">Header</span></span><br/>  | <dl> <span data-ttu-id="3cb48-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3cb48-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3cb48-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="3cb48-131">Library</span></span><br/> | <dl> <span data-ttu-id="3cb48-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3cb48-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3cb48-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3cb48-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3cb48-134">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3cb48-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3cb48-135">**IPortableDeviceValues:: GetValue**</span><span class="sxs-lookup"><span data-stu-id="3cb48-135">**IPortableDeviceValues::GetValue**</span></span>](iportabledevicevalues-getvalue.md)
</dt> <dt>

[<span data-ttu-id="3cb48-136">**IPortableDeviceValues:: RemoveValue**</span><span class="sxs-lookup"><span data-stu-id="3cb48-136">**IPortableDeviceValues::RemoveValue**</span></span>](iportabledevicevalues-removevalue.md)
</dt> </dl>

 

 




