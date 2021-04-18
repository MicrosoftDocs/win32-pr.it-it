---
description: Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo di accelerazione video DirectX (DXVA) specificato.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'Metodo IDirect3DVideoDevice9:: GetUncompressedDXVAFormats (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345076"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a><span data-ttu-id="f1b3a-103">Metodo IDirect3DVideoDevice9:: GetUncompressedDXVAFormats</span><span class="sxs-lookup"><span data-stu-id="f1b3a-103">IDirect3DVideoDevice9::GetUncompressedDXVAFormats method</span></span>

<span data-ttu-id="f1b3a-104">Ottiene un elenco di formati pixel non compressi di cui è possibile eseguire il rendering utilizzando un profilo di accelerazione video DirectX (DXVA) specificato.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-104">Gets a list of uncompressed pixel formats that can be rendered using a specified DirectX Video Acceleration (DXVA) profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1b3a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f1b3a-105">Syntax</span></span>


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a><span data-ttu-id="f1b3a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f1b3a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1b3a-107">*pGuid*</span><span class="sxs-lookup"><span data-stu-id="f1b3a-107">*pGuid*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b3a-108">Puntatore a un GUID che specifica il profilo DXVA.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-108">Pointer to a GUID that specifies the DXVA profile.</span></span> <span data-ttu-id="f1b3a-109">Per ottenere un elenco dei profili supportati, chiamare [**IDirect3DVideoDevice9:: GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span><span class="sxs-lookup"><span data-stu-id="f1b3a-109">To get a list of supported profiles, call [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md).</span></span>

</dd> <dt>

<span data-ttu-id="f1b3a-110">*pNumFormats*</span><span class="sxs-lookup"><span data-stu-id="f1b3a-110">*pNumFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b3a-111">In input, specifica il numero di elementi nella matrice *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="f1b3a-111">On input, specifies the number of elements in the *pFormats* array.</span></span> <span data-ttu-id="f1b3a-112">Se *pFormats* è **null**, il valore di `*pNumFormats` deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-112">If *pFormats* is **NULL**, the value of `*pNumFormats` must be zero.</span></span>

<span data-ttu-id="f1b3a-113">Nell'output, se *pFormats* è **null**, *pNumFormats* riceve il numero di formati di pixel supportati.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-113">On output, if *pFormats* is **NULL**, *pNumFormats* receives the number of supported pixel formats.</span></span> <span data-ttu-id="f1b3a-114">In caso contrario, *pNumFormats* riceve il numero effettivo di formati pixel copiati nella matrice *pFormats* .</span><span class="sxs-lookup"><span data-stu-id="f1b3a-114">Otherwise, *pNumFormats* receives the actual number of pixel formats copied to the *pFormats* array.</span></span>

</dd> <dt>

<span data-ttu-id="f1b3a-115">*pFormats*</span><span class="sxs-lookup"><span data-stu-id="f1b3a-115">*pFormats*</span></span> 
</dt> <dd>

<span data-ttu-id="f1b3a-116">Indirizzo di una matrice di valori **D3DFORMAT** o **null**.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-116">Address of an array of **D3DFORMAT** values, or **NULL**.</span></span> <span data-ttu-id="f1b3a-117">Se il valore è diverso da **null**, la matrice riceve un elenco di formati pixel.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-117">If the value is non-**NULL**, the array receives a list of pixel formats.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1b3a-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f1b3a-118">Return value</span></span>

<span data-ttu-id="f1b3a-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f1b3a-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f1b3a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1b3a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="f1b3a-121">Remarks</span></span>

<span data-ttu-id="f1b3a-122">Chiamare questo metodo due volte.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-122">Call this method twice.</span></span> <span data-ttu-id="f1b3a-123">Alla prima chiamata, impostare *pFormats* su **null**.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-123">On the first call, set *pFormats* to **NULL**.</span></span> <span data-ttu-id="f1b3a-124">Il parametro *pNumFormats* riceve il numero di formati.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-124">The *pNumFormats* parameter receives the number of formats.</span></span> <span data-ttu-id="f1b3a-125">Allocare una matrice **D3DFORMAT** con le dimensioni richieste e chiamare di nuovo il metodo.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-125">Allocate a **D3DFORMAT** array with the required size, and call the method again.</span></span> <span data-ttu-id="f1b3a-126">Questa volta, impostare *pFormats* sull'indirizzo della matrice.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-126">This time, set *pFormats* to the address of the array.</span></span> <span data-ttu-id="f1b3a-127">Il metodo riempie la matrice con l'elenco dei formati pixel.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-127">The method fills the array with the list of pixel formats.</span></span>

<span data-ttu-id="f1b3a-128">Il driver deve restituire i formati in ordine di preferenza decrescente, con il formato preferito elencato per primo.</span><span class="sxs-lookup"><span data-stu-id="f1b3a-128">The driver should return the formats in decreasing order of preference, with the most preferred format listed first.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1b3a-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f1b3a-129">Requirements</span></span>



| <span data-ttu-id="f1b3a-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1b3a-130">Requirement</span></span> | <span data-ttu-id="f1b3a-131">Valore</span><span class="sxs-lookup"><span data-stu-id="f1b3a-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f1b3a-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1b3a-132">Minimum supported client</span></span><br/> | <span data-ttu-id="f1b3a-133">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f1b3a-133">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f1b3a-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f1b3a-134">Minimum supported server</span></span><br/> | <span data-ttu-id="f1b3a-135">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f1b3a-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f1b3a-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f1b3a-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1b3a-137"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1b3a-137"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1b3a-138">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f1b3a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1b3a-139">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="f1b3a-139">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 




