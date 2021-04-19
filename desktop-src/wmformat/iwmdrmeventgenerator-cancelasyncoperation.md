---
title: Metodo IWMDRMEventGenerator CancelAsyncOperation (wmdrmsdk. h)
description: Il metodo CancelAsyncOperation Annulla un'operazione asincrona.
ms.assetid: 95c59e03-b6c8-40c2-b1dc-381cb6d8d558
keywords:
- Metodo CancelAsyncOperation Windows Media Format
- Metodo CancelAsyncOperation Windows Media Format, interfaccia IWMDRMEventGenerator
- Interfaccia IWMDRMEventGenerator-formato Windows Media, metodo CancelAsyncOperation
topic_type:
- apiref
api_name:
- IWMDRMEventGenerator.CancelAsyncOperation
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1223f56e820eb5927eeb972f28056baa14824774
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328535"
---
# <a name="iwmdrmeventgeneratorcancelasyncoperation-method"></a><span data-ttu-id="bdc19-106">Metodo IWMDRMEventGenerator:: CancelAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="bdc19-106">IWMDRMEventGenerator::CancelAsyncOperation method</span></span>

<span data-ttu-id="bdc19-107">Il metodo **CancelAsyncOperation** Annulla un'operazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="bdc19-107">The **CancelAsyncOperation** method cancels an asynchronous operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdc19-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bdc19-108">Syntax</span></span>


```C++
HRESULT CancelAsyncOperation(
  [in] IUnknown *punkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="bdc19-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="bdc19-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdc19-110">*punkCancelationCookie* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdc19-110">*punkCancelationCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdc19-111">Puntatore al cookie di annullamento che identifica l'operazione asincrona da annullare.</span><span class="sxs-lookup"><span data-stu-id="bdc19-111">Pointer to the cancellation cookie that identifies the asynchronous operation to be canceled.</span></span> <span data-ttu-id="bdc19-112">Questo cookie viene fornito dal metodo utilizzato per avviare l'operazione.</span><span class="sxs-lookup"><span data-stu-id="bdc19-112">This cookie is provided by the method used to start the operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdc19-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="bdc19-113">Return value</span></span>

<span data-ttu-id="bdc19-114">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="bdc19-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bdc19-115">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="bdc19-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bdc19-116">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="bdc19-116">Return code</span></span>                                                                          | <span data-ttu-id="bdc19-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdc19-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bdc19-118"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bdc19-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bdc19-119">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="bdc19-119">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bdc19-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="bdc19-120">Remarks</span></span>

<span data-ttu-id="bdc19-121">Nessuna.</span><span class="sxs-lookup"><span data-stu-id="bdc19-121">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdc19-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bdc19-122">Requirements</span></span>



| <span data-ttu-id="bdc19-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdc19-123">Requirement</span></span> | <span data-ttu-id="bdc19-124">Valore</span><span class="sxs-lookup"><span data-stu-id="bdc19-124">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bdc19-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="bdc19-125">Header</span></span><br/>  | <dl> <span data-ttu-id="bdc19-126"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdc19-126"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdc19-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="bdc19-127">Library</span></span><br/> | <dl> <span data-ttu-id="bdc19-128"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdc19-128"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdc19-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bdc19-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdc19-130">**Interfaccia IWMDRMEventGenerator**</span><span class="sxs-lookup"><span data-stu-id="bdc19-130">**IWMDRMEventGenerator Interface**</span></span>](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





