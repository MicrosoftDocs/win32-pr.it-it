---
description: "Metodo IPortableDeviceValuesCollection::RemoveAt: il metodo RemoveAt rimuove l'elemento archiviato nella posizione specificata dall'indice specificato."
ms.assetid: 380212b6-5e71-406b-8236-e06672505f17
title: Metodo IPortableDeviceValuesCollection::RemoveAt (PortableDeviceTypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.RemoveAt
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: 7db15480906bee8181bb0fc589c4f3e30ce4753c
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083169"
---
# <a name="iportabledevicevaluescollectionremoveat-method"></a><span data-ttu-id="62b52-103">Metodo IPortableDeviceValuesCollection::RemoveAt</span><span class="sxs-lookup"><span data-stu-id="62b52-103">IPortableDeviceValuesCollection::RemoveAt method</span></span>

<span data-ttu-id="62b52-104">Il **metodo RemoveAt** rimuove l'elemento archiviato nella posizione specificata dall'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="62b52-104">The **RemoveAt** method removes the element stored at the location specified by the given index.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b52-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62b52-105">Syntax</span></span>


```C++
HRESULT RemoveAt(
  [in] const DWORD dwIndex
);
```



## <a name="parameters"></a><span data-ttu-id="62b52-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="62b52-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62b52-107">*dwIndex* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="62b52-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62b52-108">Specifica l'indice dell'elemento da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="62b52-108">Specifies the index of the element to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62b52-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="62b52-109">Return value</span></span>

<span data-ttu-id="62b52-110">Il metodo restituisce un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="62b52-110">The method returns an **HRESULT**.</span></span> <span data-ttu-id="62b52-111">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="62b52-111">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="62b52-112">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="62b52-112">Return code</span></span>                                                                                  | <span data-ttu-id="62b52-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62b52-113">Description</span></span>                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="62b52-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="62b52-114"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="62b52-115">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="62b52-115">The method succeeded.</span></span><br/>                 |
| <dl> <span data-ttu-id="62b52-116"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="62b52-116"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="62b52-117">L'indice specificato non è compreso nell'intervallo.</span><span class="sxs-lookup"><span data-stu-id="62b52-117">The specified index was out of range.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62b52-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="62b52-118">Remarks</span></span>

<span data-ttu-id="62b52-119">È necessario specificare un indice in base zero.</span><span class="sxs-lookup"><span data-stu-id="62b52-119">You must specify a zero-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b52-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="62b52-120">Requirements</span></span>



| <span data-ttu-id="62b52-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="62b52-121">Requirement</span></span> | <span data-ttu-id="62b52-122">Valore</span><span class="sxs-lookup"><span data-stu-id="62b52-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b52-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="62b52-123">Header</span></span><br/>  | <dl> <span data-ttu-id="62b52-124"><dt>PortableDeviceTypes.h</dt></span><span class="sxs-lookup"><span data-stu-id="62b52-124"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="62b52-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="62b52-125">Library</span></span><br/> | <dl> <span data-ttu-id="62b52-126"><dt>PortableDeviceGUIDs.lib</dt></span><span class="sxs-lookup"><span data-stu-id="62b52-126"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b52-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="62b52-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b52-128">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="62b52-128">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




