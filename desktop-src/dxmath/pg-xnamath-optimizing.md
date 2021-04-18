---
description: In questo argomento vengono descritte le strategie e le considerazioni sull'ottimizzazione con la libreria DirectXMath.
ms.assetid: bcbf8ae1-ed49-fdf7-812d-b2089537ab28
title: Ottimizzazione del codice con la libreria DirectXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d11b331077e3d6538952a2f7956641b8b3919e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309245"
---
# <a name="code-optimization-with-the-directxmath-library"></a>Ottimizzazione del codice con la libreria DirectXMath

In questo argomento vengono descritte le strategie e le considerazioni sull'ottimizzazione con la libreria DirectXMath.

-   [Usare le funzioni di accesso sporadicamente](#use-accessors-sparingly)
-   [Usa impostazioni di compilazione corrette](#use-correct-compilation-settings)
-   [Usare le funzioni est quando appropriato](#use-est-functions-when-appropriate)
-   [Usare i tipi di dati e le operazioni allineati](#use-aligned-data-types-and-operations)
-   [Allinea correttamente le allocazioni](#properly-align-allocations)
-   [Evitare gli overload degli operatori quando possibile](#avoid-operator-overloads-when-possible)
-   [Valori denormalizzati](#denormals)
-   [Sfruttare i vantaggi della dualità a virgola mobile Integer](#take-advantage-of-the-integer-floating-point-duality)
-   [Preferisci moduli modello](#prefer-template-forms)
-   [Uso di DirectXMath con Direct3D](#using-directxmath-with-direct3d)
-   [Argomenti correlati](#related-topics)

## <a name="use-accessors-sparingly"></a>Usare le funzioni di accesso sporadicamente

Le operazioni basate su vettori usano i set di istruzioni SIMD e usano registri speciali. Per accedere ai singoli componenti è necessario eseguire il passaggio dai registri SIMD a quelli scalari e viceversa.

Quando possibile, è più efficiente inizializzare tutti i componenti di un [**XMVECTOR**](xmvector-data-type.md) in una sola volta, anziché usare una serie di singole funzioni di accesso vettoriale.

## <a name="use-correct-compilation-settings"></a>Usa impostazioni di compilazione corrette

Per le destinazioni Windows x86, abilitare/Arch: SSE2. Per tutte le destinazioni di Windows, abilitare/FP: Fast.

Per impostazione predefinita, la compilazione rispetto alla libreria DirectXMath per le destinazioni di Windows x86 viene eseguita con gli \_ \_ \_ intrinseci SSE XM \_ definiti. Ciò significa che tutte le funzionalità di DirectXMath utilizzeranno le istruzioni SSE2. Tuttavia, lo stesso non è vero per altro codice.

Il codice esterno a DirectXMath viene gestito usando le impostazioni predefinite del compilatore. Senza questa opzione, il codice generato potrebbe spesso utilizzare il codice x87 meno efficiente.

È consigliabile usare sempre la versione più recente disponibile del compilatore.

## <a name="use-est-functions-when-appropriate"></a>Usare le funzioni est quando appropriato

Molte funzioni hanno una funzione di stima equivalente che termina in est. Queste funzioni comportano una certa accuratezza per migliorare le prestazioni. Le funzioni est sono appropriate per calcoli non critici in cui l'accuratezza può essere sacrificata per la velocità. L'esatta quantità di perdita di precisione e aumento della velocità è dipendente dalla piattaforma.

Ad esempio, è possibile usare la funzione [**XMVector3AngleBetweenNormalsEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormalsest) al posto della funzione [**XMVector3AngleBetweenNormals**](/windows/win32/api/directxmath/nf-directxmath-xmvector3anglebetweennormals) .

## <a name="use-aligned-data-types-and-operations"></a>Usare i tipi di dati e le operazioni allineati

I set di istruzioni SIMD nelle versioni di Windows che supportano SSE2 hanno in genere versioni allineate e non allineate delle operazioni di memoria. L'uso delle operazioni allineate è più veloce e dovrebbe essere preferito laddove possibile.

La libreria DirectXMath fornisce funzionalità di accesso allineate e non allineate tramite tipi di vettore, struttura e funzioni varianti. Queste varianti sono indicate da "A" alla fine del nome.

Esistono, ad esempio, una struttura [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) non allineata e una struttura [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) allineata, che vengono usate rispettivamente dalle funzioni [**XMStoreFloat4**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4) e [**XMStoreFloat4A**](/windows/win32/api/directxmath/nf-directxmath-xmstorefloat4a) .

## <a name="properly-align-allocations"></a>Allinea correttamente le allocazioni

Le versioni allineate degli intrinseci [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) sottostanti la libreria DirectXMath sono più veloci di quelle non allineate.

Per questo motivo, le operazioni DirectXMath che usano gli oggetti [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) presuppongono che tali oggetti siano allineati a 16 byte. Questo è automatico per le allocazioni basate su stack, se il codice viene compilato con la libreria DirectXMath usando le finestre consigliate (vedere [usare le impostazioni di compilazione corrette](#use-correct-compilation-settings)) del compilatore. Tuttavia, è importante assicurarsi che l'allocazione dell'heap contenente oggetti **XMVECTOR** e **XMMATRIX** o cast a questi tipi soddisfi questi requisiti di allineamento.

Mentre le allocazioni di memoria di Windows a 64 bit sono allineate a 16 byte, per impostazione predefinita nelle versioni a 32 bit della memoria di Windows allocata è allineato solo a 8 byte. Per informazioni sul controllo dell'allineamento della memoria, vedere [ \_ \_ malloc allineato](https://msdn.microsoft.com/library/8z34s9c6(VS.80).aspx).

Quando si usano tipi DirectXMath allineati con la libreria STL (Standard Template Library), è necessario fornire un allocatore personalizzato che garantisca l'allineamento a 16 byte. Vedere il [Blog](https://devblogs.microsoft.com/cppblog/the-mallocator/) del Team di Visual C++ per un esempio di scrittura di un allocatore personalizzato (anziché malloc/free è necessario usare \_ malloc allineato \_ e \_ allineato \_ libero nell'implementazione).

> [!Note]  
> Alcuni modelli STL modificano l'allineamento del tipo specificato. Ad esempio, [make \_ Shared<>](/cpp/standard-library/memory-functions?view=vs-2017&preserve-view=true) aggiunge alcune informazioni di rilevamento interne che possono o meno rispettare l'allineamento del tipo di utente specificato, ottenendo i membri dati non allineati. In questo caso, è necessario utilizzare tipi non allineati anziché tipi allineati. Se si derivano da classi esistenti, inclusi molti Windows Runtime oggetti, è anche possibile modificare l'allineamento di una classe o di una struttura.

 

## <a name="avoid-operator-overloads-when-possible"></a>Evitare gli overload degli operatori quando possibile

Per praticità, molti tipi, ad esempio [**XMVECTOR**](xmvector-data-type.md) e [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) , hanno overload di operatori per operazioni aritmetiche comuni. Questi overload degli operatori tendono a creare numerosi oggetti temporanei. Si consiglia di evitare questi overload degli operatori nel codice sensibile alle prestazioni.

## <a name="denormals"></a>Valori denormalizzati

Per supportare i calcoli vicino a 0, lo standard a virgola mobile IEEE 754 include il supporto per l'underflow graduale. Il underflow graduale viene implementato tramite l'uso di valori denormalizzati e molte implementazioni hardware sono lente quando si gestiscono le denormali. Un'ottimizzazione da considerare è la disabilitazione della gestione delle denormalizzazioni per le operazioni vettoriali utilizzate da DirectXMath.

La modifica della gestione delle denormalità viene eseguita utilizzando la routine [ \_ controlfp \_ s](/cpp/c-runtime-library/reference/controlfp-s) in base a un thread preliminare e può causare miglioramenti delle prestazioni. Usare questo codice per modificare la gestione delle denormalità:


```
  #include <float.h>;
    unsigned int control_word;
    _controlfp_s( &control_word, _DN_FLUSH, _MCW_DN );
```



> [!Note]  
> Nelle versioni di Windows a 64 bit, le istruzioni [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)) vengono usate per tutti i calcoli, non solo per le operazioni vettoriali. La modifica della gestione denormalizzata influiscono su tutti i calcoli a virgola mobile nel programma, non solo sulle operazioni vettoriali utilizzate da DirectXMath.

 

## <a name="take-advantage-of-the-integer-floating-point-duality"></a>Sfruttare i vantaggi della dualità a virgola mobile Integer

DirectXMath supporta i vettori di 4 valori a virgola mobile a precisione singola o a 4 32 bit (con segno o senza segno).

Poiché i set di istruzioni usati per implementare la libreria DirectXMath sono in grado di trattare gli stessi dati di più tipi diversi, ad esempio per trattare lo stesso vettore dei dati a virgola mobile e interi, è possibile ottenere determinate ottimizzazioni. È possibile ottenere queste ottimizzazioni usando le routine di inizializzazione dei vettori di tipo integer e gli operatori bit per modificare i valori a virgola mobile.

Il formato binario dei numeri a virgola mobile e precisione singola usati dalla libreria DirectXMath è completamente conforme allo standard IEEE 764:

``` syntax
     SIGN    EXPONENT   MANTISSA
     X       XXXXXXXX   XXXXXXXXXXXXXXXXXXXXXXX
     1 bit   8 bits     23 bits
```

Quando si usa il numero a virgola mobile a precisione singola IEEE 764, è importante tenere presente che alcune rappresentazioni hanno un significato speciale (ovvero, non sono conformi alla descrizione precedente). Alcuni esempi:

-   Zero positivo è 0
-   Zero negativo è 0x80000000
-   Q \_ NaN è 07FC0000
-   + INF è 0x7F800000
-   -INF è 0xFF800000

## <a name="prefer-template-forms"></a>Preferisci moduli modello

Il modulo del modello esiste per [**XMVectorSwizzle**](/windows/win32/api/directxmath/nf-directxmath-xmvectorswizzle), [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute), [**XMVectorInsert**](/windows/win32/api/directxmath/nf-directxmath-xmvectorinsert), [**XMVectorShiftLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorshiftleft), [**XMVectorRotateLeft**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateleft)e [**XMVectorRotateRight**](/windows/win32/api/directxmath/nf-directxmath-xmvectorrotateright). L'uso di queste funzioni anziché del modulo della funzione generale consente al compilatore di creare molto più implementazioni di efficiente. Per la crittografia [SSE](/previous-versions/visualstudio/visual-studio-2010/t467de55(v=vs.100)), questo spesso comprime \_ \_ i valori PS shuffle a uno o due mm \_ . Per ARM-NEON, il modello **XMVectorSwizzle** può usare una serie di casi speciali invece di VTBL swizzle/permute più generali.

## <a name="using-directxmath-with-direct3d"></a>Uso di DirectXMath con Direct3D

Un uso comune di DirectXMath consiste nell'eseguire calcoli grafici da usare con Direct3D. Con Direct3D 10. x e Direct3D 11. x, è possibile usare la libreria DirectXMath in questi modi diretti:

-   Usare le [costanti](ovw-xnamath-reference-constants.md) dello spazio dei nomi Colors direttamente nel parametro *ColorRGBA* in una chiamata al metodo [**sul ID3D11DeviceContext:: ClearRenderTargetView**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-clearrendertargetview) o [**ID3D10Device:: ClearRenderTargetView**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-clearrendertargetview) . Per Direct3D 9 è necessario eseguire la conversione al tipo [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) per utilizzarlo come parametro *color* in una chiamata al metodo [**IDirect3DDevice9:: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) .
-   Usare i tipi [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) / [**XMVECTOR**](xmvector-data-type.md) e [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) per configurare le strutture di buffer costanti per il riferimento in base ai tipi [**HLSL float4**](../direct3dhlsl/dx-graphics-hlsl-scalar.md) o [**Matrix**](../direct3dhlsl/dx-graphics-hlsl-matrix.md)/float4x4.
    > [!Note]  
    > [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) / I tipi di [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) sono nel formato principale di riga. Se pertanto si usa l'opzione del compilatore/ZPR (il flag di compilazione [**\_ principale della colonna della \_ matrice \_ \_ D3DCOMPILE Pack**](../direct3dhlsl/d3dcompile-constants.md) ) o si omette la \_ [parola chiave](../direct3dhlsl/dx-graphics-hlsl-appendix-keywords.md) Major della riga quando si dichiara il tipo di matrice in HLSL, è necessario trasformarla quando si imposta il buffer costante.

     

-   Con Direct3D 10. x e Direct3D 11. x, è possibile presupporre che il puntatore restituito dal metodo map (ad esempio, [**sul ID3D11DeviceContext:: Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)) nel membro **pData** ([**D3D10 \_ mappato \_ TEXTURE2D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture2d).**pData**, [**D3D10 \_ mappato \_ TEXTURE3D**](/windows/win32/api/d3d10/ns-d3d10-d3d10_mapped_texture3d).**pData** o [**\_ \_ sottorisorsa mappata d3d11**](/windows/win32/api/d3d11/ns-d3d11-d3d11_mapped_subresource).**pData**) è allineato a 16 byte se si utilizza il [livello di funzionalità](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ 0 o superiore oppure quando si utilizzano risorse di [**\_ \_ gestione temporanea utilizzo d3d11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_usage) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida alla programmazione di DirectXMath](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
