---
description: Abilita o Disabilita i messaggi di debug.
ms.assetid: 5c2aa3cf-ee6a-40fd-b300-67cb6ce691b6
title: Funzione D3DX10DebugMute (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DebugMute
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 6f331e3f074a4b77a1f1a7f1a8117cf660940f7d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323182"
---
# <a name="d3dx10debugmute-function"></a><span data-ttu-id="dc11a-103">D3DX10DebugMute (funzione)</span><span class="sxs-lookup"><span data-stu-id="dc11a-103">D3DX10DebugMute function</span></span>

<span data-ttu-id="dc11a-104">Abilita o Disabilita i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="dc11a-104">Enable or disable debug messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc11a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc11a-105">Syntax</span></span>


```C++
HRESULT D3DX10DebugMute(
  _In_ BOOL Mute
);
```



## <a name="parameters"></a><span data-ttu-id="dc11a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dc11a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc11a-107">*Disattiva* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dc11a-107">*Mute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc11a-108">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dc11a-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dc11a-109">Impostare su **true** per abilitare i messaggi di debug; impostare su **false** per disabilitare i messaggi di debug.</span><span class="sxs-lookup"><span data-stu-id="dc11a-109">Set to **TRUE** to enable debug messages; set to **FALSE** to disable debug messages.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc11a-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dc11a-110">Return value</span></span>

<span data-ttu-id="dc11a-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="dc11a-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="dc11a-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="dc11a-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dc11a-113">Commenti</span><span class="sxs-lookup"><span data-stu-id="dc11a-113">Remarks</span></span>

<span data-ttu-id="dc11a-114">Usare questa funzione per disabilitare i messaggi di errore per le API D3DX10 durante il debug; l'uso di questa funzione deve essere sorvegliato dall'opzione del \_ compilatore D3D10 debug.</span><span class="sxs-lookup"><span data-stu-id="dc11a-114">Use this function to disable error messages for D3DX10 APIs during debug; the use of this function should be guarded by the D3D10\_DEBUG compiler switch.</span></span>


```
#ifdef D3D10_DEBUG
  BOOL WINAPI D3DX10DebugMute(BOOL Mute);  
#endif
```



<span data-ttu-id="dc11a-115">Lo stato predefinito è **true** per una compilazione di debug.</span><span class="sxs-lookup"><span data-stu-id="dc11a-115">The default state is **TRUE** for a debug build.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc11a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc11a-116">Requirements</span></span>



| <span data-ttu-id="dc11a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc11a-117">Requirement</span></span> | <span data-ttu-id="dc11a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dc11a-118">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dc11a-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc11a-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dc11a-120"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc11a-120"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="dc11a-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="dc11a-121">Library</span></span><br/> | <dl> <span data-ttu-id="dc11a-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dc11a-122"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dc11a-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dc11a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dc11a-124">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="dc11a-124">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
