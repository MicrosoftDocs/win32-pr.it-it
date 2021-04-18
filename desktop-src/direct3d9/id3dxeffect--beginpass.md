---
description: Inizia un passaggio, all'interno della tecnica attiva.
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'Metodo ID3DXEffect:: BeginPass (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322791"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="9e56b-103">Metodo ID3DXEffect:: BeginPass</span><span class="sxs-lookup"><span data-stu-id="9e56b-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="9e56b-104">Inizia un passaggio, all'interno della tecnica attiva.</span><span class="sxs-lookup"><span data-stu-id="9e56b-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e56b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="9e56b-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="9e56b-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="9e56b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e56b-107">*Passa* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9e56b-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9e56b-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9e56b-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9e56b-109">Indice integer in base zero nella tecnica.</span><span class="sxs-lookup"><span data-stu-id="9e56b-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e56b-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="9e56b-110">Return value</span></span>

<span data-ttu-id="9e56b-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9e56b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9e56b-112">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9e56b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="9e56b-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="9e56b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e56b-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="9e56b-114">Remarks</span></span>

<span data-ttu-id="9e56b-115">Un'applicazione imposta un passaggio attivo (all'interno di una tecnica attiva) nel sistema di effetti chiamando **ID3DXEffect:: BeginPass**.</span><span class="sxs-lookup"><span data-stu-id="9e56b-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="9e56b-116">Un'applicazione segnala la fine del passaggio attivo chiamando [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md).</span><span class="sxs-lookup"><span data-stu-id="9e56b-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="9e56b-117">**ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** devono essere presenti in una coppia corrispondente, all'interno di una coppia corrispondente di chiamate a [**ID3DXEffect:: Begin**](id3dxeffect--begin.md) e [**ID3DXEffect:: end**](id3dxeffect--end.md) .</span><span class="sxs-lookup"><span data-stu-id="9e56b-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="9e56b-118">Se l'applicazione modifica uno stato di effetto usando uno dei metodi [**Effect:: SETX**](id3dxeffect.md) all'interno di una coppia **ID3DXEffect:: BeginPass** / [**ID3DXEffect:: EndPass**](id3dxeffect--endpass.md) matching, l'applicazione deve chiamare [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md) per impostare l'aggiornamento del dispositivo con le modifiche dello stato.</span><span class="sxs-lookup"><span data-stu-id="9e56b-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="9e56b-119">Se non vengono apportate modifiche allo stato all'interno di una coppia di **ID3DXEffect:: BeginPass** e **ID3DXEffect:: EndPass** , non è necessario chiamare **ID3DXEffect:: CommitChanges**.</span><span class="sxs-lookup"><span data-stu-id="9e56b-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e56b-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="9e56b-120">Requirements</span></span>



| <span data-ttu-id="9e56b-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e56b-121">Requirement</span></span> | <span data-ttu-id="9e56b-122">Valore</span><span class="sxs-lookup"><span data-stu-id="9e56b-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e56b-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="9e56b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="9e56b-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e56b-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9e56b-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="9e56b-125">Library</span></span><br/> | <dl> <span data-ttu-id="9e56b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9e56b-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9e56b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="9e56b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e56b-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="9e56b-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
