---
description: Le direttive del compilatore ottimizzano la funzionalità utilizzata dalla libreria DirectXMath.
ms.assetid: c1746b7b-7e7e-2453-77eb-17f859a38fe2
title: Direttive del compilatore della libreria DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f1d67ecd4772116a3bf29f802c39b2e348fd5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309299"
---
# <a name="directxmath-library-compiler-directives"></a>Direttive del compilatore della libreria DirectXMath

Le direttive del compilatore ottimizzano la funzionalità utilizzata dalla libreria DirectXMath.



| Direttiva                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_\_nessun \_ INTRINSECo XM\_        | Quando \_ \_ non \_ viene definito alcun intrinseco XM \_ , le operazioni DirectXMath vengono implementate senza utilizzare funzioni intrinseche specifiche della piattaforma. DirectXMath utilizza invece solo operazioni a virgola mobile standard.<br/> Per impostazione predefinita \_ , \_ \_ non sono definiti gli intrinseci XM \_ .<br/> Questa direttiva esegue l'override di tutte le altre direttive. Si consiglia pertanto di verificare la presenza di \_ \_ \_ funzioni intrinseche senza XM \_ prima di determinare lo stato degli intrinseci XM \_ \_ ARM \_ neon \_ o degli \_ \_ \_ \_ intrinseci SSE XM \_ .<br/>                                                                              |
| \_\_ \_ intrinseci XM SSE\_       | Quando \_ \_ \_ si definisce intrinseci XM SSE \_ , il codice viene compilato per usare il supporto di SSE e SSE2 sulle piattaforme che supportano questi set di istruzioni.<br/> Le versioni di Windows che forniscono intrinseci SSE supportano sia SSE che SSE2.<br/> \_Le \_ \_ funzioni intrinseche SSE XM non \_ hanno alcun effetto sui sistemi che non supportano SSE e SSE2.<br/> Per impostazione predefinita \_ , \_ \_ gli intrinseci XM SSE \_ vengono definiti quando gli utenti si compilano per una piattaforma Windows.<br/> DirectXMath usa il compilatore standard definisce ( \_ m \_ ix86/ \_ m \_ amd64) per determinare le destinazioni Windows x86 o Windows x64.<br/> |
| \_oggetti \_ \_ intrinseci neon ARM XM \_\_ | Ciò indica che l'implementazione di DirectXMath usa gli intrinseci del NEON ARM. Per impostazione predefinita \_ , \_ \_ gli intrinseci del neon ARM XM \_ \_ vengono definiti quando gli utenti si compilano per una piattaforma Windows RT. DirectXMath usa il compilatore standard define ( \_ m \_ ARM, \_ m \_ arm64) per determinare la destinazione binaria.<br/> Il supporto per gli intrinseci del NEON ARM è una novità di DirectXMath e non è supportato da XNAMath 2. x.<br/>                                                                                                                                                                             |
| \_\_ \_ Funzioni intrinseche SSE3 XM\_      | Novità per Windows 10 Creators Update SDK. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare gli intrinseci SSE3, ove applicabile; in caso contrario, USA SSE/SSE2.<br/>                                                                                                                                                                                                                                                                                                                                                      |
| \_\_ \_ Funzioni intrinseche SSE4 XM\_      | Novità per Windows 10 Anniversary SDK.<br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare gli intrinseci SSE3 e SSE 4.1 laddove applicabile; in caso contrario, USA SSE/SSE2. Quando si specifica questa direttiva del compilatore, sono implicate anche \_ \_ \_ le funzioni intrinseche SSE3 \_ e gli \_ \_ \_ intrinseci SSE XM \_ .<br/>                                                                                                                                                                                                                                |
| \_\_ \_ funzioni intrinseche AVX XM\_       | Novità per Windows 10 Anniversary SDK.<br/> L'uso di/Arch: AVX consentirà questa direttiva. <br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath vengono implementate per usare gli intrinseci SSE3, SSE 4.1 e AVX a 128 bit, ove applicabile; in caso contrario, DirectXMath USA SSE/SSE2. Quando si specifica questa direttiva del compilatore, implica anche gli intrinseci \_ XM \_ SSE3 \_ , gli \_ \_ \_ intrinseci XM SSE4 e gli \_ \_ \_ \_ intrinseci SSE XM \_ e include un piccolo subset di istruzioni SSE3. <br/>                                                                    |
| \_ \_ Funzioni intrinseche AVX2 XM\_        | Novità di Windows 10 Fall Creators Update SDK<br/> L'uso di/Arch: AVX2 Abilita questa direttiva. Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath utilizzano le funzioni intrinseche AVX2, F16C/CVT16, FMA3, AVX a 128 bit, SSE 4.1 e SSE3, ove applicabile. Quando si usano \_ gli \_ \_ intrinseci XM AVX2 \_ , sono implicati gli intrinseci \_ XM F16C, gli intrinseci \_ \_ XM FMA3, gli intrinseci \_ \_ \_ \_ \_ \_ XM \_ AVX, gli \_ \_ \_ \_ \_ intrinseci SSE XM, gli \_ \_ \_ intrinseci XM SSE3 \_ \_ e le \_ \_ \_ funzioni intrinseche XM SSE4 \_ .<br/>                                                                                       |
| \_\_ \_ Funzioni intrinseche F16C XM\_      | Novità per Windows 10 Anniversary SDK.<br/> Quando si specifica questa direttiva del compilatore, vengono implementate le funzioni DirectXMath per l'uso di SSE3, SSE 4.1, AVX a 128 bit e F16C/CVT16, ove applicabile; in caso contrario, DirectXMath USA SSE/SSE2. Quando si usano \_ gli \_ \_ intrinseci XM F16C \_ , questo implica gli intrinseci XM AVX, gli intrinseci \_ \_ \_ SSE XM, gli intrinseci \_ \_ \_ \_ \_ \_ XM \_ SSE3 e gli \_ \_ \_ \_ \_ intrinseci XM SSE4 \_ .<br/>                                                                                                                                                 |
| \_\_ \_ Funzioni intrinseche FMA3 XM\_      | Novità di Windows 10 Fall Creators Update SDK<br/> Quando si specifica questa direttiva del compilatore, le funzioni DirectXMath utilizzeranno gli intrinseci SSE3, SSE 4.1, AVX a 128 bit e FMA3, se applicabile. in caso contrario, DirectXMath USA SSE/SSE2. Quando si usano \_ gli \_ \_ intrinseci XM FMA3 \_ , questo implica gli intrinseci XM AVX, gli intrinseci \_ \_ \_ SSE XM, gli intrinseci \_ \_ \_ \_ \_ \_ XM \_ SSE3 e gli \_ \_ \_ \_ \_ intrinseci XM SSE4 \_ . <br/>                                                                                                                                                            |
| \_\_VECTORCALL XM\_            | Questo consente l'uso della nuova \_ \_ convenzione di chiamata vectorcall per le destinazioni Windows x86 o Windows x64. Il valore predefinito è \_ XM \_ VECTORCALL \_ = 1 quando il compilatore supporta questa funzionalità. È possibile impostarlo manualmente su \_ XM \_ VECTORCALL \_ = 0 per disabilitarlo sempre. <br/> \_\_vectorcall non è supportato per la piattaforma Windows RT o C++ gestito. <br/>                                                                                                                                                                                                                 |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Guida di riferimento alla programmazione DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>

 

 




