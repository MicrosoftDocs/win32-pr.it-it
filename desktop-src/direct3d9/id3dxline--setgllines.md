---
description: Consente di impostare la modalità per creare linee di tipo OpenGL.
ms.assetid: 298bf391-9f2b-4352-b9f8-3bc2ab661eee
title: 'Metodo ID3DXLine:: SetGLLines (D3dx9core. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetGLLines
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 131c472ef4a2254880ef560edccb9c0cf1c8774b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103886330"
---
# <a name="id3dxlinesetgllines-method"></a><span data-ttu-id="f24ab-103">Metodo ID3DXLine:: SetGLLines</span><span class="sxs-lookup"><span data-stu-id="f24ab-103">ID3DXLine::SetGLLines method</span></span>

<span data-ttu-id="f24ab-104">Consente di impostare la modalità per creare linee di tipo OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f24ab-104">Toggles the mode to draw OpenGL-style lines.</span></span>

## <a name="syntax"></a><span data-ttu-id="f24ab-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f24ab-105">Syntax</span></span>


```C++
HRESULT SetGLLines(
  [in] BOOL bGLLines
);
```



## <a name="parameters"></a><span data-ttu-id="f24ab-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f24ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f24ab-107">*bGLLines* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f24ab-107">*bGLLines* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f24ab-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f24ab-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f24ab-109">Consente di abilitare o disabilitare il disegno a linee in stile OpenGL.</span><span class="sxs-lookup"><span data-stu-id="f24ab-109">Toggles OpenGL-style line drawing.</span></span> <span data-ttu-id="f24ab-110">**True** Abilita le linee di tipo OpenGL e **false** Abilita le linee di tipo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="f24ab-110">**TRUE** enables OpenGL-style lines, and **FALSE** enables Direct3D-style lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f24ab-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f24ab-111">Return value</span></span>

<span data-ttu-id="f24ab-112">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f24ab-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f24ab-113">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f24ab-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f24ab-114">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="f24ab-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f24ab-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f24ab-115">Requirements</span></span>



| <span data-ttu-id="f24ab-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f24ab-116">Requirement</span></span> | <span data-ttu-id="f24ab-117">Valore</span><span class="sxs-lookup"><span data-stu-id="f24ab-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f24ab-118">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f24ab-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f24ab-119"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f24ab-120">Libreria</span><span class="sxs-lookup"><span data-stu-id="f24ab-120">Library</span></span><br/> | <dl> <span data-ttu-id="f24ab-121"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f24ab-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f24ab-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f24ab-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f24ab-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="f24ab-123">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
