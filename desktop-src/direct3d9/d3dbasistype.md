---
description: Definisce il tipo di base di una superficie della patch di ordine superiore.
ms.assetid: 18c31c77-7ba3-449c-af4a-717b8c1dced1
title: Enumerazione D3DBASISTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBASISTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 7e166f56aa2625c868d3e2e2223efbb577e05bf5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132306"
---
# <a name="d3dbasistype-enumeration"></a>Enumerazione D3DBASISTYPE

Definisce il tipo di base di una superficie della patch di ordine superiore.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DBASISTYPE { 
  D3DBASIS_BEZIER       = 0,
  D3DBASIS_BSPLINE      = 1,
  D3DBASIS_CATMULL_ROM  = 2,
  D3DBASIS_FORCE_DWORD  = 0x7fffffff
} D3DBASISTYPE, *LPD3DBASISTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DBASIS_BEZIER"></span><span id="d3dbasis_bezier"></span>**D3DBASIS \_ Bezier**
</dt> <dd>

I vertici di input vengono considerati come una serie di patch di Bézier. Il numero di vertici specificati deve essere divisibile per 4. Non verrà eseguito il rendering di parti della mesh oltre questo criterio. Si presuppone la continuità completa tra le sottopatch all'interno dell'area sottoposta a rendering da ogni chiamata. Solo i vertici negli angoli di ogni sottopatch si trovano nella superficie risultante.

</dd> <dt>

<span id="D3DBASIS_BSPLINE"></span><span id="d3dbasis_bspline"></span>**\_Perequazione BSpline D3DBASIS**
</dt> <dd>

I vertici di input vengono trattati come punti di controllo di una superficie B-spline. Il numero di aperture di cui è stato eseguito il rendering è due meno del numero di aperture in tale direzione. In generale, la superficie generata non contiene i vertici di controllo specificati.

</dd> <dt>

<span id="D3DBASIS_CATMULL_ROM"></span><span id="d3dbasis_catmull_rom"></span>**D3DBASIS \_ CATMULL \_ ROM**
</dt> <dd>

Una base di interpolazione definisce la superficie in modo che la superficie attraversi tutti i vertici di input specificati. In DirectX 8, era D3DBASIS \_ interpolazione.

</dd> <dt>

<span id="D3DBASIS_FORCE_DWORD"></span><span id="d3dbasis_force_dword"></span>**D3DBASIS \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di **D3DBASISTYPE** specificano la formulazione da utilizzare per la valutazione della primitiva della superficie della patch di ordine superiore durante la suddivisione a mosaico.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**\_Informazioni D3DRECTPATCH**](d3drectpatch-info.md)
</dt> <dt>

[**\_Informazioni D3DTRIPATCH**](d3dtripatch-info.md)
</dt> </dl>

 

 




