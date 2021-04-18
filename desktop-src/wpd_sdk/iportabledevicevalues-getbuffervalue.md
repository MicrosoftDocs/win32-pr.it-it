---
description: Il metodo GetBufferValue recupera un valore di matrice di byte (tipo VT \_ vector \| VT \_ Ui1) specificato da una chiave.
ms.assetid: 18180a47-7d81-440b-b596-2516089a02bd
title: 'Metodo IPortableDeviceValues:: GetBufferValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetBufferValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: e5b98bb412ed648cf6ac74ec457b1e6032c009ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106331828"
---
# <a name="iportabledevicevaluesgetbuffervalue-method"></a><span data-ttu-id="51beb-103">Metodo IPortableDeviceValues:: GetBufferValue</span><span class="sxs-lookup"><span data-stu-id="51beb-103">IPortableDeviceValues::GetBufferValue method</span></span>

<span data-ttu-id="51beb-104">Il metodo **GetBufferValue** recupera un valore di **matrice di byte** (tipo VT \_ vector \| VT \_ Ui1) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="51beb-104">The **GetBufferValue** method retrieves a **byte array** value (type VT\_VECTOR \| VT\_UI1) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="51beb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51beb-105">Syntax</span></span>


```C++
HRESULT GetBufferValue(
  [in]  REFPROPERTYKEY key,
  [out] BYTE           **ppValue,
  [out] DWORD          *pcbValue
);
```



## <a name="parameters"></a><span data-ttu-id="51beb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51beb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51beb-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="51beb-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51beb-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="51beb-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="51beb-109">*ppValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="51beb-109">*ppValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51beb-110">Puntatore al **\* *valore byte _ recuperato. Il chiamante è responsabile della liberazione della memoria chiamando _* CoTaskMemFree**.</span><span class="sxs-lookup"><span data-stu-id="51beb-110">Pointer to the retrieved \**BYTE\**_ value. The caller is responsible for freeing the memory by calling _\* CoTaskMemFree\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="51beb-111">*pcbValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="51beb-111">*pcbValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="51beb-112">Puntatore alla dimensione di *ppValue*, in byte.</span><span class="sxs-lookup"><span data-stu-id="51beb-112">Pointer to the size of *ppValue*, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51beb-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51beb-113">Return value</span></span>

<span data-ttu-id="51beb-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="51beb-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="51beb-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="51beb-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="51beb-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="51beb-116">Return code</span></span>                                                                                                            | <span data-ttu-id="51beb-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51beb-117">Description</span></span>                                                          |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="51beb-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="51beb-118"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="51beb-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="51beb-119">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="51beb-120"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="51beb-120"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="51beb-121">La proprietà specificata da *Key* non è di tipo **byte** \* .</span><span class="sxs-lookup"><span data-stu-id="51beb-121">The property specified by *key* is not a **BYTE**\* type.</span></span><br/> |
| <dl> <span data-ttu-id="51beb-122"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="51beb-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="51beb-123">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="51beb-123">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="51beb-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="51beb-124">Remarks</span></span>

<span data-ttu-id="51beb-125">Il recupero di un buffer **null** o di un buffer di dimensioni zero non è supportato.</span><span class="sxs-lookup"><span data-stu-id="51beb-125">Retrieving a **NULL** buffer or a zero-sized buffer is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="51beb-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51beb-126">Requirements</span></span>



| <span data-ttu-id="51beb-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="51beb-127">Requirement</span></span> | <span data-ttu-id="51beb-128">Valore</span><span class="sxs-lookup"><span data-stu-id="51beb-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51beb-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51beb-129">Header</span></span><br/>  | <dl> <span data-ttu-id="51beb-130"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="51beb-130"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="51beb-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="51beb-131">Library</span></span><br/> | <dl> <span data-ttu-id="51beb-132"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="51beb-132"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51beb-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51beb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51beb-134">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="51beb-134">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="51beb-135">**IPortableDeviceValues::SetBufferValue**</span><span class="sxs-lookup"><span data-stu-id="51beb-135">**IPortableDeviceValues::SetBufferValue**</span></span>](iportabledevicevalues-setbuffervalue.md)
</dt> </dl>

 

 




