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
# <a name="d3dclipstatus9-structure"></a>Struttura D3DCLIPSTATUS9

Descrive lo stato corrente della clip.

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

Ritagliare i flag Unione che descrivono lo stato corrente della clip. Il membro può essere costituito da uno o più dei flag seguenti:



| Valore                                                                                                                                                      | Significato                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="D3DCS_ALL"></span><span id="d3dcs_all"></span><dl> <dt>**D3DCS \_ tutto**</dt> </dl>          | Combinazione di tutti i flag di ritaglio.<br/>                                       |
| <span id="D3DCS_LEFT"></span><span id="d3dcs_left"></span><dl> <dt>**D3DCS a \_ sinistra**</dt> </dl>       | Tutti i vertici vengono ritagliati dal piano sinistro del tronco di visualizzazione.<br/>   |
| <span id="D3DCS_RIGHT"></span><span id="d3dcs_right"></span><dl> <dt>**D3DCS a \_ destra**</dt> </dl>    | Tutti i vertici vengono ritagliati dal piano destro del tronco di visualizzazione.<br/>  |
| <span id="D3DCS_TOP"></span><span id="d3dcs_top"></span><dl> <dt>**D3DCS \_ Top**</dt> </dl>          | Tutti i vertici vengono ritagliati dal piano superiore del tronco di visualizzazione.<br/>    |
| <span id="D3DCS_BOTTOM"></span><span id="d3dcs_bottom"></span><dl> <dt>**D3DCS in \_ basso**</dt> </dl> | Tutti i vertici vengono ritagliati dal piano inferiore del tronco di visualizzazione.<br/> |
| <span id="D3DCS_FRONT"></span><span id="d3dcs_front"></span><dl> <dt>**D3DCS \_ front**</dt> </dl>    | Tutti i vertici vengono ritagliati dal piano anteriore del tronco di visualizzazione.<br/>  |
| <span id="D3DCS_BACK"></span><span id="d3dcs_back"></span><dl> <dt>**D3DCS \_ indietro**</dt> </dl>       | Tutti i vertici vengono ritagliati dal piano posteriore del tronco di visualizzazione.<br/>   |
| <span id="D3DCS_PLANE0"></span><span id="d3dcs_plane0"></span><dl> <dt>**\_PLANE0 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE1"></span><span id="d3dcs_plane1"></span><dl> <dt>**\_PLANE1 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE2"></span><span id="d3dcs_plane2"></span><dl> <dt>**\_PLANE2 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE3"></span><span id="d3dcs_plane3"></span><dl> <dt>**\_PLANE3 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE4"></span><span id="d3dcs_plane4"></span><dl> <dt>**\_PLANE4 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |
| <span id="D3DCS_PLANE5"></span><span id="d3dcs_plane5"></span><dl> <dt>**\_PLANE5 D3DCS**</dt> </dl> | Piani di ritaglio definiti dall'applicazione.<br/>                                 |



 

</dd> <dt>

**ClipIntersection**
</dt> <dd>

Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Ritagliare i flag di intersezione che descrivono lo stato corrente della clip. Questo membro può assumere gli stessi flag di ClipUnion.

</dd> </dl>

## <a name="remarks"></a>Commenti

Quando il ritaglio viene abilitato durante l'elaborazione del vertice (da [**ProcessVertices**](/windows/desktop/api), [**DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)o altre funzioni di disegno), Direct3D calcola un codice di ritaglio per ogni vertice. Il codice di ritaglio è una combinazione di D3DCS \_ \* bit. Quando un vertice è esterno a un particolare piano di ritaglio, il bit corrispondente viene impostato nel codice di ritaglio. Direct3D mantiene lo stato della clip utilizzando **D3DCLIPSTATUS9**, che include membri ClipUnion e ClipIntersection. ClipUnion è un operatore OR bit per bit di tutti i codici di clip dei vertici e ClipIntersection è un AND bit per bit di tutti i codici di ritaglio I valori iniziali sono pari a zero per ClipUnion e 0xFFFFFFFF per ClipIntersection. Quando il \_ ritaglio D3DRS è impostato su **false**, ClipUnion e ClipIntersection sono impostati su zero. Direct3D aggiorna lo stato della clip durante le chiamate di disegno. Per calcolare lo stato della clip per un determinato oggetto, impostare ClipUnion e ClipIntersection sul valore iniziale e continuare a disegnare.

Lo stato della clip non viene aggiornato da [**DrawRectPatch**](/windows/desktop/api) e [**DrawTriPatch**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawtripatch) perché non sono disponibili emulazioni software.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture Direct3D](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**GetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getclipstatus)
</dt> <dt>

[**SetClipStatus**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setclipstatus)
</dt> </dl>

 

 
