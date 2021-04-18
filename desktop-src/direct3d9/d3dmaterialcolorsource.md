---
description: Definisce la posizione in cui è necessario accedere a un componente color o color per i calcoli di illuminazione.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumerazione D3DMATERIALCOLORSOURCE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DMATERIALCOLORSOURCE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 8877eece8e33c6508768b22c989e992cf8178823
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322928"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>Enumerazione D3DMATERIALCOLORSOURCE

Definisce la posizione in cui è necessario accedere a un componente color o color per i calcoli di illuminazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DMATERIALCOLORSOURCE { 
  D3DMCS_MATERIAL     = 0,
  D3DMCS_COLOR1       = 1,
  D3DMCS_COLOR2       = 2,
  D3DMCS_FORCE_DWORD  = 0x7fffffff
} D3DMATERIALCOLORSOURCE, *LPD3DMATERIALCOLORSOURCE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**\_Materiale D3DMCS**
</dt> <dd>

Usare il colore dal materiale corrente.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**\_COLOR1 D3DMCS**
</dt> <dd>

Usare il colore del vertice diffuso.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**\_Color2 D3DMCS**
</dt> <dd>

Usare il colore del vertice speculare.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi flag vengono utilizzati per impostare il valore degli Stati di rendering seguenti nel tipo enumerato [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md) .

-   \_AMBIENTMATERIALSOURCE D3DRS
-   \_DIFFUSEMATERIALSOURCE D3DRS
-   \_EMISSIVEMATERIALSOURCE D3DRS
-   \_SPECULARMATERIALSOURCE D3DRS

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
