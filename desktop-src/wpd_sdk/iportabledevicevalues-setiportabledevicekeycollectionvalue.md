---
description: Il metodo SetIPortableDeviceKeyCollectionValue aggiunge un nuovo valore SetIPortableDeviceKeyCollectionValue (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: f470cb89-e7a0-470d-83d1-eb643b062e45
title: 'Metodo IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: face82230b9dd3bf6cbde18aaee8dd857e17d0a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326868"
---
# <a name="iportabledevicevaluessetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="74467-103">Metodo IPortableDeviceValues:: SetIPortableDeviceKeyCollectionValue</span><span class="sxs-lookup"><span data-stu-id="74467-103">IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="74467-104">Il metodo **SetIPortableDeviceKeyCollectionValue** aggiunge un nuovo valore **SETIPORTABLEDEVICEKEYCOLLECTIONVALUE** (Type VT \_ Unknown) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="74467-104">The **SetIPortableDeviceKeyCollectionValue** method adds a new **SetIPortableDeviceKeyCollectionValue** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="74467-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="74467-105">Syntax</span></span>


```C++
HRESULT SetIPortableDeviceKeyCollectionValue(
  [in] REFPROPERTYKEY               key,
  [in] IPortableDeviceKeyCollection *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="74467-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="74467-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74467-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="74467-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74467-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="74467-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="74467-109">*pValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="74467-109">*pValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="74467-110">Puntatore a un'interfaccia **IPortableDeviceKeyCollection** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="74467-110">Pointer to an **IPortableDeviceKeyCollection** interface that specifies the new value.</span></span> <span data-ttu-id="74467-111">L'SDK copia un riferimento all'interfaccia inviata e chiama **AddRef** .</span><span class="sxs-lookup"><span data-stu-id="74467-111">The SDK copies a reference to the submitted interface and calls **AddRef** on it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74467-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="74467-112">Return value</span></span>

<span data-ttu-id="74467-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="74467-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="74467-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="74467-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="74467-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="74467-115">Return code</span></span>                                                                          | <span data-ttu-id="74467-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74467-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="74467-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="74467-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="74467-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="74467-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="74467-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="74467-119">Remarks</span></span>

<span data-ttu-id="74467-120">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="74467-120">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="74467-121">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="74467-121">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="74467-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="74467-122">Requirements</span></span>



| <span data-ttu-id="74467-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="74467-123">Requirement</span></span> | <span data-ttu-id="74467-124">Valore</span><span class="sxs-lookup"><span data-stu-id="74467-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74467-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="74467-125">Header</span></span><br/>  | <dl> <span data-ttu-id="74467-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="74467-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="74467-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="74467-127">Library</span></span><br/> | <dl> <span data-ttu-id="74467-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="74467-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74467-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="74467-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74467-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="74467-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="74467-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="74467-131">**IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-getiportabledevicekeycollectionvalue.md)
</dt> </dl>

 

 




