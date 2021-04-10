---
title: Introduzione (DirectXMath)
description: La libreria DirectXMath implementa un'interfaccia ottimale e portatile per operazioni aritmetiche e di algebra lineare su vettori a virgola mobile a precisione singola (2D, 3D e 4D) o matrici (3 × 3 e 4 × 4).
ms.assetid: 9972e382-7a0f-88a7-ad44-18521af3520d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e599acfc498e28b33acfc5bbbba2bea5669d2a
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/10/2021
ms.locfileid: "104351021"
---
# <a name="getting-started-directxmath"></a>Introduzione (DirectXMath)

La libreria DirectXMath implementa un'interfaccia ottimale e portatile per operazioni aritmetiche e di algebra lineare su vettori a virgola mobile a precisione singola (2D, 3D e 4D) o matrici (3 × 3 e 4 × 4). La libreria ha un supporto limitato per le operazioni di vettori di tipo Integer. Queste operazioni vengono ampiamente utilizzate nel rendering e nell'animazione da programmi di grafica. Non è disponibile alcun supporto per i vettori a precisione doppia (compresi Long, short o byte) e solo le operazioni di vettori di tipo Integer limitate.

La libreria è disponibile in un'ampia gamma di piattaforme Windows. Poiché la libreria fornisce funzionalità non disponibili in precedenza, questa versione sostituisce le librerie seguenti:

-   Xbox Math Library fornita dall'intestazione Xboxmath. h
-   Libreria D3DX 9 fornita dalle DLL D3DX 9
-   Libreria matematica D3DX 10 fornita tramite le dll D3DX 10
-   XNA Math Library fornita dall'intestazione XNAMath. h in DirectX SDK e Xbox 360 XDK

In queste sezioni vengono illustrate le nozioni di base per iniziare.

