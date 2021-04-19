---
description: Il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: 'Metodo IPortableDevicePropVariantCollection:: RemoveAt (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDevicePropVariantCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 74c7900340caab6adfda1b4607df607a4f6f0811
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106325941"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="573eb-103">Metodo IPortableDevicePropVariantCollection:: RemoveAt</span><span class="sxs-lookup"><span data-stu-id="573eb-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="573eb-104">Il metodo **RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="573eb-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="573eb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="573eb-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="573eb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="573eb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="573eb-107">*dwIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="573eb-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="573eb-108">Specifica l'indice dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="573eb-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="573eb-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="573eb-109">Return value</span></span>

<span data-ttu-id="573eb-110">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="573eb-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="573eb-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="573eb-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="573eb-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="573eb-112">Return code</span></span>                                                                                  | <span data-ttu-id="573eb-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="573eb-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="573eb-114"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="573eb-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="573eb-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="573eb-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="573eb-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="573eb-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="573eb-117">L'indice specificato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="573eb-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="573eb-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="573eb-118">Remarks</span></span>

<span data-ttu-id="573eb-119">È necessario specificare un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="573eb-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="573eb-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="573eb-120">Requirements</span></span>



| <span data-ttu-id="573eb-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="573eb-121">Requirement</span></span> | <span data-ttu-id="573eb-122">Valore</span><span class="sxs-lookup"><span data-stu-id="573eb-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="573eb-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="573eb-123">Header</span></span><br/>  | <dl> <span data-ttu-id="573eb-124"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="573eb-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="573eb-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="573eb-125">Library</span></span><br/> | <dl> <span data-ttu-id="573eb-126"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="573eb-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="573eb-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="573eb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="573eb-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="573eb-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




