---
description: Le direttive del compilatore ottimizzano le funzionalità utilizzate dalla libreria DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Direttive del compilatore della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da7419afbab80d35feea135a25f7c5892b137a08
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826776"
---
# <a name="directxmath-library-compiler-directives"></a>Direttive del compilatore della libreria DirectXMath

Le direttive del compilatore ottimizzano le funzionalità utilizzate dalla libreria DirectXMath.



| Direttiva                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ NO \_ INTRINSICS\_        | Quando \_ si specifica \_ XM NO \_ INTRINSICS, le operazioni DirectXMath vengono implementate senza \_ usare intrinseci specifici della piattaforma. DirectXMath usa invece solo operazioni a virgola mobile standard.<br/> Per impostazione predefinita, \_ XM \_ NO \_ INTRINSICS \_ non è definito.<br/> Questa direttiva esegue l'override di tutte le altre direttive . È pertanto consigliabile cercare XM NO INTRINSICS prima di determinare lo stato di \_ \_ \_ \_ \_ XM \_ ARM NEON \_ \_ INTRINSICS o \_ \_ XM \_ SSE \_ INTRINSICS \_ .<br/>                                                                              |
| \_INTRINSECI \_ SSE \_ XM\_       | Quando \_ si definisce XM SSE INTRINSICS, il codice viene compilato per usare il supporto di SSE e SSE2 nelle piattaforme che \_ \_ \_ supportano questi set di istruzioni.<br/> Le versioni di Windows che forniscono intrinseci SSE supportano sia SSE che SSE2.<br/> \_XM \_ SSE INTRINSICS non ha alcun effetto sui sistemi \_ che non \_ supportano SSE e SSE2.<br/> Per impostazione predefinita, \_ XM \_ SSE \_ INTRINSICS viene \_ definito quando gli utenti compilano per una piattaforma Windows.<br/> DirectXMath usa le definisce del compilatore standard ( \_ M \_ IX86/M AMD64) per determinare le destinazioni \_ \_ x86 o Windows x64.<br/> |
| \_INTRINSECI NEON DI XM \_ ARM \_ \_\_ | Indica che l'implementazione DirectXMath usa gli intrinseci ARM-NEON. Per impostazione predefinita, XM ARM NEON INTRINSICS viene definito quando gli utenti compilano \_ per una piattaforma Windows in \_ \_ \_ \_ ARM/ARM64. DirectXMath usa la definizione del compilatore standard ( \_ M \_ ARM, \_ M \_ ARM64) per determinare questa destinazione binaria.<br/> Il supporto degli intrinseci ARM-NEON non è nuovo per DirectXMath e non è supportato da XNAMath 2.x.<br/>                                                                                                                                                                             |
| \_INTRINSECI DI XM \_ SSE3 \_\_      | Novità di DirectXMath 3.10. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare intrinseci SSE3, se applicabile. in caso contrario, usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_FUNZIONI INTRINSECHE DI XM \_ SSE4 \_\_      | Novità di DirectMath 3.09. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare le funzioni intrinseche SSE3 e SSE4.1, se applicabile. in caso contrario, usa SSE/SSE2. Quando si specifica questa direttiva del compilatore, implica \_ anche XM \_ SSE3 \_ INTRINSICS \_ e \_ XM \_ SSE \_ INTRINSICS \_ .<br/>                                                                                                                                                                                                                                |
| \_INTRINSECI \_ AVX \_ XM\_       | Novità di DirectXMath 3.09. <br/> L'uso di /arch:AVX abiliterà questa direttiva. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare intrinseci SSE3, SSE4.1 e AVX a 128 bit, se applicabile; in caso contrario, DirectXMath usa SSE/SSE2. Quando si specifica questa direttiva del compilatore, implica anche \_ \_ XM SSE3 \_ INTRINSICS, \_ XM \_ SSE4 \_ INTRINSICS \_ e XM SSE INTRINSICS \_ e \_ \_ \_ include un piccolo subset di istruzioni SSE3. <br/>                                                                    |
| INTRINSECI \_ AVX2 \_ XM\_        | Novità di DirectXMath 3.11. <br/> L'uso di /arch:AVX2 abilita questa direttiva. Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath usano le funzioni intrinseche AVX2, F16C/CVT16, FMA3, AVX a 128 bit, SSE4.1 e SSE3, se applicabile. Quando si usano \_ INTRINSECI XM \_ AVX2, implica \_ \_ \_ INTRINSECI XM \_ F16C, \_ \_ \_ INTRINSECI XM \_ FMA3, \_ \_ \_ INTRINSECI \_ AVX \_ \_ \_ XM, INTRINSECI \_ SSE \_ \_ \_ XM, INTRINSECI XM \_ SSE3 \_ e \_ \_ INTRINSECI XM \_ SSE4 \_ \_ .<br/>                                                                                       |
| \_FUNZIONI \_ INTRINSECHE F16C XM \_\_      | Novità di DirectXMath 3.09. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare le funzioni intrinseche SSE3, SSE4.1, AVX a 128 bit e F16C/CVT16, se applicabile; in caso contrario, DirectXMath usa SSE/SSE2. Quando si usa \_ \_ INTRINSECI F16C XM, implica \_ \_ \_ INTRINSECI \_ AVX \_ XM, \_ \_ INTRINSECI \_ SSE \_ XM, \_ \_ INTRINSECI XM \_ SSE3 e \_ \_ \_ INTRINSECI XM \_ SSE4 \_ \_ .<br/>                                                                                                                                                 |
| \_FUNZIONI \_ INTRINSECHE FMA3 \_ XM\_      | Novità di DirectXMath 3.11. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath useranno gli intrinseci SSE3, SSE4.1, AVX a 128 bit e FMA3, se applicabile; in caso contrario, DirectXMath usa SSE/SSE2. Quando si usano \_ INTRINSECI \_ FMA3 XM, implica \_ \_ \_ INTRINSECI \_ AVX \_ XM, \_ \_ INTRINSECI \_ SSE \_ \_ \_ XM, INTRINSECI XM \_ SSE3 e \_ \_ \_ INTRINSECI XM \_ SSE4 \_ \_ . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Ciò consente l'uso della convenzione di chiamata vectorcall per le destinazioni \_ \_ x86 o Windows x64. Il valore predefinito è \_ XM \_ VECTORCALL \_ =1 quando il compilatore supporta questa funzionalità. È possibile impostarlo manualmente su \_ XM \_ VECTORCALL \_ =0 per disabilitarlo sempre. <br/> \_\_vectorcall non è supportato per la piattaforma Windows in ARM/ARM64 o C++ gestito. <br/>                                                                                                                                                                                                                 |
| \_INTRINSECI \_ SVML \_ XM\_     | Novità di DirectXMath 3.16. <br/> Con VS 2019 o versione successiva, questa funzionalità consente alla libreria di usare Intel &reg; Short Vector Matrix Library per x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
