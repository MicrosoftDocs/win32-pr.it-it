---
description: Applica i dati della rilegatura di trama archiviati a un buffer di trama ID3DXPRTBuffer.
ms.assetid: 05cc0709-543a-4df5-980a-8549451d396b
title: 'Metodo ID3DXPRTBuffer:: EvalGH (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.EvalGH
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 23896ff2514db7b5e12b164ea0c0a763b5d1d3b1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323706"
---
# <a name="id3dxprtbufferevalgh-method"></a><span data-ttu-id="cd2af-103">Metodo ID3DXPRTBuffer:: EvalGH</span><span class="sxs-lookup"><span data-stu-id="cd2af-103">ID3DXPRTBuffer::EvalGH method</span></span>

<span data-ttu-id="cd2af-104">Applica i dati della rilegatura di trama archiviati a un buffer di trama [**ID3DXPRTBuffer**](id3dxprtbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="cd2af-104">Applies stored texture gutter data to an [**ID3DXPRTBuffer**](id3dxprtbuffer.md) texture buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd2af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cd2af-105">Syntax</span></span>


```C++
HRESULT EvalGH();
```



## <a name="parameters"></a><span data-ttu-id="cd2af-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="cd2af-106">Parameters</span></span>

<span data-ttu-id="cd2af-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="cd2af-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cd2af-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cd2af-108">Return value</span></span>

<span data-ttu-id="cd2af-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cd2af-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cd2af-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cd2af-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="cd2af-111">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="cd2af-111">If the method fails, the following value will be returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd2af-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="cd2af-112">Remarks</span></span>

<span data-ttu-id="cd2af-113">Questo metodo effettua una chiamata interna a [**ID3DXTextureGutterHelper:: ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) per recuperare e applicare i dati di rilegatura della trama.</span><span class="sxs-lookup"><span data-stu-id="cd2af-113">This method makes an internal call to [**ID3DXTextureGutterHelper::ApplyGuttersFloat**](id3dxtexturegutterhelper--applyguttersfloat.md) to retrieve and apply texture gutter data.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd2af-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cd2af-114">Requirements</span></span>



| <span data-ttu-id="cd2af-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd2af-115">Requirement</span></span> | <span data-ttu-id="cd2af-116">Valore</span><span class="sxs-lookup"><span data-stu-id="cd2af-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd2af-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cd2af-117">Header</span></span><br/>  | <dl> <span data-ttu-id="cd2af-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="cd2af-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="cd2af-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="cd2af-119">Library</span></span><br/> | <dl> <span data-ttu-id="cd2af-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd2af-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cd2af-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cd2af-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd2af-122">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="cd2af-122">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 




