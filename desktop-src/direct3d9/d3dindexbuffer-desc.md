---
description: Descrive un buffer di indice.
ms.assetid: 5d45213e-b3c0-4eb7-a4f9-8d8730eb3899
title: Struttura D3DINDEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DINDEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a0bf63e732541f9394231cd82c23ff71a584b1e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969384"
---
# <a name="d3dindexbuffer_desc-structure"></a><span data-ttu-id="13f8c-103">\_Struttura D3DINDEXBUFFER DESC</span><span class="sxs-lookup"><span data-stu-id="13f8c-103">D3DINDEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="13f8c-104">Descrive un buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-104">Describes an index buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f8c-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="13f8c-105">Syntax</span></span>


```C++
typedef struct D3DINDEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
} D3DINDEXBUFFER_DESC, *LPD3DINDEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="13f8c-106">Members</span><span class="sxs-lookup"><span data-stu-id="13f8c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="13f8c-107">**Formato**</span><span class="sxs-lookup"><span data-stu-id="13f8c-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="13f8c-108">Tipo: **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="13f8c-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13f8c-109">Membro del tipo enumerato [D3DFORMAT](d3dformat.md) , che descrive il formato di superficie dei dati del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the index buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="13f8c-110">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="13f8c-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="13f8c-111">Tipo: **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="13f8c-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13f8c-112">Membro del tipo enumerato [**D3DRESOURCETYPE**](./d3dresourcetype.md) , che identifica questa risorsa come buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as an index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="13f8c-113">**Utilizzo**</span><span class="sxs-lookup"><span data-stu-id="13f8c-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="13f8c-114">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13f8c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13f8c-115">Combinazione di uno o più dei flag seguenti, che specifica l'utilizzo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="13f8c-115">Combination of one or more of the following flags, specifying the usage for this resource.</span></span>



| <span data-ttu-id="13f8c-116">Valore</span><span class="sxs-lookup"><span data-stu-id="13f8c-116">Value</span></span>                                                                                                                                                                                                   | <span data-ttu-id="13f8c-117">Significato</span><span class="sxs-lookup"><span data-stu-id="13f8c-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="D3DUSAGE_DONOTCLIP"></span><span id="d3dusage_donotclip"></span><dl> <span data-ttu-id="13f8c-118"><dt>**\_DONOTCLIP D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-118"><dt>**D3DUSAGE\_DONOTCLIP**</dt></span></span> </dl>                            | <span data-ttu-id="13f8c-119">Impostare per indicare che il contenuto del buffer dell'indice non richiede mai il ritaglio.</span><span class="sxs-lookup"><span data-stu-id="13f8c-119">Set to indicate that the index buffer content will never require clipping.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_DYNAMIC"></span><span id="d3dusage_dynamic"></span><dl> <span data-ttu-id="13f8c-120"><dt>**D3DUSAGE \_ dinamico**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-120"><dt>**D3DUSAGE\_DYNAMIC**</dt></span></span> </dl>                                  | <span data-ttu-id="13f8c-121">Impostare per indicare che il buffer dell'indice richiede l'utilizzo della memoria dinamica.</span><span class="sxs-lookup"><span data-stu-id="13f8c-121">Set to indicate that the index buffer requires dynamic memory use.</span></span> <span data-ttu-id="13f8c-122">Questa operazione è utile per i driver perché consente loro di decidere dove posizionare il buffer.</span><span class="sxs-lookup"><span data-stu-id="13f8c-122">This is useful for drivers because it enables them to decide where to place the buffer.</span></span> <span data-ttu-id="13f8c-123">In generale, i buffer di indice statici vengono inseriti nella memoria video e i buffer degli indici dinamici vengono inseriti nella memoria AGP.</span><span class="sxs-lookup"><span data-stu-id="13f8c-123">In general, static index buffers are placed in video memory and dynamic index buffers are placed in AGP memory.</span></span> <span data-ttu-id="13f8c-124">Si noti che non esiste un utilizzo statico separato; Se non si specifica D3DUSAGE \_ Dynamic, il buffer di indice viene reso statico.</span><span class="sxs-lookup"><span data-stu-id="13f8c-124">Note that there is no separate static usage; if you do not specify D3DUSAGE\_DYNAMIC the index buffer is made static.</span></span> <span data-ttu-id="13f8c-125">\_La dinamica D3DUSAGE viene applicata rigorosamente tramite i \_ flag di blocco D3DLOCK scartit e D3DLOCK \_ nowrite.</span><span class="sxs-lookup"><span data-stu-id="13f8c-125">D3DUSAGE\_DYNAMIC is strictly enforced through the D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE locking flags.</span></span> <span data-ttu-id="13f8c-126">Di conseguenza, i D3DLOCK di \_ eliminazione e D3DLOCK \_ nowrite sono validi solo per i buffer di indice creati con D3DUSAGE \_ Dynamic; non sono flag validi per i buffer dei vertici statici.</span><span class="sxs-lookup"><span data-stu-id="13f8c-126">As a result, D3DLOCK\_DISCARD and D3DLOCK\_NOOVERWRITE are only valid on index buffers created with D3DUSAGE\_DYNAMIC; they are not valid flags on static vertex buffers.</span></span><br/> <span data-ttu-id="13f8c-127">Per ulteriori informazioni sull'utilizzo dei buffer di indice dinamici, vedere [utilizzo dei buffer di indice e di vertex dinamici](performance-optimizations.md).</span><span class="sxs-lookup"><span data-stu-id="13f8c-127">For more information about using dynamic index buffers, see [Using Dynamic Vertex and Index Buffers](performance-optimizations.md).</span></span><br/> <span data-ttu-id="13f8c-128">Si noti che \_ non è possibile specificare D3DUSAGE Dynamic nei buffer dell'indice gestito.</span><span class="sxs-lookup"><span data-stu-id="13f8c-128">Note that D3DUSAGE\_DYNAMIC cannot be specified on managed index buffers.</span></span> <span data-ttu-id="13f8c-129">Per ulteriori informazioni, vedere [gestione delle risorse (Direct3D 9)](managing-resources.md).</span><span class="sxs-lookup"><span data-stu-id="13f8c-129">For more information, see [Managing Resources (Direct3D 9)](managing-resources.md).</span></span><br/> |
| <span id="D3DUSAGE_RTPATCHES"></span><span id="d3dusage_rtpatches"></span><dl> <span data-ttu-id="13f8c-130"><dt>**\_RTPATCHES D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-130"><dt>**D3DUSAGE\_RTPATCHES**</dt></span></span> </dl>                            | <span data-ttu-id="13f8c-131">Impostare per indicare quando il buffer dell'indice deve essere utilizzato per il disegno di primitive di ordine superiore.</span><span class="sxs-lookup"><span data-stu-id="13f8c-131">Set to indicate when the index buffer is to be used for drawing high-order primitives.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="D3DUSAGE_NPATCHES"></span><span id="d3dusage_npatches"></span><dl> <span data-ttu-id="13f8c-132"><dt>**\_NPATCHES D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-132"><dt>**D3DUSAGE\_NPATCHES**</dt></span></span> </dl>                               | <span data-ttu-id="13f8c-133">Impostare per indicare quando deve essere utilizzato il buffer di indice per disegnare N patch.</span><span class="sxs-lookup"><span data-stu-id="13f8c-133">Set to indicate when the index buffer is to be used for drawing N patches.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="D3DUSAGE_POINTS"></span><span id="d3dusage_points"></span><dl> <span data-ttu-id="13f8c-134"><dt>**\_Punti D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-134"><dt>**D3DUSAGE\_POINTS**</dt></span></span> </dl>                                     | <span data-ttu-id="13f8c-135">Impostare per indicare quando deve essere utilizzato il buffer di indice per gli sprite del punto di disegno o gli elenchi di punti indicizzati.</span><span class="sxs-lookup"><span data-stu-id="13f8c-135">Set to indicate when the index buffer is to be used for drawing point sprites or indexed point lists.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="D3DUSAGE_SOFTWAREPROCESSING"></span><span id="d3dusage_softwareprocessing"></span><dl> <span data-ttu-id="13f8c-136"><dt>**\_SOFTWAREPROCESSING D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-136"><dt>**D3DUSAGE\_SOFTWAREPROCESSING**</dt></span></span> </dl> | <span data-ttu-id="13f8c-137">Impostare per indicare che il buffer deve essere utilizzato con l'elaborazione del software.</span><span class="sxs-lookup"><span data-stu-id="13f8c-137">Set to indicate that the buffer is to be used with software processing.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="D3DUSAGE_WRITEONLY"></span><span id="d3dusage_writeonly"></span><dl> <span data-ttu-id="13f8c-138"><dt>**\_WRITEONLY D3DUSAGE**</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-138"><dt>**D3DUSAGE\_WRITEONLY**</dt></span></span> </dl>                            | <span data-ttu-id="13f8c-139">Informa il sistema che l'applicazione scrive solo nel buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-139">Informs the system that the application writes only to the index buffer.</span></span> <span data-ttu-id="13f8c-140">L'utilizzo di questo flag consente al driver di scegliere la migliore posizione di memoria per operazioni di scrittura e rendering efficienti.</span><span class="sxs-lookup"><span data-stu-id="13f8c-140">Using this flag enables the driver to choose the best memory location for efficient write operations and rendering.</span></span> <span data-ttu-id="13f8c-141">Il tentativo di leggere da un buffer di indice creato con questa funzionalità può comportare un peggioramento delle prestazioni.</span><span class="sxs-lookup"><span data-stu-id="13f8c-141">Attempts to read from an index buffer that is created with this capability can result in degraded performance.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="13f8c-142">**Pool**</span><span class="sxs-lookup"><span data-stu-id="13f8c-142">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="13f8c-143">Tipo: **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="13f8c-143">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13f8c-144">Membro del tipo enumerato [**D3DPOOL**](./d3dpool.md) , che specifica la classe di memoria allocata per questo buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-144">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this index buffer.</span></span>

</dd> <dt>

<span data-ttu-id="13f8c-145">**Dimensioni**</span><span class="sxs-lookup"><span data-stu-id="13f8c-145">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="13f8c-146">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13f8c-146">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="13f8c-147">Dimensioni in byte del buffer dell'indice.</span><span class="sxs-lookup"><span data-stu-id="13f8c-147">Size of the index buffer, in bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="13f8c-148">Requisiti</span><span class="sxs-lookup"><span data-stu-id="13f8c-148">Requirements</span></span>



| <span data-ttu-id="13f8c-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="13f8c-149">Requirement</span></span> | <span data-ttu-id="13f8c-150">Valore</span><span class="sxs-lookup"><span data-stu-id="13f8c-150">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13f8c-151">Intestazione</span><span class="sxs-lookup"><span data-stu-id="13f8c-151">Header</span></span><br/> | <dl> <span data-ttu-id="13f8c-152"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="13f8c-152"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f8c-153">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="13f8c-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f8c-154">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="13f8c-154">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="13f8c-155">**Getdesc**</span><span class="sxs-lookup"><span data-stu-id="13f8c-155">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="13f8c-156">Buffer di indice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="13f8c-156">Index Buffers (Direct3D 9)</span></span>](index-buffers.md)
</dt> </dl>

 

 
