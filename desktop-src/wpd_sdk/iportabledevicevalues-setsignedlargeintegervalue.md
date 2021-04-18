---
description: Il metodo SetSignedLargeIntegerValue aggiunge un nuovo valore LONGLONG (Type VT \_ I8) o ne sovrascrive uno esistente.
ms.assetid: 604b48ed-3e3f-4a06-91dd-7ece9f146824
title: 'Metodo IPortableDeviceValues:: SetSignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetSignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f8c207a88e17c9a1ddf45d77e9da8b62a8396e23
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326856"
---
# <a name="iportabledevicevaluessetsignedlargeintegervalue-method"></a><span data-ttu-id="d033c-103">Metodo IPortableDeviceValues:: SetSignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="d033c-103">IPortableDeviceValues::SetSignedLargeIntegerValue method</span></span>

<span data-ttu-id="d033c-104">Il metodo **SetSignedLargeIntegerValue** aggiunge un nuovo valore **LONGLONG** (Type VT \_ I8) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="d033c-104">The **SetSignedLargeIntegerValue** method adds a new **LONGLONG** value (type VT\_I8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d033c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d033c-105">Syntax</span></span>


```C++
HRESULT SetSignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const LONGLONG       Value
);
```



## <a name="parameters"></a><span data-ttu-id="d033c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d033c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d033c-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d033c-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d033c-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="d033c-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="d033c-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d033c-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d033c-110">Oggetto **LONGLONG** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="d033c-110">A **LONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d033c-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d033c-111">Return value</span></span>

<span data-ttu-id="d033c-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d033c-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d033c-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d033c-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d033c-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d033c-114">Return code</span></span>                                                                          | <span data-ttu-id="d033c-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d033c-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d033c-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d033c-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d033c-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d033c-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d033c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d033c-118">Remarks</span></span>

<span data-ttu-id="d033c-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="d033c-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="d033c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d033c-120">Requirements</span></span>



| <span data-ttu-id="d033c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d033c-121">Requirement</span></span> | <span data-ttu-id="d033c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="d033c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d033c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d033c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d033c-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d033c-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d033c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="d033c-125">Library</span></span><br/> | <dl> <span data-ttu-id="d033c-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d033c-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d033c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d033c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d033c-128">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d033c-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d033c-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="d033c-129">**IPortableDeviceValues::GetSignedLargeIntegerValue**</span></span>](iportabledevicevalues-getsignedlargeintegervalue.md)
</dt> </dl>

 

 




