---
description: Determina se un quaternione è un quaternione di identità.
ms.assetid: 1cd39e1b-9b68-434d-b7b0-3ec6cddb8757
title: Funzione D3DXQuaternionIsIdentity (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionIsIdentity
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b2b02bdddb4b7a2d31a685f576434e34952c0a22
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323308"
---
# <a name="d3dxquaternionisidentity-function"></a><span data-ttu-id="dcf28-103">D3DXQuaternionIsIdentity (funzione)</span><span class="sxs-lookup"><span data-stu-id="dcf28-103">D3DXQuaternionIsIdentity function</span></span>

<span data-ttu-id="dcf28-104">Determina se un quaternione è un quaternione di identità.</span><span class="sxs-lookup"><span data-stu-id="dcf28-104">Determines if a quaternion is an identity quaternion.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcf28-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dcf28-105">Syntax</span></span>


```C++
BOOL D3DXQuaternionIsIdentity(
  _In_ const D3DXQUATERNION *pQ
);
```



## <a name="parameters"></a><span data-ttu-id="dcf28-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="dcf28-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf28-107">*PQ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dcf28-107">*pQ* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dcf28-108">Tipo: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="dcf28-108">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="dcf28-109">Puntatore alla struttura [**D3DXQUATERNION**](d3dxquaternion.md) che verrà testata per l'identità.</span><span class="sxs-lookup"><span data-stu-id="dcf28-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that will be tested for identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf28-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="dcf28-110">Return value</span></span>

<span data-ttu-id="dcf28-111">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="dcf28-111">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="dcf28-112">Se il quaternione è un quaternione Identity, questa funzione restituisce **true**.</span><span class="sxs-lookup"><span data-stu-id="dcf28-112">If the quaternion is an identity quaternion, this function returns **TRUE**.</span></span> <span data-ttu-id="dcf28-113">In caso contrario, la funzione restituisce **false**.</span><span class="sxs-lookup"><span data-stu-id="dcf28-113">Otherwise, this function returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf28-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="dcf28-114">Remarks</span></span>

<span data-ttu-id="dcf28-115">Usare [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) per qualsiasi input quaternione non ancora normalizzato.</span><span class="sxs-lookup"><span data-stu-id="dcf28-115">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcf28-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dcf28-116">Requirements</span></span>



| <span data-ttu-id="dcf28-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="dcf28-117">Requirement</span></span> | <span data-ttu-id="dcf28-118">Valore</span><span class="sxs-lookup"><span data-stu-id="dcf28-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf28-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dcf28-119">Header</span></span><br/>  | <dl> <span data-ttu-id="dcf28-120"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="dcf28-120"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="dcf28-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="dcf28-121">Library</span></span><br/> | <dl> <span data-ttu-id="dcf28-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dcf28-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="dcf28-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="dcf28-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf28-124">Funzioni matematiche</span><span class="sxs-lookup"><span data-stu-id="dcf28-124">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="dcf28-125">**D3DXQuaternionIdentity**</span><span class="sxs-lookup"><span data-stu-id="dcf28-125">**D3DXQuaternionIdentity**</span></span>](d3dxquaternionidentity.md)
</dt> </dl>

 

 
