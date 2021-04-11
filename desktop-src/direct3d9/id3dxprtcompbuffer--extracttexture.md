---
description: Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso ID3DXPRTCompBuffer e aggiunge i dati a un oggetto IDirect3DTexture9.
ms.assetid: 2159e57d-b8e5-421f-b20a-ac58b29e3c45
title: 'Metodo ID3DXPRTCompBuffer:: ExtractTexture (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractTexture
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a6a2200c680c19019375a5e33d2d8b675992dc38
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058634"
---
# <a name="id3dxprtcompbufferextracttexture-method"></a><span data-ttu-id="8efd8-103">Metodo ID3DXPRTCompBuffer:: ExtractTexture</span><span class="sxs-lookup"><span data-stu-id="8efd8-103">ID3DXPRTCompBuffer::ExtractTexture method</span></span>

<span data-ttu-id="8efd8-104">Estrae i coefficienti di proiezione del componente principale per campione (PCA) da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) e aggiunge i dati a un oggetto [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) .</span><span class="sxs-lookup"><span data-stu-id="8efd8-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer and adds the data to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="8efd8-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8efd8-105">Syntax</span></span>


```C++
HRESULT ExtractTexture(
  [in] UINT               StartPCA,
  [in] UINT               NumPCA,
  [in] LPDIRECT3DTEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="8efd8-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8efd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8efd8-107">*StartPCA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efd8-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efd8-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8efd8-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8efd8-109">Valore iniziale del coefficiente del buffer da cui estrarre i dati della trama.</span><span class="sxs-lookup"><span data-stu-id="8efd8-109">Starting value of the buffer coefficient from which to extract texture data.</span></span>

</dd> <dt>

<span data-ttu-id="8efd8-110">*NumPCA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efd8-110">*NumPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efd8-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8efd8-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8efd8-112">Numero di coefficienti PCA da estrarre dal buffer.</span><span class="sxs-lookup"><span data-stu-id="8efd8-112">Number of PCA coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="8efd8-113">*pTexture* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8efd8-113">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8efd8-114">Tipo: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span><span class="sxs-lookup"><span data-stu-id="8efd8-114">Type: **[**LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**</span></span>

<span data-ttu-id="8efd8-115">Puntatore a un oggetto trama [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) in cui vengono archiviati i coefficienti PCA.</span><span class="sxs-lookup"><span data-stu-id="8efd8-115">Pointer to an [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) texture object that will store PCA coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8efd8-116">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8efd8-116">Return value</span></span>

<span data-ttu-id="8efd8-117">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8efd8-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8efd8-118">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8efd8-118">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="8efd8-119">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="8efd8-119">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8efd8-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8efd8-120">Requirements</span></span>



| <span data-ttu-id="8efd8-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8efd8-121">Requirement</span></span> | <span data-ttu-id="8efd8-122">Valore</span><span class="sxs-lookup"><span data-stu-id="8efd8-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8efd8-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8efd8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="8efd8-124"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8efd8-124"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8efd8-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="8efd8-125">Library</span></span><br/> | <dl> <span data-ttu-id="8efd8-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8efd8-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8efd8-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="8efd8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8efd8-128">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="8efd8-128">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
