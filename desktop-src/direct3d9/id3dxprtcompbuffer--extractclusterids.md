---
description: Estrae gli ID cluster per campione da un buffer di dati compresso ID3DXPRTCompBuffer.
ms.assetid: d78d82ab-58bc-4b73-9ca0-8b7f06867618
title: 'Metodo ID3DXPRTCompBuffer:: ExtractClusterIDs (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.ExtractClusterIDs
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ef68a972109e89e318adb83ab388c653c6a3deed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323693"
---
# <a name="id3dxprtcompbufferextractclusterids-method"></a><span data-ttu-id="456ea-103">Metodo ID3DXPRTCompBuffer:: ExtractClusterIDs</span><span class="sxs-lookup"><span data-stu-id="456ea-103">ID3DXPRTCompBuffer::ExtractClusterIDs method</span></span>

<span data-ttu-id="456ea-104">Estrae gli ID cluster per campione da un buffer di dati compresso [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="456ea-104">Extracts the per-sample cluster IDs from an [**ID3DXPRTCompBuffer**](id3dxprtcompbuffer.md) compressed data buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="456ea-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="456ea-105">Syntax</span></span>


```C++
HRESULT ExtractClusterIDs(
  [in, out] UINT *pClusterIDs
);
```



## <a name="parameters"></a><span data-ttu-id="456ea-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="456ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="456ea-107">*pClusterIDs* \[ in uscita\]</span><span class="sxs-lookup"><span data-stu-id="456ea-107">*pClusterIDs* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="456ea-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="456ea-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="456ea-109">Puntatore alla posizione in memoria in cui vengono scritti gli ID.</span><span class="sxs-lookup"><span data-stu-id="456ea-109">Pointer to the location in memory where IDs are written.</span></span> <span data-ttu-id="456ea-110">La lunghezza della memoria necessaria è il valore restituito da [**ID3DXPRTCompBuffer:: GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span><span class="sxs-lookup"><span data-stu-id="456ea-110">The length of memory required is the value returned by [**ID3DXPRTCompBuffer::GetNumSamples**](id3dxprtcompbuffer--getnumsamples.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="456ea-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="456ea-111">Return value</span></span>

<span data-ttu-id="456ea-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="456ea-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="456ea-113">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="456ea-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="456ea-114">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="456ea-114">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="456ea-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="456ea-115">Requirements</span></span>



| <span data-ttu-id="456ea-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="456ea-116">Requirement</span></span> | <span data-ttu-id="456ea-117">Valore</span><span class="sxs-lookup"><span data-stu-id="456ea-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="456ea-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="456ea-118">Header</span></span><br/>  | <dl> <span data-ttu-id="456ea-119"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="456ea-119"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="456ea-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="456ea-120">Library</span></span><br/> | <dl> <span data-ttu-id="456ea-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="456ea-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="456ea-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="456ea-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="456ea-123">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="456ea-123">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 
