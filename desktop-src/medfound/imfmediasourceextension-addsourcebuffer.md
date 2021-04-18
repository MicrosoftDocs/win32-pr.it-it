---
description: Aggiunge un IMFSourceBuffer all'insieme di buffer associato a IMFMediaSourceExtension.
ms.assetid: 1ecb7047-4dc9-4657-8a19-12108de299c0
title: 'Metodo IMFMediaSourceExtension:: AddSourceBuffer'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaSourceExtension.AddSourceBuffer
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: a62a62d8cf11afaa0190ac442f84b00cfe23517b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320570"
---
# <a name="imfmediasourceextensionaddsourcebuffer-method"></a><span data-ttu-id="027dc-103">Metodo IMFMediaSourceExtension:: AddSourceBuffer</span><span class="sxs-lookup"><span data-stu-id="027dc-103">IMFMediaSourceExtension::AddSourceBuffer method</span></span>

<span data-ttu-id="027dc-104">Aggiunge un [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) all'insieme di buffer associato a [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span><span class="sxs-lookup"><span data-stu-id="027dc-104">Adds a [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer) to the collection of buffers associated with the [**IMFMediaSourceExtension**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension).</span></span>

## <a name="syntax"></a><span data-ttu-id="027dc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="027dc-105">Syntax</span></span>


```C++
HRESULT AddSourceBuffer(
  [in]  BSTR                  type,
  [in]  IMFSourceBufferNotify *pNotify,
  [out] IMFSourceBuffer       **ppSourceBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="027dc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="027dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="027dc-107">*tipo* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="027dc-107">*type* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="027dc-108">*pNotify* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="027dc-108">*pNotify* \[in\]</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="027dc-109">*ppSourceBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="027dc-109">*ppSourceBuffer* \[out\]</span></span>
<span data-ttu-id="027dc-110"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="027dc-110"></dt> <dd></dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="027dc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="027dc-111">Return value</span></span>

<span data-ttu-id="027dc-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="027dc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="027dc-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="027dc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="027dc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="027dc-114">Requirements</span></span>



| <span data-ttu-id="027dc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="027dc-115">Requirement</span></span> | <span data-ttu-id="027dc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="027dc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="027dc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027dc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="027dc-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="027dc-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="027dc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="027dc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="027dc-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="027dc-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="027dc-121">IDL</span><span class="sxs-lookup"><span data-stu-id="027dc-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="027dc-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="027dc-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="027dc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="027dc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="027dc-124">**IMFMediaSourceExtension**</span><span class="sxs-lookup"><span data-stu-id="027dc-124">**IMFMediaSourceExtension**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediasourceextension)
</dt> </dl>

 

 




