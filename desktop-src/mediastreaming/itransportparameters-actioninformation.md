---
title: Metodo ITransportParameters ActionInformation
description: Ottiene un'interfaccia IMediaRendererActionInformation che fornisce informazioni sui metodi che possono essere attualmente richiamati in ricevitore.
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- API di streaming multimediale del metodo ActionInformation
- API di streaming multimediale del metodo ActionInformation, interfaccia ITransportParameters
- API di streaming multimediale dell'interfaccia ITransportParameters, metodo ActionInformation
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046644"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="79d5f-106">Metodo ITransportParameters:: ActionInformation</span><span class="sxs-lookup"><span data-stu-id="79d5f-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="79d5f-107">Ottiene un'interfaccia [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) che fornisce informazioni sui metodi che possono essere attualmente richiamati in ricevitore.</span><span class="sxs-lookup"><span data-stu-id="79d5f-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="79d5f-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="79d5f-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="79d5f-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="79d5f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79d5f-110">*valore* \[ di out, retval\]</span><span class="sxs-lookup"><span data-stu-id="79d5f-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="79d5f-111">Riceve un riferimento a un'interfaccia [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) .</span><span class="sxs-lookup"><span data-stu-id="79d5f-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79d5f-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="79d5f-112">Return value</span></span>

<span data-ttu-id="79d5f-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="79d5f-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="79d5f-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="79d5f-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="79d5f-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="79d5f-115">Return code</span></span>                                                                          | <span data-ttu-id="79d5f-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="79d5f-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="79d5f-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="79d5f-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="79d5f-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="79d5f-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="79d5f-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="79d5f-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79d5f-120">**ITransportParameters**</span><span class="sxs-lookup"><span data-stu-id="79d5f-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

