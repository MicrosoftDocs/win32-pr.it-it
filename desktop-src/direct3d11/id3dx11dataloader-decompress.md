---
title: Metodo Decompress ID3DX11DataLoader (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Decomprime i dati codificati.
ms.assetid: 68579c86-9f77-444b-86b3-746cff745be8
keywords:
- Decomprimi metodo Direct3D 11
- Decomprimi metodo Direct3D 11, interfaccia ID3DX11DataLoader
- Interfaccia ID3DX11DataLoader Direct3D 11, metodo Decompress
topic_type:
- apiref
api_name:
- ID3DX11DataLoader.Decompress
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b515eb38fb70fc31f0bbd0d02e20dcfb9f66ea5b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969512"
---
# <a name="id3dx11dataloaderdecompress-method"></a><span data-ttu-id="0ada6-107">ID3DX11DataLoader::D Metodo eComPress</span><span class="sxs-lookup"><span data-stu-id="0ada6-107">ID3DX11DataLoader::Decompress method</span></span>

> [!Note]  
> <span data-ttu-id="0ada6-108">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="0ada6-108">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="0ada6-109">Decomprime i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="0ada6-109">Decompresses encoded data.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ada6-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0ada6-110">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="0ada6-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="0ada6-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ada6-112">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0ada6-112">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ada6-113">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="0ada6-113">Type: **void\*\***</span></span>

<span data-ttu-id="0ada6-114">Puntatore ai dati non elaborati da decomprimere.</span><span class="sxs-lookup"><span data-stu-id="0ada6-114">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="0ada6-115">*pcBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0ada6-115">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ada6-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)\***</span><span class="sxs-lookup"><span data-stu-id="0ada6-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="0ada6-117">Dimensione dei dati a cui punta ppData.</span><span class="sxs-lookup"><span data-stu-id="0ada6-117">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ada6-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0ada6-118">Return value</span></span>

<span data-ttu-id="0ada6-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ada6-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ada6-120">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0ada6-120">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0ada6-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0ada6-121">Remarks</span></span>

<span data-ttu-id="0ada6-122">Utilizzare questo metodo per caricare le risorse da file System, ad esempio file ZIP.</span><span class="sxs-lookup"><span data-stu-id="0ada6-122">Use this method to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="0ada6-123">Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="0ada6-123">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

<span data-ttu-id="0ada6-124">L' [**interfaccia ID3DX11DataLoader**](id3dx11dataloader.md) può essere ereditata e i membri ridefiniti per supportare i formati di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="0ada6-124">[**ID3DX11DataLoader Interface**](id3dx11dataloader.md) can be inherited and its members redefined to support custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ada6-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0ada6-125">Requirements</span></span>



| <span data-ttu-id="0ada6-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="0ada6-126">Requirement</span></span> | <span data-ttu-id="0ada6-127">Valore</span><span class="sxs-lookup"><span data-stu-id="0ada6-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ada6-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0ada6-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0ada6-129"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ada6-129"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="0ada6-130">Libreria</span><span class="sxs-lookup"><span data-stu-id="0ada6-130">Library</span></span><br/> | <dl> <span data-ttu-id="0ada6-131"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ada6-131"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0ada6-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0ada6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ada6-133">ID3DX11DataLoader</span><span class="sxs-lookup"><span data-stu-id="0ada6-133">ID3DX11DataLoader</span></span>](id3dx11dataloader.md)
</dt> <dt>

[<span data-ttu-id="0ada6-134">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="0ada6-134">D3DX Interfaces</span></span>](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

