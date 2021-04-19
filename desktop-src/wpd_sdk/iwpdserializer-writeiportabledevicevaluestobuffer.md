---
description: Il metodo WriteIPortableDeviceValuesToBuffer serializza un'interfaccia IPortableDeviceValues in una matrice di byte allocata dal chiamante.
ms.assetid: 4d0108f1-563e-42df-897b-7cc0e9ff5b3a
title: 'Metodo IWpdSerializer:: WriteIPortableDeviceValuesToBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.WriteIPortableDeviceValuesToBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f2a8f8b374f967f7231881d9e0eca6434e9c57e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324045"
---
# <a name="iwpdserializerwriteiportabledevicevaluestobuffer-method"></a><span data-ttu-id="aee7e-103">Metodo IWpdSerializer:: WriteIPortableDeviceValuesToBuffer</span><span class="sxs-lookup"><span data-stu-id="aee7e-103">IWpdSerializer::WriteIPortableDeviceValuesToBuffer method</span></span>

<span data-ttu-id="aee7e-104">Il metodo **WriteIPortableDeviceValuesToBuffer** serializza un'interfaccia **IPortableDeviceValues** in una matrice di byte allocata dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="aee7e-104">The **WriteIPortableDeviceValuesToBuffer** method serializes an **IPortableDeviceValues** interface to a caller-allocated byte array.</span></span>

## <a name="syntax"></a><span data-ttu-id="aee7e-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aee7e-105">Syntax</span></span>


```C++
HRESULT WriteIPortableDeviceValuesToBuffer(
  [in]  DWORD                 dwOutputBufferLength,
  [in]  IPortableDeviceValues *pResults,
  [out] BYTE                  *pBuffer,
  [out] DWORD                 *pdwBytesWritten
);
```



## <a name="parameters"></a><span data-ttu-id="aee7e-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="aee7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aee7e-107">*dwOutputBufferLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee7e-107">*dwOutputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7e-108">**DWORD** che specifica la dimensione di *pbuffer* in byte.</span><span class="sxs-lookup"><span data-stu-id="aee7e-108">**DWORD** that specifies the size of *pBuffer*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="aee7e-109">*pResults* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aee7e-109">*pResults* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7e-110">Puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) da serializzare.</span><span class="sxs-lookup"><span data-stu-id="aee7e-110">Pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface to serialize.</span></span>

</dd> <dt>

<span data-ttu-id="aee7e-111">*pbuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aee7e-111">*pBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7e-112">Puntatore a un buffer allocato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="aee7e-112">Pointer to a caller-allocated buffer.</span></span> <span data-ttu-id="aee7e-113">Per informazioni sulle dimensioni del buffer necessario, chiamare **GetSerializedSize**.</span><span class="sxs-lookup"><span data-stu-id="aee7e-113">To learn the size of the required buffer, call **GetSerializedSize**.</span></span>

</dd> <dt>

<span data-ttu-id="aee7e-114">*pdwBytesWritten* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="aee7e-114">*pdwBytesWritten* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aee7e-115">Puntatore a un **valore DWORD** che indica il numero di byte effettivamente scritti nel buffer allocato dal chiamante.</span><span class="sxs-lookup"><span data-stu-id="aee7e-115">Pointer to a **DWORD** that indicates the number of bytes that was actually written to the caller-allocated buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aee7e-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="aee7e-116">Return value</span></span>

<span data-ttu-id="aee7e-117">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="aee7e-117">The method returns an **HRESULT**.</span></span> <span data-ttu-id="aee7e-118">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="aee7e-118">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="aee7e-119">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="aee7e-119">Return code</span></span>                                                                                   | <span data-ttu-id="aee7e-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aee7e-120">Description</span></span>                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="aee7e-121"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="aee7e-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="aee7e-122">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="aee7e-122">The method succeeded.</span></span><br/>                          |
| <dl> <span data-ttu-id="aee7e-123"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="aee7e-123"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="aee7e-124">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="aee7e-124">A required pointer argument was **NULL**.</span></span><br/>      |
| <dl> <span data-ttu-id="aee7e-125"><dt>**E \_ OutOfMemory**</dt></span><span class="sxs-lookup"><span data-stu-id="aee7e-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="aee7e-126">Il buffer fornito dal chiamante non era sufficientemente grande.</span><span class="sxs-lookup"><span data-stu-id="aee7e-126">The caller-provided buffer was not big enough.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="aee7e-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="aee7e-127">Remarks</span></span>

<span data-ttu-id="aee7e-128">Questo metodo copia un'interfaccia **IPortableDeviceValues** in un buffer esistente.</span><span class="sxs-lookup"><span data-stu-id="aee7e-128">This method copies an **IPortableDeviceValues** interface into an existing buffer.</span></span> <span data-ttu-id="aee7e-129">Se si desidera allocare un nuovo buffer, utilizzare [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span><span class="sxs-lookup"><span data-stu-id="aee7e-129">If you want to allocate a new buffer, use [**GetBufferFromIPortableDeviceValues**](iwpdserializer-getbufferfromiportabledevicevalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="aee7e-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aee7e-130">Requirements</span></span>



| <span data-ttu-id="aee7e-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee7e-131">Requirement</span></span> | <span data-ttu-id="aee7e-132">Valore</span><span class="sxs-lookup"><span data-stu-id="aee7e-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aee7e-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="aee7e-133">Header</span></span><br/>  | <dl> <span data-ttu-id="aee7e-134"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee7e-134"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="aee7e-135">Libreria</span><span class="sxs-lookup"><span data-stu-id="aee7e-135">Library</span></span><br/> | <dl> <span data-ttu-id="aee7e-136"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="aee7e-136"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aee7e-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aee7e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aee7e-138">**Interfaccia IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="aee7e-138">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




