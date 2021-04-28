---
description: "Metodo IPortableDevicePropVariantCollection::RemoveAt: il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato."
ms.assetid: cfee2454-5103-48ce-b9f7-1f76f5c18b6d
title: Metodo IPortableDevicePropVariantCollection::RemoveAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 5c62df57a95a9f5a8238ff61c4ca6dc3cb73ed36
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109945"
---
# <a name="iportabledevicepropvariantcollectionremoveat-method"></a><span data-ttu-id="7fcab-103">Metodo IPortableDevicePropVariantCollection::RemoveAt</span><span class="sxs-lookup"><span data-stu-id="7fcab-103">IPortableDevicePropVariantCollection::RemoveAt method</span></span>

<span data-ttu-id="7fcab-104">Il **metodo RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="7fcab-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7fcab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7fcab-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="7fcab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7fcab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7fcab-107">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="7fcab-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7fcab-108">Specifica l'indice dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7fcab-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7fcab-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7fcab-109">Return value</span></span>

<span data-ttu-id="7fcab-110">Il metodo restituisce un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="7fcab-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="7fcab-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="7fcab-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="7fcab-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="7fcab-112">Return code</span></span>                                                                                  | <span data-ttu-id="7fcab-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7fcab-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="7fcab-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcab-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="7fcab-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="7fcab-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="7fcab-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="7fcab-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="7fcab-117">L'indice specificato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="7fcab-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7fcab-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="7fcab-118">Remarks</span></span>

<span data-ttu-id="7fcab-119">È necessario specificare un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="7fcab-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="7fcab-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7fcab-120">Requirements</span></span>



| <span data-ttu-id="7fcab-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="7fcab-121">Requirement</span></span> | <span data-ttu-id="7fcab-122">Valore</span><span class="sxs-lookup"><span data-stu-id="7fcab-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7fcab-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7fcab-123">Header</span></span><br/>  | <dl> <span data-ttu-id="7fcab-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="7fcab-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="7fcab-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="7fcab-125">Library</span></span><br/> | <dl> <span data-ttu-id="7fcab-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="7fcab-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7fcab-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7fcab-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7fcab-128">**Interfaccia IPortableDevicePropVariantCollection**</span><span class="sxs-lookup"><span data-stu-id="7fcab-128">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> </dl>

 

 




