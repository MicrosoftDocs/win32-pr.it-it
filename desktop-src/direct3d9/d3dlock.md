---
description: Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.
ms.assetid: 46a611bd-a1ec-4967-b68d-72661d1b5cad
title: D3DLOCK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adaeddbc1aff0812d3e0f67df90c2cf9b1118347
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/26/2021
ms.locfileid: "107999428"
---
# <a name="d3dlock"></a><span data-ttu-id="ee31d-103">D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="ee31d-103">D3DLOCK</span></span>

<span data-ttu-id="ee31d-104">Combinazione di zero o più opzioni di blocco che descrivono il tipo di blocco da eseguire.</span><span class="sxs-lookup"><span data-stu-id="ee31d-104">A combination of zero or more locking options that describe the type of lock to perform.</span></span>



| <span data-ttu-id="ee31d-105">\#Definire</span><span class="sxs-lookup"><span data-stu-id="ee31d-105">\#define</span></span>                   | <span data-ttu-id="ee31d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee31d-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee31d-107">D3DLOCK \_ DISCARD</span><span class="sxs-lookup"><span data-stu-id="ee31d-107">D3DLOCK\_DISCARD</span></span>           | <span data-ttu-id="ee31d-108">L'applicazione rimuove tutta la memoria all'interno dell'area bloccata.</span><span class="sxs-lookup"><span data-stu-id="ee31d-108">The application discards all memory within the locked region.</span></span> <span data-ttu-id="ee31d-109">Per i buffer dei vertici e degli indici, l'intero buffer verrà eliminato.</span><span class="sxs-lookup"><span data-stu-id="ee31d-109">For vertex and index buffers, the entire buffer will be discarded.</span></span> <span data-ttu-id="ee31d-110">Questa opzione è valida solo quando la risorsa viene creata con utilizzo dinamico (vedere [D3DUSAGE](d3dusage.md)).</span><span class="sxs-lookup"><span data-stu-id="ee31d-110">This option is only valid when the resource is created with dynamic usage (see [D3DUSAGE](d3dusage.md)).</span></span>                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ee31d-111">D3DLOCK \_ DONOTWAIT</span><span class="sxs-lookup"><span data-stu-id="ee31d-111">D3DLOCK\_DONOTWAIT</span></span>         | <span data-ttu-id="ee31d-112">Consente a un'applicazione di recuperare i cicli della CPU se il driver non riesce a bloccare immediatamente la superficie.</span><span class="sxs-lookup"><span data-stu-id="ee31d-112">Allows an application to gain back CPU cycles if the driver cannot lock the surface immediately.</span></span> <span data-ttu-id="ee31d-113">Se questo flag è impostato e il driver non può bloccare immediatamente la superficie, la chiamata di blocco restituirà D3DERR \_ WASSTILLDRAWING.</span><span class="sxs-lookup"><span data-stu-id="ee31d-113">If this flag is set and the driver cannot lock the surface immediately, the lock call will return D3DERR\_WASSTILLDRAWING.</span></span> <span data-ttu-id="ee31d-114">Questo flag può essere usato solo quando si blocca una superficie creata usando [**CreateOffscreenPlainSurface,**](/windows/desktop/api) [**CreateRenderTarget**](/windows/desktop/api)o [**CreateDepthStencilSurface.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface)</span><span class="sxs-lookup"><span data-stu-id="ee31d-114">This flag can only be used when locking a surface created using [**CreateOffscreenPlainSurface**](/windows/desktop/api), [**CreateRenderTarget**](/windows/desktop/api), or [**CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface).</span></span> <span data-ttu-id="ee31d-115">Questo flag può essere usato anche con un buffer nascosto.</span><span class="sxs-lookup"><span data-stu-id="ee31d-115">This flag can also be used with a back buffer.</span></span>            |
| <span data-ttu-id="ee31d-116">D3DLOCK \_ NO \_ DIRTY \_ UPDATE</span><span class="sxs-lookup"><span data-stu-id="ee31d-116">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span> | <span data-ttu-id="ee31d-117">Per impostazione predefinita, un blocco su una risorsa aggiunge un'area dirty a tale risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee31d-117">By default, a lock on a resource adds a dirty region to that resource.</span></span> <span data-ttu-id="ee31d-118">Questa opzione impedisce qualsiasi modifica allo stato dirty della risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee31d-118">This option prevents any changes to the dirty state of the resource.</span></span> <span data-ttu-id="ee31d-119">Le applicazioni devono usare questa opzione quando hanno informazioni aggiuntive sul set di aree modificate durante l'operazione di blocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-119">Applications should use this option when they have additional information about the set of regions changed during the lock operation.</span></span>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="ee31d-120">D3DLOCK \_ NOOVERWRITE</span><span class="sxs-lookup"><span data-stu-id="ee31d-120">D3DLOCK\_NOOVERWRITE</span></span>       | <span data-ttu-id="ee31d-121">Indica che la memoria a cui si è fatto riferimento in una chiamata di disegno dall'ultimo blocco senza questo flag non verrà modificata durante il blocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-121">Indicates that memory that was referred to in a drawing call since the last lock without this flag will not be modified during the lock.</span></span> <span data-ttu-id="ee31d-122">In questo modo è possibile abilitare le ottimizzazioni quando l'applicazione aggiunge dati a una risorsa.</span><span class="sxs-lookup"><span data-stu-id="ee31d-122">This can enable optimizations when the application is appending data to a resource.</span></span> <span data-ttu-id="ee31d-123">Se si specifica questo flag, il driver viene restituito immediatamente se la risorsa è in uso. In caso contrario, il driver deve completare l'uso della risorsa prima di tornare al blocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-123">Specifying this flag enables the driver to return immediately if the resource is in use, otherwise, the driver must finish using the resource before returning from locking.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="ee31d-124">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="ee31d-124">D3DLOCK\_NOSYSLOCK</span></span>         | <span data-ttu-id="ee31d-125">Il comportamento predefinito di un blocco di memoria video è riservare una sezione critica a livello di sistema, garantendo che non si verifichino modifiche alla modalità di visualizzazione per la durata del blocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-125">The default behavior of a video memory lock is to reserve a system-wide critical section, guaranteeing that no display mode changes will occur for the duration of the lock.</span></span> <span data-ttu-id="ee31d-126">Questa opzione fa sì che la sezione critica a livello di sistema non sia mantenuta per la durata del blocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-126">This option causes the system-wide critical section not to be held for the duration of the lock.</span></span><br/> <span data-ttu-id="ee31d-127">L'operazione di blocco richiede molto tempo, ma può consentire al sistema di eseguire altri compiti, ad esempio lo spostamento del cursore del mouse.</span><span class="sxs-lookup"><span data-stu-id="ee31d-127">The lock operation is time consuming, but can enable the system to perform other duties, such as moving the mouse cursor.</span></span> <span data-ttu-id="ee31d-128">Questa opzione è utile per i blocchi a lungo termine, ad esempio il blocco del buffer nascosto per il rendering del software che altrimenti influirebbe negativamente sulla velocità di risposta del sistema.</span><span class="sxs-lookup"><span data-stu-id="ee31d-128">This option is useful for long-duration locks, such as the lock of the back buffer for software rendering that would otherwise adversely affect system responsiveness.</span></span><br/> |
| <span data-ttu-id="ee31d-129">D3DLOCK \_ READONLY</span><span class="sxs-lookup"><span data-stu-id="ee31d-129">D3DLOCK\_READONLY</span></span>          | <span data-ttu-id="ee31d-130">L'applicazione non scriverà nel buffer.</span><span class="sxs-lookup"><span data-stu-id="ee31d-130">The application will not write to the buffer.</span></span> <span data-ttu-id="ee31d-131">Ciò consente alle risorse archiviate in formati non nativi di salvare il passaggio di ricompressione durante lo sblocco.</span><span class="sxs-lookup"><span data-stu-id="ee31d-131">This enables resources stored in non-native formats to save the recompression step when unlocking.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="constant-information"></a><span data-ttu-id="ee31d-132">Informazioni sulle costanti</span><span class="sxs-lookup"><span data-stu-id="ee31d-132">Constant Information</span></span>



