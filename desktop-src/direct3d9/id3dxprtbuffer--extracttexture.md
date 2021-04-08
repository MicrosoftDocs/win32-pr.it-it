---
description: Estrae i dati coefficienti da un canale colori del buffer per un intervallo di coefficienti specificato e aggiunge i dati a un oggetto IDirect3DTexture9.
ms.assetid: 75854676-706a-4675-857e-4f2f8fc8365b
title: 'Metodo ID3DXPRTBuffer:: ExtractTexture (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2ea6cfdc8fb6ec83f847ccf37d06972974ea4de8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969404"
---
# <a name="id3dxprtbufferextracttexture-method"></a><span data-ttu-id="68014-103">Metodo ID3DXPRTBuffer:: ExtractTexture</span><span class="sxs-lookup"><span data-stu-id="68014-103">ID3DXPRTBuffer::ExtractTexture method</span></span>

<span data-ttu-id="68014-104">Estrae i dati coefficienti da un canale colori del buffer per un intervallo di coefficienti specificato e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="68014-104">Extracts coefficient data from a color channel of the buffer for a specified range of coefficients, and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="68014-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="68014-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               Channel,
  [in] UINT               StartCoefficient,
  [in] UINT               NumCoefficients,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="68014-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="68014-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="68014-107">*Canale* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="68014-107">*Channel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68014-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68014-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68014-109">Canale di colore del buffer da cui estrarre i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="68014-109">Buffer color channel from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="68014-110">*StartCoefficient* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68014-110">*StartCoefficient* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68014-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68014-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68014-112">Valore iniziale del coefficiente del buffer da cui estrarre i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="68014-112">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="68014-113">*NumCoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68014-113">*NumCoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68014-114">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68014-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68014-115">Numero di scalari, a partire da StartCoefficient, da cui estrarre i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="68014-115">Number of scalars, beginning at StartCoefficient, from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="68014-116">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="68014-116">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="68014-117">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="68014-117">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="68014-118">Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) che archivia i coefficienti.</span><span class="sxs-lookup"><span data-stu-id="68014-118">Pointer to a [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="68014-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="68014-119">Return value</span></span>

<span data-ttu-id="68014-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="68014-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="68014-121">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="68014-121">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="68014-122">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="68014-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="68014-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="68014-123">Requirements</span></span>



| <span data-ttu-id="68014-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="68014-124">Requirement</span></span> | <span data-ttu-id="68014-125">Valore</span><span class="sxs-lookup"><span data-stu-id="68014-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68014-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="68014-126">Header</span></span><br/>  | <dl> <span data-ttu-id="68014-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="68014-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68014-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="68014-128">Library</span></span><br/> | <dl> <span data-ttu-id="68014-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="68014-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68014-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="68014-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68014-131">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="68014-131">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
