---
description: Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e4fcf8db9e60a30aee060dcc483b8d01e59b1c
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343196"
---
# <a name="d3dlock"></a><span data-ttu-id="2d8fe-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="2d8fe-103">D3DLOCK</span></span>

<span data-ttu-id="2d8fe-104">Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="2d8fe-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="2d8fe-105">\#define</span></span>                   | <span data-ttu-id="2d8fe-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2d8fe-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d8fe-107">D3DLOCK \_ DISCARD</span><span class="sxs-lookup"><span data-stu-id="2d8fe-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="2d8fe-108">L'applicazione rimuove tutta la memoria all'interno dell'area bloccata.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="2d8fe-109">Per i buffer dei vertici e degli indici, l'intero buffer verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="2d8fe-110">Questa opzione è valida solo quando la risorsa viene creata con l'utilizzo dinamico (vedere [D3DUSAGE).](d3dusage.md)</span><span class="sxs-lookup"><span data-stu-id="2d8fe-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="2d8fe-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="2d8fe-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="2d8fe-112">Consente a un'applicazione di recuperare i cicli della CPU se il driver non riesce a bloccare immediatamente la superficie.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="2d8fe-113">Se questo flag è impostato e il driver non può bloccare immediatamente la superficie, la chiamata di blocco restituirà D3DERR \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="2d8fe-114">Questo flag può essere usato solo quando si blocca una superficie creata usando [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)</span><span class="sxs-lookup"><span data-stu-id="2d8fe-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="2d8fe-115">Questo flag può essere usato anche con un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="2d8fe-116">D3DLOCK \_ NO \_ DIRTY \_ UPDATE</span><span class="sxs-lookup"><span data-stu-id="2d8fe-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="2d8fe-117">Per impostazione predefinita, un blocco su una risorsa aggiunge un'area dirty a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="2d8fe-118">Questa opzione impedisce qualsiasi modifica allo stato dirty della risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="2d8fe-119">Le applicazioni devono usare questa opzione quando hanno informazioni aggiuntive sul set di aree modificate durante l'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="2d8fe-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="2d8fe-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="2d8fe-121">Indica che la memoria a cui si è fatto riferimento in una chiamata di disegno dall'ultimo blocco senza questo flag non verrà modificata durante il blocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="2d8fe-122">In questo modo è possibile abilitare le ottimizzazioni quando l'applicazione aggiunge dati a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="2d8fe-123">Se si specifica questo flag, il driver può restituire immediatamente se la risorsa è in uso. In caso contrario, il driver deve completare l'uso della risorsa prima di restituire il blocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="2d8fe-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="2d8fe-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="2d8fe-125">Il comportamento predefinito di un blocco di memoria video è riservare una sezione critica a livello di sistema, garantendo che non si verifichino modifiche della modalità di visualizzazione per la durata del blocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="2d8fe-126">Questa opzione fa sì che la sezione critica a livello di sistema non sia mantenuta per la durata del blocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="2d8fe-127">L'operazione di blocco richiede molto tempo, ma può consentire al sistema di eseguire altri compiti, ad esempio lo spostamento del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="2d8fe-128">Questa opzione è utile per i blocchi di lunga durata, ad esempio il blocco del buffer nascosto per il rendering software che in caso contrario influirebbe negativamente sulla velocità di risposta del sistema.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="2d8fe-129">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="2d8fe-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="2d8fe-130">L'applicazione non scriverà nel buffer.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-130">The application will not write to the buffer.</span></span> <span data-ttu-id="2d8fe-131">Ciò consente alle risorse archiviate in formati non nativi di salvare il passaggio di ricompressione durante lo sblocco.</span><span class="sxs-lookup"><span data-stu-id="2d8fe-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="2d8fe-132">Informazioni costanti</span><span class="sxs-lookup"><span data-stu-id="2d8fe-132">Constant Information</span></span>



|  <span data-ttu-id="2d8fe-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d8fe-133">Requirement</span></span>                        | <span data-ttu-id="2d8fe-134">Valore</span><span class="sxs-lookup"><span data-stu-id="2d8fe-134">Value</span></span>            |
|--------------------------|-------------|
| <span data-ttu-id="2d8fe-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2d8fe-135">Header</span></span>                   | <span data-ttu-id="2d8fe-136">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="2d8fe-136">d3d9types.h</span></span> |
| <span data-ttu-id="2d8fe-137">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="2d8fe-137">Minimum operating system</span></span> | <span data-ttu-id="2d8fe-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="2d8fe-138">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="2d8fe-139">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d8fe-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d8fe-140">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="2d8fe-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="2d8fe-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="2d8fe-142">**Lock**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-142">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="2d8fe-143">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-143">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="2d8fe-144">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-144">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="2d8fe-145">**Lock**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-145">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="2d8fe-146">**Archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-146">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="2d8fe-147">**Archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-147">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="2d8fe-148">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-148">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="2d8fe-149">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-149">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="2d8fe-150">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-150">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="2d8fe-151">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-151">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="2d8fe-152">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-152">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="2d8fe-153">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-153">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="2d8fe-154">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2d8fe-154">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
