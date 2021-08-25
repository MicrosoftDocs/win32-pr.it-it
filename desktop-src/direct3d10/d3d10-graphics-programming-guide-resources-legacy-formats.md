---
description: Questa tabella elenca i formati Direct3D 9 di cui è possibile eseguire il mapping a un formato Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formati legacy: eseguire il mapping dei formati Direct3D 9 a Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40a437ef42b4ce24b468c39d169b39db7fb9cb7951c825da38bb63f85b9dba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895301"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formati legacy: eseguire il mapping dei formati Direct3D 9 a Direct3D 10

Questa tabella elenca i formati Direct3D 9 di cui è possibile eseguire il mapping a un formato Direct3D 10. I formati Direct3D 10 sono diversi dai formati Direct3D 9 in modo che i formati di vertice e trama possano essere uniti per abilitare le applicazioni cross-endian.



| Direct3D 9 Texture/Vertex/Index Format | Formato Direct3D 10 equivalente                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                        | FORMATO DXGI \_ \_ SCONOSCIUTO                                                |
| D3DFMT \_ R8G8B8                         | Non disponibile                                                        |
| D3DFMT \_ A8R8G8B8                       | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ X8R8G8B8                       | FORMATO DXGI \_ \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ R5G6B5                         | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM (DXGI 1.2)                               |
| D3DFMT \_ X1R5G5B5                       | Non disponibile                                                        |
| D3DFMT \_ A1R5G5B5                       | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ A4R4G4B4                       | FORMATO DXGI \_ \_ B4G4R4A4 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ R3G3B2                         | Non disponibile                                                        |
| D3DFMT \_ A8                             | FORMATO DXGI \_ \_ A8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Non disponibile                                                        |
| D3DFMT \_ X4R4G4B4                       | Non disponibile                                                        |
| D3DFMT \_ A2B10G10R10                    | FORMATO DXGI \_ \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM o DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB |
| D3DFMT \_ X8B8G8R8                       | Non disponibile                                                        |
| D3DFMT \_ G16R16                         | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Non disponibile                                                        |
| D3DFMT \_ A16B16G16R16                   | FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Non disponibile                                                        |
| D3DFMT \_ P8                             | Non disponibile                                                        |
| D3DFMT \_ L8                             | FORMATO DXGI \_ \_ R8 \_ UNORM ¹                                            |
| D3DFMT \_ A8L8                           | Non disponibile                                                        |
| D3DFMT \_ A4L4                           | Non disponibile                                                        |
| D3DFMT \_ V8U8                           | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | Non disponibile                                                        |
| D3DFMT \_ X8L8V8U8                       | Non disponibile                                                        |
| D3DFMT \_ Q8W8V8U8                       | DXGI \_ FORMAT \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | Non disponibile                                                        |
| D3DFMT \_ A2W10V10U10                    | Non disponibile                                                        |
| D3DFMT \_ UYVY                           | Non disponibile                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | FORMATO DXGI \_ \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | Non disponibile                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | FORMATO DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | FORMATO DXGI \_ \_ BC1 \_ UNORM o DXGI \_ FORMAT \_ BC1 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT2                           | FORMATO DXGI \_ \_ BC2 \_ UNORM o DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB rsi         |
| D3DFMT \_ DXT3                           | FORMATO DXGI \_ \_ BC2 \_ UNORM o DXGI \_ FORMAT \_ BC2 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT4                           | FORMATO DXGI \_ \_ BC3 \_ UNORM o DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB rsi         |
| D3DFMT \_ DXT5                           | FORMATO DXGI \_ \_ BC3 \_ UNORM o DXGI \_ FORMAT \_ BC3 \_ UNORM \_ SRGB           |
| D3DFMT \_ D16 e D3DFMT \_ D16 \_ BLOCCABILE  | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | Non disponibile                                                        |
| D3DFMT \_ D15S1                          | Non disponibile                                                        |
| D3DFMT \_ D24S8                          | Non disponibile                                                        |
| D3DFMT \_ D24X8                          | Non disponibile                                                        |
| D3DFMT \_ D24X4S4                        | Non disponibile                                                        |
| D3DFMT \_ D16                            | DXGI \_ FORMAT \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ LOCKABLE                 | FORMATO DXGI \_ \_ D32 \_ FLOAT                                             |
| D3DFMT \_ D24FS8                         | Non disponibile                                                        |
| D3DFMT \_ S1D15                          | Non disponibile                                                        |
| D3DFMT \_ S8D24                          | DXGI \_ FORMAT \_ D24 \_ UNORM \_ S8 \_ UINT                                   |
| D3DFMT \_ X8D24                          | Non disponibile                                                        |
| D3DFMT \_ X4S4D24                        | Non disponibile                                                        |
| D3DFMT \_ L16                            | FORMATO DXGI \_ \_ R16 \_ UNORM ¹                                           |
| INDICE \_ D3DFMT16                        | INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R16 \_                                              |
| INDICE \_ D3DFMT32                        | INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R32 \_                                              |
| D3DFMT \_ Q16W16V16U16                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Non disponibile                                                        |
| D3DFMT \_ R16F                           | FORMATO DXGI \_ \_ R16 \_ FLOAT                                             |
| D3DFMT \_ G16R16F                        | FORMATO DXGI \_ \_ R16G16 \_ FLOAT                                          |
| D3DFMT \_ A16B16G16R16F                  | FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT                                    |
| D3DFMT \_ R32F                           | FORMATO DXGI \_ \_ R32 \_ FLOAT                                             |
| D3DFMT \_ G32R32F                        | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                          |
| D3DFMT \_ A32B32G32R32F                  | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                    |
| D3DFMT \_ CxV8U8                         | Non disponibile                                                        |
| D3DDECLTYPE \_ FLOAT1                    | FORMATO DXGI \_ \_ R32 \_ FLOAT                                             |
| D3DDECLTYPE \_ FLOAT2                    | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT3                    | FORMATO DXGI \_ \_ R32G32B32 \_ FLOAT                                       |
| D3DDECLTYPE \_ FLOAT4                    | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                    |
| D3DDECLTYPED3DCOLOR                    | Non disponibile                                                        |
| D3DDECLTYPE \_ UBYTE4                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ UINT ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | FORMATO DXGI \_ \_ R16G16 \_ SINT                                           |
| D3DDECLTYPE \_ SHORT4                    | FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT                                     |
| D3DDECLTYPE \_ UBYTE4N                   | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Non disponibile                                                        |
| D3DDECLTYPE \_ DEC3N                     | Non disponibile                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | FORMATO DXGI \_ \_ R16G16 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT                                    |



 

1.  Usare .r swizzle in uno shader per duplicare il rosso per altri componenti per ottenere il comportamento direct3D 9.
2.  In Direct3D 9 i dati sono stati ridimensionati di 255,0f, operazione che può essere eseguita invece nel codice shader.
3.  DXT2 e DXT3 sono gli stessi dal punto di vista dell'API; DXT4 e DXT5 sono gli stessi dal punto di vista dell'API. L'unica differenza era l'alfa premoltilied, che può essere monitorato da un'applicazione e non richiede un formato separato.
4.  Uno shader ottiene valori UINT, ma se i valori integrali in stile Direct3D 9 sono float (0,0f, 1,0f... 255.f) sono necessari, UINT può essere convertito in float32 in uno shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



