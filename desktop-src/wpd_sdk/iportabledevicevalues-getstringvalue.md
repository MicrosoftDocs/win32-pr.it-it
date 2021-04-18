---
description: Il metodo GetStringValue recupera un valore stringa (di tipo VT \_ LPWSTR) specificato da una chiave.
ms.assetid: c6feecc0-7a06-4f78-9cf1-e2897333b62e
title: 'Metodo IPortableDeviceValues:: GetStringValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetStringValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: fdb4741c36445af686b7721e1f5f04dd3e45f1e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331560"
---
# <a name="iportabledevicevaluesgetstringvalue-method"></a><span data-ttu-id="5c06e-103">Metodo IPortableDeviceValues:: GetStringValue</span><span class="sxs-lookup"><span data-stu-id="5c06e-103">IPortableDeviceValues::GetStringValue method</span></span>

<span data-ttu-id="5c06e-104">Il metodo **GetStringValue** recupera un valore stringa (di tipo VT \_ LPWSTR) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="5c06e-104">The **GetStringValue** method retrieves a string value (type VT\_LPWSTR) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c06e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c06e-105">Syntax</span></span>


```C++
HRESULT GetStringValue(
  [in]  REFPROPERTYKEY key,
  [out] LPWSTR         *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="5c06e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c06e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c06e-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="5c06e-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c06e-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="5c06e-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="5c06e-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c06e-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c06e-110">Puntatore al valore **LPWSTR** recuperato.</span><span class="sxs-lookup"><span data-stu-id="5c06e-110">Pointer to the retrieved **LPWSTR** value.</span></span> <span data-ttu-id="5c06e-111">Il chiamante è responsabile della chiamata a **CoTaskMemFree** per rilasciare la memoria.</span><span class="sxs-lookup"><span data-stu-id="5c06e-111">The caller is responsible for calling **CoTaskMemFree** to release the memory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c06e-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c06e-112">Return value</span></span>

<span data-ttu-id="5c06e-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="5c06e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5c06e-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="5c06e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5c06e-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="5c06e-115">Return code</span></span>                                                                                                            | <span data-ttu-id="5c06e-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c06e-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c06e-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5c06e-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="5c06e-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="5c06e-118">The method succeeded.</span></span><br/>                                      |
| <dl> <span data-ttu-id="5c06e-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="5c06e-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="5c06e-120">La proprietà specificata da *Key* non è un tipo **LPWSTR** .</span><span class="sxs-lookup"><span data-stu-id="5c06e-120">The property specified by *key* is not an **LPWSTR** type.</span></span><br/> |
| <dl> <span data-ttu-id="5c06e-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="5c06e-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="5c06e-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="5c06e-122">The property specified by *key* is not in the collection.</span></span><br/>  |



 

## <a name="examples"></a><span data-ttu-id="5c06e-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="5c06e-123">Examples</span></span>

<span data-ttu-id="5c06e-124">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="5c06e-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c06e-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c06e-125">Requirements</span></span>



| <span data-ttu-id="5c06e-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c06e-126">Requirement</span></span> | <span data-ttu-id="5c06e-127">Valore</span><span class="sxs-lookup"><span data-stu-id="5c06e-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c06e-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c06e-128">Header</span></span><br/>  | <dl> <span data-ttu-id="5c06e-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c06e-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c06e-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c06e-130">Library</span></span><br/> | <dl> <span data-ttu-id="5c06e-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c06e-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c06e-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c06e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c06e-133">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="5c06e-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="5c06e-134">**IPortableDeviceValues:: GetA**</span><span class="sxs-lookup"><span data-stu-id="5c06e-134">**IPortableDeviceValues::GetAt**</span></span>](iportabledevicevalues-getat.md)
</dt> <dt>

[<span data-ttu-id="5c06e-135">**IPortableDeviceValues:: SetStringValue**</span><span class="sxs-lookup"><span data-stu-id="5c06e-135">**IPortableDeviceValues::SetStringValue**</span></span>](iportabledevicevalues-setstringvalue.md)
</dt> <dt>

[<span data-ttu-id="5c06e-136">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="5c06e-136">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="5c06e-137">Recupero dei formati di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="5c06e-137">Retrieving Supported Service Formats</span></span>](retrieving-supported-formats.md)
</dt> <dt>

[<span data-ttu-id="5c06e-138">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="5c06e-138">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




