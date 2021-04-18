---
description: Il metodo GetGuidValue recupera un valore GUID (tipo VT \_ CLSID) specificato da una chiave.
ms.assetid: 1cfa75e8-2c3b-4893-954e-dae25a6b8220
title: 'Metodo IPortableDeviceValues:: GetGuidValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetGuidValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 362672daad835a2e843edeaf6dc517884c25f1ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331988"
---
# <a name="iportabledevicevaluesgetguidvalue-method"></a><span data-ttu-id="60ff5-103">Metodo IPortableDeviceValues:: GetGuidValue</span><span class="sxs-lookup"><span data-stu-id="60ff5-103">IPortableDeviceValues::GetGuidValue method</span></span>

<span data-ttu-id="60ff5-104">Il metodo **GetGuidValue** recupera un valore **GUID** (tipo VT \_ CLSID) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="60ff5-104">The **GetGuidValue** method retrieves a **GUID** value (type VT\_CLSID) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="60ff5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60ff5-105">Syntax</span></span>


```C++
HRESULT GetGuidValue(
  [in]  REFPROPERTYKEY key,
  [out] GUID           *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="60ff5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="60ff5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60ff5-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="60ff5-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60ff5-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="60ff5-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="60ff5-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="60ff5-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60ff5-110">Puntatore al valore **GUID** recuperato.</span><span class="sxs-lookup"><span data-stu-id="60ff5-110">Pointer to the retrieved **GUID** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60ff5-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="60ff5-111">Return value</span></span>

<span data-ttu-id="60ff5-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="60ff5-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60ff5-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="60ff5-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60ff5-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="60ff5-114">Return code</span></span>                                                                                                            | <span data-ttu-id="60ff5-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="60ff5-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="60ff5-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="60ff5-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="60ff5-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="60ff5-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="60ff5-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="60ff5-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="60ff5-119">La proprietà specificata da *Key* non è un tipo **GUID** .</span><span class="sxs-lookup"><span data-stu-id="60ff5-119">The property specified by *key* is not a **GUID** type.</span></span><br/>   |
| <dl> <span data-ttu-id="60ff5-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="60ff5-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="60ff5-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="60ff5-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="60ff5-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="60ff5-122">Examples</span></span>

<span data-ttu-id="60ff5-123">Per un esempio di come usare questo metodo, vedere [recupero di metodi di servizio supportati](retrieving-supported-methods.md).</span><span class="sxs-lookup"><span data-stu-id="60ff5-123">For an example of how to use this method, see [Retrieving Supported Service Methods](retrieving-supported-methods.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="60ff5-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60ff5-124">Requirements</span></span>



| <span data-ttu-id="60ff5-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="60ff5-125">Requirement</span></span> | <span data-ttu-id="60ff5-126">Valore</span><span class="sxs-lookup"><span data-stu-id="60ff5-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60ff5-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60ff5-127">Header</span></span><br/>  | <dl> <span data-ttu-id="60ff5-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="60ff5-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="60ff5-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="60ff5-129">Library</span></span><br/> | <dl> <span data-ttu-id="60ff5-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60ff5-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60ff5-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60ff5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60ff5-132">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="60ff5-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="60ff5-133">**IPortableDeviceValues::SetGuidValue**</span><span class="sxs-lookup"><span data-stu-id="60ff5-133">**IPortableDeviceValues::SetGuidValue**</span></span>](iportabledevicevalues-setguidvalue.md)
</dt> <dt>

[<span data-ttu-id="60ff5-134">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="60ff5-134">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="60ff5-135">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="60ff5-135">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




