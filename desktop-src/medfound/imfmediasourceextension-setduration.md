---
description: Imposta la durata dell'origine multimediale in unità 100-nanosecondi.
ms.assetid: dc3dc600-ca81-40da-9edb-0af283ba9221
title: 'Metodo IMFMediaSourceExtension:: seduration'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.SetDuration
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: ae669bf19f531034eacafac7fb89f3c07fa1e0e9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320682"
---
# <a name="imfmediasourceextensionsetduration-method"></a><span data-ttu-id="9a5c3-103">Metodo IMFMediaSourceExtension:: seduration</span><span class="sxs-lookup"><span data-stu-id="9a5c3-103">IMFMediaSourceExtension::SetDuration method</span></span>

<span data-ttu-id="9a5c3-104">Imposta la durata dell'origine multimediale in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9a5c3-104">Sets the duration of the media source in 100-nanosecond units.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a5c3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9a5c3-105">Syntax</span></span>


```C++
HRESULT SetDuration(
  [in] double duration
);
```



## <a name="parameters"></a><span data-ttu-id="9a5c3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9a5c3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a5c3-107">*durata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9a5c3-107">*duration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9a5c3-108">Durata dell'origine del supporto in unità 100-nanosecondi.</span><span class="sxs-lookup"><span data-stu-id="9a5c3-108">The duration of the media source in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a5c3-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9a5c3-109">Return value</span></span>

<span data-ttu-id="9a5c3-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9a5c3-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9a5c3-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9a5c3-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a5c3-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9a5c3-112">Requirements</span></span>



| <span data-ttu-id="9a5c3-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a5c3-113">Requirement</span></span> | <span data-ttu-id="9a5c3-114">Valore</span><span class="sxs-lookup"><span data-stu-id="9a5c3-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a5c3-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a5c3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="9a5c3-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9a5c3-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9a5c3-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9a5c3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="9a5c3-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9a5c3-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9a5c3-119">IDL</span><span class="sxs-lookup"><span data-stu-id="9a5c3-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a5c3-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a5c3-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a5c3-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9a5c3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a5c3-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="9a5c3-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




