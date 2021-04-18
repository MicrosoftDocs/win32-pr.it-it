---
description: Ottiene un elenco di profili di accelerazione video DirectX (DXVA) supportati dal driver di visualizzazione.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'Metodo IDirect3DVideoDevice9:: GetDXVAGuids (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310833"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a><span data-ttu-id="f029f-103">Metodo IDirect3DVideoDevice9:: GetDXVAGuids</span><span class="sxs-lookup"><span data-stu-id="f029f-103">IDirect3DVideoDevice9::GetDXVAGuids method</span></span>

<span data-ttu-id="f029f-104">Ottiene un elenco di profili di accelerazione video DirectX (DXVA) supportati dal driver di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="f029f-104">Gets a list of DirectX Video Acceleration (DXVA) profiles that are supported by the display driver.</span></span>

## <a name="syntax"></a><span data-ttu-id="f029f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f029f-105">Syntax</span></span>


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a><span data-ttu-id="f029f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f029f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f029f-107">*pNumGuids*</span><span class="sxs-lookup"><span data-stu-id="f029f-107">*pNumGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="f029f-108">In input, specifica il numero di elementi nella matrice *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="f029f-108">On input, specifies the number of elements in the *pGuids* array.</span></span> <span data-ttu-id="f029f-109">Se *pGuids* è **null**, il valore di `*pNumGuids` deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="f029f-109">If *pGuids* is **NULL**, the value of `*pNumGuids` must be zero.</span></span>

<span data-ttu-id="f029f-110">Nell'output, se *pGuids* è **null**, *pNumGuids* riceve il numero di profili DXVA in modalità limitata.</span><span class="sxs-lookup"><span data-stu-id="f029f-110">On output, if *pGuids* is **NULL**, *pNumGuids* receives the number of restricted-mode DXVA profiles.</span></span> <span data-ttu-id="f029f-111">In caso contrario, *pNumGuids* riceve il numero effettivo di GUID copiati nella matrice *pGuids* .</span><span class="sxs-lookup"><span data-stu-id="f029f-111">Otherwise, *pNumGuids* receives the actual number of GUIDs that are copied to the *pGuids* array.</span></span>

</dd> <dt>

<span data-ttu-id="f029f-112">*pGuids*</span><span class="sxs-lookup"><span data-stu-id="f029f-112">*pGuids*</span></span> 
</dt> <dd>

<span data-ttu-id="f029f-113">Indirizzo di una matrice di GUID o **null**.</span><span class="sxs-lookup"><span data-stu-id="f029f-113">Address of an array of GUIDs or **NULL**.</span></span> <span data-ttu-id="f029f-114">Se il valore è diverso da **null**, la matrice riceve un elenco di GUID che specificano i profili DXVA in modalità limitata.</span><span class="sxs-lookup"><span data-stu-id="f029f-114">If the value is non-**NULL**, the array receives a list of GUIDs that specify restricted-mode DXVA profiles.</span></span> <span data-ttu-id="f029f-115">Questi GUID sono definiti in DXVA. h e sono documentati nella [specifica dxva 1,0](/windows-hardware/drivers/display/directx-video-acceleration).</span><span class="sxs-lookup"><span data-stu-id="f029f-115">These GUIDs are defined in dxva.h, and are documented in the [DXVA 1.0 specification](/windows-hardware/drivers/display/directx-video-acceleration).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f029f-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f029f-116">Return value</span></span>

<span data-ttu-id="f029f-117">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f029f-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f029f-118">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f029f-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f029f-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="f029f-119">Remarks</span></span>

<span data-ttu-id="f029f-120">Chiamare questo metodo due volte.</span><span class="sxs-lookup"><span data-stu-id="f029f-120">Call this method twice.</span></span> <span data-ttu-id="f029f-121">Alla prima chiamata, impostare *pGuids* su **null**.</span><span class="sxs-lookup"><span data-stu-id="f029f-121">On the first call, set *pGuids* to **NULL**.</span></span> <span data-ttu-id="f029f-122">Il parametro *pNumGuids* riceve il numero di GUID del profilo DXVA.</span><span class="sxs-lookup"><span data-stu-id="f029f-122">The *pNumGuids* parameter receives the number of DXVA profile GUIDs.</span></span> <span data-ttu-id="f029f-123">Allocare una matrice di GUID con la dimensione richiesta e chiamare di nuovo il metodo.</span><span class="sxs-lookup"><span data-stu-id="f029f-123">Allocate an array of GUIDs with the required size and call the method again.</span></span> <span data-ttu-id="f029f-124">Questa volta, impostare *pGuids* sull'indirizzo della matrice.</span><span class="sxs-lookup"><span data-stu-id="f029f-124">This time, set *pGuids* to the address of the array.</span></span> <span data-ttu-id="f029f-125">Il metodo riempie la matrice con l'elenco dei GUID del profilo DXVA.</span><span class="sxs-lookup"><span data-stu-id="f029f-125">The method fills the array with the list of DXVA profile GUIDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f029f-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f029f-126">Requirements</span></span>



| <span data-ttu-id="f029f-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="f029f-127">Requirement</span></span> | <span data-ttu-id="f029f-128">Valore</span><span class="sxs-lookup"><span data-stu-id="f029f-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f029f-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f029f-129">Minimum supported client</span></span><br/> | <span data-ttu-id="f029f-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f029f-130">Windows Vista \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f029f-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f029f-131">Minimum supported server</span></span><br/> | <span data-ttu-id="f029f-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f029f-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="f029f-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f029f-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="f029f-134"><dt>DXVA. h</dt></span><span class="sxs-lookup"><span data-stu-id="f029f-134"><dt>Dxva.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f029f-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f029f-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f029f-136">**IDirect3DVideoDevice9**</span><span class="sxs-lookup"><span data-stu-id="f029f-136">**IDirect3DVideoDevice9**</span></span>](idirect3dvideodevice9.md)
</dt> </dl>

 

 
