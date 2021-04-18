---
description: Crea una copia di un effetto.
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'Metodo ID3DXEffect:: CloneEffect (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322790"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="12e5f-103">Metodo ID3DXEffect:: CloneEffect</span><span class="sxs-lookup"><span data-stu-id="12e5f-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="12e5f-104">Crea una copia di un effetto.</span><span class="sxs-lookup"><span data-stu-id="12e5f-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e5f-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="12e5f-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="12e5f-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="12e5f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e5f-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12e5f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12e5f-108">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="12e5f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="12e5f-109">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato all'effetto.</span><span class="sxs-lookup"><span data-stu-id="12e5f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="12e5f-110">*ppEffect* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="12e5f-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12e5f-111">Tipo: **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="12e5f-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="12e5f-112">Puntatore a un'interfaccia [**ID3DXEffect**](id3dxeffect.md) contenente l'effetto clonato.</span><span class="sxs-lookup"><span data-stu-id="12e5f-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e5f-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="12e5f-113">Return value</span></span>

<span data-ttu-id="12e5f-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="12e5f-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="12e5f-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="12e5f-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="12e5f-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="12e5f-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e5f-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="12e5f-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="12e5f-118">Questa funzione non consente di clonare un effetto se l'utente specifica [D3DXFX \_ non \_ clonabile](d3dxfx.md) durante la creazione dell'effetto.</span><span class="sxs-lookup"><span data-stu-id="12e5f-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="12e5f-119">Per aggiornare i parametri condivisi e non condivisi in una tecnica attiva di un effetto clonato, vedere [**ID3DXEffect:: CommitChanges**](id3dxeffect--commitchanges.md).</span><span class="sxs-lookup"><span data-stu-id="12e5f-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12e5f-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="12e5f-120">Requirements</span></span>



| <span data-ttu-id="12e5f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="12e5f-121">Requirement</span></span> | <span data-ttu-id="12e5f-122">Valore</span><span class="sxs-lookup"><span data-stu-id="12e5f-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e5f-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="12e5f-123">Header</span></span><br/>  | <dl> <span data-ttu-id="12e5f-124"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="12e5f-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="12e5f-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="12e5f-125">Library</span></span><br/> | <dl> <span data-ttu-id="12e5f-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12e5f-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="12e5f-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="12e5f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e5f-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="12e5f-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
