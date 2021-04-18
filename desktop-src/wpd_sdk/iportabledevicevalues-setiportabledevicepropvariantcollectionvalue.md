---
description: Il metodo SetIPortableDevicePropVariantCollectionValue aggiunge un nuovo valore IPortableDevicePropVariantCollection (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: 8ea6be5e-1d03-4d59-9acc-5cd56ee81cd3
title: 'Metodo IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 1f39ad6745dbf30df87e87be7fba358b4d9ad2c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326866"
---
# <a name="iportabledevicevaluessetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="233ae-103">Metodo IPortableDeviceValues:: SetIPortableDevicePropVariantCollectionValue</span><span class="sxs-lookup"><span data-stu-id="233ae-103">IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="233ae-104">Il metodo **SetIPortableDevicePropVariantCollectionValue** aggiunge un nuovo valore **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (Type VT \_ Unknown) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="233ae-104">The **SetIPortableDevicePropVariantCollectionValue** method adds a new **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="233ae-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="233ae-105">Syntax</span></span>


```C++
HRESULT SetIPortableDevicePropVariantCollectionValue(
  [in] REFPROPERTYKEY                       key,
  [in] IPortableDevicePropVariantCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="233ae-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="233ae-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="233ae-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="233ae-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233ae-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="233ae-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="233ae-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="233ae-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="233ae-110">Puntatore a un'interfaccia **IPortableDevicePropVariantCollection** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="233ae-110">Pointer to an **IPortableDevicePropVariantCollection** interface that specifies the new value.</span></span> <span data-ttu-id="233ae-111">L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="233ae-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="233ae-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="233ae-112">Return value</span></span>

<span data-ttu-id="233ae-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="233ae-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="233ae-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="233ae-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="233ae-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="233ae-115">Return code</span></span>                                                                          | <span data-ttu-id="233ae-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="233ae-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="233ae-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="233ae-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="233ae-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="233ae-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="233ae-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="233ae-119">Remarks</span></span>

<span data-ttu-id="233ae-120">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="233ae-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="233ae-121">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="233ae-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="233ae-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="233ae-122">Requirements</span></span>



| <span data-ttu-id="233ae-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="233ae-123">Requirement</span></span> | <span data-ttu-id="233ae-124">Valore</span><span class="sxs-lookup"><span data-stu-id="233ae-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="233ae-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="233ae-125">Header</span></span><br/>  | <dl> <span data-ttu-id="233ae-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="233ae-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="233ae-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="233ae-127">Library</span></span><br/> | <dl> <span data-ttu-id="233ae-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="233ae-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="233ae-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="233ae-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="233ae-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="233ae-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="233ae-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="233ae-131">**IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




