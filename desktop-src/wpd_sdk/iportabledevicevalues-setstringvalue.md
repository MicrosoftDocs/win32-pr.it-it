---
description: Il metodo SetStringValue aggiunge un nuovo valore stringa (digitare VT \_ LPWSTR) o sovrascrive uno esistente.
ms.assetid: a6eba2b9-de18-431e-874e-af68695e8d3f
title: 'Metodo IPortableDeviceValues:: SetStringValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 163b5cd81ce8da64fc6d9f4304de5783b248522f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326855"
---
# <a name="iportabledevicevaluessetstringvalue-method"></a><span data-ttu-id="ad662-103">Metodo IPortableDeviceValues:: SetStringValue</span><span class="sxs-lookup"><span data-stu-id="ad662-103">IPortableDeviceValues::SetStringValue method</span></span>

<span data-ttu-id="ad662-104">Il metodo **SetStringValue** aggiunge un nuovo valore stringa (digitare VT \_ LPWSTR) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="ad662-104">The **SetStringValue** method adds a new string value (type VT\_LPWSTR) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad662-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad662-105">Syntax</span></span>


```C++
HRESULT SetStringValue(
  [in] REFPROPERTYKEY key,
  [in] LPCWSTR        Value
);
```



## <a name="parameters"></a><span data-ttu-id="ad662-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ad662-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad662-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ad662-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad662-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="ad662-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="ad662-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="ad662-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad662-110">Oggetto **LPCWSTR** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="ad662-110">A **LPCWSTR** that specifies the new value.</span></span> <span data-ttu-id="ad662-111">La stringa viene copiata, quindi il chiamante può rilasciare la memoria allocata per questo valore dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="ad662-111">The string is copied, so the caller can release the memory allocated for this value after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad662-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ad662-112">Return value</span></span>

<span data-ttu-id="ad662-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ad662-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ad662-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ad662-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ad662-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ad662-115">Return code</span></span>                                                                          | <span data-ttu-id="ad662-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ad662-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ad662-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ad662-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ad662-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ad662-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ad662-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="ad662-119">Remarks</span></span>

<span data-ttu-id="ad662-120">Eventuali memorie chiave esistenti verranno rilasciate in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="ad662-120">Any existing key memory will be released appropriately.</span></span>

## <a name="examples"></a><span data-ttu-id="ad662-121">Esempio</span><span class="sxs-lookup"><span data-stu-id="ad662-121">Examples</span></span>

<span data-ttu-id="ad662-122">Per un esempio di come usare questo metodo, vedere [specifica delle informazioni client](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="ad662-122">For an example of how to use this method, see [Specifying Client Information](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ad662-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad662-123">Requirements</span></span>



| <span data-ttu-id="ad662-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad662-124">Requirement</span></span> | <span data-ttu-id="ad662-125">Valore</span><span class="sxs-lookup"><span data-stu-id="ad662-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad662-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad662-126">Header</span></span><br/>  | <dl> <span data-ttu-id="ad662-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad662-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad662-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="ad662-128">Library</span></span><br/> | <dl> <span data-ttu-id="ad662-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad662-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad662-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad662-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad662-131">Aggiunta di una risorsa a un oggetto</span><span class="sxs-lookup"><span data-stu-id="ad662-131">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="ad662-132">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="ad662-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="ad662-133">**IPortableDeviceValues:: GetStringValue**</span><span class="sxs-lookup"><span data-stu-id="ad662-133">**IPortableDeviceValues::GetStringValue**</span></span>](iportabledevicevalues-getstringvalue.md)
</dt> <dt>

[<span data-ttu-id="ad662-134">Impostazione delle proprietà per un singolo oggetto</span><span class="sxs-lookup"><span data-stu-id="ad662-134">Setting Properties for a Single Object</span></span>](setting-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="ad662-135">Impostazione delle proprietà per più oggetti</span><span class="sxs-lookup"><span data-stu-id="ad662-135">Setting Properties for Multiple Objects</span></span>](setting-properties-for-multiple-objects.md)
</dt> <dt>

[<span data-ttu-id="ad662-136">Specifica delle informazioni client</span><span class="sxs-lookup"><span data-stu-id="ad662-136">Specifying Client Information</span></span>](specifying-client-information.md)
</dt> <dt>

[<span data-ttu-id="ad662-137">Scrittura di proprietà di contenuto-oggetto</span><span class="sxs-lookup"><span data-stu-id="ad662-137">Writing Content-Object Properties</span></span>](writing-content-object-properties.md)
</dt> </dl>

 

 




