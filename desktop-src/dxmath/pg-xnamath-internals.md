---
description: In questo argomento viene descritta la progettazione interna della libreria DirectXMath.
ms.assetid: 31512657-c413-9e6e-e343-1ea677a02b8c
title: Elementi interni della libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccac708934c393a526fdb46d73f819d6557107f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309247"
---
# <a name="library-internals"></a>Elementi interni della libreria

In questo argomento viene descritta la progettazione interna della libreria DirectXMath.

-   [Convenzioni di chiamata](#calling-conventions)
-   [Equivalenza del tipo di libreria grafica](#graphics-library-type-equivalence)
-   [Costanti globali nella libreria DirectXMath](#global-constants-in-the-directxmath-library)
-   [Windows SSE rispetto a SSE2](#windows-sse-versus-sse2)
-   [Varianti di routine](#routine-variants)
-   [Incoerenze della piattaforma](#platform-inconsistencies)
-   [Estensioni specifiche della piattaforma](#platform-specific-extensions)
-   [Argomenti correlati](#related-topics)

## <a name="calling-conventions"></a>Convenzioni di chiamata

Per migliorare la portabilità e ottimizzare il layout dei dati, è necessario usare le convenzioni di chiamata appropriate per ogni piattaforma supportata dalla libreria DirectXMath. In particolare, quando si passano gli oggetti [**XMVECTOR**](xmvector-data-type.md) come parametri, che sono definiti come allineati su un limite di 16 byte, esistono diversi set di requisiti per la chiamata, a seconda della piattaforma di destinazione:

**Per Windows a 32 bit**

Per Windows a 32 bit sono disponibili due convenzioni di chiamata per il passaggio efficiente di valori [ \_ \_ M128](/cpp/cpp/m128) (che implementa [**XMVECTOR**](xmvector-data-type.md) su tale piattaforma). Lo standard è [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), che può passare i primi tre valori [ \_ \_ M128](/cpp/cpp/m128) (istanze **XMVECTOR** ) come argomenti a una funzione in un registro *SSE/SSE2* . [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx) passa gli argomenti rimanenti tramite lo stack.

I compilatori di Microsoft Visual Studio più recenti supportano una nuova convenzione di chiamata, \_ \_ vectorcall, che può passare fino a sei valori [ \_ \_ M128](/cpp/cpp/m128) (istanze [**XMVECTOR**](xmvector-data-type.md) ) come argomenti di una funzione in un registro *SSE/SSE2* . Può anche passare aggregazioni vettoriali eterogenee (note anche come [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) tramite i registri *SSE/SSE2* se lo spazio disponibile è sufficiente.

**Per le edizioni a 64 bit di Windows**

Per le finestre a 64 bit, sono disponibili due convenzioni di chiamata per il passaggio efficiente dei valori [ \_ \_ M128](/cpp/cpp/m128) . Lo standard è [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(VS.71).aspx), che passa tutti i valori [ \_ \_ M128](/cpp/cpp/m128) nello stack.

I compilatori più recenti di Visual Studio supportano la \_ \_ convenzione di chiamata vectorcall, che può passare fino a sei valori [ \_ \_ M128](/cpp/cpp/m128) (istanze [**XMVECTOR**](xmvector-data-type.md) ) come argomenti a una funzione in un registro *SSE/SSE2* . Può anche passare aggregazioni vettoriali eterogenee (note anche come [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix)) tramite i registri *SSE/SSE2* se lo spazio disponibile è sufficiente.

**Per Windows RT**

Il sistema operativo Windows RT supporta il passaggio dei primi quattro \_ \_ valori N128 (istanze di [**XMVECTOR**](xmvector-data-type.md) ) nel registro.

**Soluzione DirectXMath**

Gli alias **FXMVECTOR**, **GXMVECTOR**, **HXMVECTOR** e **CXMVECTOR** supportano le convenzioni seguenti:

-   Utilizzare l'alias **FXMVECTOR** per passare alle prime tre istanze di [**XMVECTOR**](xmvector-data-type.md) utilizzate come argomenti per una funzione.
-   Usare l'alias **GXMVECTOR** per passare la quarta istanza di un [**XMVECTOR**](xmvector-data-type.md) usato come argomento di una funzione.
-   Usare l'alias **HXMVECTOR** per passare la quinta e la sesta istanza di un [**XMVECTOR**](xmvector-data-type.md) usato come argomento di una funzione. Per informazioni sulle considerazioni aggiuntive, vedere la \_ \_ documentazione di vectorcall.
-   Usare l'alias **CXMVECTOR** per passare eventuali altre istanze di [**XMVECTOR**](xmvector-data-type.md) utilizzate come argomenti.

> [!Note]  
> Per i parametri di output, usare sempre XMVECTOR \* o XMVECTOR& e ignorarli rispetto alle regole precedenti per i parametri di input.

 

A causa delle limitazioni di \_ \_ vectorcall, è consigliabile non usare **GXMVECTOR** o **HXMVECTOR** per i costruttori C++. Usare **FXMVECTOR** solo per i primi tre valori [**XMVECTOR**](xmvector-data-type.md) e quindi usare **CXMVECTOR** per il resto.

Gli alias **FXMMATRIX** e **CXMMATRIX** consentono di sfruttare i vantaggi dell'argomento Hva che passa con \_ \_ vectorcall.

-   Usare l'alias **FXMMATRIX** per passare il primo [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come argomento alla funzione. Si presuppone che non si disponga di più di due argomenti **FXMVECTOR** o di più di due argomenti float, Double o **FXMVECTOR** per l'oggetto "Right" della matrice. Per informazioni sulle considerazioni aggiuntive, vedere la \_ \_ documentazione di vectorcall.
-   In caso contrario, usare l'alias **CXMMATRIX** .

A causa delle limitazioni di \_ \_ vectorcall, è consigliabile non usare mai **FXMMATRIX** per i costruttori C++. Usare semplicemente **CXMMATRIX**.

Oltre agli alias di tipo, è necessario usare anche l' \_ annotazione CALLCONV XM per assicurarsi che la funzione usi la convenzione di chiamata appropriata ( \_ \_ fastcall rispetto a \_ \_ vectorcall) in base al compilatore e all'architettura. A causa delle limitazioni di \_ \_ vectorcall, è consigliabile non usare XM \_ CALLCONV per i costruttori C++.

Di seguito sono riportate le dichiarazioni di esempio che illustrano questa convenzione:


```C++
XMMATRIX XM_CALLCONV XMMatrixLookAtLH(FXMVECTOR EyePosition, FXMVECTOR FocusPosition, FXMVECTOR UpDirection);

XMMATRIX XM_CALLCONV XMMatrixTransformation2D(FXMVECTOR ScalingOrigin,  float ScalingOrientation, FXMVECTOR Scaling, FXMVECTOR RotationOrigin, float Rotation, GXMVECTOR Translation);

void XM_CALLCONV XMVectorSinCos(XMVECTOR* pSin, XMVECTOR* pCos, FXMVECTOR V);

XMVECTOR XM_CALLCONV XMVectorHermiteV(FXMVECTOR Position0, FXMVECTOR Tangent0, FXMVECTOR Position1, GXMVECTOR Tangent1, HXMVECTOR T);

XMMATRIX(FXMVECTOR R0, FXMVECTOR R1, FXMVECTOR R2, CXMVECTOR R3)

XMVECTOR XM_CALLCONV XMVector2Transform(FXMVECTOR V, FXMMATRIX M);

XMMATRIX XM_CALLCONV XMMatrixMultiplyTranspose(FXMMATRIX M1, CXMMATRIX M2);
```



Per supportare queste convenzioni di chiamata, questi alias di tipo sono definiti nel modo seguente (i parametri devono essere passati per valore affinché il compilatore li consideri per il passaggio in-Register):

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



**Per app di Windows native a 64 bit**

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



**Windows RT**


```C++
typedef const XMVECTOR  FXMVECTOR;
typedef const XMVECTOR  GXMVECTOR;
typedef const XMVECTOR& CXMVECTOR;
typedef const XMMATRIX& FXMMATRIX;
typedef const XMMATRIX& CXMMATRIX;
```



> [!Note]  
> Anche se tutte le funzioni sono dichiarate inline e in molti casi il compilatore non dovrà usare le convenzioni di chiamata per queste funzioni, in alcuni casi il compilatore potrebbe decidere che è più efficiente non incorporare la funzione e in questi casi si vuole che la convenzione di chiamata migliore sia possibile per ogni piattaforma.

 

## <a name="graphics-library-type-equivalence"></a>Equivalenza del tipo di libreria grafica

Per supportare l'uso della libreria DirectXMath, molti tipi e strutture di libreria DirectXMath sono equivalenti alle implementazioni di Windows dei tipi **D3DDECLTYPE** e **D3DFORMAT** , nonché ai tipi di [**\_ formato DXGI**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) . 

| DirectXMath                      | D3DDECLTYPE                                                                           | D3DFORMAT                                                     | \_formato DXGI                                                                                                                                                                                            |
|----------------------------------|---------------------------------------------------------------------------------------|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2)       |                                                                                       |                                                               | \_Formato DXGI \_ R8G8 \_ Sint                                                                                                                                                                                |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4)       | D3DDECLTYPE \_ BYTE4 (solo Xbox)                                                        | \_X8X8X8X8 D3DFMT                                              | \_Formato DXGI \_ x8x8x8x8 \_ Sint                                                                                                                                                                            |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2)     |                                                                                       | \_V8U8 D3DFMT                                                  | DXGI \_ Format \_ R8G8 \_ russar                                                                                                                                                                               |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4)     | D3DDECLTYPE \_ BYTE4N (solo Xbox)                                                       | \_X8X8X8X8 D3DFMT                                              | DXGI \_ Format \_ x8x8x8x8 \_ russar                                                                                                                                                                           |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor)       | \_D3DCOLOR D3DDECLTYPE                                                                 | \_A8R8G8B8 D3DFMT                                              | \_Formato DXGI \_ B8G8R8A8 \_ UNORM (DXGI 1.1 +)                                                                                                                                                               |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4)         | D3DDECLTYPE \_ DEC4 (solo Xbox)                                                         | D3DDECLTYPE \_ DEC3 (solo Xbox)                                 |                                                                                                                                                                                                         |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4)       | D3DDECLTYPE \_ DEC4N (solo Xbox)                                                        | D3DDECLTYPE \_ DEC3N (solo Xbox)                                |                                                                                                                                                                                                         |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2)     | \_FLOAT2 D3DDECLTYPE                                                                   | \_G32R32F D3DFMT                                               | \_Formato DXGI \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85))   | \_FLOAT2 D3DDECLTYPE                                                                   | \_G32R32F D3DFMT                                               | \_Formato DXGI \_ R32G32 \_ float                                                                                                                                                                             |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3)     | \_FLOAT3 D3DDECLTYPE                                                                   |                                                               | \_Formato DXGI \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a)   | \_FLOAT3 D3DDECLTYPE                                                                   |                                                               | \_Formato DXGI \_ R32G32B32 \_ float                                                                                                                                                                          |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) |                                                                                       |                                                               | \_Formato DXGI \_ R11G11B10 \_ float                                                                                                                                                                          |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) |                                                                                       |                                                               | \_Formato DXGI \_ R9G9B9E5 \_ SHAREDEXP                                                                                                                                                                       |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4)     | \_Float4 D3DDECLTYPE                                                                   | \_A32B32G32R32F D3DFMT                                         | \_Formato DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a)   | \_Float4 D3DDECLTYPE                                                                   | \_A32B32G32R32F D3DFMT                                         | \_Formato DXGI \_ R32G32B32A32 \_ float                                                                                                                                                                       |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2)       | D3DDECLTYPE \_ FLOAT16 \_ 2                                                               | \_G16R16F D3DFMT                                               | \_Formato DXGI \_ R16G16 \_ float                                                                                                                                                                             |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4)       | D3DDECLTYPE \_ FLOAT16 \_ 4                                                               | \_A16B16G16R16F D3DFMT                                         | \_Formato DXGI \_ R16G16B16A16 \_ float                                                                                                                                                                       |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2)         |                                                                                       |                                                               | \_Formato DXGI \_ R32G32 \_ Sint                                                                                                                                                                              |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3)         |                                                                                       |                                                               | \_Formato DXGI \_ R32G32B32 \_ Sint                                                                                                                                                                           |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4)         |                                                                                       |                                                               | \_Formato DXGI \_ R32G32B32A32 \_ Sint                                                                                                                                                                        |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2)     | \_SHORT2 D3DDECLTYPE                                                                   | \_V16U16 D3DFMT                                                | \_Formato DXGI \_ R16G16 \_ Sint                                                                                                                                                                              |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2)   | \_SHORT2N D3DDECLTYPE                                                                  | \_V16U16 D3DFMT                                                | DXGI \_ Format \_ R16G16 \_ russar                                                                                                                                                                             |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4)     | \_SHORT4 D3DDECLTYPE                                                                   | \_X16X16X16X16 D3DFMT                                          | \_Formato DXGI \_ R16G16B16A16 \_ Sint                                                                                                                                                                        |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4)   | \_SHORT4N D3DDECLTYPE                                                                  | \_X16X16X16X16 D3DFMT                                          | DXGI \_ Format \_ R16G16B16A16 \_ russar                                                                                                                                                                       |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2)     |                                                                                       |                                                               | \_Formato DXGI \_ R8G8 \_ uint                                                                                                                                                                                |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2)   |                                                                                       | D3DFMT \_ A8P8, D3DFMT \_ A8L8                                    | \_Formato DXGI \_ R8G8 \_ UNORM                                                                                                                                                                               |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2)       |                                                                                       |                                                               | \_Formato DXGI \_ R32G32 \_ uint                                                                                                                                                                              |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3)       |                                                                                       |                                                               | \_Formato DXGI \_ R32G32B32 \_ uint                                                                                                                                                                           |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4)       |                                                                                       |                                                               | \_Formato DXGI \_ R32G32B32A32 \_ uint                                                                                                                                                                        |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555)         |                                                                                       | D3DFMT \_ X1R5G5B5, D3DFMT \_ A1R5G5B5                            | \_Formato DXGI \_ B5G5R5A1 \_ UNORM                                                                                                                                                                           |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565)         |                                                                                       | \_R5G6B5 D3DFMT                                                | \_Formato DXGI \_ B5G6R5 \_ UNORM                                                                                                                                                                             |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4)     | \_UBYTE4 D3DDECLTYPE                                                                   | \_X8X8X8X8 D3DFMT                                              | \_Formato DXGI \_ x8x8x8x8 \_ uint                                                                                                                                                                            |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4)   | \_Dati UBYTE4N D3DDECLTYPE                                                                  | \_X8X8X8X8 D3DFMT                                              | \_Formato DXGI \_ x8x8x8x8 \_ UNORM<br/> DXGI \_ Format \_ R10G10B10 \_ XR \_ Bias \_ a2 \_ UNORM (usare [**XMLoadUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmloadudecn4_xr) e [**XMStoreUDecN4 \_ XR**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmstoreudecn4_xr)).<br/> |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4)       | D3DDECLTYPE \_ UDEC4 (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3 (solo Xbox)<br/>   | \_A2R10G10B10 D3DFMT<br/> \_A2B10G10R10 D3DFMT<br/> | \_Formato DXGI \_ R10G10B10A2 \_ uint                                                                                                                                                                         |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4)     | D3DDECLTYPE \_ UDEC4N (solo Xbox)<br/> D3DDECLTYPE \_ UDEC3N (solo Xbox)<br/> | \_A2R10G10B10 D3DFMT<br/> \_A2B10G10R10 D3DFMT<br/> | \_Formato DXGI \_ R10G10B10A2 \_ UNORM                                                                                                                                                                        |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) |                                                                                       | D3DFMT \_ A4R4G4B4, D3DFMT \_ X4R4G4B4                            | \_Formato DXGI \_ B4G4R4A4 \_ UNORM (DXGI 1.2 +)                                                                                                                                                               |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2)   | \_USHORT2 D3DDECLTYPE                                                                  | \_G16R16 D3DFMT                                                | \_Formato DXGI \_ R16G16 \_ uint                                                                                                                                                                              |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | \_USHORT2N D3DDECLTYPE                                                                 | \_G16R16 D3DFMT                                                | \_Formato DXGI \_ R16G16 \_ UNORM                                                                                                                                                                             |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4)   | D3DDECLTYPE \_ USHORT4 (solo Xbox)                                                      | \_X16X16X16X16 D3DFMT                                          | \_Formato DXGI \_ R16G16B16A16 \_ uint                                                                                                                                                                        |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | \_USHORT4N D3DDECLTYPE                                                                 | \_X16X16X16X16 D3DFMT                                          | \_Formato DXGI \_ R16G16B16A16 \_ UNORM                                                                                                                                                                       |



 

