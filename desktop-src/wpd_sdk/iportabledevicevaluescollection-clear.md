---
description: Il metodo Clear rilascia tutti gli elementi della raccolta.
ms.assetid: 151d1f61-11f0-40f0-8da1-79e9eb2001ce
title: 'Metodo IPortableDeviceValuesCollection:: Clear (PortableDeviceTypes. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPortableDeviceValuesCollection.Clear
api_type:
- COM
api_location:
- PortableDeviceGUIDs.lib
- PortableDeviceGUIDs.dll
ms.openlocfilehash: bf826b8e8a2035a0d84aec76979616fcccee9948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324510"
---
# <a name="iportabledevicevaluescollectionclear-method"></a><span data-ttu-id="66d86-103">Metodo IPortableDeviceValuesCollection:: Clear</span><span class="sxs-lookup"><span data-stu-id="66d86-103">IPortableDeviceValuesCollection::Clear method</span></span>

<span data-ttu-id="66d86-104">Il metodo **Clear** rilascia tutti gli elementi della raccolta.</span><span class="sxs-lookup"><span data-stu-id="66d86-104">The **Clear** method releases all items from the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="66d86-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="66d86-105">Syntax</span></span>


```C++
HRESULT Clear();
```



## <a name="parameters"></a><span data-ttu-id="66d86-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="66d86-106">Parameters</span></span>

<span data-ttu-id="66d86-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="66d86-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="66d86-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="66d86-108">Return value</span></span>

<span data-ttu-id="66d86-109">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="66d86-109">The method returns an **HRESULT**.</span></span> <span data-ttu-id="66d86-110">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="66d86-110">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="66d86-111">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="66d86-111">Return code</span></span>                                                                          | <span data-ttu-id="66d86-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="66d86-112">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="66d86-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="66d86-113"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="66d86-114">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="66d86-114">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="66d86-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="66d86-115">Remarks</span></span>

<span data-ttu-id="66d86-116">Il metodo rilascia tutta la memoria allocata per gli elementi nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="66d86-116">The method releases all memory that is allocated for the items in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="66d86-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="66d86-117">Requirements</span></span>



| <span data-ttu-id="66d86-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="66d86-118">Requirement</span></span> | <span data-ttu-id="66d86-119">Valore</span><span class="sxs-lookup"><span data-stu-id="66d86-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66d86-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="66d86-120">Header</span></span><br/>  | <dl> <span data-ttu-id="66d86-121"><dt>PortableDeviceTypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="66d86-121"><dt>PortableDeviceTypes.h</dt></span></span> </dl>   |
| <span data-ttu-id="66d86-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="66d86-122">Library</span></span><br/> | <dl> <span data-ttu-id="66d86-123"><dt>PortableDeviceGUIDs. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66d86-123"><dt>PortableDeviceGUIDs.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66d86-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="66d86-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66d86-125">**Interfaccia IPortableDeviceValuesCollection**</span><span class="sxs-lookup"><span data-stu-id="66d86-125">**IPortableDeviceValuesCollection Interface**</span></span>](iportabledevicevaluescollection.md)
</dt> </dl>

 

 




