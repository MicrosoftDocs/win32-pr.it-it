---
description: Estrae i vettori di base di media e dell'analisi dei componenti principali (PCA) per un determinato cluster da un buffer di dati compresso ID3DXPRTCompBuffer.
ms.assetid: dcb1372f-2c8f-4d18-9840-5982b2ed0d6e
title: 'Metodo ID3DXPRTCompBuffer:: ExtractBasis (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractBasis
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ebedef91c9f3d1e277a099ffd295903e9ba77ba8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323037"
---
# <a name="id3dxprtcompbufferextractbasis-method"></a><span data-ttu-id="c73d1-103">Metodo ID3DXPRTCompBuffer:: ExtractBasis</span><span class="sxs-lookup"><span data-stu-id="c73d1-103">ID3DXPRTCompBuffer::ExtractBasis method</span></span>

<span data-ttu-id="c73d1-104">Estrae i vettori di base di media e dell'analisi dei componenti principali (PCA) per un determinato cluster da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="c73d1-104">Extracts the mean and principal component analysis (PCA) basis vectors for a given cluster from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c73d1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c73d1-105">Syntax</span></span>


```C++
HRESULT ExtractBasis(
  [in]      UINT  Cluster,
  [in, out] FLOAT *pClusterBasis
);
```



## <a name="parameters"></a><span data-ttu-id="c73d1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c73d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c73d1-107">*Cluster* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c73d1-107">*Cluster* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c73d1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c73d1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c73d1-109">Cluster per cui verrà estratta la base.</span><span class="sxs-lookup"><span data-stu-id="c73d1-109">Cluster for which the basis will be extracted.</span></span>

</dd> <dt>

<span data-ttu-id="c73d1-110">*pClusterBasis* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="c73d1-110">*pClusterBasis* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c73d1-111">Tipo: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c73d1-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="c73d1-112">Puntatore a una matrice di dati vettoriali di base per il cluster.</span><span class="sxs-lookup"><span data-stu-id="c73d1-112">Pointer to an array of basis vector data for Cluster.</span></span> <span data-ttu-id="c73d1-113">La dimensione dei dati FLOAT archiviati sarà: (1 + numero di vettori PCA per cluster) \* (numero di coefficienti) \* (numero di canali colori)</span><span class="sxs-lookup"><span data-stu-id="c73d1-113">The size of the FLOAT data stored will be: (1 + Number of PCA vectors per cluster) \* (Number of coefficients) \* (Number of color channels)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c73d1-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c73d1-114">Return value</span></span>

<span data-ttu-id="c73d1-115">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c73d1-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c73d1-116">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c73d1-116">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="c73d1-117">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="c73d1-117">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="c73d1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c73d1-118">Requirements</span></span>



| <span data-ttu-id="c73d1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c73d1-119">Requirement</span></span> | <span data-ttu-id="c73d1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c73d1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c73d1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c73d1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c73d1-122"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c73d1-122"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c73d1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c73d1-123">Library</span></span><br/> | <dl> <span data-ttu-id="c73d1-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c73d1-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c73d1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c73d1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c73d1-126">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="c73d1-126">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
