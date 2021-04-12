---
description: Ottiene l'handle di una funzione cercandone il nome.
ms.assetid: 1e2e2dae-5084-47f3-9812-3dbf609bd70b
title: 'Metodo ID3DXBaseEffect:: GetFunctionByName (D3DX9Effect. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseEffect.GetFunctionByName
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: e1cd9ec56ff5df3bff293ade0669b4cd7c8dad5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355909"
---
# <a name="id3dxbaseeffectgetfunctionbyname-method"></a><span data-ttu-id="272fe-103">Metodo ID3DXBaseEffect:: GetFunctionByName</span><span class="sxs-lookup"><span data-stu-id="272fe-103">ID3DXBaseEffect::GetFunctionByName method</span></span>

<span data-ttu-id="272fe-104">Ottiene l'handle di una funzione cercandone il nome.</span><span class="sxs-lookup"><span data-stu-id="272fe-104">Gets the handle of a function by looking up its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="272fe-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="272fe-105">Syntax</span></span>


```C++
D3DXHANDLE GetFunctionByName(
  [in] LPCSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="272fe-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="272fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="272fe-107">*pname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="272fe-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="272fe-108">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="272fe-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="272fe-109">Stringa contenente il nome della funzione.</span><span class="sxs-lookup"><span data-stu-id="272fe-109">String containing the function name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="272fe-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="272fe-110">Return value</span></span>

<span data-ttu-id="272fe-111">Tipo: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span><span class="sxs-lookup"><span data-stu-id="272fe-111">Type: **[D3DXHANDLE](dx9-graphics-reference-effects-constants.md)**</span></span>

<span data-ttu-id="272fe-112">Restituisce l'handle della funzione specificata o **null** se il nome non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="272fe-112">Returns the handle of the specified function, or **NULL** if the name was not found.</span></span> <span data-ttu-id="272fe-113">Vedere [handle (Direct3D 9)](handles.md).</span><span class="sxs-lookup"><span data-stu-id="272fe-113">See [Handles (Direct3D 9)](handles.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="272fe-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="272fe-114">Requirements</span></span>



| <span data-ttu-id="272fe-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="272fe-115">Requirement</span></span> | <span data-ttu-id="272fe-116">Valore</span><span class="sxs-lookup"><span data-stu-id="272fe-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="272fe-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="272fe-117">Header</span></span><br/>  | <dl> <span data-ttu-id="272fe-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="272fe-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="272fe-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="272fe-119">Library</span></span><br/> | <dl> <span data-ttu-id="272fe-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="272fe-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="272fe-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="272fe-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="272fe-122">ID3DXBaseEffect</span><span class="sxs-lookup"><span data-stu-id="272fe-122">ID3DXBaseEffect</span></span>](id3dxbaseeffect.md)
</dt> </dl>

 

 
