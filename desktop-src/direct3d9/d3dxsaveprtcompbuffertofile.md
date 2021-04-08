---
description: Salva nel disco un buffer di trasferimento di luminosità precalcolata (PRT) compresso.
ms.assetid: cc94a83e-f755-411d-a993-4529c5d53cd5
title: Funzione D3DXSavePRTCompBufferToFile (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSavePRTCompBufferToFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d06629185637ce6fa0d7d33d5454282d2bbb8ec2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969344"
---
# <a name="d3dxsaveprtcompbuffertofile-function"></a><span data-ttu-id="da3ea-103">D3DXSavePRTCompBufferToFile (funzione)</span><span class="sxs-lookup"><span data-stu-id="da3ea-103">D3DXSavePRTCompBufferToFile function</span></span>

<span data-ttu-id="da3ea-104">Salva nel disco un buffer di trasferimento di luminosità precalcolata (PRT) compresso.</span><span class="sxs-lookup"><span data-stu-id="da3ea-104">Saves a compressed precomputed radiance transfer (PRT) buffer to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="da3ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da3ea-105">Syntax</span></span>

```cpp
HRESULT D3DXSavePRTCompBufferToFile(
  _In_ LPCSTR              pFileName,
  _In_ LPD3DXPRTCOMPBUFFER pBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="da3ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da3ea-106">Parameters</span></span>

<span data-ttu-id="da3ea-107">*pFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da3ea-107">*pFileName* \[in\]</span></span>

<span data-ttu-id="da3ea-108">Tipo: **[LPCSTR](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da3ea-108">Type: **[LPCSTR](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da3ea-109">Nome del file in cui deve essere salvato il buffer compresso.</span><span class="sxs-lookup"><span data-stu-id="da3ea-109">Name of the file to which the compressed buffer is to be saved.</span></span>

<span data-ttu-id="da3ea-110">*pbuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da3ea-110">*pBuffer* \[in\]</span></span>

<span data-ttu-id="da3ea-111">Tipo: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span><span class="sxs-lookup"><span data-stu-id="da3ea-111">Type: **[LPD3DXPRTCOMPBUFFER](id3dxprtcompbuffer.md)**</span></span>

<span data-ttu-id="da3ea-112">Indirizzo di un puntatore all'oggetto [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) di input.</span><span class="sxs-lookup"><span data-stu-id="da3ea-112">Address of a pointer to the input [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) object.</span></span>

## <a name="return-value"></a><span data-ttu-id="da3ea-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da3ea-113">Return value</span></span>

<span data-ttu-id="da3ea-114">Tipo: **[HRESULT](../com/structure-of-com-error-codes.md)**</span><span class="sxs-lookup"><span data-stu-id="da3ea-114">Type: **[HRESULT](../com/structure-of-com-error-codes.md)**</span></span>

<span data-ttu-id="da3ea-115">Se il metodo ha esito positivo, il valore restituito è **D3D \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="da3ea-115">If the method succeeds, then the return value is **D3D\_OK**.</span></span> <span data-ttu-id="da3ea-116">Se il metodo ha esito negativo, il valore restituito può essere **D3DERR \_ INVALIDCALL**.</span><span class="sxs-lookup"><span data-stu-id="da3ea-116">If the method fails, then the return value can be **D3DERR\_INVALIDCALL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="da3ea-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="da3ea-117">Remarks</span></span>

<span data-ttu-id="da3ea-118">L'impostazione del compilatore determina anche la versione della funzione.</span><span class="sxs-lookup"><span data-stu-id="da3ea-118">The compiler setting also determines the function version.</span></span> <span data-ttu-id="da3ea-119">Se è definito Unicode, la chiamata di funzione viene risolta in [D3DXSavePRTCompBufferToFileW]().</span><span class="sxs-lookup"><span data-stu-id="da3ea-119">If Unicode is defined, then the function call resolves to [D3DXSavePRTCompBufferToFileW]().</span></span> <span data-ttu-id="da3ea-120">In caso contrario, la chiamata di funzione viene risolta in **D3DXSavePRTCompBufferToFileA**.</span><span class="sxs-lookup"><span data-stu-id="da3ea-120">Otherwise, the function call resolves to **D3DXSavePRTCompBufferToFileA**.</span></span>

<span data-ttu-id="da3ea-121">Il formato di file PCA è un file binario sotto forma di intestazione e quindi di due o tre blocchi di dati.</span><span class="sxs-lookup"><span data-stu-id="da3ea-121">The PCA file format is a binary file in the form of a header and then two or three data blocks.</span></span>

```cpp
struct PRTCompressHeader
{
    UINT NumSamples;
    UINT NumCoeffs;
    UINT NumChannels;
    UINT TexWidth;
    UINT TexHeight;
    UINT bIsTex;
    UINT NumClusters;
    UINT NumPCA;
};
```

<span data-ttu-id="da3ea-122">Per i casi in cui *bIsTex* è diverso da zero, *NumSamples valore* deve essere uguale a `TexWidth * TexHeight` .</span><span class="sxs-lookup"><span data-stu-id="da3ea-122">For the case of *bIsTex* being non-zero, *NumSamples* should equal `TexWidth * TexHeight`.</span></span>

<span data-ttu-id="da3ea-123">Il blocco di dati di base che segue l'intestazione è `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` byte.</span><span class="sxs-lookup"><span data-stu-id="da3ea-123">The basis data block that follows the header is `NumCoeffs * NumChannels * (NumPCA + 1) * NumClusters * sizeof(float)` bytes.</span></span>

<span data-ttu-id="da3ea-124">Di seguito è riportato il blocco di dati di APC weights, che è `NumPCA * NumSamples * sizeof(float)` byte.</span><span class="sxs-lookup"><span data-stu-id="da3ea-124">Following that is the PCA weights data block, which is `NumPCA * NumSamples * sizeof(float)` bytes.</span></span>

<span data-ttu-id="da3ea-125">Se *NumClusters* è maggiore di 1, il file termina con il blocco di dati degli ID cluster di `NumSamples * sizeof(UINT)` byte.</span><span class="sxs-lookup"><span data-stu-id="da3ea-125">If *NumClusters* is greater than 1, then the file ends with the cluster IDs data block of `NumSamples * sizeof(UINT)` bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="da3ea-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da3ea-126">Requirements</span></span>

| <span data-ttu-id="da3ea-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="da3ea-127">Requirement</span></span> | <span data-ttu-id="da3ea-128">Valore</span><span class="sxs-lookup"><span data-stu-id="da3ea-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da3ea-129">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da3ea-129">Header</span></span><br/>  | <dl> <span data-ttu-id="da3ea-130"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="da3ea-130"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="da3ea-131">Libreria</span><span class="sxs-lookup"><span data-stu-id="da3ea-131">Library</span></span><br/> | <dl> <span data-ttu-id="da3ea-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da3ea-132"><dt>D3dx9.lib</dt></span></span> </dl>   |

## <a name="see-also"></a><span data-ttu-id="da3ea-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da3ea-133">See also</span></span>

[<span data-ttu-id="da3ea-134">Funzioni di trasferimento Radiance pre-calcolate</span><span class="sxs-lookup"><span data-stu-id="da3ea-134">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
