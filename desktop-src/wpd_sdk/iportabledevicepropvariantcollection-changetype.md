---
description: Il metodo ChangeType converte tutti gli elementi della raccolta nel VARTYPE specificato.
ms.assetid: b01b6205-c900-4b2e-810f-426e1e71a008
title: 'Metodo IPortableDevicePropVariantCollection:: ChangeType (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.ChangeType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: d843b62d273b28f7a694c37358742e4f3365be21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329892"
---
# <a name="iportabledevicepropvariantcollectionchangetype-method"></a><span data-ttu-id="40819-103">Metodo IPortableDevicePropVariantCollection:: ChangeType</span><span class="sxs-lookup"><span data-stu-id="40819-103">IPortableDevicePropVariantCollection::ChangeType method</span></span>

<span data-ttu-id="40819-104">Il metodo **ChangeType** converte tutti gli elementi della raccolta nel VarType specificato.</span><span class="sxs-lookup"><span data-stu-id="40819-104">The **ChangeType** method converts all items in the collection to the specified VARTYPE.</span></span>

## <a name="syntax"></a><span data-ttu-id="40819-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="40819-105">Syntax</span></span>


```C++
HRESULT ChangeType(
  [in] const VARTYPE vt
);
```



## <a name="parameters"></a><span data-ttu-id="40819-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="40819-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40819-107">*VT* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="40819-107">*vt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40819-108">Specifica il **VarType** in cui si desidera convertire tutti gli elementi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="40819-108">Specifies the **VARTYPE** to which you want to convert all items in the collection.</span></span> <span data-ttu-id="40819-109">I tipi di esempio includono VT \_ UI4 e VT \_ UI8.</span><span class="sxs-lookup"><span data-stu-id="40819-109">Example types include VT\_UI4 and VT\_UI8.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40819-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="40819-110">Return value</span></span>

<span data-ttu-id="40819-111">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="40819-111">The method returns an **HRESULT**.</span></span> <span data-ttu-id="40819-112">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="40819-112">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="40819-113">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="40819-113">Return code</span></span>                                                                          | <span data-ttu-id="40819-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="40819-114">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="40819-115"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="40819-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="40819-116">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="40819-116">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="40819-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="40819-117">Remarks</span></span>

<span data-ttu-id="40819-118">Se questo metodo ha esito negativo, è possibile che la raccolta venga lasciata in uno stato intermedio, con alcuni membri convertiti e non convertiti.</span><span class="sxs-lookup"><span data-stu-id="40819-118">If this method fails, the collection may be left in an intermediate state, with some members converted and some not converted.</span></span>

## <a name="requirements"></a><span data-ttu-id="40819-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="40819-119">Requirements</span></span>



| <span data-ttu-id="40819-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="40819-120">Requirement</span></span> | <span data-ttu-id="40819-121">Valore</span><span class="sxs-lookup"><span data-stu-id="40819-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="40819-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="40819-122">Header</span></span><br/>  | <dl> <span data-ttu-id="40819-123"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="40819-123"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="40819-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="40819-124">Library</span></span><br/> | <dl> <span data-ttu-id="40819-125"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40819-125"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40819-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="40819-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40819-127">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="40819-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




