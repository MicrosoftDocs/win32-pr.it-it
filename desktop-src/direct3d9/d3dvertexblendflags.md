---
description: Definisce i flag usati per controllare il numero o le matrici applicate dal sistema durante l'esecuzione della fusione dei vertici multimatrix.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumerazione D3DVERTEXBLENDFLAGS (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBLENDFLAGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: ecc7f99e26088ff03b626604279bffe5c64ddb82b95a6f6219b637b3fce5a59b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118527305"
---
# <a name="d3dvertexblendflags-enumeration"></a>Enumerazione D3DVERTEXBLENDFLAGS

Definisce i flag usati per controllare il numero o le matrici applicate dal sistema durante l'esecuzione della fusione dei vertici multimatrix.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DVERTEXBLENDFLAGS { 
  D3DVBF_DISABLE   = 0,
  D3DVBF_1WEIGHTS  = 1,
  D3DVBF_2WEIGHTS  = 2,
  D3DVBF_3WEIGHTS  = 3,
  D3DVBF_TWEENING  = 255,
  D3DVBF_0WEIGHTS  = 256
} D3DVERTEXBLENDFLAGS, *LPD3DVERTEXBLENDFLAGS;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**DISABILITAZIONE D3DVBF \_**
</dt> <dd>

Disabilitare la fusione dei vertici; applica solo la matrice globale impostata dalla macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) dove il valore dell'indice per lo stato della trasformazione è 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**D3DVBF \_ 1WEIGHTS**
</dt> <dd>

Abilitare la fusione dei vertici tra le due matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) dove il valore di indice per gli stati di trasformazione è 0 e 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**D3DVBF \_ 2WEIGHTS**
</dt> <dd>

Abilitare la fusione dei vertici tra le tre matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) dove il valore di indice per gli stati di trasformazione è 0, 1 e 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**D3DVBF \_ 3WEIGHTS**
</dt> <dd>

Abilitare la fusione dei vertici tra le quattro matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX,**](d3dts-worldmatrix.md) dove il valore di indice per gli stati di trasformazione è 0, 1, 2 e 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**D3DVBF \_ TWEENING**
</dt> <dd>

La fusione dei vertici viene eseguita usando il valore assegnato a D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**D3DVBF \_ 0WEIGHTS**
</dt> <dd>

Usare una singola matrice con un peso di 1,0.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questo tipo vengono usati con lo stato di rendering \_ VERTEXBLEND D3DRS.

La fusione geometrica (fusione di vertici multimatrix) richiede che l'applicazione usi un formato vertice con pesi di fusione (beta) per ogni vertice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**MONDO D3DTS \_**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
