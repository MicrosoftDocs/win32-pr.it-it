---
description: Uso del fallback dei tipi di carattere
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Uso del fallback dei tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9afb073a01cc1c5b90d4a4861a973846d3ae9ae1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760484"
---
# <a name="using-font-fallback"></a>Uso del fallback dei tipi di carattere

> [!Note]  
> In questo argomento tutti i commenti relativi a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) si applicano ugualmente a [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

L'applicazione deve usare il fallback del tipo di carattere durante la visualizzazione del testo se alcuni caratteri in una stringa non sono supportati nel tipo di carattere o se l'applicazione usa uno [script complesso](uniscribe-glossary.md) non supportato dal tipo di carattere. Il requisito per il fallback del tipo di carattere viene rilevato durante il processo di layout per il testo, quando l'applicazione chiama la funzione [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) . Per informazioni sulla visualizzazione del testo, vedere [visualizzazione di testo con Uniscribe](displaying-text-with-uniscribe.md).

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinare la necessità del fallback dei tipi di carattere per i caratteri non supportati

Se alcuni dei caratteri di una stringa non sono supportati in un tipo di carattere richiesto, una chiamata dell'applicazione a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ha esito positivo. Tuttavia, l'applicazione deve analizzare il buffer di output del glifo per la presenza di glifi mancanti. L'indice del glifo del glifo mancante può essere determinato per un tipo di carattere specifico chiamando [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Se un glifo particolare non è disponibile, l'applicazione deve eseguire il fallback a un tipo di carattere diverso per un glifo o eseguire il rendering di un simbolo grafico che indica che non è disponibile alcun glifo.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinare la necessità del fallback dei tipi di carattere per gli script complessi non supportati

Il tipo di carattere preferenziale per la visualizzazione di un'applicazione potrebbe non supportare uno script complesso richiesto dal testo. In questo caso, la chiamata dell'applicazione a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ha esito negativo con il codice di errore E lo \_ script \_ non \_ nel \_ tipo di carattere.

## <a name="assign-a-fallback-font"></a>Assegnare un tipo di carattere di fallback

Una volta stabilito che è necessario il fallback del tipo di carattere, l'applicazione deve assegnare un tipo di carattere di fallback. L'applicazione può provare le tecniche seguenti:

-   Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) per ogni tipo di carattere in un elenco di tipi di carattere finché una chiamata non ha un risultato accettabile.
-   Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con ogni tipo di carattere in un elenco fino a quando non è possibile determinare se il tipo di carattere avrà esito positivo. Se il codice di errore è sempre E \_ lo script \_ non \_ \_ è in un tipo di carattere, uno script complesso non è supportato dai tipi di carattere. Eseguire il rendering di un simbolo grafico che indica che non è disponibile alcun glifo oppure specificare di nuovo lo script come non definito (nessuna elaborazione di script) e riavviarlo. Per impostare lo script come non definito, impostare il membro **escript** della struttura di [**\_ analisi dello script**](/windows/win32/api/usp10/ns-usp10-script_analysis) in modo che lo script non sia \_ definito.
-   Chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) con ogni tipo di carattere in un elenco fino a quando non è possibile determinare se il tipo di carattere avrà esito positivo. Se il codice di errore indica che per alcuni caratteri viene utilizzato il mapping a glifi mancanti, suddividere la stringa in intervalli più piccoli. I tipi di carattere diversi possono essere assegnati a intervalli secondari, in modo che sia possibile eseguire il rendering di più caratteri.

## <a name="generate-glyph-information"></a>Genera informazioni sul glifo

Una volta che l'applicazione ha assegnato un tipo di carattere che ha avuto esito positivo nelle chiamate a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), può effettuare chiamate a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per generare la larghezza di avanzamento del glifo e le informazioni sull'offset bidimensionale dall'output di **ScriptShape**. Il tipo di carattere deve avere esito positivo nelle chiamate. Un errore del tipo di carattere in una chiamata a **ScriptPlace** dopo l'esito positivo in una chiamata **ScriptShape** indica un tipo di carattere rotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



