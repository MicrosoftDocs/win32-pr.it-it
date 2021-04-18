---
description: Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader. I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX10 che usa le pompe di thread.
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: Funzione D3DX10CreateAsyncShaderResourceViewProcessor (D3DX10Async. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323315"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="efbc6-104">D3DX10CreateAsyncShaderResourceViewProcessor (funzione)</span><span class="sxs-lookup"><span data-stu-id="efbc6-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="efbc6-105">Creare un elaboratore di dati che caricherà una risorsa e quindi crei una visualizzazione delle risorse shader.</span><span class="sxs-lookup"><span data-stu-id="efbc6-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="efbc6-106">I processori di dati sono un componente della funzionalità asincrona di caricamento dei dati in D3DX10 che usa le [**pompe di thread**](id3dx10threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="efbc6-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="efbc6-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="efbc6-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="efbc6-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="efbc6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="efbc6-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efbc6-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbc6-110">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="efbc6-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="efbc6-111">Puntatore al dispositivo Direct3D (vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) che verrà usato per creare una risorsa e una visualizzazione delle risorse dello shader per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="efbc6-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="efbc6-112">*pLoadInfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="efbc6-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="efbc6-113">Tipo: **[ **d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="efbc6-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="efbc6-114">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="efbc6-114">Optional.</span></span> <span data-ttu-id="efbc6-115">Identifica le caratteristiche di una trama (vedere [**d3dx10 \_ Image \_ Load \_ info**](d3dx10-image-load-info.md)) quando viene creato il processore di dati; impostare questa proprietà su **null** per leggere le caratteristiche di una trama quando viene caricata la trama.</span><span class="sxs-lookup"><span data-stu-id="efbc6-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="efbc6-116">*ppDataProcessor* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="efbc6-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="efbc6-117">Tipo: **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="efbc6-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="efbc6-118">Indirizzo di un puntatore a un buffer che contiene il processore di dati creato (vedere [**interfaccia ID3DX10DataProcessor**](id3dx10dataprocessor.md)).</span><span class="sxs-lookup"><span data-stu-id="efbc6-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="efbc6-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="efbc6-119">Return value</span></span>

<span data-ttu-id="efbc6-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="efbc6-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="efbc6-121">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="efbc6-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="efbc6-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="efbc6-122">Requirements</span></span>



| <span data-ttu-id="efbc6-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="efbc6-123">Requirement</span></span> | <span data-ttu-id="efbc6-124">Valore</span><span class="sxs-lookup"><span data-stu-id="efbc6-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="efbc6-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="efbc6-125">Header</span></span><br/> | <dl> <span data-ttu-id="efbc6-126"><dt>D3DX10Async. h</dt></span><span class="sxs-lookup"><span data-stu-id="efbc6-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efbc6-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="efbc6-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efbc6-128">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="efbc6-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




