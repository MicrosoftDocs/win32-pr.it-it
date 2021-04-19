---
description: Il metodo Add aggiunge una chiave di proprietà alla raccolta.
ms.assetid: 640ef1c4-2843-48dd-a30a-9a2ef9de35b9
title: 'Metodo IPortableDeviceKeyCollection:: Add (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e43fea25a08969b2ae8169884d51ddc46f8c7136
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332119"
---
# <a name="iportabledevicekeycollectionadd-method"></a><span data-ttu-id="d4dbc-103">Metodo IPortableDeviceKeyCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="d4dbc-103">IPortableDeviceKeyCollection::Add method</span></span>

<span data-ttu-id="d4dbc-104">Il metodo **Add** aggiunge una chiave di proprietà alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-104">The **Add** method adds a property key to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4dbc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d4dbc-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] REFPROPERTYKEY Key
);
```



## <a name="parameters"></a><span data-ttu-id="d4dbc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d4dbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4dbc-107">*Chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d4dbc-107">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4dbc-108">Oggetto **REFPROPERTYKEY** da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-108">A **REFPROPERTYKEY** to add to the collection.</span></span> <span data-ttu-id="d4dbc-109">Questo metodo copia la chiave nella raccolta, in modo che sia possibile rilasciare la variabile locale dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-109">This method copies the key to the collection, so you can release the local variable after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4dbc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d4dbc-110">Return value</span></span>

<span data-ttu-id="d4dbc-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4dbc-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4dbc-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d4dbc-113">Return code</span></span>                                                                                   | <span data-ttu-id="d4dbc-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4dbc-114">Description</span></span>                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d4dbc-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d4dbc-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="d4dbc-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-116">The method succeeded.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="d4dbc-117"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="d4dbc-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d4dbc-118">La memoria disponibile non è sufficiente per aggiungere la chiave alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="d4dbc-118">There is not enough memory available to add the key to the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="d4dbc-119">Esempio</span><span class="sxs-lookup"><span data-stu-id="d4dbc-119">Examples</span></span>

<span data-ttu-id="d4dbc-120">Per un esempio di come usare questo metodo, vedere [recupero delle proprietà per un singolo oggetto](retrieving-properties-for-a-single-object.md).</span><span class="sxs-lookup"><span data-stu-id="d4dbc-120">For an example of how to use this method, see [Retrieving Properties for a Single Object](retrieving-properties-for-a-single-object.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4dbc-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d4dbc-121">Requirements</span></span>



| <span data-ttu-id="d4dbc-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4dbc-122">Requirement</span></span> | <span data-ttu-id="d4dbc-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d4dbc-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4dbc-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d4dbc-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d4dbc-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4dbc-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d4dbc-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d4dbc-126">Library</span></span><br/> | <dl> <span data-ttu-id="d4dbc-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d4dbc-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4dbc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d4dbc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4dbc-129">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="d4dbc-129">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> <dt>

[<span data-ttu-id="d4dbc-130">Recupero proprietà contenuto-oggetto</span><span class="sxs-lookup"><span data-stu-id="d4dbc-130">Retrieving Content-Object Properties</span></span>](retrieving-content-object-properties.md)
</dt> <dt>

[<span data-ttu-id="d4dbc-131">Recupero di proprietà per un singolo oggetto</span><span class="sxs-lookup"><span data-stu-id="d4dbc-131">Retrieving Properties for a Single Object</span></span>](retrieving-properties-for-a-single-object.md)
</dt> <dt>

[<span data-ttu-id="d4dbc-132">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="d4dbc-132">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




