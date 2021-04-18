---
description: Il metodo SetKeyValue aggiunge un nuovo valore REFPROPERTYKEY (Type VT \_ Unknown) o ne sovrascrive uno esistente.
ms.assetid: 344c52ec-91b1-43f9-b16a-28c24971d805
title: 'Metodo IPortableDeviceValues:: SetKeyValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetKeyValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: ae55b47687043bba92afbab09f25de8a5fc679d7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326859"
---
# <a name="iportabledevicevaluessetkeyvalue-method"></a><span data-ttu-id="33767-103">Metodo IPortableDeviceValues:: SetKeyValue</span><span class="sxs-lookup"><span data-stu-id="33767-103">IPortableDeviceValues::SetKeyValue method</span></span>

<span data-ttu-id="33767-104">Il metodo **SetKeyValue** aggiunge un nuovo valore **REFPROPERTYKEY** (Type VT \_ Unknown) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="33767-104">The **SetKeyValue** method adds a new **REFPROPERTYKEY** value (type VT\_UNKNOWN) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="33767-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="33767-105">Syntax</span></span>


```C++
HRESULT SetKeyValue(
  [in] REFPROPERTYKEY key,
  [in] REFPROPERTYKEY Value
);
```



## <a name="parameters"></a><span data-ttu-id="33767-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="33767-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33767-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="33767-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33767-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="33767-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="33767-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="33767-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="33767-110">Oggetto **REFPROPERTYKEY** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="33767-110">A **REFPROPERTYKEY** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33767-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="33767-111">Return value</span></span>

<span data-ttu-id="33767-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="33767-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="33767-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="33767-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="33767-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="33767-114">Return code</span></span>                                                                          | <span data-ttu-id="33767-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33767-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="33767-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="33767-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="33767-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="33767-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="33767-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="33767-118">Remarks</span></span>

<span data-ttu-id="33767-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="33767-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="33767-120">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="33767-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="33767-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="33767-121">Requirements</span></span>



| <span data-ttu-id="33767-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="33767-122">Requirement</span></span> | <span data-ttu-id="33767-123">Valore</span><span class="sxs-lookup"><span data-stu-id="33767-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33767-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="33767-124">Header</span></span><br/>  | <dl> <span data-ttu-id="33767-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="33767-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="33767-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="33767-126">Library</span></span><br/> | <dl> <span data-ttu-id="33767-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="33767-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33767-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="33767-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33767-129">Aggiunta di una risorsa a un oggetto</span><span class="sxs-lookup"><span data-stu-id="33767-129">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="33767-130">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="33767-130">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="33767-131">**IPortableDeviceValues::GetKeyValue**</span><span class="sxs-lookup"><span data-stu-id="33767-131">**IPortableDeviceValues::GetKeyValue**</span></span>](iportabledevicevalues-getkeyvalue.md)
</dt> </dl>

 

 




