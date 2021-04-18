---
description: Definisce le costanti che descrivono i valori dello stato della trasformazione.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumerazione D3DTRANSFORMSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTRANSFORMSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: c618e0e19bf7dd01dec73d35436f23189f9e78a6
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322451"
---
# <a name="d3dtransformstatetype-enumeration"></a>Enumerazione D3DTRANSFORMSTATETYPE

Definisce le costanti che descrivono i valori dello stato della trasformazione.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DTRANSFORMSTATETYPE { 
  D3DTS_VIEW         = 2,
  D3DTS_PROJECTION   = 3,
  D3DTS_TEXTURE0     = 16,
  D3DTS_TEXTURE1     = 17,
  D3DTS_TEXTURE2     = 18,
  D3DTS_TEXTURE3     = 19,
  D3DTS_TEXTURE4     = 20,
  D3DTS_TEXTURE5     = 21,
  D3DTS_TEXTURE6     = 22,
  D3DTS_TEXTURE7     = 23,
  D3DTS_FORCE_DWORD  = 0x7fffffff
} D3DTRANSFORMSTATETYPE, *LPD3DTRANSFORMSTATETYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**\_Visualizzazione D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare come matrice di trasformazione della visualizzazione. Il valore predefinito è **null** (matrice di identità).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**\_Proiezione D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare come matrice di trasformazione della proiezione. Il valore predefinito è **null** (matrice di identità).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**\_TEXTURE0 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**\_TEXTURE1 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**\_TRAMA2 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**\_TEXTURE3 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**\_TEXTURE4 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**\_TEXTURE5 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**\_TEXTURE6 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**\_TEXTURE7 D3DTS**
</dt> <dd>

Identifica la matrice di trasformazione da impostare per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli Stati di trasformazione nell'intervallo compreso tra 256 e 511 sono riservati per archiviare fino a 256 matrici globali che possono essere indicizzate usando le \_ macro D3DTS WORLDMATRIX e D3DTS \_ World.



| Macro                                                  |                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Mondo D3DTS**](d3dts-world.md)                     | Equivale a D3DTS \_ WORLDMATRIX (0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (indice) | Identifica la matrice di trasformazione da impostare per la matrice globale in corrispondenza dell'indice. Più matrici internazionali vengono usate solo per la fusione dei vertici. In caso contrario \_ , viene usato solo D3DTS World. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9:: MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9:: setransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**\_Mondo D3DTS**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ mondo**](d3dts-worldn.md)
</dt> <dt>

[**\_WORLDMATRIX D3DTS**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
