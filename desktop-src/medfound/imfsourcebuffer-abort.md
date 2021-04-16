---
description: Interrompe l'elaborazione del segmento multimediale corrente.
ms.assetid: 31253d0d-c53f-47bd-823a-fc564cb63b78
title: 'Metodo IMFSourceBuffer:: Abort'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFSourceBuffer.Abort
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 3a8b5115032fb918af66094bb87c7118eb503da3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527679"
---
# <a name="imfsourcebufferabort-method"></a><span data-ttu-id="26ee3-103">Metodo IMFSourceBuffer:: Abort</span><span class="sxs-lookup"><span data-stu-id="26ee3-103">IMFSourceBuffer::Abort method</span></span>

<span data-ttu-id="26ee3-104">Interrompe l'elaborazione del segmento multimediale corrente.</span><span class="sxs-lookup"><span data-stu-id="26ee3-104">Aborts the processing of the current media segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="26ee3-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="26ee3-105">Syntax</span></span>


```C++
HRESULT Abort();
```



## <a name="parameters"></a><span data-ttu-id="26ee3-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="26ee3-106">Parameters</span></span>

<span data-ttu-id="26ee3-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="26ee3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="26ee3-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="26ee3-108">Return value</span></span>

<span data-ttu-id="26ee3-109">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="26ee3-109">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="26ee3-110">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="26ee3-110">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="26ee3-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="26ee3-111">Requirements</span></span>



| <span data-ttu-id="26ee3-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="26ee3-112">Requirement</span></span> | <span data-ttu-id="26ee3-113">Valore</span><span class="sxs-lookup"><span data-stu-id="26ee3-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="26ee3-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26ee3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="26ee3-115">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="26ee3-115">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="26ee3-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="26ee3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="26ee3-117">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="26ee3-117">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="26ee3-118">IDL</span><span class="sxs-lookup"><span data-stu-id="26ee3-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="26ee3-119"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="26ee3-119"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26ee3-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="26ee3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26ee3-121">**IMFSourceBuffer**</span><span class="sxs-lookup"><span data-stu-id="26ee3-121">**IMFSourceBuffer**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfsourcebuffer)
</dt> </dl>

 

 




