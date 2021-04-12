---
title: Metodo GetStreamPropertiesOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da GetStreamPropertiesAsync.
ms.assetid: D09DCDF5-2B9E-4E03-908B-AEEC7DC228C1
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia GetStreamPropertiesOperation
- API di streaming multimediale dell'interfaccia GetStreamPropertiesOperation, metodo GetResults
topic_type:
- apiref
api_name:
- GetStreamPropertiesOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 312703c28f5cdbb888b46d6ccd312dd358aa6b6b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398943"
---
# <a name="getstreampropertiesoperationgetresults-method"></a><span data-ttu-id="117a8-106">Metodo GetStreamPropertiesOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="117a8-106">GetStreamPropertiesOperation.GetResults method</span></span>

<span data-ttu-id="117a8-107">Restituisce i risultati dell'operazione asincrona avviata da [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="117a8-107">Returns the results of the asynchronous operation started by [**GetStreamPropertiesAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="117a8-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="117a8-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="117a8-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="117a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="117a8-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="117a8-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="117a8-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="117a8-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="117a8-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="117a8-112">Return value</span></span>

<span data-ttu-id="117a8-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="117a8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="117a8-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="117a8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="117a8-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="117a8-115">Return code</span></span>                                                                          | <span data-ttu-id="117a8-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="117a8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="117a8-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="117a8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="117a8-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="117a8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="117a8-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="117a8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="117a8-120">**GetStreamPropertiesOperation**</span><span class="sxs-lookup"><span data-stu-id="117a8-120">**GetStreamPropertiesOperation**</span></span>](getstreampropertiesoperation.md)
</dt> </dl>

 

