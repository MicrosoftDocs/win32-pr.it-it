---
description: Definisce il tipo di luce.
ms.assetid: 90ad82d3-ffa8-42bb-9d9c-cf28a416c32d
title: Enumerazione D3DLIGHTTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DLIGHTTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 83c94db3126443f757f01a69d7d773417f70683a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322932"
---
# <a name="d3dlighttype-enumeration"></a>Enumerazione D3DLIGHTTYPE

Definisce il tipo di luce.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DLIGHTTYPE { 
  D3DLIGHT_POINT        = 1,
  D3DLIGHT_SPOT         = 2,
  D3DLIGHT_DIRECTIONAL  = 3,
  D3DLIGHT_FORCE_DWORD  = 0x7fffffff
} D3DLIGHTTYPE, *LPD3DLIGHTTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DLIGHT_POINT"></span><span id="d3dlight_point"></span>**Punto di D3DLIGHT \_**
</dt> <dd>

Light è un'origine punto. La luce ha una posizione nello spazio e irradia la luce in tutte le direzioni.

</dd> <dt>

<span id="D3DLIGHT_SPOT"></span><span id="d3dlight_spot"></span>**Punto di D3DLIGHT \_**
</dt> <dd>

Light è un'origine Spotlight. Questa luce è simile a un punto chiaro, ad eccezione del fatto che l'illuminazione è limitata a un cono. Questo tipo di luce ha una direzione e diversi altri parametri che determinano la forma del cono che produce. Per informazioni su questi parametri, vedere la struttura [**D3DLIGHT9**](d3dlight9.md) .

</dd> <dt>

<span id="D3DLIGHT_DIRECTIONAL"></span><span id="d3dlight_directional"></span>**\_Direzionale D3DLIGHT**
</dt> <dd>

Light è una fonte di luce direzionale. Equivale all'uso di una sorgente di luce puntiforme a una distanza infinita.

</dd> <dt>

<span id="D3DLIGHT_FORCE_DWORD"></span><span id="d3dlight_force_dword"></span>**D3DLIGHT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le luci direzionali sono leggermente più veloci delle fonti di luce del punto, ma le luci puntiformi hanno un aspetto leggermente migliore. I faretti offrono effetti visivi interessanti, ma sono molto dispendiosi in termini di tempo.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DLIGHT9**](d3dlight9.md)
</dt> </dl>

 

 




