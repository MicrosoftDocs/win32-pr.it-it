---
description: Prepara un dispositivo per il disegno delle linee.
ms.assetid: c597703d-6466-4b55-b1a6-a4e7c667e50c
title: 'Metodo ID3DXLine:: begin (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.Begin
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ee241b39f2d0c1939cf2cb0cc09e079abd3430a3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323478"
---
# <a name="id3dxlinebegin-method"></a><span data-ttu-id="c999c-103">Metodo ID3DXLine:: Begin</span><span class="sxs-lookup"><span data-stu-id="c999c-103">ID3DXLine::Begin method</span></span>

<span data-ttu-id="c999c-104">Prepara un dispositivo per il disegno delle linee.</span><span class="sxs-lookup"><span data-stu-id="c999c-104">Prepares a device for drawing lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="c999c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c999c-105">Syntax</span></span>


```C++
HRESULT Begin();
```



## <a name="parameters"></a><span data-ttu-id="c999c-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="c999c-106">Parameters</span></span>

<span data-ttu-id="c999c-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="c999c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c999c-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c999c-108">Return value</span></span>

<span data-ttu-id="c999c-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c999c-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c999c-110">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c999c-110">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c999c-111">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="c999c-111">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c999c-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="c999c-112">Remarks</span></span>

<span data-ttu-id="c999c-113">La chiamata a **ID3DXLine:: Begin** è facoltativa.</span><span class="sxs-lookup"><span data-stu-id="c999c-113">Calling **ID3DXLine::Begin** is optional.</span></span> <span data-ttu-id="c999c-114">Se viene chiamato al di fuori di una sequenza ID3DXLine:: Begin/ID3DXLine:: end, le funzioni di estrazione chiameranno internamente ID3DXLine:: Begin e ID3DXLine:: end.</span><span class="sxs-lookup"><span data-stu-id="c999c-114">If called outside of a ID3DXLine::Begin/ID3DXLine::End sequence, the draw functions will internally call ID3DXLine::Begin and ID3DXLine::End.</span></span> <span data-ttu-id="c999c-115">Per evitare un sovraccarico aggiuntivo, questo metodo deve essere usato se più di una funzione di estrazione verrà chiamata successivamente.</span><span class="sxs-lookup"><span data-stu-id="c999c-115">To avoid extra overhead, this method should be used if more than one draw function will be called successively.</span></span>

<span data-ttu-id="c999c-116">Questo metodo deve essere chiamato dall'interno di una sequenza [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) e [**IDirect3DDevice9:: EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) .</span><span class="sxs-lookup"><span data-stu-id="c999c-116">This method must be called from inside an [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) and [**IDirect3DDevice9::EndScene**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-endscene) sequence.</span></span>

<span data-ttu-id="c999c-117">Impossibile utilizzare ID3DXLine:: Begin come sostituto di [**IDirect3DDevice9:: BeginScene**](/windows/desktop/api) o [**ID3DXRenderToSurface:: BeginScene**](id3dxrendertosurface--beginscene.md).</span><span class="sxs-lookup"><span data-stu-id="c999c-117">ID3DXLine::Begin cannot be used as a substitute for either [**IDirect3DDevice9::BeginScene**](/windows/desktop/api) or [**ID3DXRenderToSurface::BeginScene**](id3dxrendertosurface--beginscene.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c999c-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c999c-118">Requirements</span></span>



| <span data-ttu-id="c999c-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c999c-119">Requirement</span></span> | <span data-ttu-id="c999c-120">Valore</span><span class="sxs-lookup"><span data-stu-id="c999c-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c999c-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c999c-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c999c-122"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c999c-122"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="c999c-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="c999c-123">Library</span></span><br/> | <dl> <span data-ttu-id="c999c-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c999c-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c999c-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c999c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c999c-126">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="c999c-126">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
