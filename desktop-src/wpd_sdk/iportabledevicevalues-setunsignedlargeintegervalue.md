---
description: Il metodo SetUnsignedLargeIntegerValue aggiunge un nuovo valore ULONGLONG (Type VT \_ UI8) o ne sovrascrive uno esistente.
ms.assetid: 64874b86-7bf1-407a-8fff-a2c07c22f0cb
title: 'Metodo IPortableDeviceValues:: SetUnsignedLargeIntegerValue (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValues.SetUnsignedLargeIntegerValue
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 0c1ade76b4242c7508cb325e90c567349afcdc9d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326848"
---
# <a name="iportabledevicevaluessetunsignedlargeintegervalue-method"></a><span data-ttu-id="070d1-103">Metodo IPortableDeviceValues:: SetUnsignedLargeIntegerValue</span><span class="sxs-lookup"><span data-stu-id="070d1-103">IPortableDeviceValues::SetUnsignedLargeIntegerValue method</span></span>

<span data-ttu-id="070d1-104">Il metodo **SetUnsignedLargeIntegerValue** aggiunge un nuovo valore **ULONGLONG** (Type VT \_ UI8) o ne sovrascrive uno esistente.</span><span class="sxs-lookup"><span data-stu-id="070d1-104">The **SetUnsignedLargeIntegerValue** method adds a new **ULONGLONG** value (type VT\_UI8) or overwrites an existing one.</span></span>

## <a name="syntax"></a><span data-ttu-id="070d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="070d1-105">Syntax</span></span>


```C++
HRESULT SetUnsignedLargeIntegerValue(
  [in]       REFPROPERTYKEY key,
  [in] const ULONGLONG      Value
);
```



## <a name="parameters"></a><span data-ttu-id="070d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="070d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="070d1-107">*chiave* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="070d1-107">*key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070d1-108">Oggetto **REFPROPERTYKEY** che specifica l'elemento da creare o sovrascrivere.</span><span class="sxs-lookup"><span data-stu-id="070d1-108">A **REFPROPERTYKEY** that specifies the item to create or overwrite.</span></span>

</dd> <dt>

<span data-ttu-id="070d1-109">*Valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="070d1-109">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="070d1-110">Oggetto **ULONGLONG** che specifica il nuovo valore.</span><span class="sxs-lookup"><span data-stu-id="070d1-110">A **ULONGLONG** that specifies the new value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="070d1-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="070d1-111">Return value</span></span>

<span data-ttu-id="070d1-112">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="070d1-112">The method returns an **HRESULT**.</span></span> <span data-ttu-id="070d1-113">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="070d1-113">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="070d1-114">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="070d1-114">Return code</span></span>                                                                          | <span data-ttu-id="070d1-115">Descrizione</span><span class="sxs-lookup"><span data-stu-id="070d1-115">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="070d1-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="070d1-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="070d1-117">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="070d1-117">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="070d1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="070d1-118">Requirements</span></span>



| <span data-ttu-id="070d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="070d1-119">Requirement</span></span> | <span data-ttu-id="070d1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="070d1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="070d1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="070d1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="070d1-122"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="070d1-122"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="070d1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="070d1-123">Library</span></span><br/> | <dl> <span data-ttu-id="070d1-124"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="070d1-124"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="070d1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="070d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="070d1-126">Aggiunta di una risorsa a un oggetto</span><span class="sxs-lookup"><span data-stu-id="070d1-126">Adding a Resource to an Object</span></span>](adding-a-resource-to-an-object.md)
</dt> <dt>

[<span data-ttu-id="070d1-127">**Interfaccia IPortableDeviceValues**</span><span class="sxs-lookup"><span data-stu-id="070d1-127">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="070d1-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span><span class="sxs-lookup"><span data-stu-id="070d1-128">**IPortableDeviceValues::GetUnsignedLargeIntegerValue**</span></span>](iportabledevicevalues-getunsignedlargeintegervalue.md)
</dt> </dl>

 

 




