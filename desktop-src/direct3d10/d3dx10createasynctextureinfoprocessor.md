---
description: Creare un elaboratore di dati da utilizzare con una pompa di thread.
ms.assetid: e97b6aca-1839-48ea-8dab-b96a52ec2a68
title: Funzione D3DX10CreateAsyncTextureInfoProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureInfoProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: fe56fc217af6ebae9255b4f72d3c3af2f279fa29
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323314"
---
# <a name="d3dx10createasynctextureinfoprocessor-function"></a><span data-ttu-id="d5730-103">D3DX10CreateAsyncTextureInfoProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="d5730-103">D3DX10CreateAsyncTextureInfoProcessor function</span></span>

<span data-ttu-id="d5730-104">Creare un elaboratore di dati da utilizzare con una [**pompa di thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="d5730-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5730-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d5730-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureInfoProcessor(
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="d5730-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d5730-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5730-107">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5730-107">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5730-108">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5730-108">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="d5730-109">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="d5730-109">Optional.</span></span> <span data-ttu-id="d5730-110">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="d5730-110">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="d5730-111">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="d5730-111">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5730-112">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="d5730-112">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="d5730-113">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="d5730-113">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5730-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d5730-114">Return value</span></span>

<span data-ttu-id="d5730-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5730-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5730-116">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="d5730-116">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d5730-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="d5730-117">Remarks</span></span>

<span data-ttu-id="d5730-118">Questa API crea un'interfaccia di elaborazione dati. [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) crea l'interfaccia del processore dati e carica la trama.</span><span class="sxs-lookup"><span data-stu-id="d5730-118">This API does creates a data-processor interface; [**D3DX10CreateAsyncTextureProcessor**](d3dx10createasynctextureprocessor.md) creates the data-processor interface and loads the texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5730-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d5730-119">Requirements</span></span>



| <span data-ttu-id="d5730-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5730-120">Requirement</span></span> | <span data-ttu-id="d5730-121">Valore</span><span class="sxs-lookup"><span data-stu-id="d5730-121">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5730-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d5730-122">Header</span></span><br/>  | <dl> <span data-ttu-id="d5730-123"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5730-123"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d5730-124">Libreria</span><span class="sxs-lookup"><span data-stu-id="d5730-124">Library</span></span><br/> | <dl> <span data-ttu-id="d5730-125"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5730-125"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5730-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d5730-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5730-127">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="d5730-127">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




