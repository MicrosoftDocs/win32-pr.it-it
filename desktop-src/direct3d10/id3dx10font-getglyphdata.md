---
description: Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.
ms.assetid: 1114b06a-c0f0-4c2a-86ad-2ed72bee4049
title: 'Metodo ID3DX10Font:: GetGlyphData (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetGlyphData
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 530206c4f351cb1ef073639a21dfa37e43af5bae
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323163"
---
# <a name="id3dx10fontgetglyphdata-method"></a><span data-ttu-id="2ef06-103">Metodo ID3DX10Font:: GetGlyphData</span><span class="sxs-lookup"><span data-stu-id="2ef06-103">ID3DX10Font::GetGlyphData method</span></span>

<span data-ttu-id="2ef06-104">Restituisce informazioni sulla posizione e l'orientamento di un glifo in una cella di caratteri.</span><span class="sxs-lookup"><span data-stu-id="2ef06-104">Return information about the placement and orientation of a glyph in a character cell.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef06-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2ef06-105">Syntax</span></span>


```C++
HRESULT GetGlyphData(
  [in]  UINT                     Glyph,
  [out] ID3D10ShaderResourceView **ppTexture,
  [in]  RECT                     *pBlackBox,
  [in]  POINT                    *pCellInc
);
```



## <a name="parameters"></a><span data-ttu-id="2ef06-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2ef06-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef06-107">*Glifo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ef06-107">*Glyph* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef06-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ef06-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ef06-109">Identificatore glifo.</span><span class="sxs-lookup"><span data-stu-id="2ef06-109">Glyph identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2ef06-110">*ppTexture* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="2ef06-110">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef06-111">Tipo: **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="2ef06-111">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="2ef06-112">Indirizzo di un puntatore a un oggetto ID3D10Texture che contiene il glifo.</span><span class="sxs-lookup"><span data-stu-id="2ef06-112">Address of a pointer to a ID3D10Texture object that contains the glyph.</span></span>

</dd> <dt>

<span data-ttu-id="2ef06-113">*pBlackBox* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ef06-113">*pBlackBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef06-114">Tipo: **[ **Rect**](/previous-versions//dd162897(v=vs.85))\***</span><span class="sxs-lookup"><span data-stu-id="2ef06-114">Type: **[**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="2ef06-115">Puntatore all'oggetto rettangolo più piccolo che racchiude completamente il glifo.</span><span class="sxs-lookup"><span data-stu-id="2ef06-115">Pointer to the smallest rectangle object that completely encloses the glyph.</span></span> <span data-ttu-id="2ef06-116">Vedere [Rect](/previous-versions//ms536136(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ef06-116">See [RECT](/previous-versions//ms536136(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="2ef06-117">*pCellInc* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2ef06-117">*pCellInc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef06-118">Tipo: **punto \***</span><span class="sxs-lookup"><span data-stu-id="2ef06-118">Type: **POINT\***</span></span>

<span data-ttu-id="2ef06-119">Puntatore al vettore bidimensionale che connette l'origine della cella del carattere corrente all'origine della cella di caratteri successiva.</span><span class="sxs-lookup"><span data-stu-id="2ef06-119">Pointer to the two-dimensional vector that connects the origin of the current character cell to the origin of the next character cell.</span></span> <span data-ttu-id="2ef06-120">Vedere [punto](/previous-versions//ms536119(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2ef06-120">See [POINT](/previous-versions//ms536119(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef06-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2ef06-121">Return value</span></span>

<span data-ttu-id="2ef06-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2ef06-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2ef06-123">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ef06-123">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2ef06-124">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="2ef06-124">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef06-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2ef06-125">Requirements</span></span>



| <span data-ttu-id="2ef06-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef06-126">Requirement</span></span> | <span data-ttu-id="2ef06-127">Valore</span><span class="sxs-lookup"><span data-stu-id="2ef06-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef06-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2ef06-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2ef06-129"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ef06-129"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ef06-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="2ef06-130">Library</span></span><br/> | <dl> <span data-ttu-id="2ef06-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ef06-131"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef06-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2ef06-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef06-133">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="2ef06-133">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="2ef06-134">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="2ef06-134">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
