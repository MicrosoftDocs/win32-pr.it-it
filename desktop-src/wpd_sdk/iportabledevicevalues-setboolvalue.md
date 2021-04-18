---
description: Il Metodo SetBoolValue aggiunge un nuovo valore booleano (tipo VT \_ bool) o sovrascrive uno esistente.
ms.assetid: add30665-78f7-4037-801e-af51a4ab2f60
title: 'Metodo IPortableDeviceValues:: SetBoolValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetBoolValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7adf311e863c08873aa8300f9e940d4a5b49417f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325806"
---
# <a name="iportabledevicevaluessetboolvalue-method"></a><span data-ttu-id="d5683-103">Metodo IPortableDeviceValues:: SetBoolValue</span><span class="sxs-lookup"><span data-stu-id="d5683-103">IPortableDeviceValues::SetBoolValue method</span></span>

<span data-ttu-id="d5683-104">Il metodo **SetBoolValue** aggiunge un nuovo valore **booleano** (tipo VT \_ bool) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="d5683-104">The **SetBoolValue** method adds a new **Boolean** value (type VT\_BOOL) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5683-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5683-105">Syntax</span></span>


```C++
HRESULT SetBoolValue(
  [in]       REFPROPERTYKEY key,
  [in] const BOOL           Value
);
```



## <a name="parameters"></a><span data-ttu-id="d5683-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5683-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5683-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d5683-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5683-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="d5683-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="d5683-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="d5683-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5683-110">**Bool** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="d5683-110">A **BOOL** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5683-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5683-111">Return value</span></span>

<span data-ttu-id="d5683-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="d5683-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d5683-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="d5683-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d5683-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="d5683-114">Return code</span></span>                                                                          | <span data-ttu-id="d5683-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5683-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d5683-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5683-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d5683-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="d5683-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5683-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5683-118">Remarks</span></span>

<span data-ttu-id="d5683-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="d5683-119">If an existing value has the same key specified by the *key* parameter, it overwrites the existing value without any warning.</span></span> <span data-ttu-id="d5683-120">La memoria della chiave esistente viene rilasciata in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="d5683-120">The existing key memory is released appropriately.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5683-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5683-121">Requirements</span></span>



| <span data-ttu-id="d5683-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5683-122">Requirement</span></span> | <span data-ttu-id="d5683-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d5683-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5683-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5683-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d5683-125"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5683-125"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="d5683-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5683-126">Library</span></span><br/> | <dl> <span data-ttu-id="d5683-127"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5683-127"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5683-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5683-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5683-129">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="d5683-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="d5683-130">**IPortableDeviceValues::GetBoolValue**</span><span class="sxs-lookup"><span data-stu-id="d5683-130">**IPortableDeviceValues::GetBoolValue**</span></span>](iportabledevicevalues-getboolvalue.md)
</dt> </dl>

 

 




