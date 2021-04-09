---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura.
ms.assetid: 940f1bfd-ce62-4c86-88cc-787e62cf6a93
title: 'Metodo ID3DXBaseEffect:: GetParameter (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameter
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7c96c371b36b8dcfc2e3e64a95798347ca3a6ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058688"
---
# <a name="id3dxbaseeffectgetparameter-method"></a><span data-ttu-id="fdbe9-103">Metodo ID3DXBaseEffect:: GetParameter</span><span class="sxs-lookup"><span data-stu-id="fdbe9-103">ID3DXBaseEffect::GetParameter method</span></span>

<span data-ttu-id="fdbe9-104">Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura.</span><span class="sxs-lookup"><span data-stu-id="fdbe9-104">Gets the handle of a top-level parameter or a structure member parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="fdbe9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fdbe9-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameter(
  [in] D3DXHANDLE hParameter,
  [in] UINT       Index
);
```



## <a name="parameters"></a><span data-ttu-id="fdbe9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fdbe9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdbe9-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fdbe9-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbe9-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fdbe9-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fdbe9-109">Handle del parametro o **null** per i parametri di primo livello.</span><span class="sxs-lookup"><span data-stu-id="fdbe9-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="fdbe9-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fdbe9-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="fdbe9-111">*Indice* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="fdbe9-111">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fdbe9-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fdbe9-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fdbe9-113">Indice di parametro.</span><span class="sxs-lookup"><span data-stu-id="fdbe9-113">Parameter index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdbe9-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fdbe9-114">Return value</span></span>

<span data-ttu-id="fdbe9-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="fdbe9-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="fdbe9-116">Restituisce l'handle del parametro specificato o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="fdbe9-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="fdbe9-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="fdbe9-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fdbe9-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fdbe9-118">Requirements</span></span>



| <span data-ttu-id="fdbe9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="fdbe9-119">Requirement</span></span> | <span data-ttu-id="fdbe9-120">Valore</span><span class="sxs-lookup"><span data-stu-id="fdbe9-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdbe9-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fdbe9-121">Header</span></span><br/>  | <dl> <span data-ttu-id="fdbe9-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe9-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="fdbe9-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="fdbe9-123">Library</span></span><br/> | <dl> <span data-ttu-id="fdbe9-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fdbe9-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="fdbe9-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fdbe9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdbe9-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="fdbe9-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
