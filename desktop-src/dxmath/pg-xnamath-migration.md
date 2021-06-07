---
description: Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente tramite la libreria matematica XNA alla libreria DirectXMath.
ms.assetid: ed8463f8-8a3d-e89e-89e2-8d72a7f45cd6
title: Migrazione del codice dalla libreria matematica XNA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc7a48d30711a870c28b677e458a4f72c3b3c40
ms.sourcegitcommit: b01ad017c152c6756f3638623fe335877644d414
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/06/2021
ms.locfileid: "111549963"
---
# <a name="code-migration-from-the-xna-math-library"></a>Migrazione del codice dalla libreria matematica XNA

Questa panoramica descrive le modifiche necessarie per eseguire la migrazione del codice esistente tramite la libreria matematica XNA alla libreria DirectXMath.

## <a name="header-changes"></a>Modifiche all'intestazione

La libreria DirectXMath usa un nuovo set di intestazioni.

Sostituire `xnamath.h` l'intestazione con `DirectXMath.h` e aggiungere per i tipi di `DirectXPackedVector.h` *GPU.*

I tipi di delimitazione dell'esempio Di collisione di DirectX SDK in fanno ora `xnacollision.h` parte della libreria DirectXMath in `DirectXCollision.h` . Sono stati modificati per usare le classi C++ anziché un'API di tipo C.

## <a name="constant-changes"></a>Modifiche costanti

XNAMATH \_ VERSION (200, 201, 202, 203, 204 e così via) è stato sostituito con DIRECXTMATH \_ VERSION (300, 301, 302, 303 e così via).

> [!NOTE]  
> DirectXMath 3.00 e 3.02 sono disponibili con versioni preliminari del Windows SDK. DirectXMath 3.03 è nella versione finale di Windows 8 SDK.

## <a name="namespaces"></a>Spazi dei nomi

La libreria DirectXMath usa gli spazi dei nomi C++ per organizzare i tipi. XNA Math ha usato solo lo spazio dei nomi globale. I tipi DirectXMath in comune con i calcoli matematici XNA sono nello spazio dei nomi **DirectX** **o DirectX::P ackedVector.**

Nei file di origine C++ una soluzione semplice consiste nell'aggiungere `using` istruzioni .

```cpp
#include "DirectXMath.h"
#include "DirectXPackedVector.h"

using namespace DirectX; 
using namespace DirectX::PackedVector;
```

Per le intestazioni, non è consigliabile aggiungere istruzioni using. Aggiungere invece spazi dei nomi completi.

```
struct mystruct
{
   DirectX::XMFLOAT3 position;
   DirectX::PackedVector::HALF packedValue;
};
```

## <a name="partial-loads"></a>Caricamenti parziali

Per varie funzioni che caricano meno di 4 elementi di un XMVECTOR, la libreria matematica XNA ha lasciato gli elementi aggiuntivi indefiniti. DirectXMath riempirà sempre questi elementi aggiuntivi con 0.

## <a name="removal-of-xbox-360-specific-types"></a>Rimozione di Xbox 360 tipi specifici

I tipi, le funzioni e le costanti della libreria matematica XNA seguenti non sono disponibili in DirectXMath.

-   HENDN3, XMHEND3, XMUHENDN3, XMUHEND3, XMDHENN3, XMDHEN3, XMUDHENN3, XMUDHEN3
-   XMLoadHenDN3(), XMLoadHenD3(), XMLoadUHenDN3(), XMLoadUHenD3(), XMLoadDHenN3(), XMLoadDHen3(), XMLoadUDHenN3(), XMLoadUDHen3()
-   XMStoreHenDN3(), XMStoreHenD3(), XMStoreUHenDN3(), XMStoreUHenD3(), XMStoreDHenN3(), XMStoreDHen3(), XMStoreUDHenN3(), XMStoreUDHen3()
-   g \_ XMMaskHenD3, g \_ XMMaskDHen3, g \_ XMAddUHenD3, g \_ XMAddHenD3, g \_ XMAddDHen, g \_ XMMulHenD3, g \_ XMMulDHen3, g \_ XMXorHenD3, g \_ XMXorDHen3
-   XMXICON4, XMXICO4, XMICON4, XMICO4, XMUICON4, XMUICO4
-   XMLoadXIcoN4(), XMLoadXIco4(), XMLoadIcoN4(), XMLoadIco4(), XMLoadUIcoN4(), XMLoadUIco4()
-   XMStoreXIcoN4(), XMStoreXIco4() ,XMStoreIcoN4(), XMStoreIco4(), XMStoreUIcoN4(), XMStoreUIco4()
-   g \_ XMMaskIco4, g \_ XMXorXIco4, g \_ XMXorIco4, g \_ XMAddXIco4, g \_ XMAddUIco4, g \_ XMAddIco4, g \_ XMMulIco4

\_\_vector4i è deprecato. Usare [**invece XMVECTORI32**](xmvectori32-data-type.md) [**o XMVECTORU32.**](xmvectoru32-data-type.md)

Le funzioni e i tipi seguenti sono deprecati perché sono solo Xbox 360: XMLoadDecN4, XMStoreDecN4, XMDECN4, XMLoadDec4, XMStoreDec4, XMDEC4, XMLoadXDec4, XMStoreXDec4, XMXDEC4.

