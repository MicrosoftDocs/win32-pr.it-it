---
description: "L'applicazione implementa questo metodo. Questo metodo viene chiamato quando si verifica un callback per un set di animazioni in una delle tracce durante una chiamata a ID3DXAnimationController:: AdvanceTime."
ms.assetid: eb606fb0-d6b9-456d-97e1-b595306e6463
title: 'Metodo ID3DXAnimationCallbackHandler:: HandleCallback (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler.HandleCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49de0adef71435dbcf35afae8cfa555999826a34
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323510"
---
# <a name="id3dxanimationcallbackhandlerhandlecallback-method"></a><span data-ttu-id="598be-104">Metodo ID3DXAnimationCallbackHandler:: HandleCallback</span><span class="sxs-lookup"><span data-stu-id="598be-104">ID3DXAnimationCallbackHandler::HandleCallback method</span></span>

<span data-ttu-id="598be-105">L'applicazione implementa questo metodo.</span><span class="sxs-lookup"><span data-stu-id="598be-105">The application implements this method.</span></span> <span data-ttu-id="598be-106">Questo metodo viene chiamato quando si verifica un callback per un set di animazioni in una delle tracce durante una chiamata a [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span><span class="sxs-lookup"><span data-stu-id="598be-106">This method is called when a callback occurs for an animation set in one of the tracks during a call to [**ID3DXAnimationController::AdvanceTime**](id3dxanimationcontroller--advancetime.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="598be-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="598be-107">Syntax</span></span>


```C++
HRESULT HandleCallback(
  [in] UINT   Track,
  [in] LPVOID pCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="598be-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="598be-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="598be-109">*Traccia* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="598be-109">*Track* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598be-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="598be-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="598be-111">Identificatore della traccia in cui si verifica il callback.</span><span class="sxs-lookup"><span data-stu-id="598be-111">Identifier of the track on which the callback occurs.</span></span>

</dd> <dt>

<span data-ttu-id="598be-112">*pCallbackData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="598be-112">*pCallbackData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="598be-113">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="598be-113">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="598be-114">Puntatore ai dati di callback di proprietà dell'utente.</span><span class="sxs-lookup"><span data-stu-id="598be-114">Pointer to user-owned callback data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="598be-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="598be-115">Return value</span></span>

<span data-ttu-id="598be-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="598be-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="598be-117">I valori restituiti da questo metodo sono implementati da un programmatore di applicazioni.</span><span class="sxs-lookup"><span data-stu-id="598be-117">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="598be-118">In generale, se non si verificano errori, programmare il metodo per restituire D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="598be-118">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="598be-119">In caso contrario, programmare il metodo per restituire un messaggio di errore appropriato da [D3DERR](d3derr.md) o [**D3DXERR**](./d3dxerr.md).</span><span class="sxs-lookup"><span data-stu-id="598be-119">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="598be-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="598be-120">Requirements</span></span>



| <span data-ttu-id="598be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="598be-121">Requirement</span></span> | <span data-ttu-id="598be-122">Valore</span><span class="sxs-lookup"><span data-stu-id="598be-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="598be-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="598be-123">Header</span></span><br/>  | <dl> <span data-ttu-id="598be-124"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="598be-124"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="598be-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="598be-125">Library</span></span><br/> | <dl> <span data-ttu-id="598be-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="598be-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="598be-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="598be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="598be-128">ID3DXAnimationCallbackHandler</span><span class="sxs-lookup"><span data-stu-id="598be-128">ID3DXAnimationCallbackHandler</span></span>](id3dxanimationcallbackhandler.md)
</dt> </dl>

 

 
