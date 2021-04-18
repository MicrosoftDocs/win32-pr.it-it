---
description: Crea un oggetto della sessione di chiavi multimediali usando i dati di inizializzazione e i dati personalizzati specificati. .
ms.assetid: 9f11433c-7cff-4a59-9d4a-7f4b56ba62cf
title: 'Metodo IMFMediaKeys:: CreateSession'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFMediaKeys.CreateSession
api_type:
- COM
api_location:
- mfmediaengine.h
ms.openlocfilehash: 89d3abce0c1c15d472f7008fa0ef2c5f27bba6ad
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320736"
---
# <a name="imfmediakeyscreatesession-method"></a><span data-ttu-id="9f001-104">Metodo IMFMediaKeys:: CreateSession</span><span class="sxs-lookup"><span data-stu-id="9f001-104">IMFMediaKeys::CreateSession method</span></span>

<span data-ttu-id="9f001-105">Crea un oggetto della sessione di chiavi multimediali usando i dati di inizializzazione e i dati personalizzati specificati.</span><span class="sxs-lookup"><span data-stu-id="9f001-105">Creates a media key session object using the specified initialization data and custom data.</span></span> <span data-ttu-id="9f001-106">.</span><span class="sxs-lookup"><span data-stu-id="9f001-106">.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f001-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9f001-107">Syntax</span></span>


```C++
HRESULT CreateSession(
         BSTR                     mimeType,
   const BYTE                     *initData,
         DWORD                    cb,
   const BYTE                     *customData,
         DWORD                    cbCustomData,
         IMFMediaKeySessionNotify *notify,
         IMFMediaKeySession       **ppSession
);
```



## <a name="parameters"></a><span data-ttu-id="9f001-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="9f001-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f001-109">*mimeType*</span><span class="sxs-lookup"><span data-stu-id="9f001-109">*mimeType*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-110">Tipo MIME del contenitore multimediale utilizzato per il contenuto.</span><span class="sxs-lookup"><span data-stu-id="9f001-110">The MIME type of the media container used for the content.</span></span>

</dd> <dt>

<span data-ttu-id="9f001-111">*initData*</span><span class="sxs-lookup"><span data-stu-id="9f001-111">*initData*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-112">Dati di inizializzazione per il sistema di chiavi.</span><span class="sxs-lookup"><span data-stu-id="9f001-112">The initialization data for the key system.</span></span>

</dd> <dt>

<span data-ttu-id="9f001-113">*CB*</span><span class="sxs-lookup"><span data-stu-id="9f001-113">*cb*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-114">Conteggio in byte di *initData*.</span><span class="sxs-lookup"><span data-stu-id="9f001-114">The count in bytes of *initData*.</span></span>

</dd> <dt>

<span data-ttu-id="9f001-115">*customData*</span><span class="sxs-lookup"><span data-stu-id="9f001-115">*customData*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-116">Dati personalizzati inviati al sistema di chiavi.</span><span class="sxs-lookup"><span data-stu-id="9f001-116">Custom data sent to the key system.</span></span>

</dd> <dt>

<span data-ttu-id="9f001-117">*cbCustomData*</span><span class="sxs-lookup"><span data-stu-id="9f001-117">*cbCustomData*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-118">Conteggio in byte di *cbCustomData*.</span><span class="sxs-lookup"><span data-stu-id="9f001-118">The count in bytes of *cbCustomData*.</span></span>

</dd> <dt>

<span data-ttu-id="9f001-119">*comunica*</span><span class="sxs-lookup"><span data-stu-id="9f001-119">*notify*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-120">comunica</span><span class="sxs-lookup"><span data-stu-id="9f001-120">notify</span></span>

</dd> <dt>

<span data-ttu-id="9f001-121">*ppSession*</span><span class="sxs-lookup"><span data-stu-id="9f001-121">*ppSession*</span></span> 
</dt> <dd>

<span data-ttu-id="9f001-122">La sessione del tasto supporto.</span><span class="sxs-lookup"><span data-stu-id="9f001-122">The media key session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f001-123">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9f001-123">Return value</span></span>

<span data-ttu-id="9f001-124">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="9f001-124">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="9f001-125">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9f001-125">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f001-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9f001-126">Requirements</span></span>



| <span data-ttu-id="9f001-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f001-127">Requirement</span></span> | <span data-ttu-id="9f001-128">Valore</span><span class="sxs-lookup"><span data-stu-id="9f001-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f001-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f001-129">Minimum supported client</span></span><br/> | <span data-ttu-id="9f001-130">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="9f001-130">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="9f001-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="9f001-131">Minimum supported server</span></span><br/> | <span data-ttu-id="9f001-132">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9f001-132">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="9f001-133">IDL</span><span class="sxs-lookup"><span data-stu-id="9f001-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9f001-134"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9f001-134"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f001-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9f001-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f001-136">**IMFMediaKeys**</span><span class="sxs-lookup"><span data-stu-id="9f001-136">**IMFMediaKeys**</span></span>](/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys)
</dt> </dl>

 

 




