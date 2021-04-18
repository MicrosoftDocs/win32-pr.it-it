---
description: Descrive lo stato corrente della clip.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Struttura D3DCLIPSTATUS9 (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCLIPSTATUS9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 3b22fdfcc136c05ec8fe03ae491612606b2df62f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322376"
---
# <a name="d3dclipstatus9-structure"></a><span data-ttu-id="b34f7-103">Struttura D3DCLIPSTATUS9</span><span class="sxs-lookup"><span data-stu-id="b34f7-103">D3DCLIPSTATUS9 structure</span></span>

<span data-ttu-id="b34f7-104">Descrive lo stato corrente della clip.</span><span class="sxs-lookup"><span data-stu-id="b34f7-104">Describes the current clip status.</span></span>

## <a name="syntax"></a><span data-ttu-id="b34f7-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b34f7-105">Syntax</span></span>


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a><span data-ttu-id="b34f7-106">Members</span><span class="sxs-lookup"><span data-stu-id="b34f7-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b34f7-107">**ClipUnion**</span><span class="sxs-lookup"><span data-stu-id="b34f7-107">**ClipUnion**</span></span>
</dt> <dd>

<span data-ttu-id="b34f7-108">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b34f7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b34f7-109">Ritagliare i flag Unione che descrivono lo stato corrente della clip.</span><span class="sxs-lookup"><span data-stu-id="b34f7-109">Clip union flags that describe the current clip status.</span></span> <span data-ttu-id="b34f7-110">Il membro può essere costituito da uno o più dei flag seguenti:</span><span class="sxs-lookup"><span data-stu-id="b34f7-110">This member can be one or more of the following flags:</span></span>



| <span data-ttu-id="b34f7-111">Valore</span><span class="sxs-lookup"><span data-stu-id="b34f7-111">Value</span></span>                                                                                                                                                      | <span data-ttu-id="b34f7-112">Significato</span><span class="sxs-lookup"><span data-stu-id="b34f7-112">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <span data-ttu-id="b34f7-113"><dt>**D3DCS \_ tutto**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-113"><dt>**D3DCS\_ALL**</dt></span></span> </dl>          | <span data-ttu-id="b34f7-114">Combinazione di tutti i flag di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="b34f7-114">Combination of all clip flags.</span></span><br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <span data-ttu-id="b34f7-115"><dt>**D3DCS a \_ sinistra**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-115"><dt>**D3DCS\_LEFT**</dt></span></span> </dl>       | <span data-ttu-id="b34f7-116">Tutti i vertici vengono ritagliati dal piano sinistro del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-116">All vertices are clipped by the left plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <span data-ttu-id="b34f7-117"><dt>**D3DCS a \_ destra**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-117"><dt>**D3DCS\_RIGHT**</dt></span></span> </dl>    | <span data-ttu-id="b34f7-118">Tutti i vertici vengono ritagliati dal piano destro del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-118">All vertices are clipped by the right plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <span data-ttu-id="b34f7-119"><dt>**D3DCS \_ Top**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-119"><dt>**D3DCS\_TOP**</dt></span></span> </dl>          | <span data-ttu-id="b34f7-120">Tutti i vertici vengono ritagliati dal piano superiore del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-120">All vertices are clipped by the top plane of the viewing frustum.</span></span><br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <span data-ttu-id="b34f7-121"><dt>**D3DCS in \_ basso**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-121"><dt>**D3DCS\_BOTTOM**</dt></span></span> </dl> | <span data-ttu-id="b34f7-122">Tutti i vertici vengono ritagliati dal piano inferiore del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-122">All vertices are clipped by the bottom plane of the viewing frustum.</span></span><br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <span data-ttu-id="b34f7-123"><dt>**D3DCS \_ front**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-123"><dt>**D3DCS\_FRONT**</dt></span></span> </dl>    | <span data-ttu-id="b34f7-124">Tutti i vertici vengono ritagliati dal piano anteriore del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-124">All vertices are clipped by the front plane of the viewing frustum.</span></span><br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <span data-ttu-id="b34f7-125"><dt>**D3DCS \_ indietro**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-125"><dt>**D3DCS\_BACK**</dt></span></span> </dl>       | <span data-ttu-id="b34f7-126">Tutti i vertici vengono ritagliati dal piano posteriore del tronco di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-126">All vertices are clipped by the back plane of the viewing frustum.</span></span><br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <span data-ttu-id="b34f7-127"><dt>**\_PLANE0 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-127"><dt>**D3DCS\_PLANE0**</dt></span></span> </dl> | <span data-ttu-id="b34f7-128">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-128">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <span data-ttu-id="b34f7-129"><dt>**\_PLANE1 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-129"><dt>**D3DCS\_PLANE1**</dt></span></span> </dl> | <span data-ttu-id="b34f7-130">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-130">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <span data-ttu-id="b34f7-131"><dt>**\_PLANE2 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-131"><dt>**D3DCS\_PLANE2**</dt></span></span> </dl> | <span data-ttu-id="b34f7-132">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-132">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <span data-ttu-id="b34f7-133"><dt>**\_PLANE3 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-133"><dt>**D3DCS\_PLANE3**</dt></span></span> </dl> | <span data-ttu-id="b34f7-134">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-134">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <span data-ttu-id="b34f7-135"><dt>**\_PLANE4 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-135"><dt>**D3DCS\_PLANE4**</dt></span></span> </dl> | <span data-ttu-id="b34f7-136">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-136">Application-defined clipping planes.</span></span><br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <span data-ttu-id="b34f7-137"><dt>**\_PLANE5 D3DCS**</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-137"><dt>**D3DCS\_PLANE5**</dt></span></span> </dl> | <span data-ttu-id="b34f7-138">Piani di ritaglio definiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b34f7-138">Application-defined clipping planes.</span></span><br/>                                 |



 

</dd> <dt>

<span data-ttu-id="b34f7-139">**ClipIntersection**</span><span class="sxs-lookup"><span data-stu-id="b34f7-139">**ClipIntersection**</span></span>
</dt> <dd>

<span data-ttu-id="b34f7-140">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b34f7-140">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="b34f7-141">Ritagliare i flag di intersezione che descrivono lo stato corrente della clip.</span><span class="sxs-lookup"><span data-stu-id="b34f7-141">Clip intersection flags that describe the current clip status.</span></span> <span data-ttu-id="b34f7-142">Questo membro può assumere gli stessi flag di ClipUnion.</span><span class="sxs-lookup"><span data-stu-id="b34f7-142">This member can take the same flags as ClipUnion.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b34f7-143">Commenti</span><span class="sxs-lookup"><span data-stu-id="b34f7-143">Remarks</span></span>

<span data-ttu-id="b34f7-144">Quando il ritaglio viene abilitato durante l'elaborazione del vertice (da [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)o altre funzioni di disegno), Direct3D calcola un codice di ritaglio per ogni vertice.</span><span class="sxs-lookup"><span data-stu-id="b34f7-144">When clipping is enabled during vertex processing (by [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), or other drawing functions), Direct3D computes a clip code for every vertex.</span></span> <span data-ttu-id="b34f7-145">Il codice di ritaglio è una combinazione di D3DCS \_ \* bit.</span><span class="sxs-lookup"><span data-stu-id="b34f7-145">The clip code is a combination of D3DCS\_\* bits.</span></span> <span data-ttu-id="b34f7-146">Quando un vertice è esterno a un particolare piano di ritaglio, il bit corrispondente viene impostato nel codice di ritaglio.</span><span class="sxs-lookup"><span data-stu-id="b34f7-146">When a vertex is outside a particular clipping plane, the corresponding bit is set in the clipping code.</span></span> <span data-ttu-id="b34f7-147">Direct3D mantiene lo stato della clip utilizzando **D3DCLIPSTATUS9**, che include membri ClipUnion e ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="b34f7-147">Direct3D maintains the clip status using **D3DCLIPSTATUS9**, which has ClipUnion and ClipIntersection members.</span></span> <span data-ttu-id="b34f7-148">ClipUnion è un operatore OR bit per bit di tutti i codici di clip dei vertici e ClipIntersection è un AND bit per bit di tutti i codici di ritaglio</span><span class="sxs-lookup"><span data-stu-id="b34f7-148">ClipUnion is a bitwise OR of all vertex clip codes and ClipIntersection is a bitwise AND of all vertex clip codes.</span></span> <span data-ttu-id="b34f7-149">I valori iniziali sono pari a zero per ClipUnion e 0xFFFFFFFF per ClipIntersection.</span><span class="sxs-lookup"><span data-stu-id="b34f7-149">Initial values are zero for ClipUnion and 0xFFFFFFFF for ClipIntersection.</span></span> <span data-ttu-id="b34f7-150">Quando il \_ ritaglio D3DRS è impostato su **false**, ClipUnion e ClipIntersection sono impostati su zero.</span><span class="sxs-lookup"><span data-stu-id="b34f7-150">When D3DRS\_CLIPPING is set to **FALSE**, ClipUnion and ClipIntersection are set to zero.</span></span> <span data-ttu-id="b34f7-151">Direct3D aggiorna lo stato della clip durante le chiamate di disegno.</span><span class="sxs-lookup"><span data-stu-id="b34f7-151">Direct3D updates the clip status during drawing calls.</span></span> <span data-ttu-id="b34f7-152">Per calcolare lo stato della clip per un determinato oggetto, impostare ClipUnion e ClipIntersection sul valore iniziale e continuare a disegnare.</span><span class="sxs-lookup"><span data-stu-id="b34f7-152">To compute clip status for a particular object, set ClipUnion and ClipIntersection to their initial value and continue drawing.</span></span>

<span data-ttu-id="b34f7-153">Lo stato della clip non viene aggiornato da [**DrawRectPatch**](/windows/desktop/api) e [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) perché non sono disponibili emulazioni software.</span><span class="sxs-lookup"><span data-stu-id="b34f7-153">Clip status is not updated by [**DrawRectPatch**](/windows/desktop/api) and [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) because there is no software emulation for them.</span></span>

## <a name="requirements"></a><span data-ttu-id="b34f7-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b34f7-154">Requirements</span></span>



| <span data-ttu-id="b34f7-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b34f7-155">Requirement</span></span> | <span data-ttu-id="b34f7-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b34f7-156">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b34f7-157">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b34f7-157">Header</span></span><br/> | <dl> <span data-ttu-id="b34f7-158"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="b34f7-158"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b34f7-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b34f7-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b34f7-160">Strutture Direct3D</span><span class="sxs-lookup"><span data-stu-id="b34f7-160">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="b34f7-161">**GetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f7-161">**GetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[<span data-ttu-id="b34f7-162">**SetClipStatus**</span><span class="sxs-lookup"><span data-stu-id="b34f7-162">**SetClipStatus**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
