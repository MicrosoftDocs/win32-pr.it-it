---
description: Descrive lo stato corrente del clip.
ms.assetid: 3ea8631c-a967-4d24-a49a-1751b3ee6077
title: Struttura D3DCLIPSTATUS9 (D3D9Types.h)
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
ms.openlocfilehash: 1820e0646d735a8e1f3817832172d11e83218bbe8748e639084c47b3f77ea5df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123368"
---
# <a name="d3dclipstatus9-structure"></a>Struttura D3DCLIPSTATUS9

Descrive lo stato corrente del clip.

## <a name="syntax"></a>Sintassi


```C++
typedef struct D3DCLIPSTATUS9 {
  DWORD ClipUnion;
  DWORD ClipIntersection;
} D3DCLIPSTATUS9, *LPD3DCLIPSTATUS9;
```



## <a name="members"></a>Members

<dl> <dt>

**ClipUnion**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag di unione clip che descrivono lo stato corrente del clip. Questo membro può essere uno o più dei flag seguenti:



| Valore                                                                                                                                                      | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ ALL**</dt> </dl>          | Combinazione di tutti i flag di ritaglio.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS \_ A SINISTRA**</dt> </dl>       | Tutti i vertici vengono ritagliati dal piano sinistro del frustum di visualizzazione.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS \_ RIGHT**</dt> </dl>    | Tutti i vertici vengono ritagliati dal piano destro del frustum di visualizzazione.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ TOP**</dt> </dl>          | Tutti i vertici vengono ritagliati dal piano superiore del frustum di visualizzazione.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS \_ INFERIORE**</dt> </dl> | Tutti i vertici vengono ritagliati in base al piano inferiore del frustum di visualizzazione.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ FRONT**</dt> </dl>    | Tutti i vertici vengono ritagliati dal piano anteriore del frustum di visualizzazione.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ BACK**</dt> </dl>       | Tutti i vertici vengono ritagliati dal piano posteriore del frustum di visualizzazione.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**D3DCS \_ PLANE0**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**D3DCS \_ PLANE1**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**D3DCS \_ PLANE2**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**D3DCS \_ PLANE3**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**D3DCS \_ PLANE4**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**D3DCS \_ PLANE5**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Flag di intersezione di clip che descrivono lo stato corrente del clip. Questo membro può assumere gli stessi flag di ClipUnion.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il ritaglio è abilitato durante l'elaborazione dei vertici (da [**ProcessVertices,**](/windows/desktop/api) [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)o altre funzioni di disegno), Direct3D calcola un codice clip per ogni vertice. Il codice clip è una combinazione di \_ bit D3DCS. \* Quando un vertice si trova all'esterno di un particolare piano di ritaglio, il bit corrispondente viene impostato nel codice di ritaglio. Direct3D mantiene lo stato della clip **usando D3DCLIPSTATUS9,** che ha membri ClipUnion e ClipIntersection. ClipUnion è un OR bit per bit di tutti i codici di clip vertice e ClipIntersection è un AND bit per bit di tutti i codici di clip vertice. I valori iniziali sono zero per ClipUnion e 0xFFFFFFFF per ClipIntersection. Quando D3DRS \_ CLIPPING è impostato su **FALSE,** ClipUnion e ClipIntersection sono impostati su zero. Direct3D aggiorna lo stato della clip durante le chiamate di disegno. Per calcolare lo stato del clip per un determinato oggetto, impostare ClipUnion e ClipIntersection sul valore iniziale e continuare a disegnare.

Lo stato del clip non viene aggiornato [**da DrawRectPatch**](/windows/desktop/api) e [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) perché non è disponibile alcuna emulazione software.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