## <a name="global-constants-in-the-directxmath-library"></a>Costanti globali nella libreria DirectXMath

Per ridurre le dimensioni del segmento di dati, la libreria DirectXMath usa la macro [XMGLOBALCONST](xmglobalconst.md) per usare una serie di costanti interne globali nell'implementazione. Per convenzione, tali costanti globali interne sono precedute da **g \_ XM**. In genere, sono uno dei tipi seguenti: [**XMVECTORU32**](xmvectoru32-data-type.md), [**XMVECTORF32**](xmvectorf32-data-type.md)o **XMVECTORI32**.

Queste costanti globali interne sono soggette a modifiche nelle revisioni future della libreria DirectXMath. Usare funzioni pubbliche che incapsulano le costanti quando possibile anziché usare direttamente i valori globali **g \_ XM** . Puoi anche dichiarare le tue costanti globali usando [XMGLOBALCONST](xmglobalconst.md).

## <a name="windows-sse-versus-sse2"></a>Windows SSE rispetto a SSE2

Il set di istruzioni SSE fornisce supporto solo per vettori a virgola mobile a precisione singola. DirectXMath deve usare il set di istruzioni SSE2 per fornire supporto per vettori di tipo Integer. SSE2 è supportato da tutti i processori Intel, dall'introduzione del Pentium 4, di tutti i processori AMD K8 e versioni successive e di tutti i processori compatibili con x64.

