---
description: Descrive i dati contenuti nell'enumerazione.
ms.assetid: 6d494fe6-fcd5-4e71-939c-257978b41499
title: Enumerazione D3DXPARAMETER_TYPE (D3dx9shader. h)
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
ms.openlocfilehash: 16ff89feb694bb6aae550422b6f9546c2268fc07
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354154"
---
# <a name="d3dxparameter_type-enumeration"></a>\_Enumerazione del tipo D3DXPARAMETER

Descrive i dati contenuti nell'enumerazione.

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

<span id="D3DXPT_VOID"></span><span id="d3dxpt_void"></span>**D3DXPT \_ void**
</dt> <dd>

Il parametro è un puntatore void.

</dd> <dt>

<span id="D3DXPT_BOOL"></span><span id="d3dxpt_bool"></span>**\_Bool D3DXPT**
</dt> <dd>

Il parametro è un valore booleano. Qualsiasi valore diverso da zero passato in [**ID3DXConstantTable::**](id3dxconstanttable--setbool.md)SetValue, [**ID3DXConstantTable:: SetBoolArray**](id3dxconstanttable--setboolarray.md), [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: sevector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) verrà mappato a 1 (true) prima di essere scritto nella tabella delle costanti; in caso contrario, il valore verrà impostato su 0 nella tabella Constant.

</dd> <dt>

<span id="D3DXPT_INT"></span><span id="d3dxpt_int"></span>**\_Int D3DXPT**
</dt> <dd>

Il parametro è un numero intero. Tutti i valori a virgola mobile passati in [**ID3DXConstantTable:: SetValue**](id3dxconstanttable--setvalue.md), [**ID3DXConstantTable:: sevector**](id3dxconstanttable--setvector.md)o [**ID3DXConstantTable:: SetVectorArray**](id3dxconstanttable--setvectorarray.md) verranno arrotondati (a zero posizioni decimali) prima di essere scritti nella tabella delle costanti.

</dd> <dt>

<span id="D3DXPT_FLOAT"></span><span id="d3dxpt_float"></span>**\_Float D3DXPT**
</dt> <dd>

Il parametro è un numero a virgola mobile.

</dd> <dt>

<span id="D3DXPT_STRING"></span><span id="d3dxpt_string"></span>**\_Stringa D3DXPT**
</dt> <dd>

Il parametro è una stringa.

</dd> <dt>

<span id="D3DXPT_TEXTURE"></span><span id="d3dxpt_texture"></span>**\_Trama D3DXPT**
</dt> <dd>

Il parametro è una trama.

</dd> <dt>

<span id="D3DXPT_TEXTURE1D"></span><span id="d3dxpt_texture1d"></span>**\_TEXTURE1D D3DXPT**
</dt> <dd>

Il parametro è una trama 1D.

</dd> <dt>

<span id="D3DXPT_TEXTURE2D"></span><span id="d3dxpt_texture2d"></span>**\_TEXTURE2D D3DXPT**
</dt> <dd>

Il parametro è una trama 2D.

</dd> <dt>

<span id="D3DXPT_TEXTURE3D"></span><span id="d3dxpt_texture3d"></span>**\_TEXTURE3D D3DXPT**
</dt> <dd>

Il parametro è una trama 3D.

</dd> <dt>

<span id="D3DXPT_TEXTURECUBE"></span><span id="d3dxpt_texturecube"></span>**\_TEXTURECUBE D3DXPT**
</dt> <dd>

Il parametro è una trama del cubo.

</dd> <dt>

<span id="D3DXPT_SAMPLER"></span><span id="d3dxpt_sampler"></span>**\_Campionatore D3DXPT**
</dt> <dd>

Il parametro è un campionatore.

</dd> <dt>

<span id="D3DXPT_SAMPLER1D"></span><span id="d3dxpt_sampler1d"></span>**\_SAMPLER1D D3DXPT**
</dt> <dd>

Il parametro è un campionatore 1D.

</dd> <dt>

<span id="D3DXPT_SAMPLER2D"></span><span id="d3dxpt_sampler2d"></span>**\_SAMPLER2D D3DXPT**
</dt> <dd>

Il parametro è un campionatore 2D.

</dd> <dt>

<span id="D3DXPT_SAMPLER3D"></span><span id="d3dxpt_sampler3d"></span>**\_SAMPLER3D D3DXPT**
</dt> <dd>

Il parametro è un campionatore 3D.

</dd> <dt>

<span id="D3DXPT_SAMPLERCUBE"></span><span id="d3dxpt_samplercube"></span>**\_SAMPLERCUBE D3DXPT**
</dt> <dd>

Il parametro è un sampler del cubo.

</dd> <dt>

<span id="D3DXPT_PIXELSHADER"></span><span id="d3dxpt_pixelshader"></span>**\_PIXELSHADER D3DXPT**
</dt> <dd>

Il parametro è un pixel shader.

</dd> <dt>

<span id="D3DXPT_VERTEXSHADER"></span><span id="d3dxpt_vertexshader"></span>**\_VERTEXSHADER D3DXPT**
</dt> <dd>

Il parametro è un vertex shader.

</dd> <dt>

<span id="D3DXPT_PIXELFRAGMENT"></span><span id="d3dxpt_pixelfragment"></span>**\_PIXELFRAGMENT D3DXPT**
</dt> <dd>

Il parametro è un frammento pixel shader.

</dd> <dt>

<span id="D3DXPT_VERTEXFRAGMENT"></span><span id="d3dxpt_vertexfragment"></span>**\_VERTEXFRAGMENT D3DXPT**
</dt> <dd>

Il parametro è un frammento del vertex shader.

</dd> <dt>

<span id="D3DXPT_UNSUPPORTED"></span><span id="d3dxpt_unsupported"></span>**D3DXPT non \_ supportato**
</dt> <dd>

Il parametro non è supportato.

</dd> <dt>

<span id="D3DXPT_FORCE_DWORD"></span><span id="d3dxpt_force_dword"></span>**D3DXPT \_ Force \_ DWORD**
</dt> <dd>

Impone la compilazione di questa enumerazione a 32 bit. Senza questo valore, alcuni compilatori permetterebbero che questa enumerazione venga compilata in una dimensione diversa da 32 bit. Questo valore non viene utilizzato.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|------------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3dx9shader. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> <dt>

[**\_TYPEINFO D3DXSHADER**](d3dxshader-typeinfo.md)
</dt> <dt>

[**D3DXCONSTANT \_ DESC**](d3dxconstant-desc.md)
</dt> </dl>

 

 




