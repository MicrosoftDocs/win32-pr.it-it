---
title: Metodo IMediaRendererActionInformation IsMuteAvailable
description: Recupera un valore che indica se ricevitore è in grado di tacitare l'audio.
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- API di streaming multimediale del metodo IsMuteAvailable
- API di streaming multimediale del metodo IsMuteAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsMuteAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046631"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="f9ecc-106">Metodo IMediaRendererActionInformation:: IsMuteAvailable</span><span class="sxs-lookup"><span data-stu-id="f9ecc-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="f9ecc-107">Recupera un valore che indica se ricevitore è in grado di tacitare l'audio.</span><span class="sxs-lookup"><span data-stu-id="f9ecc-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ecc-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f9ecc-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="f9ecc-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="f9ecc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ecc-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="f9ecc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9ecc-111">Valore booleano che è **true** se ricevitore è in grado di disattivare l'audio e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="f9ecc-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ecc-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f9ecc-112">Return value</span></span>

<span data-ttu-id="f9ecc-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f9ecc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f9ecc-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="f9ecc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f9ecc-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="f9ecc-115">Return code</span></span>                                                                          | <span data-ttu-id="f9ecc-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f9ecc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f9ecc-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f9ecc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f9ecc-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="f9ecc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="f9ecc-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f9ecc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ecc-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="f9ecc-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