> [!Note]  
> Windows 8 per x86 richiede il supporto per SSE2. Tutte le versioni di Windows x64 richiedono il supporto per SSE2. Windows RT (noto anche come Windows on ARM) richiede il \_ neon ARM.

 

## <a name="routine-variants"></a>Varianti di routine

Sono disponibili diverse varianti di funzioni DirectXMath che semplificano il lavoro:

-   Funzioni di confronto per creare diramazioni condizionali complesse in base a un numero minore di operazioni di confronto vettoriale. Il nome di queste funzioni termina con "R", ad esempio XMVector3InBoundsR. Le funzioni restituiscono un record di confronto come valore restituito UINT o come parametro UINT out. È possibile usare le macro ** \* XMComparision* _ per testare il valore.
-   Funzioni batch per l'esecuzione di operazioni di tipo batch su matrici di vettori di dimensioni maggiori. Il nome di queste funzioni termina in "Stream", ad esempio [_ *XMVector3TransformStream* *](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream). Le funzioni operano su una matrice di input e generano una matrice di output. In genere, accettano uno stride di input e output.
-   Funzioni di stima che implementano una stima più veloce anziché un risultato più lento e accurato. Il nome di queste funzioni termina in "est", ad esempio [**XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest). La qualità e l'effetto sulle prestazioni dell'uso della stima variano a seconda della piattaforma, ma è consigliabile usare varianti di stima per il codice con distinzione delle prestazioni.

