---
description: Il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: 'Metodo IPortableDeviceKeyCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceKeyCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: f4e126ef5fcad74b7cee5f748322f15e75481e0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332108"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="07d24-103">Metodo IPortableDeviceKeyCollection:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="07d24-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="07d24-104">Il metodo **RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="07d24-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="07d24-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07d24-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="07d24-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="07d24-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07d24-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="07d24-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07d24-108">Specifica l'indice dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="07d24-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07d24-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="07d24-109">Return value</span></span>

<span data-ttu-id="07d24-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="07d24-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="07d24-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="07d24-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="07d24-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="07d24-112">Return code</span></span>                                                                                  | <span data-ttu-id="07d24-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07d24-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="07d24-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="07d24-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="07d24-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="07d24-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="07d24-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="07d24-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="07d24-117">L'indice specificato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="07d24-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="07d24-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="07d24-118">Remarks</span></span>

<span data-ttu-id="07d24-119">È necessario specificare un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="07d24-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="07d24-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07d24-120">Requirements</span></span>



| <span data-ttu-id="07d24-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="07d24-121">Requirement</span></span> | <span data-ttu-id="07d24-122">Valore</span><span class="sxs-lookup"><span data-stu-id="07d24-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07d24-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="07d24-123">Header</span></span><br/>  | <dl> <span data-ttu-id="07d24-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="07d24-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="07d24-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="07d24-125">Library</span></span><br/> | <dl> <span data-ttu-id="07d24-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="07d24-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07d24-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07d24-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07d24-128">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="07d24-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




