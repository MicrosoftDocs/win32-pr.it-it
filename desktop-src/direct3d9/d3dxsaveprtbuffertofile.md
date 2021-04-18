---
description: Salva nel disco un buffer di trasferimento di luminosità (PRT) pre-calcolato.
ms.assetid: 1fca69bd-6729-45af-981f-b7480c741bc2
title: Funzione D3DXSavePRTBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b796ee24be44bf65be7df938bdfe85d6784cc5f3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322602"
---
# <a name="d3dxsaveprtbuffertofile-function"></a><span data-ttu-id="f5787-103">D3DXSavePRTBufferToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="f5787-103">D3DXSavePRTBufferToFile function</span></span>

<span data-ttu-id="f5787-104">Salva nel disco un buffer di trasferimento di luminosità (PRT) pre-calcolato.</span><span class="sxs-lookup"><span data-stu-id="f5787-104">Saves a precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5787-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5787-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTBufferToFile(
  _In_ LPCSTR          pFileName,
  _In_ LPD3DXPRTBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="f5787-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5787-106">Parameters</span></span>

<span data-ttu-id="f5787-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5787-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="f5787-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f5787-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f5787-109">Nome del file in cui salvare il buffer.</span><span class="sxs-lookup"><span data-stu-id="f5787-109">Name of the file to which the buffer is to be saved.</span></span>

<span data-ttu-id="f5787-110">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5787-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="f5787-111">Tipo: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="f5787-111">Type: **[LPD3DXPRTBUFFER](id3dxprtbuffer.md)**</span></span>

<span data-ttu-id="f5787-112">Indirizzo di un puntatore all'oggetto [**ID3DXPRTBuffer**](id3dxprtbuffer.md) di input.</span><span class="sxs-lookup"><span data-stu-id="f5787-112">Address of a pointer to the input [**ID3DXPRTBuffer**](id3dxprtbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="f5787-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5787-113">Return value</span></span>

<span data-ttu-id="f5787-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="f5787-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="f5787-115">Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f5787-115">If the method succeeds, the return value is **D3D\_OK**.</span></span> <span data-ttu-id="f5787-116">Se il metodo ha esito negativo, il valore restituito può essere **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="f5787-116">If the method fails, the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5787-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="f5787-117">Remarks</span></span>

<span data-ttu-id="f5787-118">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="f5787-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="f5787-119">Se è definito Unicode, la chiamata di funzione viene risolta in [D3DXSavePRTBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="f5787-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTBufferToFileW]().</span></span> <span data-ttu-id="f5787-120">In caso contrario, la chiamata di funzione viene risolta in **D3DXSavePRTBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="f5787-120">Otherwise, the function call resolves to **D3DXSavePRTBufferToFileA**.</span></span>

<span data-ttu-id="f5787-121">Il formato del file PRT è costituito da un file binario sotto forma di intestazione e quindi da un blocco di dati.</span><span class="sxs-lookup"><span data-stu-id="f5787-121">The PRT file format is a binary file in the form of a header and then a data block.</span></span>

```cpp
struct PRTHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
};
```

<span data-ttu-id="f5787-122">Per i casi in cui *bIsTex* è diverso da zero, *NumSamples valore* deve essere uguale a `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="f5787-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="f5787-123">Il blocco di dati che segue l'intestazione è `NumSamples * NumCoeffs * NumChannels * sizeof(float)` byte.</span><span class="sxs-lookup"><span data-stu-id="f5787-123">The data block that follows the header is `NumSamples * NumCoeffs * NumChannels * sizeof(float)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5787-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5787-124">Requirements</span></span>

| <span data-ttu-id="f5787-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5787-125">Requirement</span></span> | <span data-ttu-id="f5787-126">Valore</span><span class="sxs-lookup"><span data-stu-id="f5787-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5787-127">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f5787-127">Header</span></span><br/>  | <dl> <span data-ttu-id="f5787-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5787-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="f5787-129">Libreria</span><span class="sxs-lookup"><span data-stu-id="f5787-129">Library</span></span><br/> | <dl> <span data-ttu-id="f5787-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f5787-130"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="f5787-131">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5787-131">See also</span></span>

[<span data-ttu-id="f5787-132">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="f5787-132">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
