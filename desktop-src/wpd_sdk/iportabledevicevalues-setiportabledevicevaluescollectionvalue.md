---
description: Il metodo SetIPortableDeviceValuesCollectionValue aggiunge un nuovo valore IPortableDeviceValuesCollection (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: 29bdecaa-4820-4b1d-be59-ae82f7715a53
title: 'Metodo IPortableDeviceValues:: SetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3f0c545a4daceed75971b0e659f85d72eca6d98f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326863"
---
# <a name="iportabledevicevaluessetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="f35a7-103">Metodo IPortableDeviceValues:: SetIPortableDeviceValuesCollectionValue</span><span class="sxs-lookup"><span data-stu-id="f35a7-103">IPortableDeviceValues::SetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="f35a7-104">Il metodo **SetIPortableDeviceValuesCollectionValue** aggiunge un nuovo valore **IPORTABLEDEVICEVALUESCOLLECTION** (Type VT \_ Unknown) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="f35a7-104">The **SetIPortableDeviceValuesCollectionValue** method adds a new **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="f35a7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f35a7-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceValuesCollectionValue(
  [in] REFPROPERTYKEY                  key,
  [in] IPortableDeviceValuesCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="f35a7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f35a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f35a7-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="f35a7-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f35a7-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="f35a7-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="f35a7-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f35a7-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f35a7-110">Puntatore a un'interfaccia **IPortableDeviceValuesCollection** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="f35a7-110">Pointer to an **IPortableDeviceValuesCollection** interface that specifies the new value.</span></span> <span data-ttu-id="f35a7-111">L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="f35a7-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f35a7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f35a7-112">Return value</span></span>

<span data-ttu-id="f35a7-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f35a7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f35a7-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f35a7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f35a7-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f35a7-115">Return code</span></span>                                                                          | <span data-ttu-id="f35a7-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f35a7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f35a7-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f35a7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f35a7-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f35a7-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f35a7-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f35a7-119">Remarks</span></span>

<span data-ttu-id="f35a7-120">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="f35a7-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="f35a7-121">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f35a7-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="f35a7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f35a7-122">Requirements</span></span>



| <span data-ttu-id="f35a7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f35a7-123">Requirement</span></span> | <span data-ttu-id="f35a7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="f35a7-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f35a7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f35a7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f35a7-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="f35a7-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f35a7-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="f35a7-127">Library</span></span><br/> | <dl> <span data-ttu-id="f35a7-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f35a7-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f35a7-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f35a7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f35a7-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="f35a7-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="f35a7-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="f35a7-131">**IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




