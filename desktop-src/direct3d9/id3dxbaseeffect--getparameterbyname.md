---
description: Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercandone il nome.
ms.assetid: fb03685e-e512-4293-80d7-6c2c0fc9ebfd
title: 'Metodo ID3DXBaseEffect:: GetParameterByName (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetParameterByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: f9f7457ffa3bba867d03cceb3521664fecc9d67d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969506"
---
# <a name="id3dxbaseeffectgetparameterbyname-method"></a><span data-ttu-id="15dfc-103">Metodo ID3DXBaseEffect:: GetParameterByName</span><span class="sxs-lookup"><span data-stu-id="15dfc-103">ID3DXBaseEffect::GetParameterByName method</span></span>

<span data-ttu-id="15dfc-104">Ottiene l'handle di un parametro di primo livello o di un parametro del membro della struttura cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="15dfc-104">Gets the handle of a top-level parameter or a structure member parameter by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="15dfc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="15dfc-105">Syntax</span></span>


```C++
D3DXHANDLE GetParameterByName(
  [in] D3DXHANDLE hParameter,
  [in] LPCSTR     pName
);
```



## <a name="parameters"></a><span data-ttu-id="15dfc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="15dfc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15dfc-107">*hParameter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15dfc-107">*hParameter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15dfc-108">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="15dfc-108">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="15dfc-109">Handle del parametro o **null** per i parametri di primo livello.</span><span class="sxs-lookup"><span data-stu-id="15dfc-109">Handle of the parameter, or **NULL** for top-level parameters.</span></span> <span data-ttu-id="15dfc-110">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="15dfc-110">See [Handles (Direct3D 9)](handles.md).</span></span>

</dd> <dt>

<span data-ttu-id="15dfc-111">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15dfc-111">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15dfc-112">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="15dfc-112">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="15dfc-113">Stringa contenente il nome del parametro.</span><span class="sxs-lookup"><span data-stu-id="15dfc-113">String containing the parameter name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15dfc-114">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="15dfc-114">Return value</span></span>

<span data-ttu-id="15dfc-115">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="15dfc-115">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="15dfc-116">Restituisce l'handle del parametro specificato o **null** se l'indice non è valido.</span><span class="sxs-lookup"><span data-stu-id="15dfc-116">Returns the handle of the specified parameter, or **NULL** if the index was invalid.</span></span> <span data-ttu-id="15dfc-117">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="15dfc-117">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15dfc-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="15dfc-118">Requirements</span></span>



| <span data-ttu-id="15dfc-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="15dfc-119">Requirement</span></span> | <span data-ttu-id="15dfc-120">Valore</span><span class="sxs-lookup"><span data-stu-id="15dfc-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="15dfc-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="15dfc-121">Header</span></span><br/>  | <dl> <span data-ttu-id="15dfc-122"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="15dfc-122"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="15dfc-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="15dfc-123">Library</span></span><br/> | <dl> <span data-ttu-id="15dfc-124"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15dfc-124"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="15dfc-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="15dfc-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15dfc-126">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="15dfc-126">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