-   [Scaricare](#download)
-   [Requisiti di sistema in fase di esecuzione](#run-time-system-requirements)
-   [Panoramica sulla progettazione](#design-overview)
-   [Convenzione matrice](#matrix-convention)
-   [Utilizzo di base](#basic-usage)
-   [Linee guida sull'utilizzo del tipo](#type-usage-guidelines)
-   [Creazione di vettori](#creating-vectors)
    -   [VETTORI COSTANTI](#constant-vectors)
    -   [VETTORI DA VARIABILI](#vectors-from-variables)
    -   [VETTORI DA VETTORI](#vectors-from-vectors)
    -   [VETTORI DALLA MEMORIA](#vectors-from-memory)
-   [Estrazione di componenti da vettori](#extracting-components-from-vectors)
-   [Argomenti correlati](#related-topics)

## <a name="download"></a>Scarica

La libreria DirectXMath è inclusa nella Windows SDK. In alternativa, è possibile scaricarlo da [GitHub/Microsoft/DirectXMath](https://github.com/Microsoft/DirectXMath). Questo sito contiene anche progetti di esempio correlati.

## <a name="run-time-system-requirements"></a>Requisiti di sistema Run-Time

La libreria DirectXMath usa istruzioni del processore specializzate per le operazioni vettoriali quando sono disponibili. Per evitare che un programma generi errori di "eccezione di istruzione sconosciuta", controllare il supporto del processore chiamando [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport) prima di usare la libreria DirectXMath.

Questi sono i requisiti di base per il supporto di run-time della libreria DirectXMath:

-   Per la compilazione predefinita in una piattaforma Windows (x86/x64) è necessario il supporto delle istruzioni SSE/SSE2.
-   Il valore predefinito di Compliation in una piattaforma Windows RT richiede il supporto dell'istruzione ARM-NEON.
-   Per la compilazione con [**\_ XM \_ nessun \_ intrinseco \_**](ovw-xnamath-reference-directives.md) definito è necessario solo il supporto per operazioni a virgola mobile standard.

> [!Note]  
> Quando si chiama [**XMVerifyCPUSupport**](/windows/win32/api/directxmath/nf-directxmath-xmverifycpusupport), includere <Windows. h> prima di includere <DirectXMath. h>. Questa è l'unica funzione della libreria che richiede contenuto da <Windows. h> quindi non è necessario includere <Windows. h> in ogni modulo che usa <DirectXMath. h>.

 

## <a name="design-overview"></a>Panoramica della progettazione

La libreria DirectXMath supporta principalmente il linguaggio di programmazione C++. La libreria viene implementata usando routine inline nei file di intestazione, DirectXMath \* . inl, DirectXPackedVector. inl e DirectXCollision. inl. Questa implementazione si avvale di funzioni intrinseche del compilatore ad alte prestazioni.

La libreria DirectXMath fornisce:

-   Implementazione di che utilizza intrinseci SSE/SSE2.
-   Implementazione senza intrinseci.
-   Implementazione di mediante gli intrinseci ARM-NEON.

Poiché la libreria viene recapitata usando i file di intestazione, usare il codice sorgente per personalizzare e ottimizzare per la propria app.

## <a name="matrix-convention"></a>Convenzione matrice

DirectXMath USA matrici di righe, vettori di righe e pre-moltiplicazione. La manualità è determinata dalla versione della funzione utilizzata (RH rispetto a LH); in caso contrario, la funzione funziona con le coordinate di visualizzazione a sinistra o a destra.

Per riferimento, Direct3D ha usato in passato il sistema di coordinate di sinistra, le matrici di righe, i vettori di riga e la pre-moltiplicazione. La moderna Direct3D non ha un requisito forte per le coordinate Left e Rights e in genere HLSL shaders per impostazione predefinita per l'utilizzo di matrici di colonne principali. Per informazioni dettagliate, vedere [HLSL Matrix ordering](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-per-component-math) .

## <a name="basic-usage"></a>Utilizzo di base

Per utilizzare le funzioni della libreria DirectXMath, includere le intestazioni DirectXMath. h, DirectXPackedVector. h, DirectXColors. h e/o DirectXCollision. h. Le intestazioni si trovano in Windows Software Development Kit per le app di Windows Store.

## <a name="type-usage-guidelines"></a>Linee guida sull'utilizzo del tipo

I tipi [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sono i cavalli di lavoro per la libreria DirectXMath. Ogni operazione utilizza o produce dati di questi tipi. L'uso di questi elementi è fondamentale per l'uso della libreria. Tuttavia, poiché DirectXMath usa i set di istruzioni SIMD, questi tipi di dati sono soggetti a una serie di restrizioni. È fondamentale comprendere queste restrizioni se si desidera utilizzare le funzioni DirectXMath.

Si pensi a [**XMVECTOR**](xmvector-data-type.md) come a un proxy per un registro hardware SIMD e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come proxy per un raggruppamento logico di quattro registri hardware SIMD. Questi tipi sono annotati per indicare che è necessario che l'allineamento a 16 byte funzioni correttamente. Il compilatore li posiziona automaticamente nello stack quando vengono usati come variabile locale o li inserisce nel segmento di dati quando vengono usati come variabile globale. Con le convenzioni appropriate, possono anche essere passate in modo sicuro come parametri a una funzione. per informazioni dettagliate, vedere [convenzioni di chiamata](pg-xnamath-internals.md) .

Le allocazioni dall'heap, tuttavia, sono più complesse. Di conseguenza, è necessario prestare attenzione quando si utilizza [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) come membro di una classe o di una struttura da allocare dall'heap. In Windows x64, tutte le allocazioni di heap sono allineate a 16 byte, ma per Windows x86 sono allineate solo a 8 byte. Sono disponibili opzioni per l'allocazione di strutture dall'heap con allineamento a 16 byte. vedere [allineare correttamente le allocazioni](pg-xnamath-optimizing.md). Per i programmi C++, è possibile usare gli overload di operator new/delete/New \[ \] /Delete \[ \] (globalmente o specifici della classe) per applicare l'allineamento ottimale, se lo si desidera.

> [!Note]  
> Come alternativa all'applicazione dell'allineamento nella classe C++ direttamente tramite l'overload di New/Delete, è possibile usare l' [idioma pimpl](https://en.wikipedia.org/wiki/Opaque_pointer). Se si garantisce che la classe **impl** sia allineata tramite [**\_ \_ malloc**](/cpp/c-runtime-library/reference/aligned-malloc) internamente, è possibile usare liberamente i tipi allineati all'interno dell'implementazione interna. Si tratta di un'opzione utile quando la classe ' Public ' è una Windows Runtime classe di riferimento o è destinata all'uso con [**\_<>PTR std:: Shared**](/cpp/standard-library/shared-ptr-class), che in caso contrario può compromettere un'accurata allineamento.

 

Tuttavia, spesso è più semplice e più compatta evitare l'uso di [**XMVECTOR**](xmvector-data-type.md) o [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) direttamente in una classe o una struttura. In alternativa, usare [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3), [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4), [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3), [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)e così via, come membri della struttura. Inoltre, è possibile usare le funzioni di [archiviazione](ovw-xnamath-reference-functions-storage.md) vettoriale e di [caricamento vettoriale](ovw-xnamath-reference-functions-load.md) per spostare i dati in modo efficiente in variabili locali **XMVECTOR** o **XMMATRIX** , eseguire calcoli e archiviare i risultati. Sono disponibili anche funzioni di streaming ([**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream), [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)e così via) che funzionano in modo efficiente direttamente su matrici di questi tipi di dati.

## <a name="creating-vectors"></a>Creazione di vettori

### <a name="constant-vectors"></a>VETTORI COSTANTI

Molte operazioni richiedono l'uso di costanti nei calcoli vettoriali e esistono diversi modi per caricare un [**XMVECTOR**](xmvector-data-type.md) con i valori desiderati.

-   Se si carica una costante scalare in tutti gli elementi di un [**XMVECTOR**](xmvector-data-type.md), usare [**XMVectorReplicate**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicate) o [**XMVectorReplicateInt**](/windows/win32/api/directxmath/nf-directxmath-xmvectorreplicateint).
    ```
    XMVECTOR vFive = XMVectorReplicate( 5.f );
    ```

    

-   Se si usa una costante Vector con valori fissi diversi come [**XMVECTOR**](xmvector-data-type.md), usare le strutture [**XMVECTORF32**](xmvectorf32-data-type.md), [**XMVECTORU32**](xmvectoru32-data-type.md), **XMVECTORI32** o [**XMVECTORU8**](xmvectoru8-data-type.md) . È possibile fare riferimento a queste informazioni direttamente ovunque si passi un valore **XMVECTOR** .
    ```
    static const XMVECTORF32 vFactors = { 1.0f, 2.0f, 3.0f, 4.0f };
    ```

    

    > [!Note]  
    > Non usare gli elenchi di inizializzatori direttamente con [**XMVECTOR**](xmvector-data-type.md) (ovvero XMVECTOR v = {1.0 f, 2.0 f, 3.0 f, 4.0 f}). Tale codice è inefficiente e non è portabile su tutte le piattaforme supportate da DirectXMath.

     

-   DirectXMath include una serie di costanti globali predefinite che è possibile usare nel codice (g \_ XMOne, g \_ XMOne3, g \_ XMTwo, g \_ XMOneHalf, g \_ XMHalfPi, g \_ XMPi e così via). Eseguire una ricerca nell'intestazione DirectXMath. h per i valori **XMGLOBALCONSTANT** .
-   È disponibile un set di costanti vettoriali per i colori RGB comuni (rosso, verde, blu, giallo e così via). Per altre informazioni su queste costanti vettoriali, vedere DirectXColors. h e lo spazio dei nomi DirectX:: Colors.

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

-   Se si crea un vettore da un altro vettore con un componente specifico impostato su una variabile, è possibile prendere in considerazione l'uso delle [funzioni di accesso vettoriale](ovw-xnamath-reference-functions-accessors.md).
    ```
    XMVECTOR v2 = XMVectorSetW( v1, fw );
    ```

    

-   Se si crea un vettore da un altro vettore con un singolo componente replicato, usare [**XMVectorSplatX**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatx), [**XMVectorSplatY**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplaty), [**XMVectorSplatZ**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatz)e [**XMVectorSplatW**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsplatw).
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
-   Metodi comuni per il caricamento di matrici float sono: [**XMLoadFloat2**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat2), [**XMLoadFloat3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3), [**XMLoadFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4), [**XMLoadFloat3x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat3x3), [**XMLoadFloat4x3**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x3)e [**XMLoadFloat4x4**](/windows/win32/api/directxmath/nf-directxmath-xmloadfloat4x4).
-   DirectXMath include un set completo di tipi, i carichi e gli archivi correlati per la gestione di varie strutture di dati e formati GPU comuni. Vedere [vector Load](ovw-xnamath-reference-functions-load.md) e [vector Store](ovw-xnamath-reference-functions-storage.md).

## <a name="extracting-components-from-vectors"></a>Estrazione di componenti da vettori

L'elaborazione SIMD è più efficiente quando i dati vengono caricati nei registri SIMD ed elaborati completamente prima di estrarre i risultati. La conversione tra forme scalari e vettoriali non è efficiente, quindi è consigliabile eseguirla solo quando è necessario. Per questo motivo, le funzioni nella libreria DirectXMath che producono un valore scalare vengono restituite in un formato vettoriale in cui il risultato scalare viene replicato attraverso il vettore risultante (ovvero [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot), [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length)e così via). Tuttavia, quando sono necessari valori scalari, di seguito sono riportate alcune opzioni su come procedere:

-   Se viene calcolata una singola risposta scalare, l'uso delle [funzioni di accesso Vector](ovw-xnamath-reference-functions-accessors.md) è appropriato:
    ```
    float f = XMVectorGetX( v );
    ```

    

-   Se è necessario estrarre più componenti del vettore, è consigliabile archiviare il vettore in una struttura di memoria e leggerlo di nuovo. Ad esempio:
    ```
    XMFLOAT4A t;
    XMStoreFloat4A( &t, v );
    // t.x, t.y, t.z, and t.w can be individually accessed now
    ```

    

-   Il tipo di elaborazione vettoriale più efficiente consiste nell'usare lo streaming di memoria in memoria dove i dati di input vengono caricati dalla memoria (usando le [funzioni di caricamento del vettore](ovw-xnamath-reference-functions-load.md)), elaborati completamente nel form SIMD e quindi scritti in memoria (usando le funzioni di [Archivio vettoriale](ovw-xnamath-reference-functions-storage.md)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 