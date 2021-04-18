---
description: Il metodo GetSerializedSize calcola la dimensione del buffer necessaria per mantenere un'interfaccia IPortableDeviceValues serializzata.
ms.assetid: 12fa6ed1-ce3b-4c5d-920a-87ff693fe0ea
title: 'Metodo IWpdSerializer:: GetSerializedSize (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetSerializedSize
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7b50f7f6158145cd71125b5e5f26649712bb065b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324499"
---
# <a name="iwpdserializergetserializedsize-method"></a><span data-ttu-id="415d1-103">Metodo IWpdSerializer:: GetSerializedSize</span><span class="sxs-lookup"><span data-stu-id="415d1-103">IWpdSerializer::GetSerializedSize method</span></span>

<span data-ttu-id="415d1-104">Il metodo **GetSerializedSize** calcola la dimensione del buffer necessaria per mantenere un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) serializzata.</span><span class="sxs-lookup"><span data-stu-id="415d1-104">The **GetSerializedSize** method calculates the buffer size that is required to hold a serialized [**IPortableDeviceValues**](iportabledevicevalues.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="415d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="415d1-105">Syntax</span></span>


```C++
HRESULT GetSerializedSize(
  [in]  IPortableDeviceValues *pSource,
  [out] DWORD                 *pdwSize
);
```



## <a name="parameters"></a><span data-ttu-id="415d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="415d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="415d1-107">*pSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="415d1-107">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="415d1-108">Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) la cui dimensione si desidera richiedere.</span><span class="sxs-lookup"><span data-stu-id="415d1-108">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface whose size you want to request.</span></span>

</dd> <dt>

<span data-ttu-id="415d1-109">*pdwSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="415d1-109">*pdwSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="415d1-110">Puntatore a un **valore DWORD** che indica le dimensioni del buffer necessarie per serializzare *pSource* in byte.</span><span class="sxs-lookup"><span data-stu-id="415d1-110">Pointer to a **DWORD** that indicates the buffer size that is required to serialize *pSource*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="415d1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="415d1-111">Return value</span></span>

<span data-ttu-id="415d1-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="415d1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="415d1-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="415d1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="415d1-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="415d1-114">Return code</span></span>                                                                                   | <span data-ttu-id="415d1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="415d1-115">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="415d1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="415d1-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="415d1-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="415d1-117">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="415d1-118"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="415d1-118"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="415d1-119">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="415d1-119">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="415d1-120"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="415d1-120"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="415d1-121">Memoria disponibile insufficiente per creare il buffer.</span><span class="sxs-lookup"><span data-stu-id="415d1-121">There was not enough available memory to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="415d1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="415d1-122">Requirements</span></span>



| <span data-ttu-id="415d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="415d1-123">Requirement</span></span> | <span data-ttu-id="415d1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="415d1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="415d1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="415d1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="415d1-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="415d1-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="415d1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="415d1-127">Library</span></span><br/> | <dl> <span data-ttu-id="415d1-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="415d1-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="415d1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="415d1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="415d1-130">**Interfaccia IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="415d1-130">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