## <a name="platform-inconsistencies"></a>Incoerenze della piattaforma

La libreria DirectXMath è destinata all'uso in applicazioni e giochi grafici sensibili alle prestazioni. Pertanto, l'implementazione è progettata per ottimizzare la velocità di elaborazione normale su tutte le piattaforme supportate. I risultati in base alle condizioni limite, in particolare quelli che generano speciali a virgola mobile, possono variare da destinazione a destinazione. Questo comportamento dipenderà anche da altre impostazioni della fase di esecuzione, ad esempio la parola di controllo x87 per la destinazione No-intrinseci Windows a 32 bit o la parola di controllo SSE sia per Windows 32 bit che per 64 bit. Inoltre, vi saranno differenze tra le condizioni limite tra diversi fornitori di CPU.

Non usare DirectXMath in applicazioni scientifiche o in altre applicazioni in cui l'accuratezza numerica è fondamentale. Questa limitazione, inoltre, si riflette sulla mancanza di supporto per i calcoli Double o altri calcoli con precisione estesa.

> [!Note]  
> \_ \_ \_ \_ In genere, i percorsi di codice scalari XM no Intrinsics vengono scritti per verificarne la conformità, non le prestazioni. I risultati delle condizioni limite variano anche.

 

## <a name="platform-specific-extensions"></a>Estensioni specifiche della piattaforma

