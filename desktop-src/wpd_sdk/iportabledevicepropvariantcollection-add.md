---
description: 'Metodo IPortableDevicePropVariantCollection::Add: il metodo Add aggiunge un elemento alla raccolta.'
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: Metodo IPortableDevicePropVariantCollection::Add (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.Add
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7aed732cb92ea7e0f2fb3c2ebdd615f643bc3107
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112459"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="5c4eb-103">Metodo IPortableDevicePropVariantCollection::Add</span><span class="sxs-lookup"><span data-stu-id="5c4eb-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="5c4eb-104">Il **metodo Add** aggiunge un elemento alla raccolta .</span><span class="sxs-lookup"><span data-stu-id="5c4eb-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c4eb-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5c4eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c4eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4eb-107">*pValue* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="5c4eb-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4eb-108">Puntatore a un **nuovo oggetto PROPVARIANT** da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="5c4eb-109">Questo metodo copia **PROPVARIANT** nella raccolta, pertanto è necessario rilasciare la copia locale della variabile chiamando **PropVariantClear** dopo aver chiamato questo metodo.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4eb-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c4eb-110">Return value</span></span>

<span data-ttu-id="5c4eb-111">Il metodo restituisce un **HRESULT.**</span><span class="sxs-lookup"><span data-stu-id="5c4eb-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c4eb-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c4eb-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c4eb-113">Return code</span></span>                                                                          | <span data-ttu-id="5c4eb-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c4eb-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5c4eb-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c4eb-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5c4eb-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5c4eb-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c4eb-117">Remarks</span></span>

<span data-ttu-id="5c4eb-118">Quando VARTYPE per *pValue* è VT VECTOR o \_ VT UI1, l'impostazione e il recupero di un buffer NULL o di dimensioni \_ zero non sono supportati. </span><span class="sxs-lookup"><span data-stu-id="5c4eb-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="5c4eb-119">Ad esempio, né pValue.caub.pElems = **NULL** né pValue.caub.cElems = 0 sono consentiti.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="5c4eb-120">Se un chiamante tenta di aggiungere un elemento di un tipo VARTYPE diverso contenuto nella raccolta e il valore PROPVARIANT non può essere modificato automaticamente da questa interfaccia, questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="5c4eb-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="5c4eb-121">Per modificare manualmente il tipo di raccolta, chiamare [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="5c4eb-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5c4eb-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c4eb-122">Examples</span></span>

<span data-ttu-id="5c4eb-123">Per un esempio di come usare questo metodo, vedere Recupero di un identificatore di [oggetto da un identificatore univoco persistente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="5c4eb-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4eb-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c4eb-124">Requirements</span></span>



| <span data-ttu-id="5c4eb-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c4eb-125">Requirement</span></span> | <span data-ttu-id="5c4eb-126">Valore</span><span class="sxs-lookup"><span data-stu-id="5c4eb-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4eb-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c4eb-127">Header</span></span><br/>  | <dl> <span data-ttu-id="5c4eb-128"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="5c4eb-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c4eb-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c4eb-129">Library</span></span><br/> | <dl> <span data-ttu-id="5c4eb-130"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c4eb-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c4eb-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c4eb-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4eb-132">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="5c4eb-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="5c4eb-133">Spostamento del contenuto nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="5c4eb-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="5c4eb-134">Recupero di un identificatore di oggetto da un identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="5c4eb-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




