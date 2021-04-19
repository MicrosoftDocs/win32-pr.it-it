---
description: Il metodo GetIPortableDeviceValuesValue recupera un valore IPortableDeviceValues (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: bf62c6a9-560b-4667-94d0-2dea6657eed1
title: 'Metodo IPortableDeviceValues:: GetIPortableDeviceValuesValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceValuesValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 9583ea157c1e3395fd9814b1a2e78af3f1985b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332279"
---
# <a name="iportabledevicevaluesgetiportabledevicevaluesvalue-method"></a><span data-ttu-id="278c6-103">Metodo IPortableDeviceValues:: GetIPortableDeviceValuesValue</span><span class="sxs-lookup"><span data-stu-id="278c6-103">IPortableDeviceValues::GetIPortableDeviceValuesValue method</span></span>

<span data-ttu-id="278c6-104">Il metodo **GetIPortableDeviceValuesValue** recupera un valore **IPORTABLEDEVICEVALUES** (Type VT \_ Unknown) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="278c6-104">The **GetIPortableDeviceValuesValue** method retrieves an **IPortableDeviceValues** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="278c6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="278c6-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesValue(
  [in]  REFPROPERTYKEY        key,
  [out] IPortableDeviceValues **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="278c6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="278c6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="278c6-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="278c6-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="278c6-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="278c6-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="278c6-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="278c6-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="278c6-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) recuperata.</span><span class="sxs-lookup"><span data-stu-id="278c6-110">Address of a variable that receives a pointer to the retrieved [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span> <span data-ttu-id="278c6-111">Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="278c6-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="278c6-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="278c6-112">Return value</span></span>

<span data-ttu-id="278c6-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="278c6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="278c6-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="278c6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="278c6-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="278c6-115">Return code</span></span>                                                                                                            | <span data-ttu-id="278c6-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="278c6-116">Description</span></span>                                                                               |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="278c6-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="278c6-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="278c6-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="278c6-118">The method succeeded.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="278c6-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="278c6-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="278c6-120">La proprietà specificata da *Key* non è un'interfaccia **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="278c6-120">The property specified by *key* is not an **IPortableDeviceValues** interface.</span></span><br/> |
| <dl> <span data-ttu-id="278c6-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="278c6-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="278c6-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="278c6-122">The property specified by *key* is not in the collection.</span></span><br/>                      |



 

## <a name="examples"></a><span data-ttu-id="278c6-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="278c6-123">Examples</span></span>

<span data-ttu-id="278c6-124">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="278c6-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="278c6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="278c6-125">Requirements</span></span>



| <span data-ttu-id="278c6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="278c6-126">Requirement</span></span> | <span data-ttu-id="278c6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="278c6-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="278c6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="278c6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="278c6-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="278c6-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="278c6-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="278c6-130">Library</span></span><br/> | <dl> <span data-ttu-id="278c6-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="278c6-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="278c6-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="278c6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="278c6-133">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="278c6-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="278c6-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span><span class="sxs-lookup"><span data-stu-id="278c6-134">**IPortableDeviceValues::SetIPortableDeviceValuesValue**</span></span>](iportabledevicevalues-setiportabledevicevaluesvalue.md)
</dt> <dt>

[<span data-ttu-id="278c6-135">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="278c6-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="278c6-136">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="278c6-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




