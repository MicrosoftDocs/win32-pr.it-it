---
description: Descrive i dati contenuti nell'enumerazione .
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: D3DXPARAMETER_TYPE enumerazione (D3dx9shader.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXPARAMETER_TYPE
api_type:
- HeaderDef
api_location:
- d3dx9shader.h
ms.openlocfilehash: 2d342e664aac81cf337cde2de7669c94a4ac6c94ce85c564a29da1f38dd93bd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096191"
---
# <a name="d3dxparameter_type-enumeration"></a>Enumerazione D3DXPARAMETER \_ TYPE

Descrive i dati contenuti nell'enumerazione .

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DXPARAMETER_TYPE { 
  D3DXPT_VOID,
  D3DXPT_BOOL,
  D3DXPT_INT,
  D3DXPT_FLOAT,
  D3DXPT_STRING,
  D3DXPT_TEXTURE,
  D3DXPT_TEXTURE1D,
  D3DXPT_TEXTURE2D,
  D3DXPT_TEXTURE3D,
  D3DXPT_TEXTURECUBE,
  D3DXPT_SAMPLER,
  D3DXPT_SAMPLER1D,
  D3DXPT_SAMPLER2D,
  D3DXPT_SAMPLER3D,
  D3DXPT_SAMPLERCUBE,
  D3DXPT_PIXELSHADER,
  D3DXPT_VERTEXSHADER,
  D3DXPT_PIXELFRAGMENT,
  D3DXPT_VERTEXFRAGMENT,
  D3DXPT_UNSUPPORTED,
  D3DXPT_FORCE_DWORD     = 0x7fffffff
} D3DXPARAMETER_TYPE, *LPD3DXPARAMETER_TYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ VOID**
</dt> <dd>

Il parametro è un puntatore void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**D3DXPT \_ BOOL**
</dt> <dd>

Il parametro è un valore booleano. Qualsiasi valore diverso da zero passato in [**ID3DXConstantTable::SetBool,**](id3dxconstanttable--setbool.md) [**ID3DXConstantTable::SetBoolArray,**](id3dxconstanttable--setboolarray.md) [**ID3DXConstantTable::SetValue,**](id3dxconstanttable--setvalue.md) [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) verrà mappato a 1 (TRUE) prima di essere scritto nella tabella delle costanti. In caso contrario, il valore verrà impostato su 0 nella tabella delle costanti.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**D3DXPT \_ INT**
</dt> <dd>

Il parametro è un numero intero. Tutti i valori a virgola mobile passati in [**ID3DXConstantTable::SetValue,**](id3dxconstanttable--setvalue.md) [**ID3DXConstantTable::SetVector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable::SetVectorArray**](id3dxconstanttable--setvectorarray.md) verranno arrotondati (a zero cifre decimali) prima di essere scritti nella tabella costante.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**D3DXPT \_ FLOAT**
</dt> <dd>

Il parametro è un numero a virgola mobile.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**STRINGA D3DXPT \_**
</dt> <dd>

Il parametro è una stringa.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**TRAMA D3DXPT \_**
</dt> <dd>

Il parametro è una trama.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**D3DXPT \_ TEXTURE1D**
</dt> <dd>

Il parametro è una trama 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**D3DXPT \_ TEXTURE2D**
</dt> <dd>

Il parametro è una trama 2D.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**TRAMA D3DXPT3D \_**
</dt> <dd>

Il parametro è una trama 3D.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**D3DXPT \_ TEXTURECUBE**
</dt> <dd>

Il parametro è una trama del cubo.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**D3DXPT \_ SAMPLER**
</dt> <dd>

Il parametro è un campionatore.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**D3DXPT \_ SAMPLER1D**
</dt> <dd>

Il parametro è un campionatore 1D.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**D3DXPT \_ SAMPLER2D**
</dt> <dd>

Il parametro è un campionatore 2D.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**D3DXPT \_ SAMPLER3D**
</dt> <dd>

Il parametro è un campionatore 3D.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**D3DXPT \_ SAMPLERCUBE**
</dt> <dd>

Il parametro è un campionatore di cubi.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**D3DXPT \_ PIXELSHADER**
</dt> <dd>

Il parametro è un pixel shader.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**D3DXPT \_ VERTEXSHADER**
</dt> <dd>

Il parametro è un vertex shader.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**D3DXPT \_ PIXELFRAGMENT**
</dt> <dd>

Il parametro è un pixel shader frammento.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**D3DXPT \_ VERTEXFRAGMENT**
</dt> <dd>

Il parametro è un frammento di vertex shader.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT \_ NON SUPPORTATO**
</dt> <dd>

Il parametro non è supportato.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ FORCE \_ DWORD**
</dt> <dd>

Forza la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori consentirebbe a questa enumerazione di compilare a una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**D3DXSHADER \_ TYPEINFO**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




