---
description: Definisce la posizione in cui è necessario accedere a un componente colore o colore per i calcoli di illuminazione.
ms.assetid: 76061d47-a31c-4008-aa8d-a0464dd3423f
title: Enumerazione D3DMATERIALCOLORSOURCE (D3D9Types.h)
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
ms.openlocfilehash: 3c8069fdde062fdc6dea311b40b8614d2165356ff397f0d056c43569f391e02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118988891"
---
# <a name="d3dmaterialcolorsource-enumeration"></a>Enumerazione D3DMATERIALCOLORSOURCE

Definisce la posizione in cui è necessario accedere a un componente colore o colore per i calcoli di illuminazione.

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

<span id="D3DMCS_MATERIAL"></span><span id="d3dmcs_material"></span>**MATERIALE D3DMCS \_**
</dt> <dd>

Usare il colore del materiale corrente.

</dd> <dt>

<span id="D3DMCS_COLOR1"></span><span id="d3dmcs_color1"></span>**COLORE 1 DI D3DMCS \_**
</dt> <dd>

Usare il colore del vertice diffuso.

</dd> <dt>

<span id="D3DMCS_COLOR2"></span><span id="d3dmcs_color2"></span>**D3DMCS \_ COLOR2**
</dt> <dd>

Usare il colore del vertice speculare.

</dd> <dt>

<span id="D3DMCS_FORCE_DWORD"></span><span id="d3dmcs_force_dword"></span>**D3DMCS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questi flag vengono usati per impostare il valore degli stati di rendering seguenti nel [**tipo enumerato D3DRENDERSTATETYPE.**](./d3drenderstatetype.md)

-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ EMISSIVEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
