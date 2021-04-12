---
description: Definisce i flag utilizzati per controllare il numero o le matrici applicate dal sistema quando si esegue la fusione dei vertici a più matrici.
ms.assetid: 5314f455-ce5f-4ff5-81fc-d3dffc8705b7
title: Enumerazione D3DVERTEXBLENDFLAGS (D3D9Types. h)
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
ms.openlocfilehash: 0b4d22740a9ad06a9848dc7649d62ac06d37a056
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354734"
---
# <a name="d3dvertexblendflags-enumeration"></a>Enumerazione D3DVERTEXBLENDFLAGS

Definisce i flag utilizzati per controllare il numero o le matrici applicate dal sistema quando si esegue la fusione dei vertici a più matrici.

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

<span id="D3DVBF_DISABLE"></span><span id="d3dvbf_disable"></span>**\_Disabilitazione D3DVBF**
</dt> <dd>

Disabilitare la fusione del vertice; applicare solo la matrice globale impostata dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per lo stato della trasformazione è 0.

</dd> <dt>

<span id="D3DVBF_1WEIGHTS"></span><span id="d3dvbf_1weights"></span>**\_1WEIGHTS D3DVBF**
</dt> <dd>

Abilitare la fusione dei vertici tra le due matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione è 0 e 1.

</dd> <dt>

<span id="D3DVBF_2WEIGHTS"></span><span id="d3dvbf_2weights"></span>**\_2WEIGHTS D3DVBF**
</dt> <dd>

Abilitare la fusione dei vertici tra le tre matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione è 0, 1 e 2.

</dd> <dt>

<span id="D3DVBF_3WEIGHTS"></span><span id="d3dvbf_3weights"></span>**\_3WEIGHTS D3DVBF**
</dt> <dd>

Abilitare la fusione dei vertici tra le quattro matrici impostate dalla macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) , in cui il valore di indice per gli Stati di trasformazione sono 0, 1, 2 e 3.

</dd> <dt>

<span id="D3DVBF_TWEENING"></span><span id="d3dvbf_tweening"></span>**\_Interpolazione D3DVBF**
</dt> <dd>

La fusione dei vertici viene eseguita usando il valore assegnato a D3DRS \_ TWEENFACTOR.

</dd> <dt>

<span id="D3DVBF_0WEIGHTS"></span><span id="d3dvbf_0weights"></span>**\_0WEIGHTS D3DVBF**
</dt> <dd>

Usare una singola matrice con un peso pari a 1,0.

</dd> </dl>

## <a name="remarks"></a>Commenti

I membri di questo tipo vengono utilizzati con lo \_ stato di rendering VERTEXBLEND di D3DRS.

La combinazione di geometria (combinazione di vertici multimatrice) richiede che l'applicazione usi un formato di vertice con pesi di fusione (beta) per ogni vertice.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> <dt>

[**\_Mondo D3DTS**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ mondo**](d3dts-worldn.md)
</dt> <dt>

[**\_WORLDMATRIX D3DTS**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
