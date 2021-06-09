---
description: Questo argomento descrive le considerazioni e le strategie di ottimizzazione con la libreria DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Ottimizzazione del codice con la libreria DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15369ab36e199eb1a204cc4b761dc637f114f2a1
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827255"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Ottimizzazione del codice con la libreria DirectXMath

Questo argomento descrive le considerazioni e le strategie di ottimizzazione con la libreria DirectXMath.

-   [Usare le funzioni di accesso con parsimonio](#use-accessors-sparingly)
-   [Usare le impostazioni di compilazione corrette](#use-correct-compilation-settings)
-   [Usare le funzioni Est quando appropriato](#use-est-functions-when-appropriate)
-   [Usare tipi di dati e operazioni allineati](#use-aligned-data-types-and-operations)
-   [Allineare correttamente le allocazioni](#properly-align-allocations)
-   [Evitare gli overload degli operatori quando possibile](#avoid-operator-overloads-when-possible)
-   [Valori denormalizzati](#denormals)
-   [Sfruttare la dualità a virgola mobile integer](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferisci moduli modello](#prefer-template-forms)
-   [Uso di DirectXMath con Direct3D](#using-directxmath-with-direct3d)
-   [Argomenti correlati](#related-topics)

## <a name="use-accessors-sparingly"></a>Usare le funzioni di accesso con parsimonio

Le operazioni basate su vettori usano i set di istruzioni SIMD e usano registri speciali. L'accesso ai singoli componenti richiede lo spostamento dai registri SIMD a quelli scalari e di nuovo.

Quando possibile, è più efficiente inizializzare tutti i componenti di [**un oggetto XMVECTOR**](xmvector-data-type.md) contemporaneamente, anziché usare una serie di singole funzioni di accesso vettoriali.

## <a name="use-correct-compilation-settings"></a>Usare le impostazioni di compilazione corrette

Per le destinazioni x86 di Windows, abilitare /arch:SSE2. Per tutte le destinazioni di Windows, abilitare /fp:fast.

Per impostazione predefinita, la compilazione nella libreria DirectXMath per le destinazioni x86 di Windows viene eseguita con \_ intrinseci SSE XM \_ \_ \_ definiti. Ciò significa che tutte le funzionalità di DirectXMath useranno le istruzioni SSE2. Tuttavia, lo stesso non vale per altro codice.

Il codice esterno a DirectXMath viene gestito usando le impostazioni predefinite del compilatore. Senza questa opzione, il codice generato può spesso usare il codice x87 meno efficiente.

È consigliabile usare sempre la versione più recente disponibile del compilatore.

## <a name="use-est-functions-when-appropriate"></a>Usare le funzioni Est quando appropriato

Molte funzioni hanno una funzione di stima equivalente che termina in Est. Queste funzioni scambiano una certa accuratezza per migliorare le prestazioni. Le funzioni Est sono appropriate per i calcoli non critici in cui l'accuratezza può essere sacrificata per la velocità. La quantità esatta di accuratezza persa e aumento di velocità dipende dalla piattaforma.

Ad esempio, è possibile usare la funzione [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) al posto della funzione [**XMVector3AngleBetweenNormals.**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals)

## <a name="use-aligned-data-types-and-operations"></a>Usare tipi di dati e operazioni allineati

I set di istruzioni SIMD nelle versioni di Windows che supportano SSE2 hanno in genere versioni allineate e non allineate delle operazioni di memoria. L'uso delle operazioni allineate è più rapido e deve essere preferibile laddove possibile.

La libreria DirectXMath fornisce funzionalità allineate e non allineate di accesso tramite tipi di vettori varianti, struttura e funzioni. Queste varianti sono indicate da una "A" alla fine del nome.

Ad esempio, sono presenti una struttura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) non allineata e una struttura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) allineata, usate rispettivamente dalle funzioni [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) e [**XMStoreFloat4A.**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a)

## <a name="properly-align-allocations"></a>Allineare correttamente le allocazioni

Le versioni allineate degli intrinseci [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) sottostanti la libreria DirectXMath sono più veloci rispetto a quelle non allineate.

Per questo motivo, le operazioni DirectXMath che usano [**oggetti XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) presuppongono che tali oggetti siano allineati a 16 byte. Questa operazione è automatica per le allocazioni basate su stack, se il codice viene compilato nella libreria DirectXMath usando le impostazioni del compilatore consigliate di Windows (vedere Usare le [impostazioni di](#use-correct-compilation-settings)compilazione corrette). Tuttavia, è importante assicurarsi che l'allocazione dell'heap contenente oggetti **XMVECTOR** e **XMMATRIX** o cast a questi tipi soddisfi questi requisiti di allineamento.

Mentre le allocazioni di memoria di Windows a 64 bit sono allineate a 16 byte, per impostazione predefinita nelle versioni a 32 bit della memoria di Windows allocata è allineata solo a 8 byte. Per informazioni sul controllo dell'allineamento della memoria, vedere [ \_ aligned \_ malloc](https://docs.microsoft.com/cpp/c-runtime-library/reference/aligned-malloc).

Quando si usano tipi DirectXMath allineati con la libreria STL (Standard Template Library), è necessario fornire un allocatore personalizzato che garantisca l'allineamento a 16 byte. Per un esempio di scrittura di un allocatore personalizzato, vedere il [blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) del team di Visual C++ (invece di malloc/free è possibile usare malloc allineato e allineato gratuitamente \_ \_ \_ \_ nell'implementazione).

> [!Note]  
> Alcuni modelli STL modificano l'allineamento del tipo specificato. Ad esempio, [creare \_ ](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true)<>aggiunge alcune informazioni di rilevamento interne che possono o meno rispettare l'allineamento del tipo di utente specificato, determinando membri dati non allineati. In questo caso, è necessario usare tipi non allineati anziché tipi allineati. Se si deriva da classi esistenti, inclusi molti Windows Runtime, è anche possibile modificare l'allineamento di una classe o di una struttura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evitare gli overload degli operatori quando possibile

Per praticità, diversi tipi, ad esempio [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX,**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) dispongono di overload dell'operatore per operazioni aritmetiche comuni. Questi overload degli operatori tendono a creare numerosi oggetti temporanei. È consigliabile evitare questi overload degli operatori nel codice sensibile alle prestazioni.

## <a name="denormals"></a>Valori denormalizzati

Per supportare calcoli vicini a 0, lo standard A virgola mobile IEEE 754 include il supporto per un underflow graduale. Il underflow graduale viene implementato tramite l'uso di valori denormalizzati e molte implementazioni hardware sono lente durante la gestione dei denormali. Un'ottimizzazione da considerare è disabilitare la gestione dei denormali per le operazioni vettoriali usate da DirectXMath.

La modifica della gestione dei denormali viene eseguita usando la routine [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) in base al pre-thread e può comportare miglioramenti delle prestazioni. Usare questo codice per modificare la gestione dei denormali:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> Nelle versioni a 64 bit di Windows, le istruzioni [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) vengono usate per tutti i calcoli, non solo per le operazioni vettoriali. La modifica della gestione denormale influisce su tutti i calcoli a virgola mobile nel programma, non solo sulle operazioni vettoriali usate da DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Sfruttare la dualità a virgola mobile integer

DirectXMath supporta vettori di 4 valori a virgola mobile e precisione singola o quattro valori a 32 bit (con o senza segno).

Poiché i set di istruzioni usati per implementare la libreria DirectXMath hanno la possibilità di trattare gli stessi dati di più tipi diversi, ad esempio, è possibile considerare lo stesso vettore come ottimizzazioni di dati a virgola mobile e integer. È possibile ottenere queste ottimizzazioni usando le routine di inizializzazione del vettore integer e gli operatori bit per bit per modificare i valori a virgola mobile.

Il formato binario dei numeri a virgola mobile a precisione singola usati dalla libreria DirectXMath è completamente conforme allo standard IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Quando si utilizza il numero a virgola mobile a precisione singola IEEE 764, è importante tenere presente che alcune rappresentazioni hanno un significato speciale, ovvero non sono conformi alla descrizione precedente. Alcuni esempi:

-   Lo zero positivo è 0
-   Lo zero negativo è 0x80000000
-   Q \_ NAN è 07FC0000
-   +INF è 0x7F800000
-   -INF è 0xFF800000

## <a name="prefer-template-forms"></a>Preferisci moduli modello

Il modulo modello esiste per [**XMVectorSwizzle,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle) [**XMVectorPermute,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) [**XMVectorInsert,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert) [**XMVectorShiftLeft,**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft) [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)e [**XMVectorRotateRight.**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright) L'uso di questi elementi al posto del modulo di funzione generale consente al compilatore di creare implementazioni molto più efficenti. Per [SSE,](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100))questo spesso viene compresso fino a uno o due \_ valori ps \_ \_ casuali. Per ARM-NEON, il modello **XMVectorSwizzle** può usare una serie di casi speciali anziché lo swizzle/permute VTBL più generale.

## <a name="using-directxmath-with-direct3d"></a>Uso di DirectXMath con Direct3D

Un uso comune per DirectXMath è eseguire calcoli grafici da usare con Direct3D. Con Direct3D 10.x e Direct3D 11.x è possibile usare la libreria DirectXMath in questi modi diretti:

-   Usare le [](ovw-xnamath-reference-constants.md) costanti dello spazio dei nomi Colors direttamente nel parametro *ColorRGBA* in una chiamata al metodo [**ID3D11DeviceContext::ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) [**o ID3D10Device::ClearRenderTargetView.**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) Per Direct3D 9, è necessario eseguire la conversione nel tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) per usarlo come parametro *Color* in una chiamata al metodo [**IDirect3DDevice9::Clear.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear)
-   Usare i [**tipi XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) e [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4)XMMATRIX per configurare strutture di buffer costanti per il riferimento da tipi / [](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) [**float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) o matrice /float4x4. [](../direct3dhlsl/dx-graphics-hlsl-matrix.md)
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**I tipi XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sono in formato principale di riga. Pertanto, se si usa l'opzione del compilatore /Zpr (flag di compilazione [**D3DCOMPILE \_ PACK MATRIX COLUMN \_ \_ \_ MAJOR)**](../direct3dhlsl/d3dcompile-constants.md) o si omette la parola chiave row major quando si dichiara il tipo di matrice \_ in HLSL, è necessario trasporre la matrice quando viene impostata nel buffer costante. [](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md)

     

-   Con Direct3D 10.x e Direct3D 11.x, è possibile presupporre che il puntatore restituito dal metodo Map (ad [**esempio, ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) nel membro **pData** ([**D3D10 \_ MAPPED \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d)).**pData**, [**D3D10 \_ MAPPED \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** o [**D3D11 \_ MAPPED \_ SUBRESOURCE**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) è allineato a 16 byte se si usa il livello di funzionalità [10](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 0 o superiore o ogni volta che si usano risorse \_ [**D3D11 \_ USAGE \_ STAGING.**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida per programmatori DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
