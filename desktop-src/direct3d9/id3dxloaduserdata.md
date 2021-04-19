---
description: Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x.
ms.assetid: 0d656f99-c24c-4326-bc6f-c0e7874c0fb2
title: Interfaccia ID3DXLoadUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLoadUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fcb07ba9351e5f6c23dd86c8147151932b3972ea
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322340"
---
# <a name="id3dxloaduserdata-interface"></a><span data-ttu-id="21a60-103">Interfaccia ID3DXLoadUserData</span><span class="sxs-lookup"><span data-stu-id="21a60-103">ID3DXLoadUserData interface</span></span>

<span data-ttu-id="21a60-104">Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="21a60-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="21a60-105">Un'istanza di questa interfaccia viene passata a [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md)e D3DX chiama il metodo appropriato su questa interfaccia ogni volta che vengono rilevati i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="21a60-105">An instance of this interface is passed to [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="21a60-106">Per ogni oggetto frame nel file con estensione x, ad esempio, viene chiamato [**ID3DXLoadUserData:: LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) e vengono passati i dati figlio.</span><span class="sxs-lookup"><span data-stu-id="21a60-106">For example, for each frame object in the .x file, [**ID3DXLoadUserData::LoadFrameChildData**](id3dxloaduserdata--loadframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="21a60-107">Membri</span><span class="sxs-lookup"><span data-stu-id="21a60-107">Members</span></span>

<span data-ttu-id="21a60-108">L'interfaccia **ID3DXLoadUserData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="21a60-108">The **ID3DXLoadUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21a60-109">**ID3DXLoadUserData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="21a60-109">**ID3DXLoadUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="21a60-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="21a60-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21a60-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="21a60-111">Methods</span></span>

<span data-ttu-id="21a60-112">L'interfaccia **ID3DXLoadUserData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="21a60-112">The **ID3DXLoadUserData** interface has these methods.</span></span>



| <span data-ttu-id="21a60-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="21a60-113">Method</span></span>                                                              | <span data-ttu-id="21a60-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21a60-114">Description</span></span>                                      |
|:--------------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="21a60-115">**LoadFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="21a60-115">**LoadFrameChildData**</span></span>](id3dxloaduserdata--loadframechilddata.md) | <span data-ttu-id="21a60-116">Caricare i dati figlio dei frame da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="21a60-116">Load frame child data from a .x file.</span></span><br/> |
| [<span data-ttu-id="21a60-117">**LoadMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="21a60-117">**LoadMeshChildData**</span></span>](id3dxloaduserdata--loadmeshchilddata.md)   | <span data-ttu-id="21a60-118">Caricare i dati figlio della mesh da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="21a60-118">Load mesh child data from a .x file.</span></span><br/>  |
| [<span data-ttu-id="21a60-119">**LoadTopLevelData**</span><span class="sxs-lookup"><span data-stu-id="21a60-119">**LoadTopLevelData**</span></span>](id3dxloaduserdata--loadtopleveldata.md)     | <span data-ttu-id="21a60-120">Caricare i dati di primo livello da un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="21a60-120">Load top level data from a .x file.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="21a60-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="21a60-121">Remarks</span></span>

<span data-ttu-id="21a60-122">Il tipo LPD3DXLOADUSERDATA è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="21a60-122">The LPD3DXLOADUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXLoadUserData ID3DXLoadUserData;
typedef interface ID3DXLoadUserData *LPD3DXLOADUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="21a60-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="21a60-123">Requirements</span></span>



| <span data-ttu-id="21a60-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="21a60-124">Requirement</span></span> | <span data-ttu-id="21a60-125">Valore</span><span class="sxs-lookup"><span data-stu-id="21a60-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21a60-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="21a60-126">Header</span></span><br/>  | <dl> <span data-ttu-id="21a60-127"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="21a60-127"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="21a60-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="21a60-128">Library</span></span><br/> | <dl> <span data-ttu-id="21a60-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21a60-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21a60-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="21a60-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21a60-131">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="21a60-131">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
