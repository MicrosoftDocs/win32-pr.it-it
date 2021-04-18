---
description: Ottiene lo stato di errore associato alla sessione del tasto multimediale.
ms.assetid: 4693b7d5-59ee-472f-83fc-1ecbcc165dac
title: 'Metodo IMFMediaKeySession:: GetError'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeySession.GetError
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 4f0a42601698a9cd62dc6cb23ca9e69ac2cc8a49
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320789"
---
# <a name="imfmediakeysessiongeterror-method"></a><span data-ttu-id="4c4cc-103">Metodo IMFMediaKeySession:: GetError</span><span class="sxs-lookup"><span data-stu-id="4c4cc-103">IMFMediaKeySession::GetError method</span></span>

<span data-ttu-id="4c4cc-104">Ottiene lo stato di errore associato alla sessione del tasto multimediale.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-104">Gets the error state associated with the media key session.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c4cc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c4cc-105">Syntax</span></span>


```C++
HRESULT GetError(
   USHORT *code,
   DWORD  *systemCode
);
```



## <a name="parameters"></a><span data-ttu-id="4c4cc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c4cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c4cc-107">*code*</span><span class="sxs-lookup"><span data-stu-id="4c4cc-107">*code*</span></span> 
</dt> <dd>

<span data-ttu-id="4c4cc-108">Codice di errore.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-108">The error code.</span></span>

</dd> <dt>

<span data-ttu-id="4c4cc-109">*systemCode*</span><span class="sxs-lookup"><span data-stu-id="4c4cc-109">*systemCode*</span></span> 
</dt> <dd>

<span data-ttu-id="4c4cc-110">Informazioni sugli errori specifici della piattaforma.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-110">Platform specific error information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c4cc-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c4cc-111">Return value</span></span>

<span data-ttu-id="4c4cc-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="4c4cc-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4c4cc-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4c4cc-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c4cc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c4cc-114">Requirements</span></span>



| <span data-ttu-id="4c4cc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c4cc-115">Requirement</span></span> | <span data-ttu-id="4c4cc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="4c4cc-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="4c4cc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c4cc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4c4cc-118">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="4c4cc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4c4cc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4c4cc-120">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="4c4cc-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4c4cc-121">IDL</span><span class="sxs-lookup"><span data-stu-id="4c4cc-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4c4cc-122"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4c4cc-122"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c4cc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c4cc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c4cc-124">**IMFMediaKeySession**</span><span class="sxs-lookup"><span data-stu-id="4c4cc-124">**IMFMediaKeySession**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeysession)
</dt> </dl>

 

 




