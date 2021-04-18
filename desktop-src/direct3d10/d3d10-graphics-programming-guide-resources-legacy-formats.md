---
description: Questa tabella elenca i formati Direct3D 9 di cui è possibile eseguire il mapping a un formato Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formati legacy: mappare i formati Direct3D 9 a Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304802"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formati legacy: mappare i formati Direct3D 9 a Direct3D 10

Questa tabella elenca i formati Direct3D 9 di cui è possibile eseguire il mapping a un formato Direct3D 10. I formati Direct3D 10 sono stati divergenti dai formati Direct3D 9, in modo che sia possibile unire i formati dei vertici e delle trame per abilitare le applicazioni tra più endian.



| Formato trama/vertice/Indice Direct3D 9 | Formato Direct3D 10 equivalente                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ sconosciuto                        | \_formato DXGI \_ sconosciuto                                                |
| \_R8G8B8 D3DFMT                         | Non disponibile                                                        |
| \_A8R8G8B8 D3DFMT                       | \_Formato DXGI \_ B8G8R8A8 \_ UNORM (DXGI 1,1)                             |
| \_X8R8G8B8 D3DFMT                       | \_Formato DXGI \_ B8G8R8X8 \_ UNORM (DXGI 1,1)                             |
| \_R5G6B5 D3DFMT                         | \_Formato DXGI \_ B5G6R5 \_ UNORM (DXGI 1,2)                               |
| \_X1R5G5B5 D3DFMT                       | Non disponibile                                                        |
| \_A1R5G5B5 D3DFMT                       | \_Formato DXGI \_ B5G5R5A1 \_ UNORM (DXGI 1,2)                             |
| \_A4R4G4B4 D3DFMT                       | \_Formato DXGI \_ B4G4R4A4 \_ UNORM (DXGI 1,2)                             |
| \_R3G3B2 D3DFMT                         | Non disponibile                                                        |
| D3DFMT \_ a8                             | \_Formato DXGI \_ a8 \_ UNORM                                              |
| \_A8R3G3B2 D3DFMT                       | Non disponibile                                                        |
| \_X4R4G4B4 D3DFMT                       | Non disponibile                                                        |
| \_A2B10G10R10 D3DFMT                    | \_Formato DXGI \_ R10G10B10A2                                            |
| \_A8B8G8R8 D3DFMT                       | DXGI \_ Format \_ R8G8B8A8 \_ UNORM o DXGI \_ Format \_ R8G8B8A8 \_ UNORM \_ sRGB |
| \_X8B8G8R8 D3DFMT                       | Non disponibile                                                        |
| \_G16R16 D3DFMT                         | \_Formato DXGI \_ R16G16 \_ UNORM                                          |
| \_A2R10G10B10 D3DFMT                    | Non disponibile                                                        |
| \_A16B16G16R16 D3DFMT                   | \_Formato DXGI \_ R16G16B16A16 \_ UNORM                                    |
| \_A8P8 D3DFMT                           | Non disponibile                                                        |
| D3DFMT \_ P8                             | Non disponibile                                                        |
| \_L8 D3DFMT                             | DXGI \_ formato \_ R8 \_ UNORM ¹                                            |
| \_A8L8 D3DFMT                           | Non disponibile                                                        |
| \_A4L4 D3DFMT                           | Non disponibile                                                        |
| \_V8U8 D3DFMT                           | DXGI \_ Format \_ R8G8 \_ russar                                            |
| \_L6V5U5 D3DFMT                         | Non disponibile                                                        |
| \_X8L8V8U8 D3DFMT                       | Non disponibile                                                        |
| \_Q8W8V8U8 D3DFMT                       | DXGI \_ Format \_ R8G8B8A8 \_ russar                                        |
| \_V16U16 D3DFMT                         | DXGI \_ Format \_ R16G16 \_ russar                                          |
| \_W11V11U10 D3DFMT                      | Non disponibile                                                        |
| \_A2W10V10U10 D3DFMT                    | Non disponibile                                                        |
| \_UYVY D3DFMT                           | Non disponibile                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | DXGI \_ Format \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| \_YUY2 D3DFMT                           | Non disponibile                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | DXGI \_ Format \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| \_DXT1 D3DFMT                           | DXGI \_ Format \_ BC1 \_ UNORM o DXGI \_ Format \_ BC1 \_ UNORM \_ sRGB           |
| \_DXT2 D3DFMT                           | DXGI \_ Format \_ BC2 \_ UNORM o DXGI \_ Format \_ BC2 \_ UNORM \_ sRGB ³         |
| \_DXT3 D3DFMT                           | DXGI \_ Format \_ BC2 \_ UNORM o DXGI \_ Format \_ BC2 \_ UNORM \_ sRGB           |
| \_DXT4 D3DFMT                           | DXGI \_ Format \_ BC3 \_ UNORM o DXGI \_ Format \_ BC3 \_ UNORM \_ sRGB ³         |
| \_DXT5 D3DFMT                           | DXGI \_ Format \_ BC3 \_ UNORM o DXGI \_ Format \_ BC3 \_ UNORM \_ sRGB           |
| D3DFMT \_ D16 e D3DFMT \_ D16 \_ lockable  | \_Formato DXGI \_ D16 \_ UNORM                                             |
| \_D32 D3DFMT                            | Non disponibile                                                        |
| \_D15S1 D3DFMT                          | Non disponibile                                                        |
| \_D24S8 D3DFMT                          | Non disponibile                                                        |
| \_D24X8 D3DFMT                          | Non disponibile                                                        |
| \_D24X4S4 D3DFMT                        | Non disponibile                                                        |
| \_D16 D3DFMT                            | \_Formato DXGI \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ lockable                 | \_Formato DXGI \_ D32 \_ float                                             |
| \_D24FS8 D3DFMT                         | Non disponibile                                                        |
| \_S1D15 D3DFMT                          | Non disponibile                                                        |
| \_S8D24 D3DFMT                          | DXGI \_ Format \_ D24 \_ UNORM \_ S8 \_ uint                                   |
| \_X8D24 D3DFMT                          | Non disponibile                                                        |
| \_X4S4D24 D3DFMT                        | Non disponibile                                                        |
| \_L16 D3DFMT                            | DXGI \_ Format \_ R16 \_ UNORM ¹                                           |
| \_INDEX16 D3DFMT                        | \_Formato DXGI \_ R16 \_ uint                                              |
| \_INDEX32 D3DFMT                        | \_Formato DXGI \_ R32 \_ uint                                              |
| \_Q16W16V16U16 D3DFMT                   | DXGI \_ Format \_ R16G16B16A16 \_ russar                                    |
| D3DFMT \_ MULTi2 \_ ARGB8                  | Non disponibile                                                        |
| \_R16F D3DFMT                           | \_Formato DXGI \_ R16 \_ float                                             |
| \_G16R16F D3DFMT                        | \_Formato DXGI \_ R16G16 \_ float                                          |
| \_A16B16G16R16F D3DFMT                  | \_Formato DXGI \_ R16G16B16A16 \_ float                                    |
| \_R32F D3DFMT                           | \_Formato DXGI \_ R32 \_ float                                             |
| \_G32R32F D3DFMT                        | \_Formato DXGI \_ R32G32 \_ float                                          |
| \_A32B32G32R32F D3DFMT                  | \_Formato DXGI \_ R32G32B32A32 \_ float                                    |
| \_CXV8U8 D3DFMT                         | Non disponibile                                                        |
| \_FLOAT1 D3DDECLTYPE                    | \_Formato DXGI \_ R32 \_ float                                             |
| \_FLOAT2 D3DDECLTYPE                    | \_Formato DXGI \_ R32G32 \_ float                                          |
| \_FLOAT3 D3DDECLTYPE                    | \_Formato DXGI \_ R32G32B32 \_ float                                       |
| \_Float4 D3DDECLTYPE                    | \_Formato DXGI \_ R32G32B32A32 \_ float                                    |
| D3DDECLTYPED3DCOLOR                    | Non disponibile                                                        |
| \_UBYTE4 D3DDECLTYPE                    | \_Formato DXGI \_ R8G8B8A8 \_ uint ⁴                                       |
| \_SHORT2 D3DDECLTYPE                    | \_Formato DXGI \_ R16G16 \_ Sint                                           |
| \_SHORT4 D3DDECLTYPE                    | \_Formato DXGI \_ R16G16B16A16 \_ Sint                                     |
| \_Dati UBYTE4N D3DDECLTYPE                   | \_Formato DXGI \_ R8G8B8A8 \_ UNORM                                        |
| \_SHORT2N D3DDECLTYPE                   | DXGI \_ Format \_ R16G16 \_ russar                                          |
| \_SHORT4N D3DDECLTYPE                   | DXGI \_ Format \_ R16G16B16A16 \_ russar                                    |
| \_USHORT2N D3DDECLTYPE                  | \_Formato DXGI \_ R16G16 \_ UNORM                                          |
| \_USHORT4N D3DDECLTYPE                  | \_Formato DXGI \_ R16G16B16A16 \_ UNORM                                    |
| \_UDEC3 D3DDECLTYPE                     | Non disponibile                                                        |
| \_DEC3N D3DDECLTYPE                     | Non disponibile                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | \_Formato DXGI \_ R16G16 \_ float                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | \_Formato DXGI \_ R16G16B16A16 \_ float                                    |



 

1.  Usare. r swizzle in uno shader per duplicare il rosso con altri componenti per ottenere il comportamento di Direct3D 9.
2.  In Direct3D 9 i dati sono stati ridimensionati in base a 255.0 f, che può essere eseguito nel codice dello shader.
3.  DXT2 e DXT3 sono uguali dal punto di vista dell'API. DXT4 e DXT5 sono uguali dal punto di vista dell'API. L'unica differenza è l'alfa premoltiplicato, che può essere rilevata da un'applicazione e non necessita di un formato separato.
4.  Uno shader ottiene i valori UINT, ma se lo stile Direct3D 9 è floats integrali (0,0 f, 1.0 f... 255. f) sono necessari, UINT può essere convertito in float32 in uno shader.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Risorse (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



