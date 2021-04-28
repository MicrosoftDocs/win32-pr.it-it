---
description: 'Funzione D3DX10CreateAsyncTextureProcessor: creare un processore di dati da usare con un thread pump.'
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: Funzione D3DX10CreateAsyncTextureProcessor (D3DX10Tex.h)
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
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102789"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="03237-103">Funzione D3DX10CreateAsyncTextureProcessor</span><span class="sxs-lookup"><span data-stu-id="03237-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="03237-104">Creare un processore di dati da usare con un [**thread pump**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="03237-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="03237-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="03237-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="03237-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="03237-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03237-107">*pDevice* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03237-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03237-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="03237-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="03237-109">Puntatore all'interfaccia devive (vedere [**ID3D10Device Interface).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)</span><span class="sxs-lookup"><span data-stu-id="03237-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="03237-110">*pLoadInfo* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="03237-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03237-111">Tipo: **[ **D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="03237-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="03237-112">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="03237-112">Optional.</span></span> <span data-ttu-id="03237-113">Identifica le caratteristiche di una trama (vedere [**D3DX10 \_ IMAGE \_ LOAD \_ INFO**](d3dx10-image-load-info.md)) quando viene creato il processore di dati. Impostare questo valore su **NULL** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="03237-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="03237-114">*ppDataProcessor* \[ Cambio\]</span><span class="sxs-lookup"><span data-stu-id="03237-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03237-115">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="03237-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="03237-116">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="03237-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03237-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="03237-117">Return value</span></span>

<span data-ttu-id="03237-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="03237-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="03237-119">Il valore restituito è uno dei valori elencati in Codici restituiti [Direct3D 10.](d3d10-graphics-reference-returnvalues.md)</span><span class="sxs-lookup"><span data-stu-id="03237-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="03237-120">Commenti</span><span class="sxs-lookup"><span data-stu-id="03237-120">Remarks</span></span>

<span data-ttu-id="03237-121">Questa API crea un'interfaccia del processore di dati e carica la trama. [**D3DX10CreateAsyncTextureInfoProcessor crea**](d3dx10createasynctextureinfoprocessor.md) l'interfaccia del processore di dati.</span><span class="sxs-lookup"><span data-stu-id="03237-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="03237-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="03237-122">Requirements</span></span>



| <span data-ttu-id="03237-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="03237-123">Requirement</span></span> | <span data-ttu-id="03237-124">Valore</span><span class="sxs-lookup"><span data-stu-id="03237-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03237-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="03237-125">Header</span></span><br/>  | <dl> <span data-ttu-id="03237-126"><dt>D3DX10Tex.h</dt></span><span class="sxs-lookup"><span data-stu-id="03237-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="03237-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="03237-127">Library</span></span><br/> | <dl> <span data-ttu-id="03237-128"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="03237-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="03237-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="03237-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03237-130">Funzioni di trama in D3DX 10</span><span class="sxs-lookup"><span data-stu-id="03237-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




