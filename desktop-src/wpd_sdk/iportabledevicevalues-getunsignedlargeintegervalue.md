---
description: Il metodo GetUnsignedLargeIntegerValue recupera un valore ULONGLONG (di tipo VT \_ UI8) specificato da una chiave.
ms.assetid: de37c49b-a5f4-424d-8320-1de2d5a624aa
title: 'Metodo IPortableDeviceValues:: GetUnsignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 48f6093f32d43737b1999c3474f74569ecd3f8cd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325812"
---
# <a name="iportabledevicevaluesgetunsignedlargeintegervalue-method"></a><span data-ttu-id="64141-103">Metodo IPortableDeviceValues:: GetUnsignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="64141-103">IPortableDeviceValues::GetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="64141-104">Il metodo **GetUnsignedLargeIntegerValue** recupera un valore **ULONGLONG** (di tipo VT \_ UI8) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="64141-104">The **GetUnsignedLargeIntegerValue** method retrieves a **ULONGLONG** value (type VT\_UI8) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="64141-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="64141-105">Syntax</span></span>


```C++
HRESULT GetUnsignedLargeIntegerValue(
  [in]  REFPROPERTYKEY key,
  [out] ULONGLONG      *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="64141-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="64141-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64141-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="64141-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64141-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="64141-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="64141-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="64141-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64141-110">Puntatore al valore **ULONGLONG** recuperato.</span><span class="sxs-lookup"><span data-stu-id="64141-110">Pointer to the retrieved **ULONGLONG** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64141-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="64141-111">Return value</span></span>

<span data-ttu-id="64141-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="64141-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64141-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="64141-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64141-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="64141-114">Return code</span></span>                                                                                                            | <span data-ttu-id="64141-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="64141-115">Description</span></span>                                                             |
|------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="64141-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="64141-116"><dt>**S\_OK**</dt></span></span> </dl>                                   | <span data-ttu-id="64141-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="64141-117">The method succeeded.</span></span><br/>                                        |
| <dl> <span data-ttu-id="64141-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="64141-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>                   | <span data-ttu-id="64141-119">La proprietà specificata da *Key* non è di tipo **ULONGLONG** .</span><span class="sxs-lookup"><span data-stu-id="64141-119">The property specified by *key* is not a **ULONGLONG** type.</span></span><br/> |
| <dl> <span data-ttu-id="64141-120"><dt>**HRESULT \_ da \_ Win32 (errore \_ non \_ trovato)**</dt></span><span class="sxs-lookup"><span data-stu-id="64141-120"><dt>**HRESULT\_FROM\_WIN32(ERROR\_NOT\_FOUND)**</dt></span></span> </dl> | <span data-ttu-id="64141-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="64141-121">The property specified by *key* is not in the collection.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="64141-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="64141-122">Requirements</span></span>



| <span data-ttu-id="64141-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="64141-123">Requirement</span></span> | <span data-ttu-id="64141-124">Valore</span><span class="sxs-lookup"><span data-stu-id="64141-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64141-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="64141-125">Header</span></span><br/>  | <dl> <span data-ttu-id="64141-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="64141-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="64141-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="64141-127">Library</span></span><br/> | <dl> <span data-ttu-id="64141-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="64141-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64141-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="64141-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64141-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="64141-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="64141-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="64141-131">**IPortableDeviceValues::SetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-setunsignedlargeintegervalue.md)
</dt> </dl>

 

 




