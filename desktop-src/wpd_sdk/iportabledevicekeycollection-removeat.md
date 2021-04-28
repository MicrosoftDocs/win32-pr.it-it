---
description: "Metodo IPortableDeviceKeyCollection::RemoveAt: il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato."
ms.assetid: 70f220be-d70b-4a25-8e16-82ed42adf2c4
title: Metodo IPortableDeviceKeyCollection::RemoveAt (PortableDeviceTypes.h)
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
ms.openlocfilehash: 3ec2b1137e7959a646c2943ab1aa7a5c3428d3c0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109944"
---
# <a name="iportabledevicekeycollectionremoveat-method"></a><span data-ttu-id="f5a3c-103">Metodo IPortableDeviceKeyCollection::RemoveAt</span><span class="sxs-lookup"><span data-stu-id="f5a3c-103">IPortableDeviceKeyCollection::RemoveAt method</span></span>

<span data-ttu-id="f5a3c-104">Il **metodo RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a3c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5a3c-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="f5a3c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5a3c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a3c-107">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="f5a3c-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a3c-108">Specifica l'indice dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a3c-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5a3c-109">Return value</span></span>

<span data-ttu-id="f5a3c-110">Il metodo restituisce un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f5a3c-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f5a3c-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f5a3c-112">Return code</span></span>                                                                                  | <span data-ttu-id="f5a3c-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f5a3c-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="f5a3c-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a3c-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f5a3c-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="f5a3c-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f5a3c-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f5a3c-117">L'indice specificato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5a3c-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5a3c-118">Remarks</span></span>

<span data-ttu-id="f5a3c-119">È necessario specificare un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="f5a3c-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a3c-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5a3c-120">Requirements</span></span>



| <span data-ttu-id="f5a3c-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5a3c-121">Requirement</span></span> | <span data-ttu-id="f5a3c-122">Valore</span><span class="sxs-lookup"><span data-stu-id="f5a3c-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a3c-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5a3c-123">Header</span></span><br/>  | <dl> <span data-ttu-id="f5a3c-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="f5a3c-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="f5a3c-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5a3c-125">Library</span></span><br/> | <dl> <span data-ttu-id="f5a3c-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5a3c-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5a3c-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5a3c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a3c-128">**Interfaccia IPortableDeviceKeyCollection**</span><span class="sxs-lookup"><span data-stu-id="f5a3c-128">**IPortableDeviceKeyCollection Interface**</span></span>](iportabledevicekeycollection.md)
</dt> </dl>

 

 




