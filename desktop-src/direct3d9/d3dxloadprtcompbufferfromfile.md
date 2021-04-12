---
description: Carica in memoria un buffer PRT (precomputed Radiance Transfer) compresso salvato su disco.
ms.assetid: ea8bb0d6-f3ed-4ba0-ac87-02e9ac3ae15f
title: Funzione D3DXLoadPRTCompBufferFromFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadPRTCompBufferFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 505fca7d8cb2426a49a2992c249ba45b5b7afd11
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355814"
---
# <a name="d3dxloadprtcompbufferfromfile-function"></a><span data-ttu-id="b43bf-103">D3DXLoadPRTCompBufferFromFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="b43bf-103">D3DXLoadPRTCompBufferFromFile function</span></span>

<span data-ttu-id="b43bf-104">Carica in memoria un buffer PRT (precomputed Radiance Transfer) compresso salvato su disco.</span><span class="sxs-lookup"><span data-stu-id="b43bf-104">Loads into memory a compressed precomputed radiance transfer (PRT) buffer that was saved to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="b43bf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b43bf-105">Syntax</span></span>


```C++
HRESULT D3DXLoadPRTCompBufferFromFile(
  _In_    LPCSTR              pFileName,
  _Inout_ LPD3DXPRTCOMPBUFFER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="b43bf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="b43bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b43bf-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b43bf-107">*pFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b43bf-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b43bf-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b43bf-109">Nome del file da cui caricare i dati del buffer compressi.</span><span class="sxs-lookup"><span data-stu-id="b43bf-109">Name of the file from which to load the compressed buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="b43bf-110">*ppBuffer* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="b43bf-110">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b43bf-111">Tipo: **[ **LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="b43bf-111">Type: **[**LPD3DXPRTCOMPBUFFER**](id3dxprtcompbuffer.md)\***</span></span>

<span data-ttu-id="b43bf-112">Indirizzo di un puntatore all'oggetto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) di output.</span><span class="sxs-lookup"><span data-stu-id="b43bf-112">Address of a pointer to the output [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b43bf-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b43bf-113">Return value</span></span>

<span data-ttu-id="b43bf-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b43bf-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b43bf-115">Se la funzione ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b43bf-115">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b43bf-116">Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="b43bf-116">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="b43bf-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="b43bf-117">Remarks</span></span>

<span data-ttu-id="b43bf-118">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="b43bf-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="b43bf-119">Se è definito Unicode, la chiamata di funzione viene risolta in D3DXLoadPRTCompBufferFromFileW.</span><span class="sxs-lookup"><span data-stu-id="b43bf-119">If Unicode is defined, the function call resolves to D3DXLoadPRTCompBufferFromFileW.</span></span> <span data-ttu-id="b43bf-120">In caso contrario, la chiamata di funzione viene risolta in D3DXLoadPRTCompBufferFromFileA.</span><span class="sxs-lookup"><span data-stu-id="b43bf-120">Otherwise, the function call resolves to D3DXLoadPRTCompBufferFromFileA.</span></span>

## <a name="requirements"></a><span data-ttu-id="b43bf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b43bf-121">Requirements</span></span>



| <span data-ttu-id="b43bf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b43bf-122">Requirement</span></span> | <span data-ttu-id="b43bf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="b43bf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b43bf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b43bf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b43bf-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43bf-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="b43bf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="b43bf-126">Library</span></span><br/> | <dl> <span data-ttu-id="b43bf-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b43bf-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="b43bf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b43bf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b43bf-129">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="b43bf-129">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
