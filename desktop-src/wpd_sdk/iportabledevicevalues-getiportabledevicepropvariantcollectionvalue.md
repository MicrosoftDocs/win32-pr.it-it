---
description: Il metodo GetIPortableDevicePropVariantCollectionValue recupera un valore IPortableDevicePropVariantCollection (Type VT \_ Unknown) specificato da una chiave.
ms.assetid: a7b5ba64-c28e-42ae-9f04-2bdb67e93328
title: 'Metodo IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetIPortableDevicePropVariantCollectionValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7deb73d10f2e2daa5d06d6cb4394c43778af2ad4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332659"
---
# <a name="iportabledevicevaluesgetiportabledevicepropvariantcollectionvalue-method"></a><span data-ttu-id="22d84-103">Metodo IPortableDeviceValues:: GetIPortableDevicePropVariantCollectionValue</span><span class="sxs-lookup"><span data-stu-id="22d84-103">IPortableDeviceValues::GetIPortableDevicePropVariantCollectionValue method</span></span>

<span data-ttu-id="22d84-104">Il metodo **GetIPortableDevicePropVariantCollectionValue** recupera un valore **IPORTABLEDEVICEPROPVARIANTCOLLECTION** (Type VT \_ Unknown) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="22d84-104">The **GetIPortableDevicePropVariantCollectionValue** method retrieves an **IPortableDevicePropVariantCollection** value (type VT\_UNKNOWN) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="22d84-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="22d84-105">Syntax</span></span>


```C++
HRESULT GetIPortableDevicePropVariantCollectionValue(
  [in]  REFPROPERTYKEY                       key,
  [out] IPortableDevicePropVariantCollection **ppValue
);
```



## <a name="parameters"></a><span data-ttu-id="22d84-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="22d84-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22d84-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="22d84-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22d84-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="22d84-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="22d84-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="22d84-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="22d84-110">Indirizzo di una variabile che riceve un puntatore all'interfaccia [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) recuperata.</span><span class="sxs-lookup"><span data-stu-id="22d84-110">Address of a variable that receives a pointer to the retrieved [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) interface.</span></span> <span data-ttu-id="22d84-111">Il chiamante è responsabile della chiamata della **versione** sull'interfaccia recuperata.</span><span class="sxs-lookup"><span data-stu-id="22d84-111">The caller is responsible for calling **Release** on the retrieved interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22d84-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="22d84-112">Return value</span></span>

<span data-ttu-id="22d84-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="22d84-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="22d84-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="22d84-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="22d84-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="22d84-115">Return code</span></span>                                                                                                            | <span data-ttu-id="22d84-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22d84-116">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="22d84-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="22d84-117"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="22d84-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="22d84-118">The method succeeded.</span></span><br/>                                                                         |
| <dl> <span data-ttu-id="22d84-119"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="22d84-119"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="22d84-120">La proprietà specificata da *Key* non è un'interfaccia **IPortableDevicePropVariantCollection** .</span><span class="sxs-lookup"><span data-stu-id="22d84-120">The property specified by *key* is not an **IPortableDevicePropVariantCollection** interface.</span></span><br/> |
| <dl> <span data-ttu-id="22d84-121"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="22d84-121"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="22d84-122">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="22d84-122">The property specified by *key* is not in the collection.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="22d84-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="22d84-123">Requirements</span></span>



| <span data-ttu-id="22d84-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="22d84-124">Requirement</span></span> | <span data-ttu-id="22d84-125">Valore</span><span class="sxs-lookup"><span data-stu-id="22d84-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22d84-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="22d84-126">Header</span></span><br/>  | <dl> <span data-ttu-id="22d84-127"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="22d84-127"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="22d84-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="22d84-128">Library</span></span><br/> | <dl> <span data-ttu-id="22d84-129"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="22d84-129"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22d84-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="22d84-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22d84-131">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="22d84-131">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="22d84-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span><span class="sxs-lookup"><span data-stu-id="22d84-132">**IPortableDeviceValues::SetIPortableDevicePropVariantCollectionValue**</span></span>](iportabledevicevalues-setiportabledevicepropvariantcollectionvalue.md)
</dt> </dl>

 

 




