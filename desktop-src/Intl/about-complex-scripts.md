---
description: Uno script complesso è uno script per cui il membro fComplex di PROPRIETÀ SCRIPT \_ è impostato su TRUE. In questo argomento vengono fornite informazioni dettagliate sulle proprietà di uno script complesso.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informazioni sugli script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1e865b7638419178e3339169e56e8ceb111bcc65b925d9c337b5b71d0341827
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520651"
---
# <a name="about-complex-scripts"></a>Informazioni sugli script complessi

Uno [script complesso](uniscribe-glossary.md) è uno script per cui il membro **fComplex** di PROPRIETÀ SCRIPT è impostato su [**\_**](/windows/desktop/api/Usp10/ns-usp10-script_properties) **TRUE.** In questo argomento vengono fornite informazioni dettagliate sulle proprietà di uno script complesso.

## <a name="bidirectional-rendering"></a>Rendering bidirezionale

Il rendering bidirezionale gestisce il testo che legge sia da sinistra a destra che da destra a sinistra. Nel rendering bidirezionale dell'arabo, ad esempio, la direzione di lettura predefinita per il testo è da destra a sinistra, ma è da sinistra a destra per alcuni numeri. L'elaborazione di uno script complesso deve essere la differenza tra l'ordine logico (sequenza di tasti) e l'ordine visivo dei glifi. Inoltre, l'elaborazione deve gestire correttamente lo spostamento del caret e l'hit testing. Il mapping tra la posizione dello schermo e un indice di caratteri richiede una conoscenza degli algoritmi di layout per la visualizzazione specifica, ad esempio la selezione del testo o della visualizzazione del cursore.

## <a name="contextual-shaping"></a>Shaping contestuale

Nella forma contestuale, i caratteri dello script cambiano forma a seconda dei caratteri che li circondano. Tale forma si verifica nella scrittura in formato curvo inglese quando una "l" minuscola cambia forma a seconda del carattere che la precede, ad esempio una "a" (si connette bassa alla "l") o una "o" (si connette in alto). Ad esempio, l'arabo è uno script che mostra la forma contestuale.

## <a name="combining-characters"></a>Combinazione di caratteri

I caratteri di combinazione, detti anche "legature", sono caratteri che si uniscono in un unico carattere quando vengono inseriti insieme. Arabo è uno script con molti caratteri di combinazione. Un esempio dell'uso della combinazione di caratteri è "a" seguito da "combining grave", per cui la rappresentazione sottoposta a rendering è "à". Il flusso Unicode "U+0061 U+0300" richiede un'elaborazione per assicurarsi che la "grave di combinazione" sia posizionata correttamente sopra "a".

## <a name="specialized-word-break-and-justification"></a>Interruzione di parola e giustificazione specializzate

Alcuni script, ad esempio tailandese, hanno regole complesse per dividere le parole tra le righe o giustificare il testo in una riga.

## <a name="filtering-for-illegal-character-combinations"></a>Filtro per combinazioni di caratteri non validi

Uno script complesso, ad esempio tailandese, può filtrare le combinazioni di caratteri non validi quando una lingua non consente determinate combinazioni di caratteri.

## <a name="font-fallback"></a>Fallback dei tipi di carattere

Il fallback del tipo di carattere è la selezione automatica di un tipo di carattere diverso dal tipo di carattere selezionato dall'utente. In Uniscribe il fallback del tipo di carattere viene applicato dalla funzione [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando tutto o parte del testo si trova in uno script che il tipo di carattere selezionato dall'utente non supporta. Per altre informazioni, vedere [Uso del fallback dei tipi di carattere.](using-font-fallback.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



