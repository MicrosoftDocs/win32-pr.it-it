---
title: Metodo IMediaRendererActionInformation IsVolumeAvailable
description: Recupera un valore che indica se ricevitore è in grado di regolare il livello del volume audio.
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- API di streaming multimediale del metodo IsVolumeAvailable
- API di streaming multimediale del metodo IsVolumeAvailable, interfaccia IMediaRendererActionInformation
- API di streaming multimediale dell'interfaccia IMediaRendererActionInformation, metodo IsVolumeAvailable
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117619"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="02eab-106">Metodo IMediaRendererActionInformation:: IsVolumeAvailable</span><span class="sxs-lookup"><span data-stu-id="02eab-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="02eab-107">Recupera un valore che indica se ricevitore è in grado di regolare il livello del volume audio.</span><span class="sxs-lookup"><span data-stu-id="02eab-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="02eab-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="02eab-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="02eab-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="02eab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02eab-110">*valore* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="02eab-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="02eab-111">Valore booleano che è **true** se ricevitore è in grado di regolare il livello del volume audio e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="02eab-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02eab-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="02eab-112">Return value</span></span>

<span data-ttu-id="02eab-113">Il metodo restituisce un valore **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="02eab-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="02eab-114">I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.</span><span class="sxs-lookup"><span data-stu-id="02eab-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="02eab-115">Codice restituito</span><span class="sxs-lookup"><span data-stu-id="02eab-115">Return code</span></span>                                                                          | <span data-ttu-id="02eab-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="02eab-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="02eab-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="02eab-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="02eab-118">Il metodo è riuscito.</span><span class="sxs-lookup"><span data-stu-id="02eab-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="02eab-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="02eab-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02eab-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="02eab-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

