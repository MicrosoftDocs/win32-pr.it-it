---
description: Il metodo GetIUnknownValue recupera un valore di interfaccia IUnknown (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: 2197fa1f-639d-4ac1-9d5b-c6534f3ecf1c
title: 'Metodo IPortableDeviceValues:: GetIUnknownValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIUnknownValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bc7ecfdc699cfe5f572c303d2c8a9e71bafc026b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333619"
---
# <a name="iportabledevicevaluesgetiunknownvalue-method"></a><span data-ttu-id="38730-103">Metodo IPortableDeviceValues:: GetIUnknownValue</span><span class="sxs-lookup"><span data-stu-id="38730-103">IPortableDeviceValues::GetIUnknownValue method</span></span>

<span data-ttu-id="38730-104">Il metodo **GetIUnknownValue** recupera un valore di interfaccia **IUnknown** (Type VT \_ Unknown) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="38730-104">The **GetIUnknownValue** method retrieves an **IUnknown** interface value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="38730-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="38730-105">Syntax</span></span>


```C++
HRESULT GetIUnknownValue(
  [in]  REFPROPERTYKEY key,
  [out] IUnknown       **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="38730-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="38730-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38730-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="38730-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38730-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="38730-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="38730-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="38730-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="38730-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia **IUnknown** recuperata.</span><span class="sxs-lookup"><span data-stu-id="38730-110">Address of a variable that receives a pointer to the retrieved **IUnknown** interface.</span></span> <span data-ttu-id="38730-111">Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="38730-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38730-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="38730-112">Return value</span></span>

<span data-ttu-id="38730-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="38730-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="38730-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="38730-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="38730-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="38730-115">Return code</span></span>                                                                                                            | <span data-ttu-id="38730-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38730-116">Description</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38730-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="38730-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="38730-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="38730-118">The method succeeded.</span></span><br/>                                             |
| <dl> <span data-ttu-id="38730-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="38730-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="38730-120">La proprietà specificata da *Key* non è un'interfaccia **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="38730-120">The property specified by *key* is not an **IUnknown** interface.</span></span><br/> |
| <dl> <span data-ttu-id="38730-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="38730-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="38730-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="38730-122">The property specified by *key* is not in the collection.</span></span><br/>         |



 

## <a name="requirements"></a><span data-ttu-id="38730-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="38730-123">Requirements</span></span>



| <span data-ttu-id="38730-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="38730-124">Requirement</span></span> | <span data-ttu-id="38730-125">Valore</span><span class="sxs-lookup"><span data-stu-id="38730-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38730-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="38730-126">Header</span></span><br/>  | <dl> <span data-ttu-id="38730-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="38730-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="38730-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="38730-128">Library</span></span><br/> | <dl> <span data-ttu-id="38730-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38730-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38730-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="38730-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38730-131">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="38730-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="38730-132">**IPortableDeviceValues::SetIUnknownValue**</span><span class="sxs-lookup"><span data-stu-id="38730-132">**IPortableDeviceValues::SetIUnknownValue**</span></span>](iportabledevicevalues-setiunknownvalue.md)
</dt> </dl>

 

 




