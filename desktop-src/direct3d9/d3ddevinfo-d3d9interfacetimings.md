---
description: Percentuale del tempo di elaborazione dei dati nel driver. Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Struttura D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322406"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="60f74-104">\_Struttura D3DDEVINFO D3D9INTERFACETIMINGS</span><span class="sxs-lookup"><span data-stu-id="60f74-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="60f74-105">Percentuale del tempo di elaborazione dei dati nel driver.</span><span class="sxs-lookup"><span data-stu-id="60f74-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="60f74-106">Queste statistiche possono aiutare a identificare i casi in cui il driver è in attesa di altre risorse.</span><span class="sxs-lookup"><span data-stu-id="60f74-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="60f74-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="60f74-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="60f74-108">Members</span><span class="sxs-lookup"><span data-stu-id="60f74-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="60f74-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="60f74-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="60f74-110">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f74-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60f74-111">Percentuale di tempo impiegato dal driver per attendere il completamento della GPU utilizzando una risorsa bloccata (e [D3DLOCK \_ DONOTWAIT](d3dlock.md) non è stato specificato).</span><span class="sxs-lookup"><span data-stu-id="60f74-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="60f74-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span><span class="sxs-lookup"><span data-stu-id="60f74-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="60f74-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f74-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60f74-114">Percentuale di tempo impiegato dal driver per attendere che la GPU completi l'elaborazione di alcuni comandi prima che il driver possa inviare altro.</span><span class="sxs-lookup"><span data-stu-id="60f74-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="60f74-115">Indica che il driver ha esaurito lo spazio necessario per inviare comandi alla GPU.</span><span class="sxs-lookup"><span data-stu-id="60f74-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="60f74-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span><span class="sxs-lookup"><span data-stu-id="60f74-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="60f74-117">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f74-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60f74-118">Percentuale di tempo impiegato dal driver in attesa della latenza GPU per ridurre a meno di tre fotogrammi di rendering.</span><span class="sxs-lookup"><span data-stu-id="60f74-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="60f74-119">Se un'applicazione è limitata a GPU, il driver deve bloccare la CPU fino a quando la GPU non si trova all'interno di tre frame.</span><span class="sxs-lookup"><span data-stu-id="60f74-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="60f74-120">In questo modo si impedisce a un'applicazione di accodare più secondi il numero di chiamate di rendering che possono aumentare significativamente la latenza tra il momento in cui l'utente immette nuovi dati e quando l'utente Visualizza i risultati di tale input.</span><span class="sxs-lookup"><span data-stu-id="60f74-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="60f74-121">In generale, il [**driver è in**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) grado di tenere traccia del numero di volte in cui viene chiamato il metodo per impedire l'accodamento di più di tre frame del lavoro di rendering.</span><span class="sxs-lookup"><span data-stu-id="60f74-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="60f74-122">**WaitingForGPUExclusiveResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="60f74-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="60f74-123">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f74-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60f74-124">Percentuale di tempo impiegato dal driver per l'attesa di una risorsa che non può essere pipelineta (gestita in parallelo).</span><span class="sxs-lookup"><span data-stu-id="60f74-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="60f74-125">Un'applicazione potrebbe voler evitare di usare una risorsa non pipeline per motivi di prestazioni.</span><span class="sxs-lookup"><span data-stu-id="60f74-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="60f74-126">**WaitingForGPUOtherTimePercent**</span><span class="sxs-lookup"><span data-stu-id="60f74-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="60f74-127">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60f74-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="60f74-128">Percentuale di tempo impiegato dal driver per l'attesa dell'elaborazione di altre GPU.</span><span class="sxs-lookup"><span data-stu-id="60f74-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60f74-129">Commenti</span><span class="sxs-lookup"><span data-stu-id="60f74-129">Remarks</span></span>

<span data-ttu-id="60f74-130">Queste metriche consentono di identificare il momento in cui un driver è in attesa e ciò che è in attesa.</span><span class="sxs-lookup"><span data-stu-id="60f74-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="60f74-131">Le percentuali elevate non rappresentano necessariamente un problema.</span><span class="sxs-lookup"><span data-stu-id="60f74-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="60f74-132">Queste metriche globali del sistema possono essere implementate o meno.</span><span class="sxs-lookup"><span data-stu-id="60f74-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="60f74-133">A seconda dell'hardware specifico, è possibile che queste metriche non supportino più query contemporaneamente.</span><span class="sxs-lookup"><span data-stu-id="60f74-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="60f74-134">Requisiti</span><span class="sxs-lookup"><span data-stu-id="60f74-134">Requirements</span></span>



| <span data-ttu-id="60f74-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="60f74-135">Requirement</span></span> | <span data-ttu-id="60f74-136">Valore</span><span class="sxs-lookup"><span data-stu-id="60f74-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="60f74-137">Intestazione</span><span class="sxs-lookup"><span data-stu-id="60f74-137">Header</span></span><br/> | <dl> <span data-ttu-id="60f74-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="60f74-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60f74-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="60f74-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60f74-140">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="60f74-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="60f74-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="60f74-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
