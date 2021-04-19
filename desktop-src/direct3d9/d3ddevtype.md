---
description: Definisce i tipi di dispositivo.
ms.assetid: 2bcdc476-7c42-4152-b107-58366faf2abd
title: Enumerazione D3DDEVTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 2be365ffbbe5bf778379c7be060c85c0b099422f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322395"
---
# <a name="d3ddevtype-enumeration"></a><span data-ttu-id="2993b-103">Enumerazione D3DDEVTYPE</span><span class="sxs-lookup"><span data-stu-id="2993b-103">D3DDEVTYPE enumeration</span></span>

<span data-ttu-id="2993b-104">Definisce i tipi di dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2993b-104">Defines device types.</span></span>

## <a name="syntax"></a><span data-ttu-id="2993b-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2993b-105">Syntax</span></span>


```C++
typedef enum D3DDEVTYPE { 
  D3DDEVTYPE_HAL          = 1,
  D3DDEVTYPE_NULLREF      = 4,
  D3DDEVTYPE_REF          = 2,
  D3DDEVTYPE_SW           = 3,
  D3DDEVTYPE_FORCE_DWORD  = 0xffffffff
} D3DDEVTYPE, *LPD3DDEVTYPE;
```



## <a name="constants"></a><span data-ttu-id="2993b-106">Costanti</span><span class="sxs-lookup"><span data-stu-id="2993b-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="2993b-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**\_Hal D3DDEVTYPE**</span><span class="sxs-lookup"><span data-stu-id="2993b-107"><span id="D3DDEVTYPE_HAL"></span><span id="d3ddevtype_hal"></span>**D3DDEVTYPE\_HAL**</span></span>
</dt> <dd>

<span data-ttu-id="2993b-108">Rasterizzazione dell'hardware.</span><span class="sxs-lookup"><span data-stu-id="2993b-108">Hardware rasterization.</span></span> <span data-ttu-id="2993b-109">L'ombreggiatura viene eseguita con software, hardware o trasformazione mista e illuminazione.</span><span class="sxs-lookup"><span data-stu-id="2993b-109">Shading is done with software, hardware, or mixed transform and lighting.</span></span>

</dd> <dt>

<span data-ttu-id="2993b-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**\_NULLREF D3DDEVTYPE**</span><span class="sxs-lookup"><span data-stu-id="2993b-110"><span id="D3DDEVTYPE_NULLREF"></span><span id="d3ddevtype_nullref"></span>**D3DDEVTYPE\_NULLREF**</span></span>
</dt> <dd>

<span data-ttu-id="2993b-111">Inizializzare Direct3D in un computer che non ha né hardware né la rasterizzazione dei riferimenti disponibile e abilitare le risorse per la creazione di contenuto 3D.</span><span class="sxs-lookup"><span data-stu-id="2993b-111">Initialize Direct3D on a computer that has neither hardware nor reference rasterization available, and enable resources for 3D content creation.</span></span> <span data-ttu-id="2993b-112">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="2993b-112">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2993b-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE \_ ref**</span><span class="sxs-lookup"><span data-stu-id="2993b-113"><span id="D3DDEVTYPE_REF"></span><span id="d3ddevtype_ref"></span>**D3DDEVTYPE\_REF**</span></span>
</dt> <dd>

<span data-ttu-id="2993b-114">Le funzionalità Direct3D sono implementate nel software; Tuttavia, l'rasterizzazione dei riferimenti usa istruzioni della CPU speciali ogni volta che è possibile.</span><span class="sxs-lookup"><span data-stu-id="2993b-114">Direct3D features are implemented in software; however, the reference rasterizer does make use of special CPU instructions whenever it can.</span></span>

<span data-ttu-id="2993b-115">Il dispositivo di riferimento viene installato da Windows SDK 8,0 o versione successiva ed è pensato come supporto per il debug solo a scopo di sviluppo.</span><span class="sxs-lookup"><span data-stu-id="2993b-115">The reference device is installed by the Windows SDK 8.0 or later and is intended as an aid in debugging for development only.</span></span>

</dd> <dt>

<span data-ttu-id="2993b-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE \_ SW**</span><span class="sxs-lookup"><span data-stu-id="2993b-116"><span id="D3DDEVTYPE_SW"></span><span id="d3ddevtype_sw"></span>**D3DDEVTYPE\_SW**</span></span>
</dt> <dd>

