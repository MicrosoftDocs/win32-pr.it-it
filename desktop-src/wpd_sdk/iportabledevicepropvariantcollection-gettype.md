---
description: Il metodo GetType Recupera il tipo di dati degli elementi nella raccolta.
ms.assetid: 2e389090-74ef-47af-9490-a4820d925246
title: 'Metodo IPortableDevicePropVariantCollection:: GetType (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.GetType
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: de5ea5b1eeaa9cf494c24e13b8b9b36f7490b84d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325943"
---
# <a name="iportabledevicepropvariantcollectiongettype-method"></a><span data-ttu-id="ea310-103">Metodo IPortableDevicePropVariantCollection:: GetType</span><span class="sxs-lookup"><span data-stu-id="ea310-103">IPortableDevicePropVariantCollection::GetType method</span></span>

<span data-ttu-id="ea310-104">Il metodo **GetType** Recupera il tipo di dati degli elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ea310-104">The **GetType** method retrieves the data type of the items in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea310-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ea310-105">Syntax</span></span>


```C++
HRESULT GetType(
  [out] VARTYPE *pvt
);
```



## <a name="parameters"></a><span data-ttu-id="ea310-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ea310-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea310-107">*Pvt* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ea310-107">*pvt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea310-108">Valore di enumerazione **VarType** di Platform SDK che indica il tipo di dati di tutti gli elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ea310-108">A Platform SDK **VARTYPE** enumeration value that indicates the data type of all the items in the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea310-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ea310-109">Return value</span></span>

<span data-ttu-id="ea310-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="ea310-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ea310-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="ea310-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ea310-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="ea310-112">Return code</span></span>                                                                               | <span data-ttu-id="ea310-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ea310-113">Description</span></span>                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ea310-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea310-114"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="ea310-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="ea310-115">The method succeeded.</span></span><br/>                     |
| <dl> <span data-ttu-id="ea310-116"><dt>**\_puntatore E**</dt></span><span class="sxs-lookup"><span data-stu-id="ea310-116"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="ea310-117">Un argomento obbligatorio del puntatore è **null**.</span><span class="sxs-lookup"><span data-stu-id="ea310-117">A required pointer argument was **NULL**.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ea310-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="ea310-118">Remarks</span></span>

<span data-ttu-id="ea310-119">Tutti gli elementi archiviati in un **IPortableDevicePropVariantCollection** sono dello stesso tipo.</span><span class="sxs-lookup"><span data-stu-id="ea310-119">All items that are stored in an **IPortableDevicePropVariantCollection** are the same type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea310-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ea310-120">Requirements</span></span>



| <span data-ttu-id="ea310-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea310-121">Requirement</span></span> | <span data-ttu-id="ea310-122">Valore</span><span class="sxs-lookup"><span data-stu-id="ea310-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea310-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ea310-123">Header</span></span><br/>  | <dl> <span data-ttu-id="ea310-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea310-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea310-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="ea310-125">Library</span></span><br/> | <dl> <span data-ttu-id="ea310-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea310-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea310-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ea310-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea310-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="ea310-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