## <a name="arm-neon-intrinsics"></a>Intrinseci ARM-NEON

La dichiarazione di una costante di vettore con questo codice verrà compilata per XNA Math per SSE e NO-INTRINSICS, ma avrà esito negativo per DirectXMath tramite ARM-NEON.

```
XMVECTOR v = { 1.f, 2.f, 3.f, 4.f }
```

In generale, non è consigliabile usare questo metodo di inizializzazione di [**XMVECTOR.**](xmvector-data-type.md) Tuttavia, se si vuole una costante vettore, la classe [**XMVECTORF32**](xmvectorf32-data-type.md) supporta questo stile di inizializzazione e restituisce automaticamente il tipo **XMVECTOR** in modo da poter usare **XMVECTORF32** nella maggior parte degli stessi contesti. Per qualsiasi operazione di scrittura in **una classe XMVECTORF32** è necessario fare riferimento in modo esplicito al membro **XMVECTOR** .v.

## <a name="permute"></a>Permuta

La libreria matematica XNA aveva il formato seguente per la permuta vettore generale:

```
XMVECTOR XMVectorPermuteControl(UINT ElementIndex0, UINT ElementIndex1, UINT ElementIndex2, UINT ElementIndex3);
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, FXMVECTOR Control);
```

Per DirectXMath, **XMVectorPermuteControl** è stato eliminato e XM \_ PERMUTE \_ 0X . Le costanti \_ XM PERMUTE 1Z sono state ridefinite in modo da \_ essere semplici indici 0-7. Ecco la nuova firma per [**XMVectorPermute:**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)

```
XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2, uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW);
```

Anziché una parola di controllo, questa funzione accetta direttamente i 4 indici come parametri, il che lo rende analogo alla funzione [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) usando il nuovo XM \_ SWIZZLE \_ X . Costanti \_ XM SWIZZLE \_ W definite come indici 0-3 semplici.

```
XMVECTOR XMVectorSwizzle(FXMVECTOR V, uint32_t E0, uint32_t E1, uint32_t E2, uint32_t E3);
```

> [!NOTE]
> Per i valori costanti, esiste un modo molto più efficiente per implementare permute. Invece di usare il formato di funzione [**di XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute)usare il **formato modello:**

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)</code></pre></td>
```

## <a name="template-forms"></a>Moduli modello

In generale, l'uso di un modulo modello su una forma di funzione delle funzioni seguenti è molto più efficiente e consente alla libreria di eseguire ottimizzazioni specifiche della piattaforma tramite la specializzazione dei modelli.

```
template<uint32_t PermuteX, uint32_t PermuteY, uint32_t PermuteZ, uint32_t PermuteW>
    XMVECTOR XMVectorPermute(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t SwizzleX, uint32_t SwizzleY, uint32_t SwizzleZ, uint32_t SwizzleW>
    XMVECTOR XMVectorSwizzle(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorShiftLeft(FXMVECTOR V1, FXMVECTOR V2)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateLeft(FXMVECTOR V)

template<uint32_t Elements>
    XMVECTOR XMVectorRotateRight(FXMVECTOR V)

template<uint32_t VSLeftRotateElements, uint32_t Select0, uint32_t Select1, uint32_t Select2, uint32_t Select3>
    XMVECTOR XMVectorInsert(FXMVECTOR VD, FXMVECTOR VS)</code></pre></td>
```

## <a name="eliminated-functions"></a>Funzioni eliminate

| Funzione eliminata        | Sostituzione                                                                                                       |
|----------------------------|-------------------------------------------------------------------------------------------------------------------|
| XMStoreFloat3x3NC          | [**XMStoreFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat3x3)                                                                        |
| XMStoreFloat4NC            | [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4)                                                                            |
| XMStoreFloat4x3NC          | [**XMStoreFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x3)                                                                        |
| XMStoreFloat4x4NC          | [**XMStoreFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4x4)                                                                        |
| XMStoreInt4NC              | [**XMStoreInt4**](/windows/win32/api/directxmath/nf-directxmath-xmstoreint4)                                                                                |
| XMVector2InBoundsR         | [**XMVector2InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector2inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector2TransformStreamNC | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                      |
| XMVector3InBoundsR         | [**XMVector3InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector3inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVector3TransformStreamNC | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                      |
| XMVector4InBoundsR         | [**XMVector4InBounds**](/windows/win32/api/directxmath/nf-directxmath-xmvector4inbounds) ? [XM \_ CRMASK \_ CR6BOUNDS:](ovw-xnamath-reference-constants.md) 0 |
| XMVectorCosHEst            | [**XMVectorCosH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcosh)                                                                              |
| XMVectorExpEst             | [**XMVectorExp**](/windows/win32/api/directxmath/nf-directxmath-xmvectorexp)                                                                                |
| XMVectorLogEst             | [**XMVectorLog**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlog)                                                                                |
| XMVectorPowEst             | [**XMVectorPow**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpow)                                                                                |
| XMVectorSinHEst            | [**XMVectorSinH**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsinh)                                                                              |
| XMVectorTanHEst            | [**XMVectorTanH**](/windows/win32/api/directxmath/nf-directxmath-xmvectortanh)                                                                              |

## <a name="related-topics"></a>Argomenti correlati

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
