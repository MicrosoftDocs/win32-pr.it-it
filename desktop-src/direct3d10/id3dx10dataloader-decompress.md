---
description: Utilizzato per decomprimere i dati codificati. Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP. Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.
ms.assetid: 7f7e3ffd-8dac-403f-813b-d6d21d146fa7
title: Metodo ID3DX10DataLoader::D eComPress (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader.Decompress
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e6f711722852cba4b671cc84416055d279fd7cc6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322763"
---
# <a name="id3dx10dataloaderdecompress-method"></a><span data-ttu-id="6c66e-105">ID3DX10DataLoader::D Metodo eComPress</span><span class="sxs-lookup"><span data-stu-id="6c66e-105">ID3DX10DataLoader::Decompress method</span></span>

<span data-ttu-id="6c66e-106">Utilizzato per decomprimere i dati codificati.</span><span class="sxs-lookup"><span data-stu-id="6c66e-106">Used to decompress encoded data.</span></span> <span data-ttu-id="6c66e-107">Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP.</span><span class="sxs-lookup"><span data-stu-id="6c66e-107">Typically this would be used to load resources from file systems, such as ZIP files.</span></span> <span data-ttu-id="6c66e-108">Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.</span><span class="sxs-lookup"><span data-stu-id="6c66e-108">When loading from an uncompressed resource, the decompression stage does not have to do any work.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c66e-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c66e-109">Syntax</span></span>


```C++
HRESULT Decompress(
  [out] void   **ppData,
  [in]  SIZE_T *pcBytes
);
```



## <a name="parameters"></a><span data-ttu-id="6c66e-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c66e-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c66e-111">*ppData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="6c66e-111">*ppData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c66e-112">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="6c66e-112">Type: **void\*\***</span></span>

<span data-ttu-id="6c66e-113">Puntatore ai dati non elaborati da decomprimere.</span><span class="sxs-lookup"><span data-stu-id="6c66e-113">Pointer to the raw data to decompress.</span></span>

</dd> <dt>

<span data-ttu-id="6c66e-114">*pcBytes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c66e-114">*pcBytes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c66e-115">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="6c66e-115">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="6c66e-116">Dimensione dei dati a cui punta ppData.</span><span class="sxs-lookup"><span data-stu-id="6c66e-116">The size of the data pointed to by ppData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c66e-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c66e-117">Return value</span></span>

<span data-ttu-id="6c66e-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6c66e-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6c66e-119">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="6c66e-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6c66e-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c66e-120">Remarks</span></span>

<span data-ttu-id="6c66e-121">L' [**interfaccia ID3DX10DataLoader**](id3dx10dataloader.md) può essere ereditata e i relativi membri sono stati ridefiniti.</span><span class="sxs-lookup"><span data-stu-id="6c66e-121">[**ID3DX10DataLoader Interface**](id3dx10dataloader.md) can be inherited and its members redefined.</span></span> <span data-ttu-id="6c66e-122">Decomprimere può essere ridefinito per supportare formati di file personalizzati.</span><span class="sxs-lookup"><span data-stu-id="6c66e-122">Decompress could be redefined to support your own custom file formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c66e-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c66e-123">Requirements</span></span>



| <span data-ttu-id="6c66e-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c66e-124">Requirement</span></span> | <span data-ttu-id="6c66e-125">Valore</span><span class="sxs-lookup"><span data-stu-id="6c66e-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6c66e-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c66e-126">Header</span></span><br/>  | <dl> <span data-ttu-id="6c66e-127"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c66e-127"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c66e-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="6c66e-128">Library</span></span><br/> | <dl> <span data-ttu-id="6c66e-129"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c66e-129"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c66e-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6c66e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c66e-131">ID3DX10DataLoader</span><span class="sxs-lookup"><span data-stu-id="6c66e-131">ID3DX10DataLoader</span></span>](id3dx10dataloader.md)
</dt> <dt>

[<span data-ttu-id="6c66e-132">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="6c66e-132">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
