---
description: Il metodo GetIPortableDeviceValuesFromBuffer deserializza una matrice di byte in un'interfaccia IPortableDeviceValues.
ms.assetid: 93bea711-74d5-407a-a707-a3abe47bc2cd
title: 'Metodo IWpdSerializer:: GetIPortableDeviceValuesFromBuffer (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWpdSerializer.GetIPortableDeviceValuesFromBuffer
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 639a9455349e1d016b71d9c9717940695e9c0a85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324497"
---
# <a name="iwpdserializergetiportabledevicevaluesfrombuffer-method"></a><span data-ttu-id="96c4f-103">Metodo IWpdSerializer:: GetIPortableDeviceValuesFromBuffer</span><span class="sxs-lookup"><span data-stu-id="96c4f-103">IWpdSerializer::GetIPortableDeviceValuesFromBuffer method</span></span>

<span data-ttu-id="96c4f-104">Il metodo **GetIPortableDeviceValuesFromBuffer** deserializza una matrice di byte in un'interfaccia **IPortableDeviceValues** .</span><span class="sxs-lookup"><span data-stu-id="96c4f-104">The **GetIPortableDeviceValuesFromBuffer** method deserializes a byte array to an **IPortableDeviceValues** interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="96c4f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96c4f-105">Syntax</span></span>


```C++
HRESULT GetIPortableDeviceValuesFromBuffer(
  [in]  BYTE                  *pBuffer,
  [in]  DWORD                 dwInputBufferLength,
  [out] IPortableDeviceValues **ppParams
);
```



## <a name="parameters"></a><span data-ttu-id="96c4f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96c4f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96c4f-107">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96c4f-107">*pBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c4f-108">Puntatore al buffer da deserializzare.</span><span class="sxs-lookup"><span data-stu-id="96c4f-108">Pointer to the buffer to deserialize.</span></span>

</dd> <dt>

<span data-ttu-id="96c4f-109">*dwInputBufferLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96c4f-109">*dwInputBufferLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96c4f-110">**DWORD** che specifica la dimensione, in byte, del buffer.</span><span class="sxs-lookup"><span data-stu-id="96c4f-110">**DWORD** that specifies the size of the buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="96c4f-111">*ppParams* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="96c4f-111">*ppParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="96c4f-112">Indirizzo di una variabile che riceve un puntatore a un'interfaccia [**IPortableDeviceValues**](iportabledevicevalues.md) creata dal buffer.</span><span class="sxs-lookup"><span data-stu-id="96c4f-112">Address of a variable that receives a pointer to an [**IPortableDeviceValues**](iportabledevicevalues.md) interface created from the buffer.</span></span> <span data-ttu-id="96c4f-113">L'applicazione è responsabile della chiamata del **rilascio** sull'interfaccia.</span><span class="sxs-lookup"><span data-stu-id="96c4f-113">The application is responsible for calling **Release** on the interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96c4f-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96c4f-114">Return value</span></span>

<span data-ttu-id="96c4f-115">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="96c4f-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="96c4f-116">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="96c4f-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="96c4f-117">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="96c4f-117">Return code</span></span>                                                                                  | <span data-ttu-id="96c4f-118">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96c4f-118">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="96c4f-119"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="96c4f-119"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="96c4f-120">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="96c4f-120">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="96c4f-121"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="96c4f-121"><dt>**E\_POINTER**</dt></span></span> </dl>    | <span data-ttu-id="96c4f-122">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="96c4f-122">A required pointer argument was **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="96c4f-123"><dt>**E \_ imprevisto**</dt></span><span class="sxs-lookup"><span data-stu-id="96c4f-123"><dt>**E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="96c4f-124">Si è verificato un errore di conversione non specificato.</span><span class="sxs-lookup"><span data-stu-id="96c4f-124">An unspecified conversion error occurred.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="96c4f-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96c4f-125">Requirements</span></span>



| <span data-ttu-id="96c4f-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="96c4f-126">Requirement</span></span> | <span data-ttu-id="96c4f-127">Valore</span><span class="sxs-lookup"><span data-stu-id="96c4f-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96c4f-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96c4f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="96c4f-129"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="96c4f-129"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="96c4f-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="96c4f-130">Library</span></span><br/> | <dl> <span data-ttu-id="96c4f-131"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96c4f-131"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96c4f-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96c4f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96c4f-133">**Interfaccia IWpdSerializer**</span><span class="sxs-lookup"><span data-stu-id="96c4f-133">**IWpdSerializer Interface**</span></span>](iwpdserializer.md)
</dt> </dl>

 

 




