---
description: Definisce la modalità di Blend supportata.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Enumerazione D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d8d779ad714e396f9c9a82bbbc42ddd09b76e2ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969320"
---
# <a name="d3dblend-enumeration"></a>Enumerazione D3DBLEND

Definisce la modalità di Blend supportata.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ zero**
</dt> <dd>

Il fattore di Blend è (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ One**
</dt> <dd>

Il fattore di Blend è (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**\_SRCCOLOR D3DBLEND**
</dt> <dd>

Il fattore di Blend è (RS, GS, BS, As).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**\_INVSRCCOLOR D3DBLEND**
</dt> <dd>

Il fattore di Blend è (1-RS, 1-GS, 1-BS, 1-As).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**\_SRCALPHA D3DBLEND**
</dt> <dd>

Il fattore di Blend è (come, come, come).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**\_INVSRCALPHA D3DBLEND**
</dt> <dd>

Il fattore di Blend è (1-As, 1-As, 1-As, 1-As).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**\_DESTALPHA D3DBLEND**
</dt> <dd>

Il fattore di Blend è<sub>(a d</sub> <sub>d a d</sub> <sub>a d</sub> <sub>).</sub>

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**\_INVDESTALPHA D3DBLEND**
</dt> <dd>

Il fattore di Blend è (1<sub>-a d 1-</sub> a<sub>d</sub> 1-A<sub>d</sub> 1-a<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**\_DESTCOLOR D3DBLEND**
</dt> <dd>

Il fattore di Blend è (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**\_INVDESTCOLOR D3DBLEND**
</dt> <dd>

Il fattore di Blend è (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**\_SRCALPHASAT D3DBLEND**
</dt> <dd>

Il fattore di Blend è (f, f, f, 1); dove f = min (As, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**\_BOTHSRCALPHA D3DBLEND**
</dt> <dd>

**Obsoleto**. A partire da DirectX 6, è possibile ottenere lo stesso risultato impostando i fattori di Blend di origine e di destinazione su D3DBLEND \_ SRCALPHA e D3DBLEND \_ INVSRCALPHA in chiamate separate.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**\_BOTHINVSRCALPHA D3DBLEND**
</dt> <dd>

**Obsoleto**. Il fattore di fusione di origine è (1-As, 1-As, 1-As, 1-As) e il fattore di Blend di destinazione è (come, come, As, As viene eseguito l'override della selezione di Blend di destinazione. Questa modalità di Blend è supportata solo per lo \_ stato di rendering SRCBLEND di D3DRS.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**\_BLENDFACTOR D3DBLEND**
</dt> <dd>

Fattore di fusione dei colori costante utilizzato dal Blender del buffer dei frame. Questa modalità di Blend è supportata solo se D3DPBLENDCAPS \_ BLENDFACTOR è impostato nei membri **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**\_INVBLENDFACTOR D3DBLEND**
</dt> <dd>

Fattore di fusione dei colori costante invertito usato dal Blender del buffer di frame. Questa modalità di Blend è supportata solo se il \_ bit BLENDFACTOR di D3DPBLENDCAPS è impostato nei membri **SrcBlendCaps** o **DestBlendCaps** di [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**\_SRCCOLOR2 D3DBLEND**
</dt> <dd>

Il fattore di Blend è (PSOutColor \[ 1 \] <sub>r</sub>, PSOutColor \[ 1 \] <sub>g</sub>, PSOutColor \[ 1 \] <sub>b</sub>, non usato). Vedere [fusione della destinazione di rendering](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**\_INVSRCCOLOR2 D3DBLEND**
</dt> <dd>

Il fattore di Blend è (1-PSOutColor \[ 1 \] <sub>r</sub>, 1-PSOutColor \[ 1 \] <sub>g</sub>, 1-PSOutColor \[ 1 \] <sub>b</sub>, non usato). Vedere [fusione della destinazione di rendering](#render-target-blending).



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| Differenze tra Direct3D 9 e Direct3D 9Ex:<br/> Questo flag è disponibile solo in Direct3D 9Ex.<br/> |



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Nelle descrizioni dei membri precedenti, i valori RGBA dell'origine e della destinazione sono indicati dagli indici s e d.

I valori in questo tipo enumerato vengono utilizzati dagli Stati di rendering seguenti:

-   \_DESTBLEND D3DRS
-   \_SRCBLEND D3DRS
-   \_DESTBLENDALPHA D3DRS
-   \_SRCBLENDALPHA D3DRS

Vedere [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Blend di destinazione di rendering

Direct3D 9Ex ha migliorato le funzionalità di rendering del testo. Il rendering di tipi di carattere Clear-Type richiede in genere due passaggi. Per eliminare il secondo passaggio, è possibile usare un pixel shader per restituire due colori, che è possibile chiamare PSOutColor \[ 0 \] e PSOutColor \[ 1 \] . Il primo colore conterrà i componenti standard 3 Color (RGB). Il secondo colore conterrebbe 3 componenti alfa (uno per ogni componente del primo colore).

Queste nuove modalità di fusione vengono usate solo per il rendering del testo nella prima destinazione di rendering.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
