---
description: Creare un elaboratore di dati da utilizzare con una pompa di thread.
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Funzione D3DX10CreateAsyncTextureProcessor (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d1d9c61729e72cc4ae5432361e9c1d968551b9c2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058662"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="0121c-103">D3DX10CreateAsyncTextureProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="0121c-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="0121c-104">Creare un elaboratore di dati da utilizzare con una [**pompa di thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="0121c-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0121c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0121c-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="0121c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0121c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0121c-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0121c-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0121c-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0121c-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0121c-109">Puntatore a Devive (vedere l' [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span><span class="sxs-lookup"><span data-stu-id="0121c-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="0121c-110">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0121c-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0121c-111">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0121c-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="0121c-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="0121c-112">Optional.</span></span> <span data-ttu-id="0121c-113">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="0121c-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0121c-114">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0121c-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0121c-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0121c-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="0121c-116">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="0121c-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0121c-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0121c-117">Return value</span></span>

<span data-ttu-id="0121c-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0121c-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0121c-119">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="0121c-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0121c-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="0121c-120">Remarks</span></span>

<span data-ttu-id="0121c-121">Questa API crea un'interfaccia del processore dati e carica la trama; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) crea l'interfaccia del processore dati.</span><span class="sxs-lookup"><span data-stu-id="0121c-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0121c-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0121c-122">Requirements</span></span>



| <span data-ttu-id="0121c-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0121c-123">Requirement</span></span> | <span data-ttu-id="0121c-124">Valore</span><span class="sxs-lookup"><span data-stu-id="0121c-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0121c-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0121c-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0121c-126"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="0121c-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="0121c-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="0121c-127">Library</span></span><br/> | <dl> <span data-ttu-id="0121c-128"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0121c-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="0121c-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0121c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0121c-130">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="0121c-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




