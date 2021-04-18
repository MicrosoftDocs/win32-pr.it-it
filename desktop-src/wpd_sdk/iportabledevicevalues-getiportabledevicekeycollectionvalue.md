---
description: Il metodo GetIPortableDeviceKeyCollectionValue recupera un valore IPortableDeviceKeyCollection (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: 131c8e05-9224-4db4-bdf6-0fd9c563e049
title: 'Metodo IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDeviceKeyCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7868b71790f6dbb7525fcd1be49b197042a196f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328101"
---
# <a name="iportabledevicevaluesgetiportabledevicekeycollectionvalue-method"></a><span data-ttu-id="afff2-103">Metodo IPortableDeviceValues:: GetIPortableDeviceKeyCollectionValue</span><span class="sxs-lookup"><span data-stu-id="afff2-103">IPortableDeviceValues::GetIPortableDeviceKeyCollectionValue method</span></span>

<span data-ttu-id="afff2-104">Il metodo **GetIPortableDeviceKeyCollectionValue** recupera un valore **IPORTABLEDEVICEKEYCOLLECTION** (Type VT \_ Unknown) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="afff2-104">The **GetIPortableDeviceKeyCollectionValue** method retrieves an **IPortableDeviceKeyCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="afff2-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="afff2-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceKeyCollectionValue(
  [in]  REFPROPERTYKEY               key,
  [out] IPortableDeviceKeyCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="afff2-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="afff2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afff2-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="afff2-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afff2-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="afff2-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="afff2-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="afff2-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="afff2-110">Puntatore al puntatore all'interfaccia [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) recuperato.</span><span class="sxs-lookup"><span data-stu-id="afff2-110">Pointer to the retrieved [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface pointer.</span></span> <span data-ttu-id="afff2-111">Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="afff2-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afff2-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="afff2-112">Return value</span></span>

<span data-ttu-id="afff2-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="afff2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="afff2-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="afff2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="afff2-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="afff2-115">Return code</span></span>                                                                                                            | <span data-ttu-id="afff2-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="afff2-116">Description</span></span>                                                                                      |
|------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afff2-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="afff2-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="afff2-118">The method succeeded.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="afff2-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="afff2-120">La proprietà specificata da *Key* non è un'interfaccia **IPortableDeviceKeyCollection** .</span><span class="sxs-lookup"><span data-stu-id="afff2-120">The property specified by *key* is not an **IPortableDeviceKeyCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="afff2-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="afff2-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="afff2-122">The property specified by *key* is not in the collection.</span></span><br/>                             |



 

## <a name="examples"></a><span data-ttu-id="afff2-123">Esempio</span><span class="sxs-lookup"><span data-stu-id="afff2-123">Examples</span></span>

<span data-ttu-id="afff2-124">Per un esempio di come usare questo metodo, vedere [recupero di eventi del servizio supportati](retrieving-supported-events.md).</span><span class="sxs-lookup"><span data-stu-id="afff2-124">For an example of how to use this method, see [Retrieving Supported Service Events](retrieving-supported-events.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="afff2-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="afff2-125">Requirements</span></span>



| <span data-ttu-id="afff2-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="afff2-126">Requirement</span></span> | <span data-ttu-id="afff2-127">Valore</span><span class="sxs-lookup"><span data-stu-id="afff2-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afff2-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="afff2-128">Header</span></span><br/>  | <dl> <span data-ttu-id="afff2-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="afff2-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="afff2-130">Library</span></span><br/> | <dl> <span data-ttu-id="afff2-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afff2-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="afff2-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="afff2-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afff2-133">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="afff2-133">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="afff2-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="afff2-134">**IPortableDeviceValues::SetIPortableDeviceKeyCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicekeycollectionvalue.md)
</dt> <dt>

[<span data-ttu-id="afff2-135">Recupero degli eventi del servizio supportati</span><span class="sxs-lookup"><span data-stu-id="afff2-135">Retrieving Supported Service Events</span></span>](retrieving-supported-events.md)
</dt> <dt>

[<span data-ttu-id="afff2-136">Recupero di metodi di servizio supportati</span><span class="sxs-lookup"><span data-stu-id="afff2-136">Retrieving Supported Service Methods</span></span>](retrieving-supported-methods.md)
</dt> </dl>

 

 




