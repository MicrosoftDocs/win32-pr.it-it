---
description: Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'Metodo IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308753"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a><span data-ttu-id="51340-103">Metodo IDirect3DVideoDevice9:: GetDXVACompressedBufferInfo</span><span class="sxs-lookup"><span data-stu-id="51340-103">IDirect3DVideoDevice9::GetDXVACompressedBufferInfo method</span></span>

<span data-ttu-id="51340-104">Ottiene informazioni sui buffer compressi necessari per la decodifica con accelerazione hardware.</span><span class="sxs-lookup"><span data-stu-id="51340-104">Gets information about the compressed buffers needed for hardware-accelerated decoding.</span></span>

## <a name="syntax"></a><span data-ttu-id="51340-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="51340-105">Syntax</span></span>


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
);
```



## <a name="parameters"></a><span data-ttu-id="51340-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="51340-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51340-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="51340-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="51340-108">Puntatore a un GUID che specifica il profilo DXVA.</span><span class="sxs-lookup"><span data-stu-id="51340-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="51340-109">Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="51340-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="51340-110">*pUncompData*</span><span class="sxs-lookup"><span data-stu-id="51340-110">*pUncompData*</span></span> 
</dt> <dd>

<span data-ttu-id="51340-111">Puntatore a una struttura [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) che specifica le dimensioni e il formato pixel dei dati non compressi.</span><span class="sxs-lookup"><span data-stu-id="51340-111">Pointer to a [**DXVAUncompDataInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) structure that specifies the size and pixel format of the uncompressed data.</span></span>

</dd> <dt>

<span data-ttu-id="51340-112">*pNumBuffers*</span><span class="sxs-lookup"><span data-stu-id="51340-112">*pNumBuffers*</span></span> 
</dt> <dd>

<span data-ttu-id="51340-113">In input, specifica il numero di elementi nella matrice *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="51340-113">On input, specifies the number of elements in the *pBufferInfo* array.</span></span> <span data-ttu-id="51340-114">Se *pBufferInfo* è **null**, il valore di `*pNumBuffers` deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="51340-114">If *pBufferInfo* is **NULL**, the value of `*pNumBuffers` must be zero.</span></span>

<span data-ttu-id="51340-115">Nell'output, se *pBufferInfo* è **null**, *pNumBuffers* riceve la dimensione della matrice da allocare.</span><span class="sxs-lookup"><span data-stu-id="51340-115">On output, if *pBufferInfo* is **NULL**, *pNumBuffers* receives the size of array to allocate.</span></span> <span data-ttu-id="51340-116">In caso contrario, *pNumBuffers* riceve il numero effettivo di elementi che vengono copiati nella matrice *pBufferInfo* .</span><span class="sxs-lookup"><span data-stu-id="51340-116">Otherwise, *pNumBuffers* receives the actual number of elements that are copied to the *pBufferInfo* array.</span></span>

</dd> <dt>

<span data-ttu-id="51340-117">*pBufferInfo*</span><span class="sxs-lookup"><span data-stu-id="51340-117">*pBufferInfo*</span></span> 
</dt> <dd>

<span data-ttu-id="51340-118">Indirizzo di una matrice di strutture [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) o **null**.</span><span class="sxs-lookup"><span data-stu-id="51340-118">Address of an array of [**DXVACompBufferInfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) structures or **NULL**.</span></span> <span data-ttu-id="51340-119">Se il valore è diverso da **null**, il metodo copia un elenco di strutture **DXVACompBufferInfo** in questa matrice.</span><span class="sxs-lookup"><span data-stu-id="51340-119">If the value is non-**NULL**, the method copies a list of **DXVACompBufferInfo** structures to this array.</span></span> <span data-ttu-id="51340-120">Ogni struttura corrisponde a un tipo di buffer di dati compresso utilizzato dal tasto di scelta rapida del video.</span><span class="sxs-lookup"><span data-stu-id="51340-120">Each structure corresponds to one type of compressed data buffer that is used by the video accelerator.</span></span>

<span data-ttu-id="51340-121">Impostare tutti gli elementi della matrice su zero prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="51340-121">Set all of the array elements to zero before calling this method.</span></span>

<span data-ttu-id="51340-122">Ogni indice di matrice corrisponde a uno dei tipi di superficie DXVA definiti in DXVA. h.</span><span class="sxs-lookup"><span data-stu-id="51340-122">Each array index corresponds to one of the DXVA surface types defined in dxva.h.</span></span> <span data-ttu-id="51340-123">L'acceleratore video restituisce un elenco di DXVA numero massimo di **\_ tipi di \_ \_ \_ buffer comp** .</span><span class="sxs-lookup"><span data-stu-id="51340-123">The video accelerator returns a list of up to **DXVA\_NUM\_TYPES\_COMP\_BUFFERS** array entries.</span></span> <span data-ttu-id="51340-124">Per informazioni dettagliate, vedere la [specifica DXVA 1,0](/windows-hardware/drivers/display/directx-video-acceleration), sezione 3,4, "elenco di descrizioni del buffer".</span><span class="sxs-lookup"><span data-stu-id="51340-124">For details, refer to the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration), section 3.4, "Buffer Description List."</span></span> <span data-ttu-id="51340-125">Se un particolare tipo di buffer non viene utilizzato dal profilo DXVA, la voce in corrispondenza dell'indice contiene zeri per tutti i valori.</span><span class="sxs-lookup"><span data-stu-id="51340-125">If a particular buffer type is not used by the DXVA profile, the entry at that index contains zeros for all values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51340-126">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="51340-126">Return value</span></span>

<span data-ttu-id="51340-127">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="51340-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="51340-128">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="51340-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="51340-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="51340-129">Requirements</span></span>



| <span data-ttu-id="51340-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="51340-130">Requirement</span></span> | <span data-ttu-id="51340-131">Valore</span><span class="sxs-lookup"><span data-stu-id="51340-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="51340-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51340-132">Minimum supported client</span></span><br/> | <span data-ttu-id="51340-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="51340-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51340-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="51340-134">Minimum supported server</span></span><br/> | <span data-ttu-id="51340-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="51340-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="51340-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="51340-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="51340-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="51340-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51340-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="51340-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51340-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="51340-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
