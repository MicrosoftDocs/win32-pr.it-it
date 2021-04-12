---
title: Metodo IMediaRendererActionInformation PlaySpeeds
description: Recupera l'elenco completo dei valori PlaySpeed accettati da ricevitore.
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- API di streaming multimediale del metodo PlaySpeeds
- API di streaming multimediale del metodo PlaySpeeds, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo PlaySpeeds
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337278"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="c7165-106">IMediaRendererActionInformation::P metodo laySpeeds</span><span class="sxs-lookup"><span data-stu-id="c7165-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="c7165-107">Recupera l'elenco completo dei valori [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) accettati da ricevitore.</span><span class="sxs-lookup"><span data-stu-id="c7165-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7165-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c7165-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="c7165-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c7165-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7165-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="c7165-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c7165-111">Riceve un vettore di strutture [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) che specifica l'elenco completo dei valori **PlaySpeed** accettati da ricevitore.</span><span class="sxs-lookup"><span data-stu-id="c7165-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7165-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c7165-112">Return value</span></span>

<span data-ttu-id="c7165-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="c7165-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c7165-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="c7165-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c7165-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="c7165-115">Return code</span></span>                                                                          | <span data-ttu-id="c7165-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7165-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c7165-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c7165-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c7165-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="c7165-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="c7165-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c7165-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7165-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="c7165-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

