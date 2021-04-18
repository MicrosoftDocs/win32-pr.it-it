---
title: Metodo IMediaRenderer IsImageSupported
description: Recupera un valore che indica se ricevitore è in grado di visualizzare le immagini.
ms.assetid: 3941789B-0FFF-4F00-B63C-2586B39B6546
keywords:
- API di streaming multimediale del metodo IsImageSupported
- API di streaming multimediale del metodo IsImageSupported, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo IsImageSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsImageSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd68f4d758c67b81c1eefcbc83a0f0a505ec27b6
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299225"
---
# <a name="imediarendererisimagesupported-method"></a><span data-ttu-id="f29c9-106">Metodo IMediaRenderer:: IsImageSupported</span><span class="sxs-lookup"><span data-stu-id="f29c9-106">IMediaRenderer::IsImageSupported method</span></span>

<span data-ttu-id="f29c9-107">Recupera un valore che indica se ricevitore è in grado di visualizzare le immagini.</span><span class="sxs-lookup"><span data-stu-id="f29c9-107">Retrieves a value that indicates whether the DMR is capable of displaying images.</span></span>

## <a name="syntax"></a><span data-ttu-id="f29c9-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f29c9-108">Syntax</span></span>


```C++
HRESULT IsImageSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f29c9-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f29c9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f29c9-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f29c9-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f29c9-111">Valore booleano che è **true** se ricevitore è in grado di visualizzare le immagini e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f29c9-111">A boolean value that is **True** if the DMR is capable of displaying images and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f29c9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f29c9-112">Return value</span></span>

<span data-ttu-id="f29c9-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f29c9-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f29c9-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f29c9-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f29c9-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f29c9-115">Return code</span></span>                                                                          | <span data-ttu-id="f29c9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f29c9-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f29c9-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f29c9-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f29c9-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f29c9-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f29c9-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f29c9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f29c9-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="f29c9-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





