---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 80a78e68-6f88-4cd2-bb7b-0c608ae700aa
title: 'Metodo ID3DXFont:: GetGlyphData (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFont.GetGlyphData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 31f8d2e9d61cd7a8d6bd96fbdd3f6f6a7d895568
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322617"
---
# <a name="id3dxfontgetglyphdata-method"></a><span data-ttu-id="3f90a-103">Metodo ID3DXFont:: GetGlyphData</span><span class="sxs-lookup"><span data-stu-id="3f90a-103">ID3DXFont::GetGlyphData method</span></span>

<span data-ttu-id="3f90a-104">Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.</span><span class="sxs-lookup"><span data-stu-id="3f90a-104">Returns information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f90a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3f90a-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT               Glyph,
  [out] LPDIRECT3DTEXTURE9 *ppTexture,
  [out] RECT               *pBlackBox,
  [out] POINT              *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="3f90a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="3f90a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f90a-107">*Glifo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3f90a-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3f90a-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3f90a-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3f90a-109">Identificatore glifo.</span><span class="sxs-lookup"><span data-stu-id="3f90a-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="3f90a-110">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f90a-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f90a-111">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span><span class="sxs-lookup"><span data-stu-id="3f90a-111">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)\***</span></span>

<span data-ttu-id="3f90a-112">Indirizzo di un puntatore a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che contiene il glifo.</span><span class="sxs-lookup"><span data-stu-id="3f90a-112">Address of a pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="3f90a-113">*pBlackBox* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f90a-113">*pBlackBox* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f90a-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="3f90a-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="3f90a-115">Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo.</span><span class="sxs-lookup"><span data-stu-id="3f90a-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="3f90a-116">*pCellInc* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="3f90a-116">*pCellInc* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f90a-117">Tipo: **[ **punto**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="3f90a-117">Type: **[**POINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="3f90a-118">Puntatore al vettore bidimensionale che connette l'origine della cella del carattere corrente all'origine della cella di caratteri successiva.</span><span class="sxs-lookup"><span data-stu-id="3f90a-118">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="3f90a-119">Vedere [**punto**](../winprog/windows-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="3f90a-119">See [**POINT**](../winprog/windows-data-types.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f90a-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="3f90a-120">Return value</span></span>

<span data-ttu-id="3f90a-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3f90a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3f90a-122">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3f90a-122">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="3f90a-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="3f90a-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f90a-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3f90a-124">Requirements</span></span>



| <span data-ttu-id="3f90a-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f90a-125">Requirement</span></span> | <span data-ttu-id="3f90a-126">Valore</span><span class="sxs-lookup"><span data-stu-id="3f90a-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f90a-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="3f90a-127">Header</span></span><br/>  | <dl> <span data-ttu-id="3f90a-128"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f90a-128"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="3f90a-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="3f90a-129">Library</span></span><br/> | <dl> <span data-ttu-id="3f90a-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="3f90a-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="3f90a-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3f90a-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f90a-132">ID3DXFont</span><span class="sxs-lookup"><span data-stu-id="3f90a-132">ID3DXFont</span></span>](id3dxfont.md)
</dt> </dl>

 

 
