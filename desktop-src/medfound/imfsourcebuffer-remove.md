---
description: Rimuove i segmenti di supporto definiti dall'intervallo di tempo specificato da IMFSourceBuffer.
ms.assetid: 86536d73-18c0-4acc-81ec-72f1dfe400c5
title: 'Metodo IMFSourceBuffer:: Remove'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Remove
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: d82660d08efe651b321672b6ccd0cb475875beee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308746"
---
# <a name="imfsourcebufferremove-method"></a><span data-ttu-id="26675-103">Metodo IMFSourceBuffer:: Remove</span><span class="sxs-lookup"><span data-stu-id="26675-103">IMFSourceBuffer::Remove method</span></span>

<span data-ttu-id="26675-104">Rimuove i segmenti di supporto definiti dall'intervallo di tempo specificato da [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span><span class="sxs-lookup"><span data-stu-id="26675-104">Removes the media segments defined by the specified time range from the [**IMFSourceBuffer**](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer).</span></span>

## <a name="syntax"></a><span data-ttu-id="26675-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26675-105">Syntax</span></span>


```C++
HRESULT Remove(
  [in] double start,
  [in] double end
);
```



## <a name="parameters"></a><span data-ttu-id="26675-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26675-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26675-107">*inizio* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26675-107">*start* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26675-108">Inizio dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="26675-108">The start of the time range.</span></span>

</dd> <dt>

<span data-ttu-id="26675-109">*fine* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="26675-109">*end* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="26675-110">Fine dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="26675-110">The end of the time range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26675-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26675-111">Return value</span></span>

<span data-ttu-id="26675-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26675-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26675-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26675-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26675-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26675-114">Requirements</span></span>



| <span data-ttu-id="26675-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="26675-115">Requirement</span></span> | <span data-ttu-id="26675-116">Valore</span><span class="sxs-lookup"><span data-stu-id="26675-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26675-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26675-117">Minimum supported client</span></span><br/> | <span data-ttu-id="26675-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26675-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26675-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26675-119">Minimum supported server</span></span><br/> | <span data-ttu-id="26675-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="26675-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="26675-121">IDL</span><span class="sxs-lookup"><span data-stu-id="26675-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26675-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26675-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26675-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26675-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26675-124">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="26675-124">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




