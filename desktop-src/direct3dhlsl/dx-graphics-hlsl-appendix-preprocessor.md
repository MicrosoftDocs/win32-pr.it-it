---
title: Direttive per il preprocessore (HLSL)
description: Le direttive per il preprocessore, ad esempio \ define e \ ifdef, vengono in genere utilizzate per rendere i programmi di origine facili da modificare e facili da compilare in ambienti di esecuzione diversi.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739231"
---
# <a name="preprocessor-directives-hlsl"></a>Direttive per il preprocessore (HLSL)

Le direttive per il preprocessore, ad esempio [ \# define](dx-graphics-hlsl-appendix-pre-define.md) e [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), vengono in genere utilizzate per rendere i programmi di origine facili da modificare e facili da compilare in ambienti di esecuzione diversi. Le direttive nel file di origine indicano al preprocessore di eseguire azioni specifiche. Ad esempio, il preprocessore può sostituire i token nel testo, inserire il contenuto di altri file nel file di origine o eliminare la compilazione di parte del file rimuovendo sezioni di testo. Le righe del preprocessore vengono riconosciute ed eseguite prima dell'espansione di una macro. Pertanto, se una macro si espande in modo da risultare simile a un comando del preprocessore, tale comando non sarà riconosciuto dal preprocessore.

Le istruzioni del preprocessore utilizzano lo stesso set di caratteri delle istruzioni del file di origine, con l'eccezione che le sequenze di escape non sono supportate. Il set di caratteri utilizzati nelle istruzioni del preprocessore equivale al set di caratteri di esecuzione. Il preprocessore riconosce anche i valori di carattere negativi.

Il preprocessore HLSL riconosce le direttive seguenti:

-   [\#definire](dx-graphics-hlsl-appendix-pre-define.md)
-   [\#elif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#else](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#endif](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#errore](dx-graphics-hlsl-appendix-pre-error.md)
-   [\#if](dx-graphics-hlsl-appendix-pre-if.md)
-   [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#ifndef](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [\#includere](dx-graphics-hlsl-appendix-pre-include.md)
-   [\#linea](dx-graphics-hlsl-appendix-pre-line.md)
-   [\#pragma](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [\#undef](dx-graphics-hlsl-appendix-pre-undef.md)

Il simbolo di cancelletto ( \# ) deve essere il primo carattere di spazio non vuoto nella riga contenente la direttiva; gli spazi vuoti possono essere visualizzati tra il simbolo di cancelletto e la prima lettera della direttiva. Alcune direttive includono argomenti o valori. Qualsiasi testo che segue una direttiva (eccetto un argomento o un valore che fa parte della direttiva) deve essere preceduto dal delimitatore di commento a riga singola (//) o racchiuso tra delimitatori di commento (/ \* \* /). Le righe che contengono le direttive per il preprocessore possono essere continuate immediatamente prima del marcatore di fine riga con una barra rovesciata ( \) .

Le direttive del preprocessore possono essere visualizzate in qualsiasi punto di un file di origine, ma si applicano solo al resto del file di origine.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Appendice (DirectX HLSL)](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




