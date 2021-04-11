---
description: Attiva o disattiva l'output di debug di D3DX.
ms.assetid: e35cbfd2-401e-47ec-9f5b-e2ed63ea1fcd
title: Funzione D3DXDebugMute (D3dx9core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXDebugMute
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9259fa43a6a64829e42cbaa661aa7223a958f22d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235023"
---
# <a name="d3dxdebugmute-function"></a><span data-ttu-id="58f56-103">D3DXDebugMute (funzione)</span><span class="sxs-lookup"><span data-stu-id="58f56-103">D3DXDebugMute function</span></span>

<span data-ttu-id="58f56-104">Attiva o disattiva l'output di debug di D3DX.</span><span class="sxs-lookup"><span data-stu-id="58f56-104">Turns on or off all D3DX debug output.</span></span>

## <a name="syntax"></a><span data-ttu-id="58f56-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="58f56-105">Syntax</span></span>


```C++
BOOL D3DXDebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="58f56-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="58f56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58f56-107">*Disattiva* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="58f56-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="58f56-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58f56-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58f56-109">Se **true**, l'output del debugger viene interrotto; Se **false**, l'output di debug è abilitato.</span><span class="sxs-lookup"><span data-stu-id="58f56-109">If **TRUE**, debugger output is halted; if **FALSE**, debug output is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="58f56-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="58f56-110">Return value</span></span>

<span data-ttu-id="58f56-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="58f56-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="58f56-112">Restituisce il valore precedente di mute.</span><span class="sxs-lookup"><span data-stu-id="58f56-112">Returns the previous value of Mute.</span></span>

## <a name="requirements"></a><span data-ttu-id="58f56-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="58f56-113">Requirements</span></span>



| <span data-ttu-id="58f56-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="58f56-114">Requirement</span></span> | <span data-ttu-id="58f56-115">Valore</span><span class="sxs-lookup"><span data-stu-id="58f56-115">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="58f56-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="58f56-116">Header</span></span><br/>  | <dl> <span data-ttu-id="58f56-117"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="58f56-117"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="58f56-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="58f56-118">Library</span></span><br/> | <dl> <span data-ttu-id="58f56-119"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="58f56-119"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="58f56-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="58f56-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58f56-121">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="58f56-121">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
