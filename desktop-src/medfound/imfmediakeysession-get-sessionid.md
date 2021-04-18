---
description: Ottiene un ID di sessione univoco creato per questa sessione.
ms.assetid: 779ebea9-69ff-469a-8ee0-06d570ede6cb
title: 'Metodo IMFMediaKeySession:: get_SessionId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.get_SessionId
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 7110dbe6c24d1189019fb242621c7e3c01253264
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320572"
---
# <a name="imfmediakeysessionget_sessionid-method"></a><span data-ttu-id="2dac8-103">Metodo IMFMediaKeySession:: Get \_ SessionID</span><span class="sxs-lookup"><span data-stu-id="2dac8-103">IMFMediaKeySession::get\_SessionId method</span></span>

<span data-ttu-id="2dac8-104">Ottiene un ID di sessione univoco creato per questa sessione.</span><span class="sxs-lookup"><span data-stu-id="2dac8-104">Gets a unique session id created for this session.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dac8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2dac8-105">Syntax</span></span>


```C++
HRESULT get_SessionId(
   BSTR *sessionId
);
```



## <a name="parameters"></a><span data-ttu-id="2dac8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2dac8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dac8-107">*sessionId*</span><span class="sxs-lookup"><span data-stu-id="2dac8-107">*sessionId*</span></span> 
</dt> <dd>

<span data-ttu-id="2dac8-108">ID della sessione chiave multimediale.</span><span class="sxs-lookup"><span data-stu-id="2dac8-108">The media key session id.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dac8-109">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2dac8-109">Return value</span></span>

<span data-ttu-id="2dac8-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="2dac8-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="2dac8-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="2dac8-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="2dac8-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2dac8-112">Requirements</span></span>



| <span data-ttu-id="2dac8-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2dac8-113">Requirement</span></span> | <span data-ttu-id="2dac8-114">Valore</span><span class="sxs-lookup"><span data-stu-id="2dac8-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dac8-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dac8-115">Minimum supported client</span></span><br/> | <span data-ttu-id="2dac8-116">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2dac8-116">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2dac8-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2dac8-117">Minimum supported server</span></span><br/> | <span data-ttu-id="2dac8-118">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2dac8-118">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="2dac8-119">IDL</span><span class="sxs-lookup"><span data-stu-id="2dac8-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2dac8-120"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2dac8-120"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2dac8-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2dac8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dac8-122">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="2dac8-122">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




