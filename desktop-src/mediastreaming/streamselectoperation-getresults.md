---
title: Metodo StreamSelectOperation. GetResults
description: Restituisce i risultati dell'operazione asincrona avviata da SelectBestStreamAsync.
ms.assetid: 2D9887E7-17C8-4161-984F-FA44591D2052
keywords:
- API di streaming multimediale metodo GetResults
- API di streaming multimediale del metodo GetResults, interfaccia StreamSelectOperation
- API di streaming multimediale dell'interfaccia StreamSelectOperation, metodo GetResults
topic_type:
- apiref
api_name:
- StreamSelectOperation.GetResults
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c52479949413d32ca54654f355a06a2dee70866e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299666"
---
# <a name="streamselectoperationgetresults-method"></a><span data-ttu-id="8a080-106">Metodo StreamSelectOperation. GetResults</span><span class="sxs-lookup"><span data-stu-id="8a080-106">StreamSelectOperation.GetResults method</span></span>

<span data-ttu-id="8a080-107">Restituisce i risultati dell'operazione asincrona avviata da [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="8a080-107">Returns the results of the asynchronous operation started by [**SelectBestStreamAsync**](/previous-versions/windows/desktop/legacy/hh829001(v=vs.85)).</span></span>

## <a name="syntax"></a><span data-ttu-id="8a080-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8a080-108">Syntax</span></span>


```C++
HRESULT GetResults(
  [out, retval] UINT32 *value
);
```



## <a name="parameters"></a><span data-ttu-id="8a080-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="8a080-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a080-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="8a080-110">*value* \[out, retval\]</span></span>
<span data-ttu-id="8a080-111"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="8a080-111"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="8a080-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8a080-112">Return value</span></span>

<span data-ttu-id="8a080-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="8a080-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8a080-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="8a080-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8a080-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="8a080-115">Return code</span></span>                                                                          | <span data-ttu-id="8a080-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a080-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8a080-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="8a080-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8a080-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="8a080-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="8a080-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8a080-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a080-120">**StreamSelectOperation**</span><span class="sxs-lookup"><span data-stu-id="8a080-120">**StreamSelectOperation**</span></span>](streamselectoperation.md)
</dt> </dl>

 

