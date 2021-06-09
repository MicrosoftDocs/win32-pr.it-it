---
description: Questo argomento descrive la progettazione interna della libreria DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Elementi interni della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f7c1843a83a81e7acac241c66dd18ff26217569
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827235"
---
# <a name="library-internals"></a>Elementi interni della libreria

Questo argomento descrive la progettazione interna della libreria DirectXMath.

-   [Convenzioni di chiamata](#calling-conventions)
-   [Equivalenza dei tipi della libreria grafica](#graphics-library-type-equivalence)
-   [Costanti globali nella libreria DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE e SSE2](#windows-sse-versus-sse2)
-   [Varianti di routine](#routine-variants)
-   [Incoerenze della piattaforma](#platform-inconsistencies)
-   [Estensioni specifiche della piattaforma](#platform-specific-extensions)
-   [Argomenti correlati](#related-topics)

## <a name="calling-conventions"></a>Convenzioni di chiamata

Per migliorare la portabilità e ottimizzare il layout dei dati, è necessario usare le convenzioni di chiamata appropriate per ogni piattaforma supportata dalla libreria DirectXMath. In particolare, quando si passano oggetti [**XMVECTOR**](xmvector-data-type.md) come parametri, definiti come allineati su un limite di 16 byte, esistono diversi set di requisiti di chiamata, a seconda della piattaforma di destinazione:

**Per Windows a 32 bit**

Per Windows a 32 bit, sono disponibili due convenzioni di chiamata per il passaggio efficiente di valori [ \_ \_ m128](/cpp/cpp/m128) (che implementa [**XMVECTOR**](xmvector-data-type.md) su tale piattaforma). Lo standard è [ \_ \_ fastcall,](https://docs.microsoft.com/cpp/cpp/fastcall)che può passare i primi tre valori [ \_ \_ m128](/cpp/cpp/m128) (istanze **XMVECTOR)** come argomenti a una funzione in un registro *SSE/SSE2.* [ \_ \_ fastcall](https://docs.microsoft.com/cpp/cpp/fastcall) passa gli argomenti rimanenti tramite lo stack.

I compilatori Microsoft Visual Studio supportano una nuova convenzione di chiamata, vectorcall, che può passare fino a sei valori \_ \_ [ \_ \_ m128](/cpp/cpp/m128) (istanze [**XMVECTOR)**](xmvector-data-type.md) come argomenti di una funzione in un registro *SSE/SSE2.* Può anche passare aggregazioni vettoriali eterogenee (note anche come [**XMMATRIX)**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)tramite registri *SSE/SSE2* se è disponibile spazio sufficiente.

**Per le edizioni a 64 bit di Windows**

Per Windows a 64 bit sono disponibili due convenzioni di chiamata per il passaggio efficiente dei [ \_ \_ valori m128.](/cpp/cpp/m128) Lo standard è [ \_ \_ fastcall,](https://docs.microsoft.com/cpp/cpp/fastcall)che passa tutti i [ \_ \_ valori m128](/cpp/cpp/m128) nello stack.

I compilatori Visual Studio supportano la convenzione di chiamata vectorcall, che può passare fino a sei valori \_ \_ [ \_ \_ m128](/cpp/cpp/m128) (istanze [**XMVECTOR)**](xmvector-data-type.md) come argomenti di una funzione in un registro *SSE/SSE2.* Può anche passare aggregazioni vettoriali eterogenee (note anche come [**XMMATRIX)**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)tramite registri *SSE/SSE2* se è disponibile spazio sufficiente.

**Per Windows in ARM**

Windows in ARM & ARM64 supporta il passaggio dei primi quattro \_ \_ valori n128 (istanze [**XMVECTOR)**](xmvector-data-type.md) nel registro.

**Soluzione DirectXMath**

Gli alias **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR** e **CXMVECTOR** supportano queste convenzioni:

-   Usare **l'alias FXMVECTOR** per passare fino alle prime tre istanze di [**XMVECTOR**](xmvector-data-type.md) usate come argomenti a una funzione.
-   Usare **l'alias GXMVECTOR** per passare la 4a istanza di [**un XMVECTOR**](xmvector-data-type.md) usato come argomento a una funzione.
-   Usare **l'alias HXMVECTOR** per passare la 5a e la sesima istanza di un [**XMVECTOR**](xmvector-data-type.md) usato come argomento a una funzione. Per informazioni su considerazioni aggiuntive, vedere la \_ \_ documentazione di vectorcall.
-   Usare **l'alias CXMVECTOR** per passare eventuali altre istanze di [**XMVECTOR**](xmvector-data-type.md) usate come argomenti.

> [!Note]  
> Per i parametri di output, usare sempre XMVECTOR o XMVECTOR& e ignorarli rispetto alle regole precedenti per \* i parametri di input.

 

A causa delle limitazioni di vectorcall, è consigliabile non usare \_ \_ **GXMVECTOR** o **HXMVECTOR** per i costruttori C++. È sufficiente **usare FXMVECTOR** per i primi tre valori [**XMVECTOR,**](xmvector-data-type.md) quindi **usare CXMVECTOR** per il resto.

Gli alias **FXMMATRIX** **e CXMMATRIX** consentono di sfruttare i vantaggi del passaggio dell'argomento HVA con \_ \_ vectorcall.

-   Usare **l'alias FXMMATRIX** per passare il [**primo oggetto XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come argomento alla funzione. Si presuppone che non siano disponibili più di due argomenti **FXMVECTOR** o più di due argomenti float, double o **FXMVECTOR** a 'destra' della matrice. Per informazioni su considerazioni aggiuntive, vedere la \_ \_ documentazione di vectorcall.
-   In caso contrario, usare l'alias **CXMMATRIX.**

A causa delle limitazioni di vectorcall, è consigliabile non usare \_ \_ mai **FXMMATRIX** per i costruttori C++. È sufficiente usare **CXMMATRIX**.

Oltre agli alias di tipo, è necessario usare anche l'annotazione XM CALLCONV per assicurarsi che la funzione usi la convenzione di chiamata appropriata \_ \_ \_ (fastcall o \_ vectorcall) in base al compilatore e \_ all'architettura. A causa delle limitazioni di vectorcall, è consigliabile non usare \_ \_ XM \_ CALLCONV per i costruttori C++.

Di seguito sono riportate dichiarazioni di esempio che illustrano questa convenzione:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Per supportare queste convenzioni di chiamata, questi alias di tipo sono definiti come segue (i parametri devono essere passati per valore perché il compilatore li consideri per il passaggio nel registro):

**Per le app di Windows a 32 bit**

Quando si usa \_ \_ fastcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quando si usa \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Per le app native di Windows a 64 bit**

Quando si usa \_ \_ fastcall:


```C++
typedef const XMVECTOR& FXMVECTOR;
typedef const XMVECTOR& GXMVECTOR;
typedef const XMVECTOR& HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



Quando si usa \_ \_ vectorcall:


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR  HXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX  FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



**Windows in ARM**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Anche se tutte le funzioni sono dichiarate inline e in molti casi il compilatore non dovrà usare convenzioni di chiamata per queste funzioni, in alcuni casi il compilatore può decidere che è più efficiente non eseguire l'inline della funzione e in questi casi è necessaria la migliore convenzione di chiamata possibile per ogni piattaforma.

 

## <a name="graphics-library-type-equivalence"></a>Equivalenza dei tipi della libreria grafica

Per supportare l'uso della libreria DirectXMath, molti tipi e strutture della libreria DirectXMath sono equivalenti alle implementazioni di Windows dei tipi **D3DDECLTYPE** e **D3DFORMAT,** nonché ai tipi [**DXGI \_ FORMAT.**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | FORMATO \_ DXGI                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R8G8 \_ SINT                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (solo Xbox)                                                        | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ SINT                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | D3DFMT \_ V8U8                                                  | DXGI \_ FORMAT \_ R8G8 \_ SNORM                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (solo Xbox)                                                       | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ SNORM                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | D3DDECLTYPE \_ D3DCOLOR                                                                 | D3DFMT \_ A8R8G8B8                                              | FORMATO DXGI \_ \_ B8G8R8A8 \_ UNORM (DXGI 1.1+)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (solo Xbox)                                                         | D3DDECLTYPE \_ DEC3 (solo Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (solo Xbox)                                                        | D3DDECLTYPE \_ DEC3N (solo Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | D3DDECLTYPE \_ FLOAT2                                                                   | D3DFMT \_ G32R32F                                               | FORMATO DXGI \_ \_ R32G32 \_ FLOAT                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | D3DDECLTYPE \_ FLOAT3                                                                   |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | FORMATO DXGI \_ \_ R11G11B10 \_ FLOAT                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | FORMATO DXGI \_ \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | D3DDECLTYPE \_ FLOAT4                                                                   | D3DFMT \_ A32B32G32R32F                                         | FORMATO DXGI \_ \_ R32G32B32A32 \_ FLOAT                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | D3DFMT \_ G16R16F                                               | FORMATO DXGI \_ \_ R16G16 \_ FLOAT                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | D3DFMT \_ A16B16G16R16F                                         | FORMATO DXGI \_ \_ R16G16B16A16 \_ FLOAT                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32 \_ SINT                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ SINT                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32A32 \_ SINT                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | D3DDECLTYPE \_ SHORT2                                                                   | D3DFMT \_ V16U16                                                | FORMATO DXGI \_ \_ R16G16 \_ SINT                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | D3DDECLTYPE \_ SHORT2N                                                                  | D3DFMT \_ V16U16                                                | DXGI \_ FORMAT \_ R16G16 \_ SNORM                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | D3DDECLTYPE \_ SHORT4                                                                   | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ SINT                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | D3DDECLTYPE \_ SHORT4N                                                                  | D3DFMT \_ x16x16x16x16                                          | DXGI \_ FORMAT \_ R16G16B16A16 \_ SNORM                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R8G8 \_                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | DXGI \_ FORMAT \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32 \_ UINT                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32 \_ UINT                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | FORMATO DXGI \_ \_ R32G32B32A32 \_ UINT                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | FORMATO DXGI \_ \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | D3DFMT \_ R5G6B5                                                | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | D3DDECLTYPE \_ UBYTE4                                                                   | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UINT                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | D3DDECLTYPE \_ UBYTE4N                                                                  | D3DFMT \_ x8x8x8x8                                              | DXGI \_ FORMAT \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ FORMAT \_ R10G10B10 \_ XR BIAS \_ \_ A2 \_ UNORM (usare [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) e [**XMStoreUDecn4 \_ XR).**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3 (solo Xbox)<br/>   | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | FORMATO DXGI \_ \_ R10G10B10A2 \_ UINT                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3N (solo Xbox)<br/> | D3DFMT \_ A2R10G10B10<br/> D3DFMT \_ A2B10G10R10<br/> | FORMATO DXGI \_ \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | FORMATO DXGI \_ \_ B4G4R4A4 \_ UNORM (DXGI 1.2+)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | D3DDECLTYPE \_ USHORT2                                                                  | D3DFMT \_ G16R16                                                | INTERFACCIA UTENTE DI DXGI \_ FORMAT \_ R16G16 \_                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | D3DDECLTYPE \_ USHORT2N                                                                 | D3DFMT \_ G16R16                                                | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (solo Xbox)                                                      | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ UINT                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | D3DDECLTYPE \_ USHORT4N                                                                 | D3DFMT \_ x16x16x16x16                                          | FORMATO DXGI \_ \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Costanti globali nella libreria DirectXMath

Per ridurre le dimensioni del segmento di dati, la libreria DirectXMath usa la macro [XMGLOBALCONST](xmglobalconst.md) per usare una serie di costanti interne globali nella relativa implementazione. Per convenzione, queste costanti globali interne sono precedute da **g \_ XM**. In genere, sono uno dei tipi seguenti: [**XMVECTORU32,**](xmvectoru32-data-type.md) [**XMVECTORF32**](xmvectorf32-data-type.md)o **XMVECTORI32**.

Queste costanti globali interne sono soggette a modifiche nelle revisioni future della libreria DirectXMath. Usare funzioni pubbliche che incapsulano le costanti quando possibile anziché usare direttamente **i \_ valori globali XM g.** È anche possibile dichiarare costanti globali usando [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE e SSE2

Il set di istruzioni SSE fornisce il supporto solo per vettori a virgola mobile e precisione singola. DirectXMath deve usare il set di istruzioni SSE2 per fornire il supporto del vettore integer. SSE2 è supportato da tutti i processori Intel a partire dall'introduzione del Processore Pentium 4, di tutti i processori AMD K8 e versioni successive e di tutti i processori con supporto x64.

> [!Note]  
> Windows 8 per x86 o versioni successive richiede il supporto per SSE2. Tutte le versioni di Windows x64 richiedono il supporto per SSE2. Windows in ARM/ARM64 richiede ARM \_ NEON.

 

## <a name="routine-variants"></a>Varianti di routine

Esistono diverse varianti di funzioni DirectXMath che semplificano l'attività:

-   Funzioni di confronto per creare diramazioni condizionali complesse in base a un numero inferiore di operazioni di confronto tra vettori. Il nome di queste funzioni termina con "R", ad esempio XMVector3InBoundsR. Le funzioni restituiscono un record di confronto come valore restituito UINT o come parametro UINT out. È possibile usare le macro **XMComparision \*** per testare il valore.
-   Funzioni batch per l'esecuzione di operazioni di tipo batch in matrici di vettori più grandi. Il nome di queste funzioni termina con "Stream", ad [**esempio XMVector3TransformStream.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream) Le funzioni operano su una matrice di input e generano una matrice di output. In genere, accettano uno stride di input e output.
-   Funzioni di stima che implementano una stima più veloce anziché un risultato più lento e accurato. Il nome di queste funzioni termina con "Est", ad esempio [**XMVector3NormalizeEst.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest) L'impatto sulla qualità e sulle prestazioni dell'uso della stima varia da piattaforma a piattaforma, ma è consigliabile usare varianti di stima per il codice sensibile alle prestazioni.

## <a name="platform-inconsistencies"></a>Incoerenze della piattaforma

La libreria DirectXMath è destinata all'uso in giochi e applicazioni grafiche sensibili alle prestazioni. Pertanto, l'implementazione è progettata per velocizzare l'elaborazione normale in tutte le piattaforme supportate. I risultati in corrispondenza delle condizioni limite, in particolare quelli che generano speciali a virgola mobile, possono variare da destinazione a destinazione. Questo comportamento dipende anche da altre impostazioni di run-time, ad esempio la parola di controllo x87 per la destinazione no-intrinsics di Windows a 32 bit o la parola di controllo SSE per Windows a 32 bit e a 64 bit. Inoltre, ci saranno differenze nelle condizioni limite tra i vari fornitori di CPU.

Non usare DirectXMath in applicazioni scientifiche o di altro tipo in cui l'accuratezza numerica è fondamentale. Questa limitazione si riflette anche nella mancanza di supporto per calcoli di precisione doppia o di altro tipo esteso.

> [!Note]  
> I \_ percorsi del codice scalare NO INTRINSICS XM vengono in genere scritti per garantire la \_ \_ \_ conformità, non per le prestazioni. Anche i risultati della condizione limite variano.

 

## <a name="platform-specific-extensions"></a>Estensioni specifiche della piattaforma

La libreria DirectXMath è progettata per semplificare la programmazione SIMD C++ offrendo un eccellente supporto per le piattaforme x86, x64 e Windows RT usando istruzioni intrinseche ampiamente supportate (SSE2 e ARM-NEON).

In alcuni casi, tuttavia, le istruzioni specifiche della piattaforma possono risultare utili. A causa del modo in cui viene implementato DirectXMath, in molti casi è semplice usare i tipi DirectXMath direttamente nelle istruzioni intrinseche standard supportate dal compilatore e usare DirectXMath come percorso di fallback per le piattaforme che non supportano l'istruzione estesa.

Ecco ad esempio un esempio semplificato di uso dell'istruzione dot-product SSE 4.1. Si noti che è necessario proteggere in modo esplicito il percorso del codice per evitare la generazione di eccezioni di istruzione non valide in fase di esecuzione. Assicurarsi che i percorsi di codice esercitino un lavoro sufficientemente significativo per giustificare il costo aggiuntivo della diramazione, la complessità della gestione di più percorsi di codice e così via.


```
#include <Windows.h>
#include <stdio.h>

#include <DirectXMath.h>

#include <intrin.h>
#include <smmintrin.h>

using namespace DirectX;

bool g_bSSE41 = false;

void DetectCPUFeatures()
{
#ifndef _M_ARM
   // See __cpuid documentation on MSDN for more information

   int CPUInfo[4] = {-1};
#if defined(__clang__) || defined(__GNUC__)
   __cpuid(0, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
   __cpuid(CPUInfo, 0);
#endif

   if ( CPUInfo[0] >= 1 )
   {
#if defined(__clang__) || defined(__GNUC__)
        __cpuid(1, CPUInfo[0], CPUInfo[1], CPUInfo[2], CPUInfo[3]);
#else
        __cpuid(CPUInfo, 1);
#endif

       if ( CPUInfo[2] & 0x80000 )
           g_bSSE41 = true;
   }
#endif
}

int main()
{
   if ( !XMVerifyCPUSupport() )
       return -1;

   DetectCPUFeatures();

   ...

   XMVECTORF32 v1 = { 1.f, 2.f, 3.f, 4.f };
   XMVECTORF32 v2 = { 5.f, 6.f, 7.f, 8.f };

   XMVECTOR r2, r3, r4;

   if ( g_bSSE41 )
   {
#ifndef _M_ARM
       r2 = _mm_dp_ps( v1, v2, 0x3f );
       r3 = _mm_dp_ps( v1, v2, 0x7f );
       r4 = _mm_dp_ps( v1, v2, 0xff );
#endif
   }
   else
   {
       r2 = XMVector2Dot( v1, v2 );
       r3 = XMVector3Dot( v1, v2 );
       r4 = XMVector4Dot( v1, v2 );
   }

   ...

   return 0;
}
```



Per altre informazioni sulle estensioni specifiche della piattaforma, vedere:

<dl>

[DirectXMath: SSE, SSE2 e ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 e SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE4.1 e SSE4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C e FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
