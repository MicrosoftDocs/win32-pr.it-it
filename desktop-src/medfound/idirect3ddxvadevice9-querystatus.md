---
description: Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA (DirectX Video Acceleration).
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'Metodo IDirect3DDXVADevice9:: QueryStatus (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308754"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a><span data-ttu-id="b9294-103">Metodo IDirect3DDXVADevice9:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="b9294-103">IDirect3DDXVADevice9::QueryStatus method</span></span>

<span data-ttu-id="b9294-104">Esegue una query sullo stato di lettura/scrittura di una superficie di decodifica DXVA (DirectX Video Acceleration).</span><span class="sxs-lookup"><span data-stu-id="b9294-104">Queries the read/write status of a DirectX Video Acceleration (DXVA) decoding surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9294-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b9294-105">Syntax</span></span>


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a><span data-ttu-id="b9294-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b9294-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9294-107">*pSurface*</span><span class="sxs-lookup"><span data-stu-id="b9294-107">*pSurface*</span></span> 
</dt> <dd>

<span data-ttu-id="b9294-108">Puntatore all'interfaccia **IDirect3DSurface9** della superficie su cui eseguire una query.</span><span class="sxs-lookup"><span data-stu-id="b9294-108">Pointer to the **IDirect3DSurface9** interface of the surface to query.</span></span>

</dd> <dt>

<span data-ttu-id="b9294-109">*Flag*</span><span class="sxs-lookup"><span data-stu-id="b9294-109">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="b9294-110">Specifica il tipo di query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="b9294-110">Specifies the type of query to perform.</span></span>



| <span data-ttu-id="b9294-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b9294-111">Value</span></span>                                                                                                                             | <span data-ttu-id="b9294-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b9294-112">Meaning</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <span data-ttu-id="b9294-113"><dt>**0x00**</dt></span><span class="sxs-lookup"><span data-stu-id="b9294-113"><dt>**0x00**</dt></span></span> </dl> | <span data-ttu-id="b9294-114">Verificare se la superficie è sicura da utilizzare per la scrittura.</span><span class="sxs-lookup"><span data-stu-id="b9294-114">Test whether the surface is safe to use for writing.</span></span><br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <span data-ttu-id="b9294-115"><dt>**0x01**</dt></span><span class="sxs-lookup"><span data-stu-id="b9294-115"><dt>**0x01**</dt></span></span> </dl> | <span data-ttu-id="b9294-116">Verificare se la superficie è sicura da utilizzare per la lettura.</span><span class="sxs-lookup"><span data-stu-id="b9294-116">Test whether the surface is safe to use for reading.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9294-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b9294-117">Return value</span></span>

<span data-ttu-id="b9294-118">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b9294-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b9294-119">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b9294-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9294-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b9294-120">Requirements</span></span>



| <span data-ttu-id="b9294-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9294-121">Requirement</span></span> | <span data-ttu-id="b9294-122">Valore</span><span class="sxs-lookup"><span data-stu-id="b9294-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="b9294-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9294-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b9294-124">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b9294-124">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b9294-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b9294-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b9294-126">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b9294-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9294-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b9294-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9294-128"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9294-128"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9294-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b9294-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9294-130">**IDirect3DDXVADevice9**</span><span class="sxs-lookup"><span data-stu-id="b9294-130">**IDirect3DDXVADevice9**</span></span>](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




