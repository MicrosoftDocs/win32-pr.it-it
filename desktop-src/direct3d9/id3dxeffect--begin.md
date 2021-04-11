---
description: Avvia una tecnica attiva.
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'Metodo ID3DXEffect:: begin (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235051"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="6620b-103">Metodo ID3DXEffect:: Begin</span><span class="sxs-lookup"><span data-stu-id="6620b-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="6620b-104">Avvia una tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="6620b-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="6620b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6620b-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="6620b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6620b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6620b-107">*pPasses* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6620b-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6620b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6620b-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6620b-109">Puntatore a un valore restituito che indica il numero di passaggi necessari per eseguire il rendering della tecnica corrente.</span><span class="sxs-lookup"><span data-stu-id="6620b-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="6620b-110">*Flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6620b-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6620b-111">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6620b-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6620b-112">DWORD che determina se lo stato modificato da un effetto viene salvato e ripristinato.</span><span class="sxs-lookup"><span data-stu-id="6620b-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="6620b-113">Il valore predefinito 0 indica che **ID3DXEffect:: Begin** e [**ID3DXEffect:: end**](id3dxeffect--end.md) salveranno e ripristineranno tutti gli stati modificati dall'effetto (incluse le costanti pixel e vertex shader).</span><span class="sxs-lookup"><span data-stu-id="6620b-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="6620b-114">I flag validi possono essere visualizzati con i [flag di salvataggio e ripristino dello stato effettivo](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="6620b-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6620b-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6620b-115">Return value</span></span>

<span data-ttu-id="6620b-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6620b-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6620b-117">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6620b-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6620b-118">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="6620b-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="6620b-119">Commenti</span><span class="sxs-lookup"><span data-stu-id="6620b-119">Remarks</span></span>

<span data-ttu-id="6620b-120">Un'applicazione imposta una tecnica attiva nel sistema degli effetti chiamando **ID3DXEffect:: Begin**.</span><span class="sxs-lookup"><span data-stu-id="6620b-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="6620b-121">Il sistema di effetto risponde acquisendo tutto lo stato della pipeline che può essere modificato dalla tecnica in un blocco di stato.</span><span class="sxs-lookup"><span data-stu-id="6620b-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="6620b-122">Un'applicazione segnala la fine di una tecnica chiamando [**ID3DXEffect:: end**](id3dxeffect--end.md), che usa il blocco state per ripristinare lo stato originale.</span><span class="sxs-lookup"><span data-stu-id="6620b-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="6620b-123">Il sistema di effetto, pertanto, si occupa del salvataggio dello stato quando una tecnica diventa attiva e il ripristino dello stato al termine di una tecnica.</span><span class="sxs-lookup"><span data-stu-id="6620b-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="6620b-124">Se si sceglie di disabilitare questa funzionalità di salvataggio e ripristino, vedere [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md).</span><span class="sxs-lookup"><span data-stu-id="6620b-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="6620b-125">All'interno della coppia **ID3DXEffect:: Begin** e [**ID3DXEffect:: end**](id3dxeffect--end.md) , un'applicazione usa [**ID3DXEffect:: BeginPass**](id3dxeffect--beginpass.md) per impostare il passaggio attivo, [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) se sono state apportate modifiche di stato dopo l'attivazione del passaggio e [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) per terminare il passaggio attivo.</span><span class="sxs-lookup"><span data-stu-id="6620b-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="6620b-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6620b-126">Requirements</span></span>



| <span data-ttu-id="6620b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6620b-127">Requirement</span></span> | <span data-ttu-id="6620b-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6620b-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6620b-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6620b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6620b-130"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="6620b-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="6620b-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="6620b-131">Library</span></span><br/> | <dl> <span data-ttu-id="6620b-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6620b-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6620b-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6620b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6620b-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="6620b-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
