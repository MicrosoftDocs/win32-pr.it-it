---
description: Definisce un tipo di dati di dichiarazione dei vertici.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Enumerazione D3DDECLTYPE (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDECLTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 23b22a70077eb6f37a5baeb3193b23ee853be4c3123c781293f2e300d597aaaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119728631"
---
# <a name="d3ddecltype-enumeration"></a>Enumerazione D3DDECLTYPE

Definisce un tipo di dati di dichiarazione dei vertici.

## <a name="syntax"></a>Sintassi


```C++
typedef enum D3DDECLTYPE { 
  D3DDECLTYPE_FLOAT1     = 0,
  D3DDECLTYPE_FLOAT2     = 1,
  D3DDECLTYPE_FLOAT3     = 2,
  D3DDECLTYPE_FLOAT4     = 3,
  D3DDECLTYPE_D3DCOLOR   = 4,
  D3DDECLTYPE_UBYTE4     = 5,
  D3DDECLTYPE_SHORT2     = 6,
  D3DDECLTYPE_SHORT4     = 7,
  D3DDECLTYPE_UBYTE4N    = 8,
  D3DDECLTYPE_SHORT2N    = 9,
  D3DDECLTYPE_SHORT4N    = 10,
  D3DDECLTYPE_USHORT2N   = 11,
  D3DDECLTYPE_USHORT4N   = 12,
  D3DDECLTYPE_UDEC3      = 13,
  D3DDECLTYPE_DEC3N      = 14,
  D3DDECLTYPE_FLOAT16_2  = 15,
  D3DDECLTYPE_FLOAT16_4  = 16,
  D3DDECLTYPE_UNUSED     = 17
} D3DDECLTYPE, *LPD3DDECLTYPE;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**D3DDECLTYPE \_ FLOAT1**
</dt> <dd>

Float a un componente espanso a (float, 0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**D3DDECLTYPE \_ FLOAT2**
</dt> <dd>

Float a due componenti espanso in (float, float, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**D3DDECLTYPE \_ FLOAT3**
</dt> <dd>

Float a tre componenti espanso in (float, float, float, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**D3DDECLTYPE \_ FLOAT4**
</dt> <dd>

Float a quattro componenti espanso in (float, float, float, float).

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**D3DDECLTYPE \_ D3DCOLOR**
</dt> <dd>

Quattro componenti, byte compressi e senza segno mappati a un intervallo da 0 a 1. L'input è [**D3DCOLOR**](d3dcolor.md) e viene espanso nell'ordine RGBA.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**D3DDECLTYPE \_ UBYTE4**
</dt> <dd>

Byte senza segno a quattro componenti.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**D3DDECLTYPE \_ SHORT2**
</dt> <dd>

Two-component, signed short expanded to (value, value, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**D3DDECLTYPE \_ SHORT4**
</dt> <dd>

Quattro componenti, con segno short espanso in (valore, valore, valore, valore).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**D3DDECLTYPE \_ UBYTE4N**
</dt> <dd>

Byte a quattro componenti con ogni byte normalizzato dividendo con 255,0f.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**D3DDECLTYPE \_ SHORT2N**
</dt> <dd>

Normalizzato, a due componenti, con segno breve, espanso in (primo short/32767.0, secondo short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**D3DDECLTYPE \_ SHORT4N**
</dt> <dd>

Normalizzato, a quattro componenti, con segno short, espanso a (primo short/32767.0, secondo short/32767.0, terzo short/32767.0, quarto short/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**D3DDECLTYPE \_ USHORT2N**
</dt> <dd>

Normalizzato, a due componenti, unsigned short, espanso in (first short/65535.0, short short/65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**D3DDECLTYPE \_ USHORT4N**
</dt> <dd>

Normalizzato, a quattro componenti, unsigned short, espanso in (first short/65535.0, second short/65535.0, third short/65535.0, fourth short/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**D3DDECLTYPE \_ UDEC3**
</dt> <dd>

Formato a tre componenti, senza segno, 10 10 10 espanso in (valore, valore, valore, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**D3DDECLTYPE \_ DEC3N**
</dt> <dd>

Formato a tre componenti, con segno, 10 10 10 normalizzato ed espanso a (v \[ 0 \] /511.0, v \[ 1 \] /511.0, v \[ 2 \] /511.0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

A due componenti, a 16 bit, a virgola mobile espansa in (valore, valore, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

A quattro componenti, a 16 bit, a virgola mobile espansa in (valore, valore, valore, valore).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE \_ NON USATO**
</dt> <dd>

Il campo Type nella dichiarazione non viene usato. È progettato per l'uso con D3DDECLMETHOD \_ UV e D3DDECLMETHOD \_ LOOKUPPRESAMPLED.

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono dichiarati con una matrice [**di strutture D3DVERTEXELEMENT9.**](d3dvertexelement9.md) Ogni elemento nella matrice contiene un tipo di dati di dichiarazione dei vertici.

Usare lo strumento DirectX Caps Viewer (DXCapsViewer.exe) per visualizzare i tipi supportati nel dispositivo. È possibile ottenere questo strumento e ottenere informazioni da DirectX SDK. Per informazioni su DirectX SDK, vedere [Dove si trova DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
