---
description: Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Interfaccia ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322549"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="1dc4c-103">Interfaccia ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="1dc4c-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="1dc4c-104">Questa interfaccia viene implementata dall'applicazione per salvare eventuali dati utente aggiuntivi incorporati nei file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="1dc4c-105">Un'istanza di questa interfaccia viene passata a [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md)e D3DX chiama il metodo appropriato su questa interfaccia ogni volta che vengono rilevati i dati appropriati.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="1dc4c-106">Per ogni oggetto frame nel file con estensione x, ad esempio, viene chiamato [**ID3DXSaveUserData:: AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) e vengono passati i dati figlio.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="1dc4c-107">Membri</span><span class="sxs-lookup"><span data-stu-id="1dc4c-107">Members</span></span>

<span data-ttu-id="1dc4c-108">L'interfaccia **ID3DXSaveUserData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1dc4c-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1dc4c-109">**ID3DXSaveUserData** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="1dc4c-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="1dc4c-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="1dc4c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1dc4c-111">Metodi</span><span class="sxs-lookup"><span data-stu-id="1dc4c-111">Methods</span></span>

<span data-ttu-id="1dc4c-112">L'interfaccia **ID3DXSaveUserData** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="1dc4c-113">Metodo</span><span class="sxs-lookup"><span data-stu-id="1dc4c-113">Method</span></span>                                                                              | <span data-ttu-id="1dc4c-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dc4c-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="1dc4c-115">**AddFrameChildData**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="1dc4c-116">Aggiungere i dati figlio al frame.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="1dc4c-117">**AddMeshChildData**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="1dc4c-118">Aggiungere i dati figlio alla rete.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="1dc4c-119">**AddTopLevelDataObjectsPost**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="1dc4c-120">Aggiungere un oggetto di primo livello dopo la gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="1dc4c-121">**AddTopLevelDataObjectsPre**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="1dc4c-122">Aggiungere un oggetto di primo livello prima della gerarchia dei frame.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="1dc4c-123">**RegisterTemplates**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="1dc4c-124">Callback che consente all'utente di registrare un modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="1dc4c-125">**SaveTemplates**</span><span class="sxs-lookup"><span data-stu-id="1dc4c-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="1dc4c-126">Callback che consente all'utente di salvare un modello di file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="1dc4c-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="1dc4c-127">Remarks</span></span>

<span data-ttu-id="1dc4c-128">Il tipo LPD3DXSAVEUSERDATA è definito come puntatore a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="1dc4c-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="1dc4c-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1dc4c-129">Requirements</span></span>



| <span data-ttu-id="1dc4c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="1dc4c-130">Requirement</span></span> | <span data-ttu-id="1dc4c-131">Valore</span><span class="sxs-lookup"><span data-stu-id="1dc4c-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dc4c-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1dc4c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="1dc4c-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4c-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="1dc4c-134">Libreria</span><span class="sxs-lookup"><span data-stu-id="1dc4c-134">Library</span></span><br/> | <dl> <span data-ttu-id="1dc4c-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dc4c-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dc4c-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1dc4c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dc4c-137">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="1dc4c-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
