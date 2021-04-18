---
description: Definisce la classe di memoria che include i buffer per una risorsa.
ms.assetid: 29720b5f-16d7-4bd9-a7bd-e4dbfb00070b
title: Enumerazione D3DPOOL (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPOOL
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dc1d69d094b2f810855f9ce2116c472ba8ab605e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322924"
---
# <a name="d3dpool-enumeration"></a><span data-ttu-id="2c2af-103">Enumerazione D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="2c2af-103">D3DPOOL enumeration</span></span>

<span data-ttu-id="2c2af-104">Definisce la classe di memoria che include i buffer per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="2c2af-104">Defines the memory class that holds the buffers for a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c2af-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2c2af-105">Syntax</span></span>


```C++
typedef enum D3DPOOL { 
  D3DPOOL_DEFAULT      = 0,
  D3DPOOL_MANAGED      = 1,
  D3DPOOL_SYSTEMMEM    = 2,
  D3DPOOL_SCRATCH      = 3,
  D3DPOOL_FORCE_DWORD  = 0x7fffffff
} D3DPOOL, *LPD3DPOOL;
```



## <a name="constants"></a><span data-ttu-id="2c2af-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="2c2af-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2c2af-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**\_Impostazione predefinita D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="2c2af-107"><span id="D3DPOOL_DEFAULT"></span><span id="d3dpool_default"></span>**D3DPOOL\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="2c2af-108">Le risorse vengono inserite nel pool di memoria più appropriato per il set di utilizzi richiesti per la risorsa specificata.</span><span class="sxs-lookup"><span data-stu-id="2c2af-108">Resources are placed in the memory pool most appropriate for the set of usages requested for the given resource.</span></span> <span data-ttu-id="2c2af-109">Si tratta in genere di memoria video, inclusa la memoria video locale e la memoria AGP.</span><span class="sxs-lookup"><span data-stu-id="2c2af-109">This is usually video memory, including both local video memory and AGP memory.</span></span> <span data-ttu-id="2c2af-110">Il \_ pool predefinito D3DPOOL è separato da D3DPOOL \_ Managed e D3DPOOL \_ SYSTEMMEM e specifica che la risorsa viene posizionata nella memoria preferita per l'accesso al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2c2af-110">The D3DPOOL\_DEFAULT pool is separate from D3DPOOL\_MANAGED and D3DPOOL\_SYSTEMMEM, and it specifies that the resource is placed in the preferred memory for device access.</span></span> <span data-ttu-id="2c2af-111">Si noti che D3DPOOL \_ default non indica mai che D3DPOOL \_ Managed o D3DPOOL \_ SYSTEMMEM deve essere scelto come tipo di pool di memoria per questa risorsa.</span><span class="sxs-lookup"><span data-stu-id="2c2af-111">Note that D3DPOOL\_DEFAULT never indicates that either D3DPOOL\_MANAGED or D3DPOOL\_SYSTEMMEM should be chosen as the memory pool type for this resource.</span></span> <span data-ttu-id="2c2af-112">Le trame posizionate nel \_ pool predefinito D3DPOOL non possono essere bloccate a meno che non siano trame dinamiche oppure sono formati di driver privati, FourCC e.</span><span class="sxs-lookup"><span data-stu-id="2c2af-112">Textures placed in the D3DPOOL\_DEFAULT pool cannot be locked unless they are dynamic textures or they are private, FOURCC, driver formats.</span></span> <span data-ttu-id="2c2af-113">Per accedere a trame sbloccabili, è necessario usare funzioni quali [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9:: GetFrontBufferData**](/windows/desktop/api)e [**IDirect3DDevice9:: GetRenderTargetData**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2c2af-113">To access unlockable textures, you must use functions such as [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api), [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture), [**IDirect3DDevice9::GetFrontBufferData**](/windows/desktop/api), and [**IDirect3DDevice9::GetRenderTargetData**](/windows/desktop/api).</span></span> <span data-ttu-id="2c2af-114">D3DPOOL \_ Managed è probabilmente una scelta migliore rispetto \_ a D3DPOOL default per la maggior parte delle applicazioni.</span><span class="sxs-lookup"><span data-stu-id="2c2af-114">D3DPOOL\_MANAGED is probably a better choice than D3DPOOL\_DEFAULT for most applications.</span></span> <span data-ttu-id="2c2af-115">Si noti che alcune trame create in formati pixel proprietari del driver, sconosciute al runtime Direct3D, possono essere bloccate.</span><span class="sxs-lookup"><span data-stu-id="2c2af-115">Note that some textures created in driver-proprietary pixel formats, unknown to the Direct3D runtime, can be locked.</span></span> <span data-ttu-id="2c2af-116">Si noti anche che, a differenza delle trame, è possibile bloccare i buffer indietro della catena di scambio, le destinazioni di rendering, i buffer dei vertici e i buffer di indice.</span><span class="sxs-lookup"><span data-stu-id="2c2af-116">Also note that - unlike textures - swap chain back buffers, render targets, vertex buffers, and index buffers can be locked.</span></span> <span data-ttu-id="2c2af-117">Quando un dispositivo viene perso, è necessario rilasciare le risorse create con D3DPOOL \_ default prima di chiamare [**IDirect3DDevice9:: Reset**](/windows/desktop/api).</span><span class="sxs-lookup"><span data-stu-id="2c2af-117">When a device is lost, resources created using D3DPOOL\_DEFAULT must be released before calling [**IDirect3DDevice9::Reset**](/windows/desktop/api).</span></span> <span data-ttu-id="2c2af-118">Per altre informazioni, vedere [dispositivi persi (Direct3D 9)](lost-devices.md).</span><span class="sxs-lookup"><span data-stu-id="2c2af-118">For more information, see [Lost Devices (Direct3D 9)](lost-devices.md).</span></span>

<span data-ttu-id="2c2af-119">Quando si creano risorse con D3DPOOL \_ predefinito, se è già stato eseguito il commit della memoria della scheda video, le risorse gestite verranno rimosse per liberare memoria sufficiente per soddisfare la richiesta.</span><span class="sxs-lookup"><span data-stu-id="2c2af-119">When creating resources with D3DPOOL\_DEFAULT, if video card memory is already committed, managed resources will be evicted to free enough memory to satisfy the request.</span></span>

</dd> <dt>

<span data-ttu-id="2c2af-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL \_ gestito**</span><span class="sxs-lookup"><span data-stu-id="2c2af-120"><span id="D3DPOOL_MANAGED"></span><span id="d3dpool_managed"></span>**D3DPOOL\_MANAGED**</span></span>
</dt> <dd>

<span data-ttu-id="2c2af-121">Le risorse vengono copiate automaticamente nella memoria accessibile dal dispositivo in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2c2af-121">Resources are copied automatically to device-accessible memory as needed.</span></span> <span data-ttu-id="2c2af-122">Le risorse gestite sono supportate dalla memoria di sistema e non devono essere ricreate quando un dispositivo viene perso.</span><span class="sxs-lookup"><span data-stu-id="2c2af-122">Managed resources are backed by system memory and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="2c2af-123">Per ulteriori informazioni, vedere [gestione delle risorse (Direct3D 9)](managing-resources.md) .</span><span class="sxs-lookup"><span data-stu-id="2c2af-123">See [Managing Resources (Direct3D 9)](managing-resources.md) for more information.</span></span> <span data-ttu-id="2c2af-124">È possibile bloccare le risorse gestite.</span><span class="sxs-lookup"><span data-stu-id="2c2af-124">Managed resources can be locked.</span></span> <span data-ttu-id="2c2af-125">Viene direttamente modificata solo la copia della memoria di sistema.</span><span class="sxs-lookup"><span data-stu-id="2c2af-125">Only the system-memory copy is directly modified.</span></span> <span data-ttu-id="2c2af-126">Direct3D copia le modifiche apportate alla memoria accessibile dal driver in base alle esigenze.</span><span class="sxs-lookup"><span data-stu-id="2c2af-126">Direct3D copies your changes to driver-accessible memory as needed.</span></span>



|                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2af-127">Differenze tra Direct3D 9 e Direct3D 9Ex:</span><span class="sxs-lookup"><span data-stu-id="2c2af-127">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="2c2af-128">D3DPOOL \_ gestito è valido con [**IDirect3DDevice9**](/windows/desktop/api); tuttavia, non è valido con [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span><span class="sxs-lookup"><span data-stu-id="2c2af-128">D3DPOOL\_MANAGED is valid with [**IDirect3DDevice9**](/windows/desktop/api); however, it is not valid with [**IDirect3DDevice9Ex**](/windows/desktop/api/d3d9/nn-d3d9-idirect3ddevice9ex).</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="2c2af-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**\_SYSTEMMEM D3DPOOL**</span><span class="sxs-lookup"><span data-stu-id="2c2af-129"><span id="D3DPOOL_SYSTEMMEM"></span><span id="d3dpool_systemmem"></span>**D3DPOOL\_SYSTEMMEM**</span></span>
</dt> <dd>

<span data-ttu-id="2c2af-130">Le risorse vengono inserite in memoria che in genere non è accessibile dal dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="2c2af-130">Resources are placed in memory that is not typically accessible by the Direct3D device.</span></span> <span data-ttu-id="2c2af-131">Questa allocazione di memoria utilizza la RAM di sistema, ma non riduce la RAM paginabile.</span><span class="sxs-lookup"><span data-stu-id="2c2af-131">This memory allocation consumes system RAM but does not reduce pageable RAM.</span></span> <span data-ttu-id="2c2af-132">Queste risorse non devono essere ricreate quando un dispositivo viene perso.</span><span class="sxs-lookup"><span data-stu-id="2c2af-132">These resources do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="2c2af-133">Le risorse in questo pool possono essere bloccate e possono essere usate come origine per un'operazione [**IDirect3DDevice9:: UpdateSurface**](/windows/desktop/api) o [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) in una risorsa di memoria creata con D3DPOOL \_ valore predefinito.</span><span class="sxs-lookup"><span data-stu-id="2c2af-133">Resources in this pool can be locked and can be used as the source for a [**IDirect3DDevice9::UpdateSurface**](/windows/desktop/api) or [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture) operation to a memory resource created with D3DPOOL\_DEFAULT.</span></span>

</dd> <dt>

<span data-ttu-id="2c2af-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL \_ Scratch**</span><span class="sxs-lookup"><span data-stu-id="2c2af-134"><span id="D3DPOOL_SCRATCH"></span><span id="d3dpool_scratch"></span>**D3DPOOL\_SCRATCH**</span></span>
</dt> <dd>

<span data-ttu-id="2c2af-135">Le risorse vengono inserite nella RAM di sistema e non devono essere ricreate quando un dispositivo viene perso.</span><span class="sxs-lookup"><span data-stu-id="2c2af-135">Resources are placed in system RAM and do not need to be recreated when a device is lost.</span></span> <span data-ttu-id="2c2af-136">Queste risorse non sono vincolate dalle dimensioni del dispositivo o dalle restrizioni di formato.</span><span class="sxs-lookup"><span data-stu-id="2c2af-136">These resources are not bound by device size or format restrictions.</span></span> <span data-ttu-id="2c2af-137">Per questo motivo, non è possibile accedere a queste risorse dal dispositivo Direct3D né impostare come destinazioni di rendering o trame.</span><span class="sxs-lookup"><span data-stu-id="2c2af-137">Because of this, these resources cannot be accessed by the Direct3D device nor set as textures or render targets.</span></span> <span data-ttu-id="2c2af-138">Tuttavia, queste risorse possono sempre essere create, bloccate e copiate.</span><span class="sxs-lookup"><span data-stu-id="2c2af-138">However, these resources can always be created, locked, and copied.</span></span>

</dd> <dt>

<span data-ttu-id="2c2af-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2c2af-139"><span id="D3DPOOL_FORCE_DWORD"></span><span id="d3dpool_force_dword"></span>**D3DPOOL\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2c2af-140">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2c2af-140">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2c2af-141">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2c2af-141">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2c2af-142">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2c2af-142">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2c2af-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="2c2af-143">Remarks</span></span>

<span data-ttu-id="2c2af-144">Tutti i tipi di pool sono validi con tutte le risorse, tra cui: buffer dei vertici, buffer di indice, trame e superfici.</span><span class="sxs-lookup"><span data-stu-id="2c2af-144">All pool types are valid with all resources including: vertex buffers, index buffers, textures, and surfaces.</span></span>

<span data-ttu-id="2c2af-145">Le tabelle seguenti indicano restrizioni sui tipi di pool per le destinazioni di rendering, gli stencil di profondità e gli utilizzi dinamici e mipmap.</span><span class="sxs-lookup"><span data-stu-id="2c2af-145">The following tables indicate restrictions on pool types for render targets, depth stencils, and dynamic and mipmap usages.</span></span> <span data-ttu-id="2c2af-146">Una x indica una combinazione compatibile. la mancanza di una x indica l'incompatibilità.</span><span class="sxs-lookup"><span data-stu-id="2c2af-146">An x indicates a compatible combination; lack of an x indicates incompatibility.</span></span>



| <span data-ttu-id="2c2af-147">Pool</span><span class="sxs-lookup"><span data-stu-id="2c2af-147">Pool</span></span>               | <span data-ttu-id="2c2af-148">\_RENDERTARGET D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="2c2af-148">D3DUSAGE\_RENDERTARGET</span></span> | <span data-ttu-id="2c2af-149">\_DEPTHSTENCIL D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="2c2af-149">D3DUSAGE\_DEPTHSTENCIL</span></span> |
|--------------------|------------------------|------------------------|
| <span data-ttu-id="2c2af-150">\_Impostazione predefinita D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="2c2af-150">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="2c2af-151">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-151">x</span></span>                      | <span data-ttu-id="2c2af-152">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-152">x</span></span>                      |
| <span data-ttu-id="2c2af-153">D3DPOOL \_ gestito</span><span class="sxs-lookup"><span data-stu-id="2c2af-153">D3DPOOL\_MANAGED</span></span>   |                        |                        |
| <span data-ttu-id="2c2af-154">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="2c2af-154">D3DPOOL\_SCRATCH</span></span>   |                        |                        |
| <span data-ttu-id="2c2af-155">\_SYSTEMMEM D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="2c2af-155">D3DPOOL\_SYSTEMMEM</span></span> |                        |                        |



 



| <span data-ttu-id="2c2af-156">Pool</span><span class="sxs-lookup"><span data-stu-id="2c2af-156">Pool</span></span>               | <span data-ttu-id="2c2af-157">D3DUSAGE \_ dinamico</span><span class="sxs-lookup"><span data-stu-id="2c2af-157">D3DUSAGE\_DYNAMIC</span></span> | <span data-ttu-id="2c2af-158">\_AUTOGENMIPMAP D3DUSAGE</span><span class="sxs-lookup"><span data-stu-id="2c2af-158">D3DUSAGE\_AUTOGENMIPMAP</span></span> |
|--------------------|-------------------|-------------------------|
| <span data-ttu-id="2c2af-159">\_Impostazione predefinita D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="2c2af-159">D3DPOOL\_DEFAULT</span></span>   | <span data-ttu-id="2c2af-160">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-160">x</span></span>                 | <span data-ttu-id="2c2af-161">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-161">x</span></span>                       |
| <span data-ttu-id="2c2af-162">D3DPOOL \_ gestito</span><span class="sxs-lookup"><span data-stu-id="2c2af-162">D3DPOOL\_MANAGED</span></span>   |                   | <span data-ttu-id="2c2af-163">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-163">x</span></span>                       |
| <span data-ttu-id="2c2af-164">D3DPOOL \_ Scratch</span><span class="sxs-lookup"><span data-stu-id="2c2af-164">D3DPOOL\_SCRATCH</span></span>   |                   |                         |
| <span data-ttu-id="2c2af-165">\_SYSTEMMEM D3DPOOL</span><span class="sxs-lookup"><span data-stu-id="2c2af-165">D3DPOOL\_SYSTEMMEM</span></span> | <span data-ttu-id="2c2af-166">x</span><span class="sxs-lookup"><span data-stu-id="2c2af-166">x</span></span>                 |                         |



 

<span data-ttu-id="2c2af-167">Per ulteriori informazioni sui tipi di utilizzo, vedere [**D3DUSAGE**](d3dusage.md).</span><span class="sxs-lookup"><span data-stu-id="2c2af-167">For more information about usage types, see [**D3DUSAGE**](d3dusage.md).</span></span>

<span data-ttu-id="2c2af-168">Non è possibile combinare i pool per oggetti diversi contenuti all'interno di una risorsa (livelli MIP in una mipmap) e, quando si sceglie un pool, non è possibile modificarli.</span><span class="sxs-lookup"><span data-stu-id="2c2af-168">Pools cannot be mixed for different objects contained within one resource (mip levels in a mipmap) and, when a pool is chosen, it cannot be changed.</span></span>

<span data-ttu-id="2c2af-169">Le applicazioni devono usare D3DPOOL \_ gestiti per la maggior parte delle risorse statiche, perché questo evita che l'applicazione debba gestire i dispositivi smarriti.</span><span class="sxs-lookup"><span data-stu-id="2c2af-169">Applications should use D3DPOOL\_MANAGED for most static resources because this saves the application from having to deal with lost devices.</span></span> <span data-ttu-id="2c2af-170">(Le risorse gestite vengono ripristinate dal Runtime). Questa operazione è particolarmente utile per i sistemi di architettura della memoria unificata (UMA).</span><span class="sxs-lookup"><span data-stu-id="2c2af-170">(Managed resources are restored by the runtime.) This is especially beneficial for unified memory architecture (UMA) systems.</span></span> <span data-ttu-id="2c2af-171">Altre risorse dinamiche non sono una corrispondenza corretta per D3DPOOL \_ gestito.</span><span class="sxs-lookup"><span data-stu-id="2c2af-171">Other dynamic resources are not a good match for D3DPOOL\_MANAGED.</span></span> <span data-ttu-id="2c2af-172">In realtà, i buffer di indice e i buffer dei vertici non possono essere creati usando D3DPOOL \_ gestiti insieme a D3DUSAGE \_ Dynamic.</span><span class="sxs-lookup"><span data-stu-id="2c2af-172">In fact, index buffers and vertex buffers cannot be created using D3DPOOL\_MANAGED together with D3DUSAGE\_DYNAMIC.</span></span>

<span data-ttu-id="2c2af-173">Per le trame dinamiche è talvolta consigliabile usare una coppia di trame di memoria video e di memoria di sistema, allocando la memoria video usando D3DPOOL \_ default e la memoria di sistema usando D3DPOOL \_ SYSTEMMEM.</span><span class="sxs-lookup"><span data-stu-id="2c2af-173">For dynamic textures, it is sometimes desirable to use a pair of video memory and system memory textures, allocating the video memory using D3DPOOL\_DEFAULT and the system memory using D3DPOOL\_SYSTEMMEM.</span></span> <span data-ttu-id="2c2af-174">È possibile bloccare e modificare i bit della trama della memoria di sistema usando un metodo di blocco.</span><span class="sxs-lookup"><span data-stu-id="2c2af-174">You can lock and modify the bits of the system memory texture using a locking method.</span></span> <span data-ttu-id="2c2af-175">È quindi possibile aggiornare la trama della memoria video usando [**IDirect3DDevice9:: UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span><span class="sxs-lookup"><span data-stu-id="2c2af-175">Then you can update the video memory texture using [**IDirect3DDevice9::UpdateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-updatetexture).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c2af-176">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2c2af-176">Requirements</span></span>



| <span data-ttu-id="2c2af-177">Requisito</span><span class="sxs-lookup"><span data-stu-id="2c2af-177">Requirement</span></span> | <span data-ttu-id="2c2af-178">Valore</span><span class="sxs-lookup"><span data-stu-id="2c2af-178">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c2af-179">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2c2af-179">Header</span></span><br/> | <dl> <span data-ttu-id="2c2af-180"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2c2af-180"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c2af-181">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2c2af-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c2af-182">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="2c2af-182">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2c2af-183">**D3DUSAGE**</span><span class="sxs-lookup"><span data-stu-id="2c2af-183">**D3DUSAGE**</span></span>](d3dusage.md)
</dt> <dt>

[<span data-ttu-id="2c2af-184">**IDirect3DDevice9:: CreateCubeTexture**</span><span class="sxs-lookup"><span data-stu-id="2c2af-184">**IDirect3DDevice9::CreateCubeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture)
</dt> <dt>

[<span data-ttu-id="2c2af-185">**IDirect3DDevice9:: CreateIndexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2c2af-185">**IDirect3DDevice9::CreateIndexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createindexbuffer)
</dt> <dt>

[<span data-ttu-id="2c2af-186">**IDirect3DDevice9:: CreateTexture**</span><span class="sxs-lookup"><span data-stu-id="2c2af-186">**IDirect3DDevice9::CreateTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture)
</dt> <dt>

[<span data-ttu-id="2c2af-187">**IDirect3DDevice9:: CreateVolumeTexture**</span><span class="sxs-lookup"><span data-stu-id="2c2af-187">**IDirect3DDevice9::CreateVolumeTexture**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture)
</dt> <dt>

[<span data-ttu-id="2c2af-188">**IDirect3DDevice9:: CreateVertexBuffer**</span><span class="sxs-lookup"><span data-stu-id="2c2af-188">**IDirect3DDevice9::CreateVertexBuffer**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvertexbuffer)
</dt> <dt>

[<span data-ttu-id="2c2af-189">**D3DINDEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2c2af-189">**D3DINDEXBUFFER\_DESC**</span></span>](d3dindexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="2c2af-190">**D3DSURFACE \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2c2af-190">**D3DSURFACE\_DESC**</span></span>](d3dsurface-desc.md)
</dt> <dt>

[<span data-ttu-id="2c2af-191">**D3DVERTEXBUFFER \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2c2af-191">**D3DVERTEXBUFFER\_DESC**</span></span>](d3dvertexbuffer-desc.md)
</dt> <dt>

[<span data-ttu-id="2c2af-192">**D3DVOLUME \_ DESC**</span><span class="sxs-lookup"><span data-stu-id="2c2af-192">**D3DVOLUME\_DESC**</span></span>](d3dvolume-desc.md)
</dt> </dl>

 

 
