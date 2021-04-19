---
description: Crea un oggetto Sprite associato a un dispositivo specifico. Gli oggetti Sprite vengono usati per creare immagini 2D sullo schermo.
ms.assetid: 1611073f-0590-415a-8ea5-dc1d224f20b9
title: Funzione D3DXCreateSprite (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSprite
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1e16feb2ff07f10703c5243ebeaaee3a2a15e7f0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322727"
---
# <a name="d3dxcreatesprite-function"></a><span data-ttu-id="a69d1-104">D3DXCreateSprite (funzione)</span><span class="sxs-lookup"><span data-stu-id="a69d1-104">D3DXCreateSprite function</span></span>

<span data-ttu-id="a69d1-105">Crea un oggetto Sprite associato a un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="a69d1-105">Creates a sprite object which is associated with a particular device.</span></span> <span data-ttu-id="a69d1-106">Gli oggetti Sprite vengono usati per creare immagini 2D sullo schermo.</span><span class="sxs-lookup"><span data-stu-id="a69d1-106">Sprite objects are used to draw 2D images to the screen.</span></span>

## <a name="syntax"></a><span data-ttu-id="a69d1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a69d1-107">Syntax</span></span>


```C++
HRESULT D3DXCreateSprite(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXSPRITE      *ppSprite
);
```



## <a name="parameters"></a><span data-ttu-id="a69d1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="a69d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a69d1-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a69d1-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a69d1-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="a69d1-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="a69d1-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , il dispositivo da associare allo sprite.</span><span class="sxs-lookup"><span data-stu-id="a69d1-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device to be associated with the sprite.</span></span>

</dd> <dt>

<span data-ttu-id="a69d1-112">*ppSprite* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a69d1-112">*ppSprite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a69d1-113">Tipo: **[ **LPD3DXSPRITE**](id3dxsprite.md)\***</span><span class="sxs-lookup"><span data-stu-id="a69d1-113">Type: **[**LPD3DXSPRITE**](id3dxsprite.md)\***</span></span>

<span data-ttu-id="a69d1-114">Indirizzo di un puntatore a un'interfaccia [**ID3DXSprite**](id3dxsprite.md) .</span><span class="sxs-lookup"><span data-stu-id="a69d1-114">Address of a pointer to an [**ID3DXSprite**](id3dxsprite.md) interface.</span></span> <span data-ttu-id="a69d1-115">Questa interfaccia consente all'utente di accedere alle funzioni sprite.</span><span class="sxs-lookup"><span data-stu-id="a69d1-115">This interface allows the user to access sprite functions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a69d1-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a69d1-116">Return value</span></span>

<span data-ttu-id="a69d1-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a69d1-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a69d1-118">Se la funzione ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a69d1-118">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a69d1-119">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="a69d1-119">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a69d1-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="a69d1-120">Remarks</span></span>

<span data-ttu-id="a69d1-121">Questa interfaccia può essere usata per creare due immagini dimensionali nello spazio dello schermo del dispositivo associato.</span><span class="sxs-lookup"><span data-stu-id="a69d1-121">This interface can be used to draw two dimensional images in screen space of the associated device.</span></span>

## <a name="requirements"></a><span data-ttu-id="a69d1-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a69d1-122">Requirements</span></span>



| <span data-ttu-id="a69d1-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="a69d1-123">Requirement</span></span> | <span data-ttu-id="a69d1-124">Valore</span><span class="sxs-lookup"><span data-stu-id="a69d1-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a69d1-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a69d1-125">Header</span></span><br/>  | <dl> <span data-ttu-id="a69d1-126"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a69d1-126"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a69d1-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="a69d1-127">Library</span></span><br/> | <dl> <span data-ttu-id="a69d1-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a69d1-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a69d1-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a69d1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a69d1-130">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="a69d1-130">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
