---
description: Definisce un tipo di dati di dichiarazione vertici.
ms.assetid: 993fc7e4-4752-4bce-82d0-0a034fdc69c0
title: Enumerazione D3DDECLTYPE (D3D9Types. h)
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
ms.openlocfilehash: 3edb3f936772a7265c627f10eeb7aeb4f461701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354379"
---
# <a name="d3ddecltype-enumeration"></a>Enumerazione D3DDECLTYPE

Definisce un tipo di dati di dichiarazione vertici.

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

<span id="D3DDECLTYPE_FLOAT1"></span><span id="d3ddecltype_float1"></span>**\_FLOAT1 D3DDECLTYPE**
</dt> <dd>

Float a un componente espanso fino a (float, 0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT2"></span><span id="d3ddecltype_float2"></span>**\_FLOAT2 D3DDECLTYPE**
</dt> <dd>

Float a due componenti espanso a (float, float, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT3"></span><span id="d3ddecltype_float3"></span>**\_FLOAT3 D3DDECLTYPE**
</dt> <dd>

Float a tre componenti espanso a (float, float, float, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT4"></span><span id="d3ddecltype_float4"></span>**\_Float4 D3DDECLTYPE**
</dt> <dd>

Float a quattro componenti espanso a (float, float, float, float).

</dd> <dt>

<span id="D3DDECLTYPE_D3DCOLOR"></span><span id="d3ddecltype_d3dcolor"></span>**\_D3DCOLOR D3DDECLTYPE**
</dt> <dd>

Byte con quattro componenti, compressi e senza segno mappati a un intervallo compreso tra 0 e 1. Input è un [**D3DCOLOR**](d3dcolor.md) ed è espanso nell'ordine RGBA.

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4"></span><span id="d3ddecltype_ubyte4"></span>**\_UBYTE4 D3DDECLTYPE**
</dt> <dd>

Byte senza segno a quattro componenti.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2"></span><span id="d3ddecltype_short2"></span>**\_SHORT2 D3DDECLTYPE**
</dt> <dd>

A due componenti, con segno Short espanso a (valore, valore, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4"></span><span id="d3ddecltype_short4"></span>**\_SHORT4 D3DDECLTYPE**
</dt> <dd>

A quattro componenti, con segno Short espanso a (valore, valore, valore, valore).

</dd> <dt>

<span id="D3DDECLTYPE_UBYTE4N"></span><span id="d3ddecltype_ubyte4n"></span>**\_Dati UBYTE4N D3DDECLTYPE**
</dt> <dd>

Byte a quattro componenti con ogni byte normalizzato dividendo con 255.0 f.

</dd> <dt>

<span id="D3DDECLTYPE_SHORT2N"></span><span id="d3ddecltype_short2n"></span>**\_SHORT2N D3DDECLTYPE**
</dt> <dd>

Normalizzato, a due componenti, con segno Short, espanso in (First short/32767.0, Second short/32767.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_SHORT4N"></span><span id="d3ddecltype_short4n"></span>**\_SHORT4N D3DDECLTYPE**
</dt> <dd>

Normalizzato, a quattro componenti, con segno Short, espanso a (First short/32767.0, Second short/32767.0, terzo short/32767.0, Fourth short/32767.0).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT2N"></span><span id="d3ddecltype_ushort2n"></span>**\_USHORT2N D3DDECLTYPE**
</dt> <dd>

Normalizzato, a due componenti, a breve senza segno, espanso a (First Short/65535.0, Short Short/65535.0, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_USHORT4N"></span><span id="d3ddecltype_ushort4n"></span>**\_USHORT4N D3DDECLTYPE**
</dt> <dd>

Normalizzato, a quattro componenti, senza segno breve, espanso in (First Short/65535.0, Second Short/65535.0, terzo Short/65535.0, Fourth Short/65535.0).

</dd> <dt>

<span id="D3DDECLTYPE_UDEC3"></span><span id="d3ddecltype_udec3"></span>**\_UDEC3 D3DDECLTYPE**
</dt> <dd>

Formato a tre componenti, senza segno, 10 10 10 espanso a (valore, valore, valore, 1).

</dd> <dt>

<span id="D3DDECLTYPE_DEC3N"></span><span id="d3ddecltype_dec3n"></span>**\_DEC3N D3DDECLTYPE**
</dt> <dd>

Formato a tre componenti, firmato, 10 10 10 normalizzato ed espanso a (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_2"></span><span id="d3ddecltype_float16_2"></span>**D3DDECLTYPE \_ FLOAT16 \_ 2**
</dt> <dd>

A due componenti, a 16 bit, a virgola mobile espansa (valore, valore, 0, 1).

</dd> <dt>

<span id="D3DDECLTYPE_FLOAT16_4"></span><span id="d3ddecltype_float16_4"></span>**D3DDECLTYPE \_ FLOAT16 \_ 4**
</dt> <dd>

A quattro componenti, a 16 bit, a virgola mobile espansa (valore, valore, valore, valore).

</dd> <dt>

<span id="D3DDECLTYPE_UNUSED"></span><span id="d3ddecltype_unused"></span>**D3DDECLTYPE non \_ usato**
</dt> <dd>

Il campo tipo nella dichiarazione non è usato. Questa soluzione è progettata per l'uso con D3DDECLMETHOD \_ UV e D3DDECLMETHOD \_ LOOKUPPRESAMPLED.

</dd> </dl>

## <a name="remarks"></a>Commenti

I dati dei vertici vengono dichiarati con una matrice di strutture [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) . Ogni elemento nella matrice contiene un tipo di dati di dichiarazione vertici.

Usare lo strumento DirectX Caps Viewer (DXCapsViewer.exe) per vedere quali tipi sono supportati nel dispositivo. È possibile ottenere questo strumento e ottenere informazioni su di esso da DirectX SDK. Per informazioni su DirectX SDK, vedere [dove è DirectX SDK?](../directx-sdk--august-2009-.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------|----------------------------------------------------------------------------------------|
| Intestazione<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Enumerazioni Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DDECLMETHOD**](./d3ddeclmethod.md)
</dt> </dl>

 

 
