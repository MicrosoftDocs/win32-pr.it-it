---
title: Introduzione (DirectXMath)
description: La libreria DirectXMath implementa un'interfaccia ottimale e portabile per operazioni algebra aritmetiche e lineari su vettori a virgola mobile a precisione singola (2D, 3D e 4D) o matrici (3×3 e 4×4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ad7de99a462dc533d8010c45dfadcb1bcfa1b6f33317a941e91c16f30c3d2c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120117501"
---
# <a name="getting-started-directxmath"></a>Introduzione (DirectXMath)

La libreria DirectXMath implementa un'interfaccia ottimale e portabile per operazioni algebra aritmetiche e lineari su vettori a virgola mobile a precisione singola (2D, 3D e 4D) o matrici (3×3 e 4×4). La libreria ha un supporto limitato per le operazioni su vettori integer. Queste operazioni vengono ampiamente usate nel rendering e nell'animazione dai programmi di grafica. Non è disponibile alcun supporto per i vettori a precisione doppia (inclusi long, short o byte) e solo per operazioni limitate sui vettori integer.

La libreria è disponibile in un'ampia gamma di Windows. Poiché la libreria fornisce funzionalità non disponibili in precedenza, questa versione sostituisce le librerie seguenti:

-   Libreria xbox math fornita dall'intestazione Xboxmath.h
-   Libreria D3DX 9 fornita dalle DLL D3DX 9
-   Libreria matematica D3DX 10 fornita tramite le DLL D3DX 10
-   Libreria matematica XNA fornita dall'intestazione xnamath.h in DirectX SDK e Xbox 360 XDK

Queste sezioni descrivono le nozioni di base per iniziare.

