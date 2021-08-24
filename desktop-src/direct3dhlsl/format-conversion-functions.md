---
title: Funzioni di conversione del formato (informazioni di riferimento su HLSL)
description: La sezione contiene le funzioni di conversione del formato usate in Compute e Pixel Shaders.
ms.assetid: 05575ee8-4428-437f-bfb6-e5c676405d65
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f1158a45ce2fc5df0bdc762a5d422492522886b8025c940e807c80707be173e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672921"
---
# <a name="format-conversion-functions-hlsl-reference"></a>Funzioni di conversione del formato (informazioni di riferimento su HLSL)

La sezione contiene le funzioni di conversione del formato usate in Compute e Pixel Shaders.

-   [Funzioni del convertitore](#converter-functions)
-   [Argomenti correlati](#related-topics)

> L'intestazione D3DX_DXGIFormatConvert.inl viene fornita in DirectX SDK legacy e si basa sul supporto di XNAMath per C++. È incluso anche nel pacchetto di NuGet [Microsoft.DXSDK.D3DX.](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) La versione più recente usa DirectXMath per il supporto C++ e tutte le funzioni sono definite nello spazio **dei nomi DirectX** C++.

## <a name="converter-functions"></a>Funzioni del convertitore

### <a name="dxgi_format_r10g10b10a2_unorm"></a>FORMATO DXGI \_ \_ R10G10B10A2 \_ UNORM

<dl>

[**Da D3DX \_ R10G10B10A2 UNORM a \_ \_ \_ FLOAT4**](d3dx-r10g10b10a2-unorm-to-float4.md)  
[**DA D3DX \_ FLOAT4 \_ a \_ R10G10B10A2 \_ UNORM**](d3dx-float4-to-r10g10b10a2-unorm.md)  
</dl>

### <a name="dxgi_format_r10g10b10a2_uint"></a>FORMATO DXGI \_ \_ R10G10B10A2 \_ UINT

<dl>

[**DA D3DX \_ R10G10B10A2 \_ UINT \_ a \_ UINT4**](d3dx-r10g10b10a2-uint-to-uint4.md)  
[**DA D3DX \_ UINT4 a \_ \_ R10G10B10A2 \_ UINT**](d3dx-uint4-to-r10g10b10a2-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm"></a>DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM:

<dl>

[**Da D3DX \_ R8G8B8A8 \_ UNORM \_ a \_ FLOAT4**](d3dx-r8g8b8a8-unorm-to-float4.md)  
[**DA D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM**](d3dx-float4-to-r8g8b8a8-unorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_unorm_srgb"></a>FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB

<dl>

[**Da D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB a \_ \_ FLOAT4 \_ inesatta**](d3dx-r8g8b8a8-unorm-srgb-to-float4-inexact.md)  
[**Da D3DX \_ R8G8B8A8 \_ UNORM \_ SRGB \_ a \_ FLOAT4**](d3dx-r8g8b8a8-unorm-srgb-to-float4.md)  
[**Da D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ SRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_uint"></a>FORMATO DXGI \_ \_ R8G8B8A8 \_ UINT

<dl>

[**Da D3DX \_ R8G8B8A8 \_ UINT \_ a \_ UINT4**](d3dx-r8g8b8a8-uint-to-uint4.md)  
[**DA D3DX \_ UINT4 \_ a \_ R8G8B8A8 \_ UINT**](d3dx-uint4-to-r8g8b8a8-uint.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_snorm"></a>DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM

<dl>

[**Da D3DX \_ R8G8B8A8 \_ SNORM \_ a \_ FLOAT4**](d3dx-r8g8b8a8-snorm-to-float4.md)  
[**Da D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ SNORM**](d3dx-float4-to-r8g8b8a8-snorm.md)  
</dl>

### <a name="dxgi_format_r8g8b8a8_sint"></a>FORMATO DXGI \_ \_ R8G8B8A8 \_ SINT

<dl>

[**DA D3DX \_ R8G8B8A8 \_ SINT \_ a \_ INT4**](d3dx-r8g8b8a8-sint-to-int4.md)  
[**DA D3DX \_ INT4 \_ a \_ R8G8B8A8 \_ SINT**](d3dx-int4-to-r8g8b8a8-sint.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm"></a>FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM

<dl>

[**Da D3DX \_ B8G8R8A8 \_ UNORM \_ a \_ FLOAT4**](d3dx-b8g8r8a8-unorm-to-float4.md)  
[**DA D3DX \_ FLOAT4 \_ a \_ B8G8R8A8 \_ UNORM**](d3dx-float4-to-b8g8r8a8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8a8_unorm_srgb"></a>FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM \_ SRGB

<dl>

[**Da D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB a \_ \_ FLOAT4 \_ inesatta**](d3dx-b8g8r8a8-unorm-srgb-to-float4-inexact.md)  
[**Da D3DX \_ B8G8R8A8 \_ UNORM \_ SRGB \_ a \_ FLOAT4**](d3dx-b8g8r8a8-unorm-srgb-to-float4.md)  
[**Da D3DX \_ FLOAT4 \_ a \_ R8G8B8A8 \_ UNORM \_ SRGB**](d3dx-float4-to-r8g8b8a8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm"></a>FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM

<dl>

[**Da D3DX \_ B8G8R8X8 \_ UNORM \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-to-float3.md)  
[**DA D3DX \_ FLOAT3 \_ a \_ B8G8R8X8 \_ UNORM**](d3dx-float3-to-b8g8r8x8-unorm.md)  
</dl>

### <a name="dxgi_format_b8g8r8x8_unorm_srgb"></a>FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM \_ SRGB

<dl>

[**Da D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB a \_ \_ FLOAT3 \_ inesatto**](d3dx-b8g8r8x8-unorm-srgb-to-float3-inexact.md)  
[**Da D3DX \_ B8G8R8X8 \_ UNORM \_ SRGB \_ a \_ FLOAT3**](d3dx-b8g8r8x8-unorm-srgb-to-float3.md)  
[**Da D3DX \_ FLOAT3 a \_ \_ B8G8R8X8 \_ UNORM \_ SRGB**](d3dx-float3-to-b8g8r8x8-unorm-srgb.md)  
</dl>

### <a name="dxgi_format_r16g16_float"></a>FORMATO DXGI \_ \_ R16G16 \_ FLOAT

<dl>

[**Da D3DX \_ R16G16 \_ FLOAT \_ a \_ FLOAT2**](d3dx-r16g16-float-to-float2.md)  
[**DA D3DX \_ FLOAT2 a \_ \_ R16G16 \_ FLOAT**](d3dx-float2-to-r16g16-float.md)  
</dl>

### <a name="dxgi_format_r16g16_unorm"></a>DXGI \_ FORMAT \_ R16G16 \_ UNORM

<dl>

[**Da D3DX \_ R16G16 \_ UNORM \_ a \_ FLOAT2**](d3dx-r16g16-unorm-to-float2.md)  
[**DA D3DX \_ FLOAT2 \_ a \_ R16G16 \_ UNORM**](d3dx-float2-to-r16g16-unorm.md)  
</dl>

### <a name="dxgi_format_r16g16_uint"></a>INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R16G16 \_

<dl>

[**Da D3DX \_ R16G16 \_ UINT \_ a \_ UINT2**](d3dx-r16g16-uint-to-uint2.md)  
[**DA D3DX \_ UINT2 a \_ \_ R16G16 \_ UINT**](d3dx-uint2-to-r16g16-uint.md)  
</dl>

### <a name="dxgi_format_r16g16_snorm"></a>DXGI \_ FORMAT \_ R16G16 \_ SNORM

<dl>

[**Da D3DX \_ R16G16 \_ SNORM \_ a \_ FLOAT2**](d3dx-r16g16-snorm-to-float2.md)  
[**SNORM da D3DX FLOAT2 a \_ \_ \_ R16G16 \_**](d3dx-float2-to-r16g16-snorm.md)  
</dl>

### <a name="dxgi_format_r16g16_sint"></a>FORMATO DXGI \_ \_ R16G16 \_ SINT

<dl>

[**DA D3DX \_ R16G16 \_ SINT \_ a \_ INT2**](d3dx-r16g16-sint-to-int2.md)  
[**DA D3DX \_ INT2 \_ a \_ R16G16 \_ SINT**](d3dx-int2-to-r16g16-sint.md)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla conversione del formato inline](inline-format-conversion-reference.md)
</dt> <dt>

[Decompressione e impacchettamento del formato DXGI \_ per In-Place di immagini](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 
