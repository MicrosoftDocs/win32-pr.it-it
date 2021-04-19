---
description: Il metodo SetUnsignedIntegerValue aggiunge un nuovo valore ULONG (Type VT \_ UI4) o ne sovrascrive uno esistente.
ms.assetid: 9b5d1b8c-7863-4807-a34b-56d30a47bd5c
title: 'Metodo IPortableDeviceValues:: SetUnsignedIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7dc237e5cdba120a08899035dc20f6fb6b2b63f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326850"
---
# <a name="iportabledevicevaluessetunsignedintegervalue-method"></a><span data-ttu-id="453e4-103">Metodo IPortableDeviceValues:: SetUnsignedIntegerValue</span><span class="sxs-lookup"><span data-stu-id="453e4-103">IPortableDeviceValues::SetUnsignedIntegerValue method</span></span>

<span data-ttu-id="453e4-104">Il metodo **SetUnsignedIntegerValue** aggiunge un nuovo valore **ULONG** (Type VT \_ UI4) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="453e4-104">The **SetUnsignedIntegerValue** method adds a new **ULONG** value (type VT\_UI4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="453e4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="453e4-105">Syntax</span></span>


```C++
HRESULT SetUnsignedIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONG          Value
);
```



## <a name="parameters"></a><span data-ttu-id="453e4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="453e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="453e4-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="453e4-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453e4-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="453e4-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="453e4-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="453e4-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="453e4-110">**ULONG** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="453e4-110">A **ULONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="453e4-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="453e4-111">Return value</span></span>

<span data-ttu-id="453e4-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="453e4-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="453e4-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="453e4-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="453e4-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="453e4-114">Return code</span></span>                                                                          | <span data-ttu-id="453e4-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="453e4-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="453e4-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="453e4-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="453e4-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="453e4-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="453e4-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="453e4-118">Remarks</span></span>

<span data-ttu-id="453e4-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="453e4-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="examples"></a><span data-ttu-id="453e4-120">Esempio</span><span class="sxs-lookup"><span data-stu-id="453e4-120">Examples</span></span>

<span data-ttu-id="453e4-121">Per un esempio di come usare questo metodo, vedere [**specifica delle informazioni client**](specifying-client-information.md).</span><span class="sxs-lookup"><span data-stu-id="453e4-121">For an example of how to use this method, see [**Specifying Client Information**](specifying-client-information.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="453e4-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="453e4-122">Requirements</span></span>



| <span data-ttu-id="453e4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="453e4-123">Requirement</span></span> | <span data-ttu-id="453e4-124">Valore</span><span class="sxs-lookup"><span data-stu-id="453e4-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="453e4-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="453e4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="453e4-126"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="453e4-126"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="453e4-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="453e4-127">Library</span></span><br/> | <dl> <span data-ttu-id="453e4-128"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="453e4-128"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="453e4-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="453e4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="453e4-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="453e4-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="453e4-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="453e4-131">**IPortableDeviceValues::GetUnsignedIntegerValue**</span></span>](iportabledevicevalues-getunsignedintegervalue.md)
</dt> <dt>

[<span data-ttu-id="453e4-132">**Specifica delle informazioni client**</span><span class="sxs-lookup"><span data-stu-id="453e4-132">**Specifying Client Information**</span></span>](specifying-client-information.md)
</dt> </dl>

 

 




