---
description: Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso ID3DXPRTCompBuffer.
ms.assetid: 149098c2-35ca-46e9-a13a-94906c95cfd9
title: 'Metodo ID3DXPRTCompBuffer:: ExtractPCA (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractPCA
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6ef949e9f88a843f4636643dadd7d00ffd94d98b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322322"
---
# <a name="id3dxprtcompbufferextractpca-method"></a><span data-ttu-id="c12cb-103">Metodo ID3DXPRTCompBuffer:: ExtractPCA</span><span class="sxs-lookup"><span data-stu-id="c12cb-103">ID3DXPRTCompBuffer::ExtractPCA method</span></span>

<span data-ttu-id="c12cb-104">Estrae i coefficienti di proiezione dell'analisi dei componenti principale per campione da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c12cb-104">Extracts the per-sample principal component analysis (PCA) projection coefficients from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c12cb-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c12cb-105">Syntax</span></span>


```C++
HRESULT ExtractPCA(
  [in] UINT  StartPCA,
  [in] UINT  NumExtract,
  [in] FLOAT *pPCACoefficients
);
```



## <a name="parameters"></a><span data-ttu-id="c12cb-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c12cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c12cb-107">*StartPCA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c12cb-107">*StartPCA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12cb-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c12cb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c12cb-109">Indice iniziale per i coefficienti di proiezione PCA da estrarre dal buffer.</span><span class="sxs-lookup"><span data-stu-id="c12cb-109">Starting index for PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c12cb-110">*NumExtract* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c12cb-110">*NumExtract* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12cb-111">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c12cb-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c12cb-112">Numero di coefficienti di proiezione PCA da estrarre dal buffer.</span><span class="sxs-lookup"><span data-stu-id="c12cb-112">Number of PCA projection coefficients to extract from the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="c12cb-113">*pPCACoefficients* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c12cb-113">*pPCACoefficients* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c12cb-114">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c12cb-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c12cb-115">Puntatore alla posizione in cui vengono scritti i coefficienti AP (Principal Component Analysis) del cluster.</span><span class="sxs-lookup"><span data-stu-id="c12cb-115">Pointer to the location where clustered principal component analysis (CPCA) coefficients are written.</span></span> <span data-ttu-id="c12cb-116">La dimensione dei dati scritti è (numero di campioni) \* (numero di coefficienti PCA).</span><span class="sxs-lookup"><span data-stu-id="c12cb-116">The size of the data written is (Number of Samples) \* (Number of PCA Coefficients).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c12cb-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c12cb-117">Return value</span></span>

<span data-ttu-id="c12cb-118">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c12cb-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c12cb-119">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c12cb-119">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c12cb-120">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="c12cb-120">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c12cb-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c12cb-121">Requirements</span></span>



| <span data-ttu-id="c12cb-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="c12cb-122">Requirement</span></span> | <span data-ttu-id="c12cb-123">Valore</span><span class="sxs-lookup"><span data-stu-id="c12cb-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c12cb-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c12cb-124">Header</span></span><br/>  | <dl> <span data-ttu-id="c12cb-125"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c12cb-125"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c12cb-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="c12cb-126">Library</span></span><br/> | <dl> <span data-ttu-id="c12cb-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c12cb-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c12cb-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c12cb-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c12cb-129">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="c12cb-129">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
