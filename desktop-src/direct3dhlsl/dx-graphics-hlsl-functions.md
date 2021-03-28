---
title: Funzioni (riferimento HLSL)
description: Funzioni incapsulano le istruzioni HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 11/23/2019
ms.locfileid: "104335660"
---
# <a name="functions-hlsl-reference"></a>Funzioni (riferimento HLSL)

Funzioni incapsulano le istruzioni HLSL. In questo modo è possibile eseguire il debug di un set di funzioni e riutilizzarle in shader o effetti. Potrebbe essere necessario creare una funzione che incapsula la funzionalità di un vertex shader, pixel shader o trama shader. In altri casi, è possibile scrivere una funzione helper che esegue un'attività di uso comune e quindi chiamare tale funzione di supporto dalla funzione shader. Le regole per la scrittura di funzioni shader per HLSL sono molto simili alla scrittura di funzioni C.

-   [Sintassi](dx-graphics-hlsl-function-syntax.md)
-   [Parametri](dx-graphics-hlsl-function-parameters.md)
-   [Istruzione Return](dx-graphics-hlsl-return.md)
-   [Firme](dx-graphics-hlsl-signatures.md)

HLSL include anche una serie di [**funzioni intrinseche predefinite (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Poiché tutte le funzioni intrinseche sono testate e le prestazioni sono ottimizzate, è consigliabile usare una funzione intrinseca laddove possibile anziché creare una funzione personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