-   [Scaricare](#download)
-   [Requisiti di sistema in fase di esecuzione](#run-time-system-requirements)
-   [Panoramica della progettazione](#design-overview)
-   [Convenzione di matrice](#matrix-convention)
-   [Utilizzo di base](#basic-usage)
-   [Linee guida sull'utilizzo dei tipi](#type-usage-guidelines)
-   [Creazione di vettori](#creating-vectors)
    -   [VETTORI COSTANTI](#constant-vectors)
    -   [VETTORI DA VARIABILI](#vectors-from-variables)
    -   [VETTORI DA VETTORI](#vectors-from-vectors)
    -   [VETTORI DALLA MEMORIA](#vectors-from-memory)
-   [Estrazione di componenti da vettori](#extracting-components-from-vectors)
-   [Argomenti correlati](#related-topics)

## <a name="download"></a>Scarica

La libreria DirectXMath è inclusa in Windows SDK. In alternativa, è possibile scaricarlo [da GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Questo sito contiene anche progetti di esempio correlati.

## <a name="run-time-system-requirements"></a>Run-Time di sistema

La libreria DirectXMath usa istruzioni specifiche del processore per le operazioni vettoriali quando sono disponibili. Per evitare che un programma generi errori di "eccezione di istruzione sconosciuta", verificare il supporto del processore chiamando [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) prima di usare la libreria DirectXMath.

Di seguito sono i requisiti di supporto di base della libreria DirectXMath:

-   La compilazione predefinita in una Windows (x86/x64) richiede il supporto delle istruzioni SSE/SSE2.
-   La compilazione predefinita in una piattaforma Windows RT richiede il supporto per le istruzioni ARM-NEON.
-   La compilazione [**\_ con XM \_ NO \_ INTRINSICS \_**](ovw-xnamath-reference-directives.md) definito richiede solo il supporto delle operazioni a virgola mobile standard.

> [!Note]  
> Quando si chiama [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport), includere <windows.h> prima di includere <DirectXMath.h>. Questa è l'unica funzione nella libreria che richiede qualsiasi contenuto da <windows.h> quindi non è necessario includere <windows.h> in ogni modulo che usa <DirectXMath.h>.

 

## <a name="design-overview"></a>Panoramica della progettazione

La libreria DirectXMath supporta principalmente il linguaggio di programmazione C++. La libreria viene implementata usando routine inline nei file di intestazione, DirectXMath \* .inl, DirectXPackedVector.inl e DirectXCollision.inl. Questa implementazione usa intrinseci del compilatore ad alte prestazioni.

La libreria DirectXMath offre:

-   Implementazione con funzioni intrinseche SSE/SSE2.
-   Implementazione senza intrinseci.
-   Implementazione che usa intrinseci ARM-NEON.

Poiché la libreria viene recapitata usando i file di intestazione, usare il codice sorgente per personalizzare e ottimizzare la propria app.

## <a name="matrix-convention"></a>Convenzione di matrice

DirectXMath usa matrici principali di riga, vettori di riga e pre-moltiplicazione. La mano è determinata dalla versione della funzione usata (RH e LH), in caso contrario la funzione funziona con le coordinate di visualizzazione mancino o destro.

Per riferimento, Direct3D ha usato in passato il sistema di coordinate mancino, le matrici principali di riga, i vettori di riga e la pre-moltiplicazione. Direct3D moderno non ha un requisito sicuro per le coordinate sinistra e destra e in genere gli shader HLSL utilizzano per impostazione predefinita matrici di colonne principali. Per informazioni [dettagliate, vedere Ordinamento delle matrici HLSL.](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math)

## <a name="basic-usage"></a>Utilizzo di base

Per usare le funzioni della libreria DirectXMath, includere le intestazioni DirectXMath.h, DirectXPackedVector.h, DirectXColors.h e/o DirectXCollision.h. Le intestazioni sono disponibili in Windows Software Development Kit per le app Windows Store.

## <a name="type-usage-guidelines"></a>Linee guida sull'utilizzo dei tipi

I [**tipi XMVECTOR**](xmvector-data-type.md) [**e XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sono i cavalli di lavoro per la libreria DirectXMath. Ogni operazione utilizza o produce dati di questi tipi. L'uso di questi elementi è fondamentale per l'uso della libreria. Tuttavia, poiché DirectXMath usa i set di istruzioni SIMD, questi tipi di dati sono soggetti a una serie di restrizioni. È fondamentale comprendere queste restrizioni se si vuole usare in modo utile le funzioni DirectXMath.

È consigliabile pensare a [**XMVECTOR**](xmvector-data-type.md) come a un proxy per un registro hardware SIMD e a [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come un proxy per un raggruppamento logico di quattro registri hardware SIMD. Questi tipi vengono annotati per indicare che è necessario un allineamento a 16 byte per il corretto funzionamento. Il compilatore li inserirà automaticamente nello stack quando vengono usati come variabile locale o li inserirà nel segmento di dati quando vengono usati come variabile globale. Con le convenzioni appropriate, possono anche essere passate in modo sicuro come parametri a una funzione (per informazioni dettagliate, vedere [Convenzioni di](pg-xnamath-internals.md) chiamata).

Le allocazioni dall'heap, tuttavia, sono più complesse. Di conseguenza, è necessario prestare attenzione ogni volta che si usa [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come membro di una classe o di una struttura da allocare dall'heap. In Windows x64, tutte le allocazioni di heap sono allineate a 16 byte, ma per Windows x86, sono allineate solo a 8 byte. Sono disponibili opzioni per l'allocazione di strutture dall'heap con allineamento a 16 byte (vedere [Allineare correttamente le allocazioni](pg-xnamath-optimizing.md)). Per i programmi C++, è possibile usare gli overload dell'operatore new/delete/new /delete (a livello globale o specifico della classe) per applicare l'allineamento \[ \] \[ \] ottimale, se necessario.

> [!Note]  
> In alternativa all'applicazione dell'allineamento nella classe C++ direttamente tramite l'overload di new/delete, è possibile usare [l'idiom pImpl](https://en.wikipedia.org/wiki/Opaque_pointer). Se si garantisce che la **classe Impl** sia allineata internamente tramite [**\_ \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) allineata, è possibile usare liberamente tipi allineati all'interno dell'implementazione interna. Si tratta di un'opzione valida quando la classe "public" è una classe di riferimento del runtime di Windows o destinata all'uso con [**std::shared \_ ptr<>**](/cpp/standard-library/shared-ptr-class), che altrimenti può interrompere l'allineamento attento.

 

Tuttavia, spesso è più semplice e compatto evitare l'uso di [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) direttamente in una classe o struttura. Usare invece [**XMFLOAT3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) [**XMFLOAT4,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) [**XMFLOAT4X3,**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) [**XMFLOAT4X4 e**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)così via come membri della struttura. È anche possibile usare le funzioni [Vector Loading](ovw-xnamath-reference-functions-load.md) e Vector Archiviazione per spostare i dati [in](ovw-xnamath-reference-functions-storage.md) modo efficiente nelle variabili locali **XMVECTOR** o **XMMATRIX,** eseguire calcoli e archiviare i risultati. Esistono anche funzioni di streaming ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)e così via) che operano in modo efficiente direttamente sulle matrici di questi tipi di dati.

## <a name="creating-vectors"></a>Creazione di vettori

### <a name="constant-vectors"></a>VETTORI COSTANTI

Molte operazioni richiedono l'uso di costanti nei calcoli vettoriali e esistono diversi modi per caricare [**un oggetto XMVECTOR**](xmvector-data-type.md) con i valori desiderati.

-   Se si carica una costante scalare in tutti gli elementi di [**un oggetto XMVECTOR,**](xmvector-data-type.md)usare [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) o [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Se si usa una costante vettoriale con valori fissi diversi come [**XMVECTOR,**](xmvector-data-type.md)usare le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** o [**XMVECTORU8.**](xmvectoru8-data-type.md) È quindi possibile farvi riferimento direttamente ovunque si passi un **valore XMVECTOR.**
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > Non usare elenchi di inizializzatori direttamente con [**XMVECTOR**](xmvector-data-type.md) ,ovvero XMVECTOR v = { 1.0f, 2.0f, 3.0f, 4.0f }). Questo codice non è efficiente e non è portabile in tutte le piattaforme supportate da DirectXMath.

     

-   DirectXMath include una serie di costanti globali predefinite che è possibile usare nel codice (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi e così via). Cercare i valori **XMGLOBALCONSTANT nell'intestazione** DirectXMath.h.
-   È presente un set di costanti vettoriali per i colori RGB comuni (rosso, verde, blu, giallo e così via). Per altre informazioni su queste costanti vettoriali, vedere DirectXColors.h e lo spazio dei nomi DirectX::Colors.

### <a name="vectors-from-variables"></a>VETTORI DA VARIABILI

-   Se si crea un vettore da una singola variabile scalare, vedere [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) e [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR v = XMVectorReplicate( f  );
    ```

    

-   Se si crea un vettore da quattro variabili scalari, vedere [**XMVectorSet**](/windows/win32/api/directxmath/nf-directxmath-xmvectorset) e [**XMVectorSetInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsetint).
    ```
    XMVECTOR v = XMVectorSet( fx, fy, fz, fw );
    ```

    

### <a name="vectors-from-vectors"></a>VETTORI DA VETTORI

-   Se si crea un vettore da un altro vettore con un componente specifico impostato su una variabile, è possibile prendere in considerazione l'uso di Funzioni [di accesso vettoriale](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Se si crea un vettore da un altro vettore con un singolo componente replicato, usare [**XMVectorSplatX,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx) [**XMVectorSplatY,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty) [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)e [**XMVectorSplatW.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw)
    ```
    XMVECTOR vz = XMVectorSplatZ( v );
    ```

    

-   Se si crea un vettore da un altro vettore o coppia di vettori con componenti riordinati, vedere [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) e [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute).
    ```
    XMVECTOR v2 = XMVectorSwizzle<XM_SWIZZLE_Z, XM_SWIZZLE_Y, XM_SWIZZLE_W, XM_SWIZZLE_X>( v1 );

    XMVECTOR v3 = XMVectorPermute<XM_PERMUTE_0W, XM_PERMUTE_1X, XM_PERMUTE_0X, XM_PERMUTE_1Z>( v1, v2 );
    ```

    

### <a name="vectors-from-memory"></a>VETTORI DALLA MEMORIA

-   Per il caricamento di un singolo valore float dalla memoria, vedere [**XMVectorReplicatePtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateptr), [**XMVectorReplicateIntPtr**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateintptr), [**XMLoadFloat**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat)e [**XMLoadInt**](/windows/win32/api/directxmath/nf-directxmath-xmloadint).
-   I modi comuni per caricare matrici float sono: [**XMLoadFloat2,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2) [**XMLoadFloat3,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3) [**XMLoadFloat4,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4) [**XMLoadFloat3x3,**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3) [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)e [**XMLoadFloat4x4.**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4)
-   DirectXMath include un set di tipi e carichi e archivi correlati per la gestione di varie strutture di dati e formati GPU comuni. Vedere [Caricamento vettoriale](ovw-xnamath-reference-functions-load.md) e [Archivio vettori](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Estrazione di componenti da vettori

L'elaborazione SIMD è più efficiente quando i dati vengono caricati nei registri SIMD ed elaborati completamente prima di estrarre i risultati. La conversione tra forme scalari e vettoriali è inefficiente, quindi è consigliabile eseguire questa operazione solo quando necessario. Per questo motivo, le funzioni nella libreria DirectXMath che producono un valore scalare vengono restituite in forma di vettore in cui il risultato scalare viene replicato nel vettore risultante, ovvero [**XMVector2Dot,**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot) [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)e così via. Tuttavia, quando sono necessari valori scalari, ecco alcune opzioni su come eseguire questa procedura:

-   Se viene calcolata una singola risposta scalare, l'uso delle funzioni [di accesso vettoriale](ovw-xnamath-reference-functions-accessors.md) è appropriato:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Se è necessario estrarre più componenti del vettore, è consigliabile archiviare il vettore in una struttura di memoria e leggerlo di nuovo. Esempio:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   La forma più efficiente di elaborazione vettoriale è usare lo streaming da memoria a memoria in cui i dati di input vengono caricati dalla memoria (tramite funzioni di caricamento [vettoriale),](ovw-xnamath-reference-functions-load.md)elaborati completamente in formato SIMD e quindi scritti in memoria [(usando](ovw-xnamath-reference-functions-storage.md)funzioni di archivio vettoriali).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 