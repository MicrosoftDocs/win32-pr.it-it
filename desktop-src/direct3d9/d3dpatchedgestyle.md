---
description: Definisce se la modalità a tessellazione corrente è discreta o continua.
ms.assetid: d8055a25-6a8e-4018-a993-762f6f0e0cd3
title: Enumerazione D3DPATCHEDGESTYLE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPATCHEDGESTYLE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 717139a33e260aa29bc8d0e244fa49b3cb324c5249614f513faf0624ccf21841
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987241"
---
# <a name="d3dpatchedgestyle-enumeration"></a>Enumerazione D3DPATCHEDGESTYLE

Definisce se la modalità a tessellazione corrente è discreta o continua.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DPATCHEDGESTYLE { 
  D3DPATCHEDGE_DISCRETE     = 0,
  D3DPATCHEDGE_CONTINUOUS   = 1,
  D3DPATCHEDGE_FORCE_DWORD  = 0x7fffffff
} D3DPATCHEDGESTYLE, *LPD3DPATCHEDGESTYLE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DPATCHEDGE_DISCRETE"></span><span id="d3dpatchedge_discrete"></span>**D3DPATCHEDGE \_ DISCRETE**
</dt> <dd>

Stile del bordo discreto. In modalità discreta è possibile specificare la virgola mobile, ma verrà troncata a numeri interi.

</dd> <dt>

<span id="D3DPATCHEDGE_CONTINUOUS"></span><span id="d3dpatchedge_continuous"></span>**D3DPATCHEDGE \_ CONTINUOUS**
</dt> <dd>

Stile bordo continuo. In modalità continua, la tessellazione viene specificata come valori float che possono essere variati senza problemi per ridurre gli artefatti "popping".

</dd> <dt>

<span id="D3DPATCHEDGE_FORCE_DWORD"></span><span id="d3dpatchedge_force_dword"></span>**D3DPATCHEDGE \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Si noti che la tessellazione continua produce un modello a tessellazione completamente diverso da quello discreto per gli stessi valori a tessellazione (questo è più evidente in modalità wireframe). Pertanto, 4.0 continuous non è uguale a 4 discrete.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




