---
title: Metodo IMediaRenderer IsVideoSupported
description: Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto video.
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- API di streaming multimediale del metodo IsVideoSupported
- API di streaming multimediale del metodo IsVideoSupported, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo IsVideoSupported
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104334628"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="390ff-106">Metodo IMediaRenderer:: IsVideoSupported</span><span class="sxs-lookup"><span data-stu-id="390ff-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="390ff-107">Recupera un valore che indica se ricevitore è in grado di riprodurre contenuto video.</span><span class="sxs-lookup"><span data-stu-id="390ff-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="390ff-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="390ff-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="390ff-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="390ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="390ff-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="390ff-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="390ff-111">Valore booleano che è **true** se ricevitore è in grado di riprodurre contenuto video e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="390ff-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="390ff-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="390ff-112">Return value</span></span>

<span data-ttu-id="390ff-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="390ff-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="390ff-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="390ff-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="390ff-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="390ff-115">Return code</span></span>                                                                          | <span data-ttu-id="390ff-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="390ff-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="390ff-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="390ff-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="390ff-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="390ff-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="390ff-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="390ff-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="390ff-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="390ff-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





