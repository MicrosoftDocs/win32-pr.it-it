---
description: Il metodo GetUnsignedIntegerValue recupera un valore ULONG (Type VT \_ UI4) specificato da una chiave.
ms.assetid: 167163fa-6583-4e6b-b801-3a441a95644b
title: 'Metodo IPortableDeviceValues:: GetUnsignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 5c7deb0b6ebfdb8feb90248f9d8e1cdf68411d9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325815"
---
# <a name="iportabledevicevaluesgetunsignedintegervalue-method"></a><span data-ttu-id="e115b-103">Metodo IPortableDeviceValues:: GetUnsignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="e115b-103">IPortableDeviceValues::GetUnsignedIntegerValue method</span></span>

<span data-ttu-id="e115b-104">Il metodo **GetUnsignedIntegerValue** recupera un valore **ULONG** (Type VT \_ UI4) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="e115b-104">The **GetUnsignedIntegerValue** method retrieves a **ULONG** value (type VT\_UI4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="e115b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e115b-105">Syntax</span></span>


```C++
HRESULT GetUnsignedIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONG          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="e115b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e115b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e115b-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e115b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e115b-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="e115b-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="e115b-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e115b-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e115b-110">Puntatore al valore **ULONG** recuperato.</span><span class="sxs-lookup"><span data-stu-id="e115b-110">Pointer to the retrieved **ULONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e115b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e115b-111">Return value</span></span>

<span data-ttu-id="e115b-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e115b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e115b-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e115b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e115b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e115b-114">Return code</span></span>                                                                                                            | <span data-ttu-id="e115b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e115b-115">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="e115b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e115b-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="e115b-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e115b-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="e115b-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="e115b-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="e115b-119">La proprietà specificata da *Key* non è di tipo **ULONG** .</span><span class="sxs-lookup"><span data-stu-id="e115b-119">The property specified by *key* is not a **ULONG** type.</span></span><br/>  |
| <dl> <span data-ttu-id="e115b-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="e115b-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="e115b-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="e115b-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="e115b-122">Esempio</span><span class="sxs-lookup"><span data-stu-id="e115b-122">Examples</span></span>

<span data-ttu-id="e115b-123">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="e115b-123">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e115b-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e115b-124">Requirements</span></span>



| <span data-ttu-id="e115b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="e115b-125">Requirement</span></span> | <span data-ttu-id="e115b-126">Valore</span><span class="sxs-lookup"><span data-stu-id="e115b-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e115b-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e115b-127">Header</span></span><br/>  | <dl> <span data-ttu-id="e115b-128"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="e115b-128"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="e115b-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="e115b-129">Library</span></span><br/> | <dl> <span data-ttu-id="e115b-130"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e115b-130"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e115b-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e115b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e115b-132">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="e115b-132">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e115b-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="e115b-133">**IPortableDeviceValues::SetUnsignedIntegerValue**</span></span>](iportabledevicevalues-setunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="e115b-134">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="e115b-134">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="e115b-135">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="e115b-135">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> <dt>

[<span data-ttu-id="e115b-136">Recupero delle funzionalità di rendering supportate da un dispositivo</span><span class="sxs-lookup"><span data-stu-id="e115b-136">Retrieving the Rendering Capabilities Supported by a Device</span></span>](retrieving-the-rendering-capabilities-supported-by-a-device.md)
</dt> </dl>

 

 




