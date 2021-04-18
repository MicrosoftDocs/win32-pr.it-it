---
description: Imposta l'esempio per l'origine del flusso multimediale.
ms.assetid: a35c5e18-f307-4e40-bc92-f91aa9eb80ba
title: 'Metodo IMFMediaStreamSourceSampleRequest:: sesample'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaStreamSourceSampleRequest.SetSample
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: bc3b2693a4690207f0b39d7f1b846e1e63069a8c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320681"
---
# <a name="imfmediastreamsourcesamplerequestsetsample-method"></a><span data-ttu-id="21a70-103">Metodo IMFMediaStreamSourceSampleRequest:: sesample</span><span class="sxs-lookup"><span data-stu-id="21a70-103">IMFMediaStreamSourceSampleRequest::SetSample method</span></span>

<span data-ttu-id="21a70-104">Imposta l'esempio per l'origine del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="21a70-104">Sets the sample for the media stream source.</span></span>

## <a name="syntax"></a><span data-ttu-id="21a70-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="21a70-105">Syntax</span></span>


```C++
HRESULT SetSample(
  [in] IMFSample *value
);
```



## <a name="parameters"></a><span data-ttu-id="21a70-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="21a70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21a70-107">*valore* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="21a70-107">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21a70-108">Esempio per l'origine del flusso multimediale.</span><span class="sxs-lookup"><span data-stu-id="21a70-108">The sample for the media stream source.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21a70-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="21a70-109">Return value</span></span>

<span data-ttu-id="21a70-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="21a70-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="21a70-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="21a70-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="21a70-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21a70-112">Requirements</span></span>



| <span data-ttu-id="21a70-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a70-113">Requirement</span></span> | <span data-ttu-id="21a70-114">Valore</span><span class="sxs-lookup"><span data-stu-id="21a70-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="21a70-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a70-115">Minimum supported client</span></span><br/> | <span data-ttu-id="21a70-116">App \[ desktop di Windows 8.1 app \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="21a70-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="21a70-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="21a70-117">Minimum supported server</span></span><br/> | <span data-ttu-id="21a70-118">App desktop di Windows Server 2012 R2 \[ \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="21a70-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                       |
| <span data-ttu-id="21a70-119">IDL</span><span class="sxs-lookup"><span data-stu-id="21a70-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="21a70-120"><dt>Mfidl. idl</dt></span><span class="sxs-lookup"><span data-stu-id="21a70-120"><dt>Mfidl.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21a70-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21a70-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a70-122">**IMFMediaStreamSourceSampleRequest**</span><span class="sxs-lookup"><span data-stu-id="21a70-122">**IMFMediaStreamSourceSampleRequest**</span></span>](imfmediastreamsourcesamplerequest.md)
</dt> </dl>

 

 




