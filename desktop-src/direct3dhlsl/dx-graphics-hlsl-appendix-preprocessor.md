---
title: Direttive per il preprocessore (HLSL)
description: Le direttive per il preprocessore, ad esempio \ define e \ ifdef, vengono in genere usate per semplificare la modifica dei programmi di origine e la compilazione in ambienti di esecuzione diversi.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386830"
---
# <a name="preprocessor-directives-hlsl"></a>Direttive per il preprocessore (HLSL)

Le direttive per il preprocessore, ad esempio [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), vengono in genere usate per semplificare la modifica e la compilazione dei programmi di origine in ambienti di esecuzione diversi. Le direttive nel file di origine indicano al preprocessore di eseguire azioni specifiche. Ad esempio, il preprocessore può sostituire i token nel testo, inserire il contenuto di altri file nel file di origine o eliminare la compilazione di parte del file rimuovendo sezioni di testo. Le righe del preprocessore vengono riconosciute ed eseguite prima dell'espansione di una macro. Pertanto, se una macro si espande in modo da risultare simile a un comando del preprocessore, tale comando non sarà riconosciuto dal preprocessore.

Le istruzioni del preprocessore utilizzano lo stesso set di caratteri delle istruzioni del file di origine, con l'eccezione che le sequenze di escape non sono supportate. Il set di caratteri utilizzati nelle istruzioni del preprocessore equivale al set di caratteri di esecuzione. Il preprocessore riconosce anche i valori di carattere negativi.

Il preprocessore HLSL riconosce le direttive seguenti:

-   [\#Definire](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#Errore](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#if](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#Includono](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#Linea](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

Il simbolo di numero ( ) deve essere il primo carattere senza spazio nella riga contenente la direttiva . Gli spazi vuoti possono essere presenti tra il simbolo di numero e la prima lettera \# della direttiva. Alcune direttive includono argomenti o valori. Qualsiasi testo che segue una direttiva (ad eccezione di un argomento o di un valore che fa parte della direttiva ) deve essere preceduto dal delimitatore di commento a riga singola (//) o racchiuso tra delimitatori di commento (/ \* \* /). Le righe contenenti direttive del preprocessore possono essere continuate precedendo immediatamente il marcatore di fine riga con una barra rovesciata ( \\ ).

Le direttive del preprocessore possono essere visualizzate in qualsiasi punto di un file di origine, ma si applicano solo al resto del file di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




