---
description: Le applicazioni utilizzano l'interfaccia ID3DXEffectPool per identificare i parametri che verranno condivisi tra gli effetti. Vedere condivisione di parametri in clonazione e condivisione (Direct3D 9). Questa interfaccia non dispone di metodi.
ms.assetid: dd5e55eb-9436-422d-9743-38be44d05962
title: Interfaccia ID3DXEffectPool (D3DX9Effect. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectPool
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893116d7e99bd720f098a8b536f1ad4fd02563ab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401934"
---
# <a name="id3dxeffectpool-interface"></a><span data-ttu-id="d76aa-105">Interfaccia ID3DXEffectPool</span><span class="sxs-lookup"><span data-stu-id="d76aa-105">ID3DXEffectPool interface</span></span>

<span data-ttu-id="d76aa-106">Le applicazioni utilizzano l'interfaccia **ID3DXEffectPool** per identificare i parametri che verranno condivisi tra gli effetti.</span><span class="sxs-lookup"><span data-stu-id="d76aa-106">Applications use the **ID3DXEffectPool** interface to identify parameters that are going to be shared across effects.</span></span> <span data-ttu-id="d76aa-107">Vedere condivisione di parametri in [clonazione e condivisione (Direct3D 9)](cloning-and-sharing.md).</span><span class="sxs-lookup"><span data-stu-id="d76aa-107">See parameter sharing in [Cloning and Sharing (Direct3D 9)](cloning-and-sharing.md).</span></span> <span data-ttu-id="d76aa-108">Questa interfaccia non dispone di metodi.</span><span class="sxs-lookup"><span data-stu-id="d76aa-108">This interface has no methods.</span></span>

## <a name="members"></a><span data-ttu-id="d76aa-109">Membri</span><span class="sxs-lookup"><span data-stu-id="d76aa-109">Members</span></span>

<span data-ttu-id="d76aa-110">L'interfaccia **ID3DXEffectPool** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) ma non dispone di membri aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="d76aa-110">The **ID3DXEffectPool** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="d76aa-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="d76aa-111">Remarks</span></span>

<span data-ttu-id="d76aa-112">L'interfaccia ID3DXEffectPool viene ottenuta chiamando [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span><span class="sxs-lookup"><span data-stu-id="d76aa-112">The ID3DXEffectPool interface is obtained by calling [**D3DXCreateEffectPool**](d3dxcreateeffectpool.md).</span></span>

<span data-ttu-id="d76aa-113">Il tipo LPD3DXEFFECTPOOL è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="d76aa-113">The LPD3DXEFFECTPOOL type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXEffectPool ID3DXEffectPool;
typedef interface ID3DXEffectPool *LPD3DXEFFECTPOOL;
```



## <a name="requirements"></a><span data-ttu-id="d76aa-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d76aa-114">Requirements</span></span>



| <span data-ttu-id="d76aa-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d76aa-115">Requirement</span></span> | <span data-ttu-id="d76aa-116">Valore</span><span class="sxs-lookup"><span data-stu-id="d76aa-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d76aa-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d76aa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d76aa-118"><dt>D3DX9Effect. h</dt></span><span class="sxs-lookup"><span data-stu-id="d76aa-118"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="d76aa-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="d76aa-119">Library</span></span><br/> | <dl> <span data-ttu-id="d76aa-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d76aa-120"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="d76aa-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d76aa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d76aa-122">Interfacce degli effetti</span><span class="sxs-lookup"><span data-stu-id="d76aa-122">Effect Interfaces</span></span>](dx9-graphics-reference-effects-interfaces.md)
</dt> </dl>

 

 
