---
description: Rimuove il buffer di origine specificato dalla raccolta di buffer di origine gestiti dall'oggetto IMFMediaSourceExtension.
ms.assetid: 2f29cbac-4261-41ee-84c8-cb73686aeee5
title: 'Metodo IMFMediaSourceExtension:: RemoveSourceBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.RemoveSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 2a093401058895f31b29843778a18a040e722c33
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351516"
---
# <a name="imfmediasourceextensionremovesourcebuffer-method"></a><span data-ttu-id="85661-103">Metodo IMFMediaSourceExtension:: RemoveSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="85661-103">IMFMediaSourceExtension::RemoveSourceBuffer method</span></span>

<span data-ttu-id="85661-104">Rimuove il buffer di origine specificato dalla raccolta di buffer di origine gestiti dall'oggetto [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) .</span><span class="sxs-lookup"><span data-stu-id="85661-104">Removes the specified source buffer from the collection of source buffers managed by the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="85661-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="85661-105">Syntax</span></span>


```C++
HRESULT RemoveSourceBuffer(
  [in] IMFSourceBuffer *pSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="85661-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="85661-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85661-107">*pSourceBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85661-107">*pSourceBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85661-108">Buffer da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="85661-108">The buffer to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85661-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="85661-109">Return value</span></span>

<span data-ttu-id="85661-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="85661-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="85661-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="85661-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="85661-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="85661-112">Requirements</span></span>



| <span data-ttu-id="85661-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="85661-113">Requirement</span></span> | <span data-ttu-id="85661-114">Valore</span><span class="sxs-lookup"><span data-stu-id="85661-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="85661-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85661-115">Minimum supported client</span></span><br/> | <span data-ttu-id="85661-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="85661-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="85661-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="85661-117">Minimum supported server</span></span><br/> | <span data-ttu-id="85661-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="85661-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="85661-119">IDL</span><span class="sxs-lookup"><span data-stu-id="85661-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="85661-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="85661-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85661-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="85661-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85661-122">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="85661-122">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




