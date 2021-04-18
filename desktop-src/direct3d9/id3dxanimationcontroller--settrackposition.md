---
description: Imposta la traccia sull'ora di animazione locale specificata.
ms.assetid: 2ce87b06-1196-415f-958c-7bd407d6c69c
title: 'Metodo ID3DXAnimationController:: SetTrackPosition (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPosition
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 95c408a43df3047a52d93da0cca3d9b17053d320
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323281"
---
# <a name="id3dxanimationcontrollersettrackposition-method"></a><span data-ttu-id="2f4f1-103">Metodo ID3DXAnimationController:: SetTrackPosition</span><span class="sxs-lookup"><span data-stu-id="2f4f1-103">ID3DXAnimationController::SetTrackPosition method</span></span>

<span data-ttu-id="2f4f1-104">Imposta la traccia sull'ora di animazione locale specificata.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-104">Sets the track to the specified local animation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f4f1-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2f4f1-105">Syntax</span></span>


```C++
HRESULT SetTrackPosition(
  [in] UINT   Track,
  [in] DOUBLE Position
);
```



## <a name="parameters"></a><span data-ttu-id="2f4f1-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="2f4f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f4f1-107">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4f1-107">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4f1-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4f1-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4f1-109">Identificatore di traccia.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-109">Track identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2f4f1-110">*Posizione* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2f4f1-110">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f4f1-111">Tipo: **[ **Double**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f4f1-111">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f4f1-112">Valore dell'ora di animazione locale da assegnare alla traccia.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-112">Local animation time value to assign to the track.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f4f1-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="2f4f1-113">Return value</span></span>

<span data-ttu-id="2f4f1-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f4f1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f4f1-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2f4f1-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DERR \_ INVALIDCALL, E \_ OutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="2f4f1-116">If the method fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f4f1-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2f4f1-117">Requirements</span></span>



| <span data-ttu-id="2f4f1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f4f1-118">Requirement</span></span> | <span data-ttu-id="2f4f1-119">Valore</span><span class="sxs-lookup"><span data-stu-id="2f4f1-119">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f4f1-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2f4f1-120">Header</span></span><br/>  | <dl> <span data-ttu-id="2f4f1-121"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f4f1-121"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2f4f1-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="2f4f1-122">Library</span></span><br/> | <dl> <span data-ttu-id="2f4f1-123"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f4f1-123"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2f4f1-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2f4f1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f4f1-125">ID3DXAnimationController</span><span class="sxs-lookup"><span data-stu-id="2f4f1-125">ID3DXAnimationController</span></span>](id3dxanimationcontroller.md)
</dt> </dl>

 

 
