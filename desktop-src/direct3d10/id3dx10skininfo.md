---
description: ID3DX10SkinInfo consente di ottimizzare, elaborare e impostare manualmente la relazione tra le ossa e i vertici nelle mesh (vedere animazione scheletrica su Wikipedia).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Interfaccia ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354929"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="7dd6d-103">Interfaccia ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="7dd6d-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="7dd6d-104">ID3DX10SkinInfo consente di ottimizzare, elaborare e impostare manualmente la relazione tra le ossa e i vertici nelle mesh (vedere [animazione scheletrica su Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="7dd6d-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="7dd6d-105">È particolarmente utile per la creazione di file con estensione x esportati da app DCC (ad esempio 3DS Max e Maya) più intuitivi e per il miglioramento della velocità di rendering delle mesh con skin in modalità di rendering software.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="7dd6d-106">Membri</span><span class="sxs-lookup"><span data-stu-id="7dd6d-106">Members</span></span>

<span data-ttu-id="7dd6d-107">L'interfaccia **ID3DX10SkinInfo** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="7dd6d-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="7dd6d-108">**ID3DX10SkinInfo** dispone anche di questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="7dd6d-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="7dd6d-109">Metodi</span><span class="sxs-lookup"><span data-stu-id="7dd6d-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="7dd6d-110">Metodi</span><span class="sxs-lookup"><span data-stu-id="7dd6d-110">Methods</span></span>

<span data-ttu-id="7dd6d-111">L'interfaccia **ID3DX10SkinInfo** dispone di questi metodi.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="7dd6d-112">Metodo</span><span class="sxs-lookup"><span data-stu-id="7dd6d-112">Method</span></span>                                                                   | <span data-ttu-id="7dd6d-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7dd6d-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7dd6d-114">**AddBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="7dd6d-115">Consentire a un osso esistente di influenzare un gruppo di vertici e definire la quantità di influenza dell'osso su ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="7dd6d-116">**AddBones**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="7dd6d-117">Allocare spazio per più ossa.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="7dd6d-118">**AddVertices**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="7dd6d-119">Allocare spazio per altri vertici.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="7dd6d-120">**ClearBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="7dd6d-121">Cancellare l'elenco di vertici di un osso che influenza.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="7dd6d-122">**Compact**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="7dd6d-123">Limitare il numero di ossa che possono influenzare un vertice e/o limitare la quantità di influenza che può avere un osso su un vertice.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="7dd6d-124">**DoSoftwareSkinning**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="7dd6d-125">Eseguire il skining del software su una matrice di vertici.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="7dd6d-126">**FindBoneInfluenceIndex**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="7dd6d-127">Trovare l'indice che indica la posizione in cui un vertice specificato si trova in un elenco di vertici influenzato di un dato osso.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="7dd6d-128">**GetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="7dd6d-129">Ottenere la quantità di influenza di un dato osso su un vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="7dd6d-130">**GetBoneInfluenceCount**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="7dd6d-131">Ottiene il numero di vertici influenzati da un determinato osso.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="7dd6d-132">**GetBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="7dd6d-133">Ottiene un elenco di vertici influenzati da un dato osso e un elenco della quantità di influenza che l'osso ha su ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="7dd6d-134">**GetMaxBoneInfluences**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="7dd6d-135">Ottenere il numero di vertici a cui un osso può influenzare al massimo.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="7dd6d-136">**GetNumBones**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="7dd6d-137">Ottenere il numero di Bones in ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="7dd6d-138">**GetNumVertices**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="7dd6d-139">Ottenere il numero di vertici in ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="7dd6d-140">**RemapBones**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="7dd6d-141">Modificare le ossa che influenzano i vertici.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="7dd6d-142">**RemapVertices**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="7dd6d-143">Modificare i vertici influenzati da quali ossa.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="7dd6d-144">**RemoveBone**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="7dd6d-145">Rimuovere un osso.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="7dd6d-146">**SetBoneInfluence**</span><span class="sxs-lookup"><span data-stu-id="7dd6d-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="7dd6d-147">Imposta la quantità di influenza di un dato osso su un vertice specificato.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7dd6d-148">Commenti</span><span class="sxs-lookup"><span data-stu-id="7dd6d-148">Remarks</span></span>

<span data-ttu-id="7dd6d-149">Creare un'interfaccia ID3DX10SkinInfo con [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** o **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="7dd6d-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="7dd6d-150">Il tipo LPD3DX10SKININFO è definito come puntatore all'interfaccia **ID3DX10SkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="7dd6d-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="7dd6d-151">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7dd6d-151">Requirements</span></span>



| <span data-ttu-id="7dd6d-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dd6d-152">Requirement</span></span> | <span data-ttu-id="7dd6d-153">Valore</span><span class="sxs-lookup"><span data-stu-id="7dd6d-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7dd6d-154">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7dd6d-154">Header</span></span><br/>  | <dl> <span data-ttu-id="7dd6d-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dd6d-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7dd6d-156">Libreria</span><span class="sxs-lookup"><span data-stu-id="7dd6d-156">Library</span></span><br/> | <dl> <span data-ttu-id="7dd6d-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7dd6d-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dd6d-158">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7dd6d-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dd6d-159">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="7dd6d-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
