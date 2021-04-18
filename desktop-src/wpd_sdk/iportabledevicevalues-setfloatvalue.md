---
description: Il metodo SetFloatValue aggiunge un nuovo valore FLOAT (tipo VT \_ R4) o sovrascrive uno esistente.
ms.assetid: 1e0c9d19-47bf-4d93-a0c0-27e2c4897012
title: 'Metodo IPortableDeviceValues:: SetFloatValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetFloatValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 60b42217c925c83e96f2c893c7bc7f11449ebdd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326956"
---
# <a name="iportabledevicevaluessetfloatvalue-method"></a><span data-ttu-id="a9c5b-103">Metodo IPortableDeviceValues:: SetFloatValue</span><span class="sxs-lookup"><span data-stu-id="a9c5b-103">IPortableDeviceValues::SetFloatValue method</span></span>

<span data-ttu-id="a9c5b-104">Il metodo **SetFloatValue** aggiunge un nuovo valore **float** (tipo VT \_ R4) o sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-104">The **SetFloatValue** method adds a new **FLOAT** value (type VT\_R4) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9c5b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a9c5b-105">Syntax</span></span>


```C++
HRESULT SetFloatValue(
  [in]       REFPROPERTYKEY key,
  [in] const FLOAT          Value
);
```



## <a name="parameters"></a><span data-ttu-id="a9c5b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a9c5b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9c5b-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a9c5b-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c5b-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="a9c5b-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="a9c5b-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9c5b-110">**Float** che contiene il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-110">A **FLOAT** that contains the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9c5b-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a9c5b-111">Return value</span></span>

<span data-ttu-id="a9c5b-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9c5b-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9c5b-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="a9c5b-114">Return code</span></span>                                                                          | <span data-ttu-id="a9c5b-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9c5b-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9c5b-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9c5b-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9c5b-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-117">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9c5b-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a9c5b-118">Remarks</span></span>

<span data-ttu-id="a9c5b-119">Se un valore esistente ha la stessa chiave specificata dal parametro *Key* , sovrascrive il valore esistente senza alcun avviso.</span><span class="sxs-lookup"><span data-stu-id="a9c5b-119">If an existing value has the same key that is specified by the *key* parameter, it overwrites the existing value without any warning.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9c5b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a9c5b-120">Requirements</span></span>



| <span data-ttu-id="a9c5b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9c5b-121">Requirement</span></span> | <span data-ttu-id="a9c5b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="a9c5b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9c5b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a9c5b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="a9c5b-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9c5b-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9c5b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="a9c5b-125">Library</span></span><br/> | <dl> <span data-ttu-id="a9c5b-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9c5b-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9c5b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a9c5b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9c5b-128">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="a9c5b-128">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a9c5b-129">**IPortableDeviceValues::GetFloatValue**</span><span class="sxs-lookup"><span data-stu-id="a9c5b-129">**IPortableDeviceValues::GetFloatValue**</span></span>](iportabledevicevalues-getfloatvalue.md)
</dt> </dl>

 

 




