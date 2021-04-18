---
description: Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'Metodo IDirect3DVideoDevice9:: GetDXVAInternalInfo (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308752"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a><span data-ttu-id="c2a67-103">Metodo IDirect3DVideoDevice9:: GetDXVAInternalInfo</span><span class="sxs-lookup"><span data-stu-id="c2a67-103">IDirect3DVideoDevice9::GetDXVAInternalInfo method</span></span>

<span data-ttu-id="c2a67-104">Esegue una query per la quantità di memoria Scratch che l'HAL (Hardware Abstraction Layer) alloca per l'uso privato.</span><span class="sxs-lookup"><span data-stu-id="c2a67-104">Queries for the amount of scratch memory that the hardware abstraction layer (HAL) will allocate for its private use.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a67-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c2a67-105">Syntax</span></span>


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a><span data-ttu-id="c2a67-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c2a67-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a67-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="c2a67-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a67-108">Puntatore a un GUID che specifica il profilo DXVA.</span><span class="sxs-lookup"><span data-stu-id="c2a67-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="c2a67-109">Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="c2a67-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="c2a67-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="c2a67-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a67-111">Puntatore a una struttura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica le dimensioni e il formato pixel dei dati non compressi.</span><span class="sxs-lookup"><span data-stu-id="c2a67-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="c2a67-112">*pMemoryUsed*</span><span class="sxs-lookup"><span data-stu-id="c2a67-112">*pMemoryUsed*</span></span> 
</dt> <dd>

<span data-ttu-id="c2a67-113">Riceve la quantità di memoria Scratch che l'HAL allocherà in byte.</span><span class="sxs-lookup"><span data-stu-id="c2a67-113">Receives the amount of scratch memory that the HAL will allocate, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a67-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c2a67-114">Return value</span></span>

<span data-ttu-id="c2a67-115">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="c2a67-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c2a67-116">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c2a67-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2a67-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c2a67-117">Requirements</span></span>



| <span data-ttu-id="c2a67-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="c2a67-118">Requirement</span></span> | <span data-ttu-id="c2a67-119">Valore</span><span class="sxs-lookup"><span data-stu-id="c2a67-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="c2a67-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a67-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a67-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c2a67-121">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c2a67-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="c2a67-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a67-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c2a67-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="c2a67-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c2a67-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a67-125"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a67-125"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2a67-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c2a67-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a67-127">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="c2a67-127">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




