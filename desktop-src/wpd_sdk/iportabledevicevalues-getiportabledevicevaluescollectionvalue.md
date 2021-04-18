---
description: Il metodo GetIPortableDeviceValuesCollectionValue recupera un valore IPortableDeviceValuesCollection (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: 07b41ef8-d299-4d69-98ad-f1818c09ef6c
title: 'Metodo IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 3db3b8410ca82a97a41fdf45ee3f866cb8d2e4b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326958"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluescollectionvalue-method"></a><span data-ttu-id="1fb1a-103">Metodo IPortableDeviceValues:: GetIPortableDeviceValuesCollectionValue</span><span class="sxs-lookup"><span data-stu-id="1fb1a-103">IPortableDeviceValues::GetIPortableDeviceValuesCollectionValue method</span></span>

<span data-ttu-id="1fb1a-104">Il metodo **GetIPortableDeviceValuesCollectionValue** recupera un valore **IPORTABLEDEVICEVALUESCOLLECTION** (Type VT \_ Unknown) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-104">The **GetIPortableDeviceValuesCollectionValue** method retrieves an **IPortableDeviceValuesCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fb1a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1fb1a-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesCollectionValue(
  [in]  REFPROPERTYKEY                  key,
  [out] IPortableDeviceValuesCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="1fb1a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1fb1a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fb1a-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1fb1a-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb1a-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="1fb1a-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1fb1a-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fb1a-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) recuperata.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) interface.</span></span> <span data-ttu-id="1fb1a-111">Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fb1a-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1fb1a-112">Return value</span></span>

<span data-ttu-id="1fb1a-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1fb1a-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1fb1a-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="1fb1a-115">Return code</span></span>                                                                                                            | <span data-ttu-id="1fb1a-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1fb1a-116">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1fb1a-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb1a-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="1fb1a-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-118">The method succeeded.</span></span><br/>                                                                    |
| <dl> <span data-ttu-id="1fb1a-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb1a-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="1fb1a-120">La proprietà specificata da *Key* non è un'interfaccia **IPortableDeviceValuesCollection** .</span><span class="sxs-lookup"><span data-stu-id="1fb1a-120">The property specified by *key* is not an **IPortableDeviceValuesCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="1fb1a-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="1fb1a-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="1fb1a-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="1fb1a-122">The property specified by *key* is not in the collection.</span></span><br/>                                |



 

## <a name="examples"></a><span data-ttu-id="1fb1a-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="1fb1a-123">Examples</span></span>

<span data-ttu-id="1fb1a-124">Per un esempio di come usare questo metodo, vedere [recupero delle funzionalità di rendering supportate da un dispositivo](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span><span class="sxs-lookup"><span data-stu-id="1fb1a-124">For an example of how to use this method, see [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fb1a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1fb1a-125">Requirements</span></span>



| <span data-ttu-id="1fb1a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fb1a-126">Requirement</span></span> | <span data-ttu-id="1fb1a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="1fb1a-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fb1a-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1fb1a-128">Header</span></span><br/>  | <dl> <span data-ttu-id="1fb1a-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fb1a-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fb1a-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="1fb1a-130">Library</span></span><br/> | <dl> <span data-ttu-id="1fb1a-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fb1a-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fb1a-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1fb1a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fb1a-133">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="1fb1a-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="1fb1a-134">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="1fb1a-134">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> <dt>

[<span data-ttu-id="1fb1a-135">**SetIPortableDeviceValuesCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="1fb1a-135">**SetIPortableDeviceValuesCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicevaluescollectionvalue.md)
</dt> </dl>

 

 




