---
description: Le direttive del compilatore ottimizzano le funzionalità utilizzate dalla libreria DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Direttive del compilatore della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 261b4d7dec2c9c3fda7413c0559ad95b7b6a46d31ad2f273c04c8e2bd4c30054
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119118211"
---
# <a name="directxmath-library-compiler-directives"></a>Direttive del compilatore della libreria DirectXMath

Le direttive del compilatore ottimizzano le funzionalità utilizzate dalla libreria DirectXMath.



| Direttiva                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_XM \_ NO \_ INTRINSICS\_        | Quando \_ si specifica XM NO \_ \_ INTRINSICS, le operazioni DirectXMath vengono implementate senza \_ usare oggetti intrinseci specifici della piattaforma. DirectXMath usa invece solo operazioni a virgola mobile standard.<br/> Per impostazione predefinita, \_ XM \_ NO \_ INTRINSICS \_ non è definito.<br/> Questa direttiva esegue l'override di tutte le altre direttive . È pertanto consigliabile cercare XM NO INTRINSICS prima di determinare lo stato di \_ \_ \_ \_ XM ARM NEON INTRINSICS o \_ \_ \_ \_ \_ \_ XM \_ SSE \_ \_ INTRINSICS.<br/>                                                                              |
| \_INTRINSECI SSE XM \_ \_\_       | Quando \_ si definisce XM SSE INTRINSICS, il codice viene compilato per l'uso di SSE e SSE2 di supporto nelle piattaforme che \_ \_ \_ supportano questi set di istruzioni.<br/> Le Windows che forniscono intrinseci SSE supportano sia SSE che SSE2.<br/> \_XM \_ SSE \_ INTRINSICS \_ non ha alcun effetto sui sistemi che non supportano SSE e SSE2.<br/> Per impostazione predefinita, \_ XM SSE INTRINSICS viene definito quando gli utenti compilano per \_ \_ una Windows \_ predefinita.<br/> DirectXMath usa le definizione del compilatore standard ( \_ M \_ IX86/M AMD64) per determinare Windows \_ destinazioni x86 o Windows \_ x64.<br/> |
| \_INTRINSECI \_ ARM \_ NEON XM \_\_ | Ciò indica che l'implementazione DirectXMath usa gli intrinseci ARM-NEON. Per impostazione predefinita, gli intrinseci ARM NEON XM vengono definiti quando gli utenti compilano per un \_ \_ Windows nella piattaforma \_ \_ \_ ARM/ARM64. DirectXMath usa la definizione del compilatore standard \_ (M \_ ARM, \_ M \_ ARM64) per determinare questa destinazione binaria.<br/> Il supporto degli intrinseci ARM-NEON non è una novità di DirectXMath e non è supportato da XNAMath 2.x.<br/>                                                                                                                                                                             |
| \_INTRINSECI \_ SSE3 XM \_\_      | Novità di DirectXMath 3.10. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare intrinseci SSE3, se applicabile. in caso contrario, usa SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_INTRINSECI \_ SSE4 XM \_\_      | Novità di DirectMath 3.09. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare intrinseci SSE3 e SSE4.1, se applicabile. in caso contrario, usa SSE/SSE2. Quando si specifica questa direttiva del compilatore, implica anche \_ \_ INTRINSECI SSE3 XM e \_ \_ \_ INTRINSECI \_ SSE \_ XM \_ .<br/>                                                                                                                                                                                                                                |
| \_INTRINSECI \_ AVX \_ XM\_       | Novità di DirectXMath 3.09. <br/> L'uso di /arch:AVX abiliterà questa direttiva. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare intrinseci SSE3, SSE4.1 e AVX a 128 bit, se applicabile; In caso contrario, DirectXMath usa SSE/SSE2. Quando si specifica questa direttiva del compilatore, implica anche \_ XM \_ SSE3 \_ INTRINSICS, \_ XM \_ SSE4 \_ INTRINSICS \_ e XM SSE INTRINSICS \_ e \_ \_ \_ include un piccolo subset di istruzioni SSE3. <br/>                                                                    |
| INTRINSECI \_ AVX2 \_ XM\_        | Novità di DirectXMath 3.11. <br/> L'uso di /arch:AVX2 abilita questa direttiva. Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath usano oggetti intrinseci AVX2, F16C/CVT16, FMA3, AVX a 128 bit, SSE4.1 e SSE3, se applicabile. Quando si usano INTRINSECI \_ \_ AVX2 \_ \_ XM, implica \_ INTRINSECI \_ F16C XM, INTRINSECI \_ \_ \_ FMA3 XM, INTRINSECI \_ \_ \_ \_ \_ AVX \_ \_ \_ XM, INTRINSECI SSE XM, INTRINSECI \_ \_ \_ \_ SSE3 XM e INTRINSECI \_ \_ \_ \_ \_ SSE4 \_ XM. \_<br/>                                                                                       |
| \_INTRINSECI \_ F16C XM \_\_      | Novità di DirectXMath 3.09. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare le funzioni intrinseche SSE3, SSE4.1, AVX a 128 bit e F16C/CVT16, se applicabile; In caso contrario, DirectXMath usa SSE/SSE2. Quando si usa \_ INTRINSECI \_ F16C \_ \_ XM, implica \_ INTRINSECI \_ AVX XM, INTRINSECI \_ \_ \_ \_ SSE \_ XM, \_ \_ INTRINSECI SSE3 XM \_ \_ \_ \_ \_ \_ \_ e INTRINSECI XM SSE4 .<br/>                                                                                                                                                 |
| \_FUNZIONI INTRINSECHE \_ FMA3 \_ XM\_      | Novità di DirectXMath 3.11. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath useranno gli intrinseci SSE3, SSE4.1, AVX a 128 bit e FMA3, dove applicabile; In caso contrario, DirectXMath usa SSE/SSE2. Quando si usano \_ INTRINSECI \_ FMA3 \_ \_ XM, implica \_ INTRINSECI AVX XM, INTRINSECI \_ \_ \_ \_ SSE \_ \_ XM, \_ \_ INTRINSECI SSE3 XM \_ \_ \_ \_ \_ \_ \_ e INTRINSECI XM SSE4 . <br/>                                                                                                                                                            |
| \_XM \_ VECTORCALL\_            | Ciò consente l'uso della \_ \_ convenzione di chiamata vectorcall per Windows destinazioni x86 o Windows x64. Il valore predefinito è \_ XM \_ VECTORCALL \_ =1 quando il compilatore supporta questa funzionalità. È possibile impostarlo manualmente su \_ XM \_ VECTORCALL \_ =0 per disabilitarlo sempre. <br/> \_\_vectorcall non è supportato per l'Windows nella piattaforma ARM/ARM64 o in C++ gestito. <br/>                                                                                                                                                                                                                 |
| \_INTRINSECI \_ SVML \_ XM\_     | Novità di DirectXMath 3.16. <br/> Con VISUAL Studio 2019 o versioni successive, ciò consente alla libreria di usare la libreria Intel &reg; Short Vector Matrix Library per x86/x64. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento sulla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 
