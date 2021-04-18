---
description: Il metodo Add aggiunge un elemento alla raccolta.
ms.assetid: e9e8975f-f9b8-4940-b967-020cf3812582
title: 'Metodo IPortableDevicePropVariantCollection:: Add (PortableDeviceTypes. h)'
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
ms.openlocfilehash: d9d5b4ee664d2fbbcc78550b1af5a48874d153d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329893"
---
# <a name="iportabledevicepropvariantcollectionadd-method"></a><span data-ttu-id="50347-103">Metodo IPortableDevicePropVariantCollection:: Add</span><span class="sxs-lookup"><span data-stu-id="50347-103">IPortableDevicePropVariantCollection::Add method</span></span>

<span data-ttu-id="50347-104">Il metodo **Add** aggiunge un elemento alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="50347-104">The **Add** method adds an item to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="50347-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="50347-105">Syntax</span></span>


```C++
HRESULT Add(
  [in] const PROPVARIANT *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="50347-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="50347-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="50347-107">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="50347-107">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="50347-108">Puntatore a un nuovo oggetto **PROPVARIANT** da aggiungere alla raccolta.</span><span class="sxs-lookup"><span data-stu-id="50347-108">Pointer to a new **PROPVARIANT** object to add to the collection.</span></span> <span data-ttu-id="50347-109">Questo metodo copia **PROPVARIANT** nella raccolta, quindi è necessario rilasciare la copia locale della variabile chiamando **PropVariantClear** dopo la chiamata a questo metodo.</span><span class="sxs-lookup"><span data-stu-id="50347-109">This method copies the **PROPVARIANT** to the collection, so you should release your local copy of the variable by calling **PropVariantClear** after calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="50347-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="50347-110">Return value</span></span>

<span data-ttu-id="50347-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="50347-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="50347-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="50347-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="50347-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="50347-113">Return code</span></span>                                                                          | <span data-ttu-id="50347-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50347-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="50347-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="50347-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="50347-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="50347-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="50347-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="50347-117">Remarks</span></span>

<span data-ttu-id="50347-118">Quando VARTYPE for *pValue* è VT \_ vector o VT \_ Ui1, non è supportata l'impostazione e il recupero di un buffer di dimensioni **null** o zero.</span><span class="sxs-lookup"><span data-stu-id="50347-118">When the VARTYPE for *pValue* is VT\_VECTOR or VT\_UI1, setting and retrieving a **NULL** or zero-sized buffer is not supported.</span></span> <span data-ttu-id="50347-119">Ad esempio, non sono consentiti né pValue. Campo CAUB. pElems = **null** né pValue. Campo CAUB. cElems = 0.</span><span class="sxs-lookup"><span data-stu-id="50347-119">For example, neither pValue.caub.pElems = **NULL** nor pValue.caub.cElems = 0 are allowed.</span></span>

<span data-ttu-id="50347-120">Se un chiamante tenta di aggiungere un elemento di un VARTYPE diverso contenuto nella raccolta e il valore PROPVARIANT non può essere modificato automaticamente da questa interfaccia, questo metodo avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="50347-120">If a caller tries to add an item of a different VARTYPE contained in the collection and the PROPVARIANT value cannot be changed by this interface automatically, this method will fail.</span></span> <span data-ttu-id="50347-121">Per modificare il tipo di raccolta manualmente, chiamare [**IPortableDevicePropVariantCollection:: ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span><span class="sxs-lookup"><span data-stu-id="50347-121">To change the collection type manually, call [**IPortableDevicePropVariantCollection::ChangeType**](iportabledevicepropvariantcollection-changetype.md).</span></span>

## <a name="examples"></a><span data-ttu-id="50347-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="50347-122">Examples</span></span>

<span data-ttu-id="50347-123">Per un esempio di come usare questo metodo, vedere [recupero di un identificatore di oggetto da un identificatore univoco permanente](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span><span class="sxs-lookup"><span data-stu-id="50347-123">For an example of how to use this method, see [Retrieving an Object Identifier from a Persistent Unique Identifier](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)</span></span>

## <a name="requirements"></a><span data-ttu-id="50347-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="50347-124">Requirements</span></span>



| <span data-ttu-id="50347-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="50347-125">Requirement</span></span> | <span data-ttu-id="50347-126">Valore</span><span class="sxs-lookup"><span data-stu-id="50347-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50347-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="50347-127">Header</span></span><br/>  | <dl> <span data-ttu-id="50347-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="50347-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="50347-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="50347-129">Library</span></span><br/> | <dl> <span data-ttu-id="50347-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="50347-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50347-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="50347-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50347-132">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="50347-132">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="50347-133">Trasferimento del contenuto nel dispositivo</span><span class="sxs-lookup"><span data-stu-id="50347-133">Moving Content on the Device</span></span>](moving-content-on-the-device.md)
</dt> <dt>

[<span data-ttu-id="50347-134">Recupero di un identificatore di oggetto da un identificatore univoco permanente</span><span class="sxs-lookup"><span data-stu-id="50347-134">Retrieving an Object Identifier from a Persistent Unique Identifier</span></span>](retrieving-an-object-identifier-from-a-persistent-unique-identifier.md)
</dt> </dl>

 

 