<span data-ttu-id="2993b-117">Un dispositivo software collegabile che è stato registrato con [**IDirect3D9:: RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span><span class="sxs-lookup"><span data-stu-id="2993b-117">A pluggable software device that has been registered with [**IDirect3D9::RegisterSoftwareDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-registersoftwaredevice).</span></span>

</dd> <dt>

<span data-ttu-id="2993b-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="2993b-118"><span id="D3DDEVTYPE_FORCE_DWORD"></span><span id="d3ddevtype_force_dword"></span>**D3DDEVTYPE\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="2993b-119">Impone la compilazione di questa enumerazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2993b-119">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="2993b-120">Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2993b-120">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="2993b-121">Questo valore non viene utilizzato.</span><span class="sxs-lookup"><span data-stu-id="2993b-121">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2993b-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="2993b-122">Remarks</span></span>

<span data-ttu-id="2993b-123">Tutti i metodi dell'interfaccia [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) che accettano un tipo di dispositivo **D3DDEVTYPE** avranno esito negativo se \_ si specifica D3DDEVTYPE NULLREF.</span><span class="sxs-lookup"><span data-stu-id="2993b-123">All methods of the [**IDirect3D9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3d9) interface that take a **D3DDEVTYPE** device type will fail if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="2993b-124">Per usare questi metodi, sostituire D3DDEVTYPE \_ ref nella chiamata al metodo.</span><span class="sxs-lookup"><span data-stu-id="2993b-124">To use these methods, substitute D3DDEVTYPE\_REF in the method call.</span></span>

<span data-ttu-id="2993b-125">\_È necessario creare un dispositivo Ref D3DDEVTYPE in D3DPOOL \_ Scratch Memory, a meno che non siano necessari buffer di Vertex e index.</span><span class="sxs-lookup"><span data-stu-id="2993b-125">A D3DDEVTYPE\_REF device should be created in D3DPOOL\_SCRATCH memory, unless vertex and index buffers are required.</span></span> <span data-ttu-id="2993b-126">Per supportare i buffer dei vertici e degli indici, creare il dispositivo in D3DPOOL \_ SYSTEMMEM Memory.</span><span class="sxs-lookup"><span data-stu-id="2993b-126">To support vertex and index buffers, create the device in D3DPOOL\_SYSTEMMEM memory.</span></span>

<span data-ttu-id="2993b-127">Se D3dref9.dll è installato, Direct3D utilizzerà l'unità di rasterizzazione dei riferimenti per creare un \_ tipo di dispositivo Ref D3DDEVTYPE, anche se \_ è specificato D3DDEVTYPE NULLREF.</span><span class="sxs-lookup"><span data-stu-id="2993b-127">If D3dref9.dll is installed, Direct3D will use the reference rasterizer to create a D3DDEVTYPE\_REF device type, even if D3DDEVTYPE\_NULLREF is specified.</span></span> <span data-ttu-id="2993b-128">Se D3dref9.dll non è disponibile e \_ viene specificato D3DDEVTYPE NULLREF, Direct3D non eseguirà né il rendering né la presentazione della scena.</span><span class="sxs-lookup"><span data-stu-id="2993b-128">If D3dref9.dll is not available and D3DDEVTYPE\_NULLREF is specified, Direct3D will neither render nor present the scene.</span></span>

## <a name="requirements"></a><span data-ttu-id="2993b-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2993b-129">Requirements</span></span>



| <span data-ttu-id="2993b-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="2993b-130">Requirement</span></span> | <span data-ttu-id="2993b-131">Valore</span><span class="sxs-lookup"><span data-stu-id="2993b-131">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2993b-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="2993b-132">Header</span></span><br/> | <dl> <span data-ttu-id="2993b-133"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="2993b-133"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2993b-134">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2993b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2993b-135">Enumerazioni Direct3D</span><span class="sxs-lookup"><span data-stu-id="2993b-135">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="2993b-136">**IDirect3D9:: CheckDeviceFormat**</span><span class="sxs-lookup"><span data-stu-id="2993b-136">**IDirect3D9::CheckDeviceFormat**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)
</dt> <dt>

[<span data-ttu-id="2993b-137">**IDirect3D9:: CheckDeviceMultiSampleType**</span><span class="sxs-lookup"><span data-stu-id="2993b-137">**IDirect3D9::CheckDeviceMultiSampleType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype)
</dt> <dt>

[<span data-ttu-id="2993b-138">**IDirect3D9:: CheckDeviceType**</span><span class="sxs-lookup"><span data-stu-id="2993b-138">**IDirect3D9::CheckDeviceType**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)
</dt> <dt>

[<span data-ttu-id="2993b-139">**IDirect3D9:: CreateDevice**</span><span class="sxs-lookup"><span data-stu-id="2993b-139">**IDirect3D9::CreateDevice**</span></span>](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[<span data-ttu-id="2993b-140">**IDirect3D9:: GetDeviceCaps**</span><span class="sxs-lookup"><span data-stu-id="2993b-140">**IDirect3D9::GetDeviceCaps**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3d9-getdevicecaps)
</dt> <dt>

[<span data-ttu-id="2993b-141">**\_Parametri di creazione D3DDEVICE \_**</span><span class="sxs-lookup"><span data-stu-id="2993b-141">**D3DDEVICE\_CREATION\_PARAMETERS**</span></span>](d3ddevice-creation-parameters.md)
</dt> </dl>

 

 
