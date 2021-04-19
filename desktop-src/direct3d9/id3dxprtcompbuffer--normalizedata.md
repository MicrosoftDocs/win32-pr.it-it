---
description: Normalizza tutti i pesi di analisi del componente principale (PCA) in modo che siano compresi tra-1 e 1. I vettori di base vengono modificati per riflettere questa normalizzazione.
ms.assetid: f1c87049-a1ec-452e-b556-a2dc95324d5d
title: 'Metodo ID3DXPRTCompBuffer:: NormalizeData (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTCompBuffer.NormalizeData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9a69dacb25d04b56a14e27a43487911e56a038ef
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323459"
---
# <a name="id3dxprtcompbuffernormalizedata-method"></a><span data-ttu-id="eeeef-104">Metodo ID3DXPRTCompBuffer:: NormalizeData</span><span class="sxs-lookup"><span data-stu-id="eeeef-104">ID3DXPRTCompBuffer::NormalizeData method</span></span>

<span data-ttu-id="eeeef-105">Normalizza tutti i pesi di analisi del componente principale (PCA) in modo che siano compresi tra-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="eeeef-105">Normalizes all principal component analysis (PCA) weights so that they are between -1 and 1.</span></span> <span data-ttu-id="eeeef-106">I vettori di base vengono modificati per riflettere questa normalizzazione.</span><span class="sxs-lookup"><span data-stu-id="eeeef-106">Basis vectors are modified to reflect this normalization.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeeef-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eeeef-107">Syntax</span></span>


```C++
HRESULT NormalizeData();
```



## <a name="parameters"></a><span data-ttu-id="eeeef-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="eeeef-108">Parameters</span></span>

<span data-ttu-id="eeeef-109">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="eeeef-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eeeef-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eeeef-110">Return value</span></span>

<span data-ttu-id="eeeef-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eeeef-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eeeef-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="eeeef-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="eeeef-113">Se il metodo ha esito negativo, verrà restituito il valore seguente.</span><span class="sxs-lookup"><span data-stu-id="eeeef-113">If the method fails, the following value will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="eeeef-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eeeef-114">Requirements</span></span>



| <span data-ttu-id="eeeef-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="eeeef-115">Requirement</span></span> | <span data-ttu-id="eeeef-116">Valore</span><span class="sxs-lookup"><span data-stu-id="eeeef-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeef-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eeeef-117">Header</span></span><br/>  | <dl> <span data-ttu-id="eeeef-118"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeeef-118"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="eeeef-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="eeeef-119">Library</span></span><br/> | <dl> <span data-ttu-id="eeeef-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eeeef-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="eeeef-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eeeef-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeeef-122">ID3DXPRTCompBuffer</span><span class="sxs-lookup"><span data-stu-id="eeeef-122">ID3DXPRTCompBuffer</span></span>](id3dxprtcompbuffer.md)
</dt> </dl>

 

 




