---
description: Il metodo GetFloatValue recupera un valore FLOAT (tipo VT \_ R4) specificato da una chiave.
ms.assetid: 8a134dfb-f671-4cde-ae35-c8a41be270cf
title: 'Metodo IPortableDeviceValues:: GetFloatValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.GetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c99dcbb2d8436df7e3d593aa53efd086dc965ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327685"
---
# <a name="iportabledevicevaluesgetfloatvalue-method"></a><span data-ttu-id="3ccca-103">Metodo IPortableDeviceValues:: GetFloatValue</span><span class="sxs-lookup"><span data-stu-id="3ccca-103">IPortableDeviceValues::GetFloatValue method</span></span>

<span data-ttu-id="3ccca-104">Il metodo **GetFloatValue** recupera un valore **float** (tipo VT \_ R4) specificato da una chiave.</span><span class="sxs-lookup"><span data-stu-id="3ccca-104">The **GetFloatValue** method retrieves a **FLOAT** value (type VT\_R4) specified by a key.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ccca-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3ccca-105">Syntax</span></span>


```C++
HRESULT GetFloatValue(
  [in]  REFPROPERTYKEY key,
  [out] FLOAT          *pValue
);
```



## <a name="parameters"></a><span data-ttu-id="3ccca-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3ccca-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ccca-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="3ccca-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccca-108">Chiave **REFPROPERTYKEY** che specifica l'elemento da recuperare.</span><span class="sxs-lookup"><span data-stu-id="3ccca-108">A **REFPROPERTYKEY** key that specifies the item to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="3ccca-109">*pValue* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3ccca-109">*pValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ccca-110">Puntatore al valore **float** recuperato.</span><span class="sxs-lookup"><span data-stu-id="3ccca-110">Pointer to the retrieved **FLOAT** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ccca-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3ccca-111">Return value</span></span>

<span data-ttu-id="3ccca-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="3ccca-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3ccca-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="3ccca-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3ccca-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="3ccca-114">Return code</span></span>                                                                                             | <span data-ttu-id="3ccca-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ccca-115">Description</span></span>                                                          |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="3ccca-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3ccca-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="3ccca-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="3ccca-117">The method succeeded.</span></span><br/>                                     |
| <dl> <span data-ttu-id="3ccca-118"><dt>**DISP \_ E \_ TYPEMISMATCH**</dt></span><span class="sxs-lookup"><span data-stu-id="3ccca-118"><dt>**DISP\_E\_TYPEMISMATCH**</dt></span></span> </dl>    | <span data-ttu-id="3ccca-119">La proprietà specificata da *Key* non è di tipo **float** .</span><span class="sxs-lookup"><span data-stu-id="3ccca-119">The property specified by *key* is not a **FLOAT** type.</span></span><br/>  |
| <dl> <span data-ttu-id="3ccca-120"><dt>**\_ID Prop \_ non \_ supportato**</dt></span><span class="sxs-lookup"><span data-stu-id="3ccca-120"><dt>**E\_PROP\_ID\_UNSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="3ccca-121">La proprietà specificata dalla *chiave* non è presente nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="3ccca-121">The property specified by *key* is not in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3ccca-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3ccca-122">Requirements</span></span>



| <span data-ttu-id="3ccca-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="3ccca-123">Requirement</span></span> | <span data-ttu-id="3ccca-124">Valore</span><span class="sxs-lookup"><span data-stu-id="3ccca-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ccca-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3ccca-125">Header</span></span><br/>  | <dl> <span data-ttu-id="3ccca-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ccca-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="3ccca-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="3ccca-127">Library</span></span><br/> | <dl> <span data-ttu-id="3ccca-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3ccca-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ccca-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3ccca-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ccca-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="3ccca-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="3ccca-131">**IPortableDeviceValues::SetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="3ccca-131">**IPortableDeviceValues::SetFloatValue**</span></span>](iportabledevicevalues-setfloatvalue.md)
</dt> </dl>

 

 