|                          |             |
|--------------------------|-------------|
| <span data-ttu-id="ee31d-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ee31d-133">Header</span></span>                   | <span data-ttu-id="ee31d-134">d3d9types.h</span><span class="sxs-lookup"><span data-stu-id="ee31d-134">d3d9types.h</span></span> |
| <span data-ttu-id="ee31d-135">Sistema operativo minimo</span><span class="sxs-lookup"><span data-stu-id="ee31d-135">Minimum operating system</span></span> | <span data-ttu-id="ee31d-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="ee31d-136">Windows 98</span></span>  |



 

## <a name="related-topics"></a><span data-ttu-id="ee31d-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="ee31d-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee31d-138">Costanti Direct3D</span><span class="sxs-lookup"><span data-stu-id="ee31d-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="ee31d-139">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="ee31d-139">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="ee31d-140">**Lock**</span><span class="sxs-lookup"><span data-stu-id="ee31d-140">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="ee31d-141">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="ee31d-141">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="ee31d-142">**LockRect**</span><span class="sxs-lookup"><span data-stu-id="ee31d-142">**LockRect**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-lockrect)
</dt> <dt>

[<span data-ttu-id="ee31d-143">**Lock**</span><span class="sxs-lookup"><span data-stu-id="ee31d-143">**Lock**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dindexbuffer9-lock)
</dt> <dt>

[<span data-ttu-id="ee31d-144">**Archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="ee31d-144">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="ee31d-145">**Archivio protetto**</span><span class="sxs-lookup"><span data-stu-id="ee31d-145">**LockBox**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolume9-lockbox)
</dt> <dt>

[<span data-ttu-id="ee31d-146">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-146">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="ee31d-147">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)
</dt> <dt>

<span data-ttu-id="ee31d-148">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-148">**LockVertexBuffer**</span></span>
</dt> <dt>

[<span data-ttu-id="ee31d-149">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-149">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="ee31d-150">**LockAttributeBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-150">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)
</dt> <dt>

[<span data-ttu-id="ee31d-151">**LockIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-151">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)
</dt> <dt>

[<span data-ttu-id="ee31d-152">**LockVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="ee31d-152">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)
</dt> </dl>

 

 
