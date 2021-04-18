---
description: Inizia l'elaborazione per creare un'immagine decodificata.
ms.assetid: 80471cc6-c66d-49d9-8593-780e41ac39b9
title: 'Metodo IDirect3DDXVADevice9:: BeginFrame (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.BeginFrame
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3090d7868316d08fa91f36dffcc938eb31e06a7d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310839"
---
# <a name="idirect3ddxvadevice9beginframe-method"></a><span data-ttu-id="3e2e7-103">Metodo IDirect3DDXVADevice9:: BeginFrame</span><span class="sxs-lookup"><span data-stu-id="3e2e7-103">IDirect3DDXVADevice9::BeginFrame method</span></span>

<span data-ttu-id="3e2e7-104">Inizia l'elaborazione per creare un'immagine decodificata.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-104">Begins the processing to create a decoded picture.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2e7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3e2e7-105">Syntax</span></span>


```C++
HRESULT BeginFrame(
   IDirect3DSurface9 *pDstSurface,
   DWORD             SizeInputData,
   VOID              *pInputData,
   DWORD             *pSizeOutputData,
   VOID              *pOutputData
);
```



## <a name="parameters"></a><span data-ttu-id="3e2e7-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3e2e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2e7-107">*pDstSurface*</span><span class="sxs-lookup"><span data-stu-id="3e2e7-107">*pDstSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="3e2e7-108">Puntatore all'interfaccia **IDirect3DSurface9** della superficie di destinazione non compressa.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-108">A pointer to the **IDirect3DSurface9** interface of the uncompressed destination surface.</span></span>

</dd> <dt>

<span data-ttu-id="3e2e7-109">*SizeInputData*</span><span class="sxs-lookup"><span data-stu-id="3e2e7-109">*SizeInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="3e2e7-110">Dimensioni del buffer specificato da *pInputData*, in byte.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-110">The size of the buffer specified by *pInputData*, in bytes.</span></span> <span data-ttu-id="3e2e7-111">Il valore deve essere 2.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-111">The value must be 2.</span></span>

</dd> <dt>

<span data-ttu-id="3e2e7-112">*pInputData*</span><span class="sxs-lookup"><span data-stu-id="3e2e7-112">*pInputData*</span></span> 
</dt> <dd>

<span data-ttu-id="3e2e7-113">Puntatore a un buffer che contiene i dati per il tasto di scelta rapida del video.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-113">Pointer to a buffer that contains data for the video accelerator.</span></span> <span data-ttu-id="3e2e7-114">Questo buffer deve contenere l'indice del frame in base zero, specificato come valore di **parola** .</span><span class="sxs-lookup"><span data-stu-id="3e2e7-114">This buffer must contain the zero-based frame index, specified as a **WORD** value.</span></span>

</dd> <dt>

<span data-ttu-id="3e2e7-115">*pSizeOutputData*</span><span class="sxs-lookup"><span data-stu-id="3e2e7-115">*pSizeOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="3e2e7-116">Dimensioni del buffer specificato da *pOutputData*, in byte.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-116">The size of the buffer specified by *pOutputData*, in bytes.</span></span> <span data-ttu-id="3e2e7-117">Il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-117">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3e2e7-118">*pOutputData*</span><span class="sxs-lookup"><span data-stu-id="3e2e7-118">*pOutputData*</span></span> 
</dt> <dd>

<span data-ttu-id="3e2e7-119">Puntatore a un buffer in cui l'acceleratore video può scrivere.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-119">Pointer to a buffer that the video accelerator can write to.</span></span> <span data-ttu-id="3e2e7-120">Impostare questo parametro su **null**.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-120">Set this parameter to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2e7-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3e2e7-121">Return value</span></span>

<span data-ttu-id="3e2e7-122">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="3e2e7-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e2e7-123">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3e2e7-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2e7-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="3e2e7-124">Remarks</span></span>

<span data-ttu-id="3e2e7-125">Per ogni chiamata a **BeginFrame**, il decodificatore deve effettuare una chiamata corrispondente a [**IDirect3DDXVADevice9:: EndFrame**](idirect3ddxvadevice9-endframe.md).</span><span class="sxs-lookup"><span data-stu-id="3e2e7-125">For each call to **BeginFrame**, the decoder must make a corresponding call to [**IDirect3DDXVADevice9::EndFrame**](idirect3ddxvadevice9-endframe.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3e2e7-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3e2e7-126">Requirements</span></span>



| <span data-ttu-id="3e2e7-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e2e7-127">Requirement</span></span> | <span data-ttu-id="3e2e7-128">Valore</span><span class="sxs-lookup"><span data-stu-id="3e2e7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="3e2e7-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e2e7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2e7-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3e2e7-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3e2e7-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3e2e7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2e7-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3e2e7-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="3e2e7-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3e2e7-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e2e7-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e2e7-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e2e7-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3e2e7-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2e7-136">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="3e2e7-136">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




