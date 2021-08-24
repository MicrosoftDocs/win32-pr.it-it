---
description: Uso del fallback dei caratteri
ms.assetid: 952f33b6-ca52-40a2-b914-52c1c62ae0e0
title: Uso del fallback dei caratteri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db9a4e9b329e2c3257ae9fad02f1fb4774a63dc1d4b4e804c0dca8e690cbf4d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787871"
---
# <a name="using-font-fallback"></a>Uso del fallback dei caratteri

> [!Note]  
> In questo argomento tutte le osservazioni su [**ScriptShape si**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) applicano in modo uniforme a [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).

 

L'applicazione deve usare il fallback dei caratteri durante la visualizzazione del testo se alcuni caratteri in una stringa non sono supportati nel tipo di carattere o se l'applicazione usa uno [script](uniscribe-glossary.md) complesso non supportato dal tipo di carattere. Il requisito per il fallback del tipo di carattere viene rilevato durante il processo di layout per il testo, quando l'applicazione chiama la [**funzione ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Per informazioni sulla visualizzazione del testo, vedere [Visualizzazione di testo con Uniscribe.](displaying-text-with-uniscribe.md)

## <a name="determine-the-need-for-font-fallback-for-unsupported-characters"></a>Determinare la necessità di fallback dei caratteri per i caratteri non supportati

Se alcuni caratteri di una stringa non sono supportati in un tipo di carattere richiesto, una chiamata dell'applicazione a [**ScriptShape ha**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) esito positivo. Tuttavia, l'applicazione deve analizzare il buffer di output del glifo per la presenza di glifi mancanti. L'indice del glifo mancante può essere determinato per un tipo di carattere specifico chiamando [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Se un particolare glifo non è disponibile, l'applicazione deve eseguire il fall back a un tipo di carattere diverso per un glifo o eseguire il rendering di un simbolo grafico che indica che non è disponibile alcun glifo.

## <a name="determine-the-need-for-font-fallback-for-unsupported-complex-scripts"></a>Determinare la necessità di fallback dei caratteri per gli script complessi non supportati

Il tipo di carattere preferito da un'applicazione per la visualizzazione potrebbe non supportare uno script complesso richiesto dal testo. In questo caso, la chiamata dell'applicazione a [**ScriptShape ha**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) esito negativo con il codice di errore E \_ SCRIPT NOT IN \_ \_ \_ FONT.

## <a name="assign-a-fallback-font"></a>Assegnare un tipo di carattere di fallback

Dopo aver determinato che è necessario il fallback del tipo di carattere, l'applicazione deve assegnare un tipo di carattere di fallback. L'applicazione può provare le tecniche seguenti:

-   Chiamare [**ScriptShape per**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ogni tipo di carattere in un elenco di tipi di carattere fino a quando una chiamata non restituisce un valore accettabile.
-   Chiamare [**ScriptShape con**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ogni tipo di carattere in un elenco finché non è possibile determinare che nessun tipo di carattere avrà esito positivo. Se il codice di errore è sempre E SCRIPT NOT IN FONT, uno script complesso \_ non è supportato dai tipi di \_ \_ \_ carattere. Eseguire il rendering di un simbolo grafico che indica che non è disponibile alcun glifo oppure specificare nuovamente lo script come non definito (nessuna elaborazione dello script) e ricominciare. Per impostare lo script come non definito, impostare il membro **eScript** della struttura [**SCRIPT \_ ANALYSIS**](/windows/win32/api/usp10/ns-usp10-script_analysis) su SCRIPT \_ UNDEFINED.
-   Chiamare [**ScriptShape con**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) ogni tipo di carattere in un elenco finché non è possibile determinare che nessun tipo di carattere avrà esito positivo. Se il codice di errore indica che alcuni caratteri sono mappati a glifi mancanti, suddividere la stringa in intervalli più piccoli. È possibile assegnare tipi di carattere diversi alle aree secondarie in modo che sia possibile eseguire il rendering di una maggior parte dei caratteri.

## <a name="generate-glyph-information"></a>Generare informazioni sui glifi

Dopo che l'applicazione ha assegnato un tipo di carattere che ha esito positivo nelle chiamate a [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape), può effettuare chiamate a [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace) per generare la larghezza di avanzamento del glifo e le informazioni sull'offset bidimensionale dall'output di **ScriptShape**. Il tipo di carattere deve avere esito positivo in queste chiamate. Un errore del tipo di carattere in una chiamata a **ScriptPlace** dopo l'esito positivo in una **chiamata ScriptShape** indica un tipo di carattere interrotto.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