La libreria DirectXMath ha lo scopo di semplificare la programmazione SIMD C++ offrendo un supporto eccellente per le piattaforme x86, x64 e Windows RT usando le istruzioni intrinseche supportate a grandi linee (SSE2 e ARM-NEON).

In alcuni casi, tuttavia, le istruzioni specifiche della piattaforma possono risultare utili. A causa della modalità di implementazione di DirectXMath, in molti casi è semplice utilizzare i tipi DirectXMath direttamente nelle istruzioni standard intrinseche supportate dal compilatore e utilizzare DirectXMath come percorso di fallback per le piattaforme che non supportano l'istruzione estesa.

Ad esempio, di seguito è riportato un esempio semplificato di utilizzo dell'istruzione SSE 4,1 dot-product. Si noti che è necessario proteggere in modo esplicito il percorso del codice per evitare la generazione di eccezioni di istruzione non valide in fase di esecuzione. Assicurarsi che i percorsi del codice eseguano un lavoro abbastanza significativo per giustificare il costo aggiuntivo della diramazione, la complessità della gestione di più percorsi di codice e così via.


```
#include <windows.h>
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
   __cpuid( CPUInfo, 0 );

   if ( CPUInfo[0] >= 1 )
   {
       __cpuid(CPUInfo, 1 );
 
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



Per ulteriori informazioni sulle estensioni specifiche della piattaforma, vedere:

<dl>

[DirectXMath: SSE, SSE2 e ARM-NEON](https://walbourn.github.io/directxmath-sse-sse2-and-arm-neon/)  
[DirectXMath: SSE3 e SSSE3](https://walbourn.github.io/directxmath-sse3-and-ssse3/)  
[DirectXMath: SSE 4.1 e SSE 4.2](https://walbourn.github.io/directxmath-sse4-1-and-sse4-2/)  
[DirectXMath: AVX](https://walbourn.github.io/directxmath-avx/)  
[DirectXMath: F16C e FMA](https://walbourn.github.io/directxmath-f16c-and-fma/)  
[DirectXMath: AVX2](https://walbourn.github.io/directxmath-avx2/)  
[DirectXMath: ARM64](https://walbourn.github.io/directxmath-arm64/)  
</dl>

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
