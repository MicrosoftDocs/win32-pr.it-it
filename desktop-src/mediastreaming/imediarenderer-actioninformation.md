---
title: Metodo IMediaRenderer ActionInformation
description: Recupera informazioni sui metodi che possono essere attualmente richiamati in ricevitore.
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- API di streaming multimediale del metodo ActionInformation
- API di streaming multimediale del metodo ActionInformation, interfaccia IMediaRenderer
- API di streaming multimediale dell'interfaccia IMediaRenderer, metodo ActionInformation
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046659"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="e7bae-106">Metodo IMediaRenderer:: ActionInformation</span><span class="sxs-lookup"><span data-stu-id="e7bae-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="e7bae-107">Recupera informazioni sui metodi che possono essere attualmente richiamati in ricevitore.</span><span class="sxs-lookup"><span data-stu-id="e7bae-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bae-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e7bae-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="e7bae-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="e7bae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bae-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="e7bae-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bae-111">Riceve un riferimento a un'interfaccia [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="e7bae-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bae-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e7bae-112">Return value</span></span>

<span data-ttu-id="e7bae-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="e7bae-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e7bae-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="e7bae-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e7bae-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="e7bae-115">Return code</span></span>                                                                          | <span data-ttu-id="e7bae-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e7bae-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e7bae-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e7bae-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e7bae-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="e7bae-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e7bae-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e7bae-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bae-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="e7bae-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

