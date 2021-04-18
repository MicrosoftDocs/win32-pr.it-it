---
description: Il metodo GetBufferFromIPortableDeviceValues serializza un'interfaccia IPortableDeviceValues inviata in una matrice di byte allocata. La matrice di byte restituita è allocata per il chiamante e deve essere liberata dal chiamante utilizzando CoTaskMemFree.
ms.assetid: fd856394-9cb3-41cb-875b-1d490ca859df
title: 'Metodo IWpdSerializer:: GetBufferFromIPortableDeviceValues (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetBufferFromIPortableDeviceValues
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 44f4e9e7011e6a4766183307e81ef7e783da899f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324501"
---
# <a name="iwpdserializergetbufferfromiportabledevicevalues-method"></a><span data-ttu-id="7ab5e-104">Metodo IWpdSerializer:: GetBufferFromIPortableDeviceValues</span><span class="sxs-lookup"><span data-stu-id="7ab5e-104">IWpdSerializer::GetBufferFromIPortableDeviceValues method</span></span>

<span data-ttu-id="7ab5e-105">Il metodo **GetBufferFromIPortableDeviceValues** serializza un'interfaccia **IPortableDeviceValues** inviata in una matrice di byte allocata.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-105">The **GetBufferFromIPortableDeviceValues** method serializes a submitted **IPortableDeviceValues** interface to an allocated byte array.</span></span> <span data-ttu-id="7ab5e-106">La matrice di byte restituita è allocata per il chiamante e deve essere liberata dal chiamante utilizzando **CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-106">The byte array returned is allocated for the caller and should be freed by the caller using **CoTaskMemFree**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ab5e-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ab5e-107">Syntax</span></span>


```C++
HRESULT GetBufferFromIPortableDeviceValues(
  [in]  IPortableDeviceValues *pSource,
  [out] BYTE                  **ppBuffer,
  [out] DWORD                 *pdwBufferSize
);
```



## <a name="parameters"></a><span data-ttu-id="7ab5e-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="7ab5e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ab5e-109">*pSource* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ab5e-109">*pSource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab5e-110">Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="7ab5e-111">*ppBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ab5e-111">*ppBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab5e-112">Puntatore a un **byte \* *_ che contiene i dati serializzati. I dispositivi portatili Windows allocano questa memoria; il chiamante deve liberarlo chiamando _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-112">Pointer to a \**BYTE\**_ that contains the serialized data. Windows Portable Devices allocates this memory; the caller must free it by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="7ab5e-113">*pdwBufferSize* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="7ab5e-113">*pdwBufferSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ab5e-114">Puntatore a un **valore DWORD** che specifica la dimensione del buffer allocato, in byte.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-114">Pointer to a **DWORD** that specifies the size of allocated buffer, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ab5e-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7ab5e-115">Return value</span></span>

<span data-ttu-id="7ab5e-116">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7ab5e-117">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7ab5e-118">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7ab5e-118">Return code</span></span>                                                                                   | <span data-ttu-id="7ab5e-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ab5e-119">Description</span></span>                                                            |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ab5e-120"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ab5e-120"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="7ab5e-121">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-121">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="7ab5e-122"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="7ab5e-122"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="7ab5e-123">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-123">A required pointer argument was **NULL**.</span></span><br/>                   |
| <dl> <span data-ttu-id="7ab5e-124"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="7ab5e-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="7ab5e-125">Memoria disponibile insufficiente per creare il buffer.</span><span class="sxs-lookup"><span data-stu-id="7ab5e-125">There was not enough memory available to create the buffer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7ab5e-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ab5e-126">Requirements</span></span>



| <span data-ttu-id="7ab5e-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ab5e-127">Requirement</span></span> | <span data-ttu-id="7ab5e-128">Valore</span><span class="sxs-lookup"><span data-stu-id="7ab5e-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab5e-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7ab5e-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7ab5e-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ab5e-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7ab5e-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="7ab5e-131">Library</span></span><br/> | <dl> <span data-ttu-id="7ab5e-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7ab5e-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ab5e-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ab5e-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ab5e-134">**Interfaccia IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="7ab5e-134">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




