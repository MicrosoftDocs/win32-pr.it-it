---
title: Funzioni (informazioni di riferimento su HLSL)
description: Le funzioni incapsulano istruzioni HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37086a030ad902f2bfb5deab52ffba620e97890bd13e7c6957170572087ce7c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514579"
---
# <a name="functions-hlsl-reference"></a>Funzioni (informazioni di riferimento su HLSL)

Le funzioni incapsulano istruzioni HLSL. In questo modo è possibile eseguire il debug di un set di funzioni e quindi riutilizzarle tra shader o effetti. È possibile creare una funzione che incapsula la funzionalità di un vertex shader, pixel shader o texture shader. Altre volte, potrebbe essere necessario scrivere una funzione helper che esegue alcune attività di uso comune e quindi chiamare tale funzione helper dalla funzione shader. Le regole per la scrittura di funzioni shader per HLSL sono molto simili alla scrittura di funzioni C.

-   [Sintassi](dx-graphics-hlsl-function-syntax.md)
-   [Parametri](dx-graphics-hlsl-function-parameters.md)
-   [Istruzione Return](dx-graphics-hlsl-return.md)
-   [Firme](dx-graphics-hlsl-signatures.md)

HLSL include anche una serie di funzioni [**intrinseche incorporate (DirectX HLSL).**](dx-graphics-hlsl-intrinsic-functions.md) Poiché tutte le funzioni intrinseche vengono testate e ottimizzate per le prestazioni, è consigliabile usare una funzione intrinseca laddove possibile anziché creare una funzione personalizzata.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sintassi del linguaggio (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




