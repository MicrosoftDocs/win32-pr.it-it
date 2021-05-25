---
description: Definisce costanti che descrivono i valori dello stato di trasformazione.
ms.assetid: 53535d9f-246a-42cf-82a2-fb3cf6d4ebac
title: Enumerazione D3DTRANSFORMSTATETYPE (D3D9Types.h)
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
ms.openlocfilehash: 022aa20fab0739b32aa75eb5f4bc575c0a8ad853
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342996"
---
# <a name="d3dtransformstatetype-enumeration"></a>Enumerazione D3DTRANSFORMSTATETYPE

Definisce costanti che descrivono i valori dello stato di trasformazione.

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

<span id="D3DTS_VIEW"></span><span id="d3dts_view"></span>**VISTA D3DTS \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata come matrice di trasformazione della visualizzazione. Il valore predefinito è **NULL** (matrice di identità).

</dd> <dt>

<span id="D3DTS_PROJECTION"></span><span id="d3dts_projection"></span>**PROIEZIONE D3DTS \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata come matrice di trasformazione della proiezione. Il valore predefinito è **NULL** (matrice di identità).

</dd> <dt>

<span id="D3DTS_TEXTURE0"></span><span id="d3dts_texture0"></span>**TRAMA D3DTS0 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE1"></span><span id="d3dts_texture1"></span>**TRAMA D3DTS1 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE2"></span><span id="d3dts_texture2"></span>**TRAMA D3DTS2 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE3"></span><span id="d3dts_texture3"></span>**TRAMA D3DTS3 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE4"></span><span id="d3dts_texture4"></span>**TRAMA D3DTS4 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE5"></span><span id="d3dts_texture5"></span>**TRAMA D3DTS5 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE6"></span><span id="d3dts_texture6"></span>**TRAMA D3DTS6 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_TEXTURE7"></span><span id="d3dts_texture7"></span>**TRAMA D3DTS7 \_**
</dt> <dd>

Identifica la matrice di trasformazione impostata per la fase di trama specificata.

</dd> <dt>

<span id="D3DTS_FORCE_DWORD"></span><span id="d3dts_force_dword"></span>**D3DTS \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbero la compilazione di questa enumerazione a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="remarks"></a>Commenti

Gli stati di trasformazione nell'intervallo da 256 a 511 sono riservati per archiviare fino a 256 matrici del mondo che possono essere indicizzate usando le macro D3DTS \_ WORLDMATRIX e D3DTS \_ WORLD.



| Macro                                                  | Descrizione                                                                                                                                                                      |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MONDO D3DTS \_**](d3dts-world.md)                     | Equivalente a D3DTS \_ WORLDMATRIX(0).                                                                                                                                  |
| [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) (indice) | Identifica la matrice di trasformazione da impostare per la matrice globale in corrispondenza dell'indice. Più matrici di mondo vengono usate solo per la fusione dei vertici. In caso contrario, viene usato solo D3DTS \_ WORLD. |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettransform)
</dt> <dt>

[**IDirect3DDevice9::MultiplyTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-multiplytransform)
</dt> <dt>

[**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)
</dt> <dt>

[**MONDO D3DTS \_**](d3dts-world.md)
</dt> <dt>

[**D3DTS \_ WORLDn**](d3dts-worldn.md)
</dt> <dt>

[**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)
</dt> </dl>

 

 
