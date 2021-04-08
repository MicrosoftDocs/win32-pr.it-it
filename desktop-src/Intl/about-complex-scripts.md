---
description: Uno script complesso è uno script per il quale il membro fComplex delle \_ proprietà dello script è impostato su true. In questo argomento vengono illustrate in dettaglio le proprietà che possono essere presenti in uno script complesso.
ms.assetid: bceeb0d6-bda3-43bf-984e-87fbfb327578
title: Informazioni sugli script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edb1929a58e7810fb51bcb2b7a6bf9d5a762282e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104057817"
---
# <a name="about-complex-scripts"></a>Informazioni sugli script complessi

Uno [script complesso](uniscribe-glossary.md) è uno script per il quale  il membro FComplex [**delle \_ proprietà dello script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) è impostato su **true**. In questo argomento vengono illustrate in dettaglio le proprietà che possono essere presenti in uno script complesso.

## <a name="bidirectional-rendering"></a>Rendering bidirezionale

Il rendering bidirezionale sta gestendo il testo che legge sia da sinistra a destra che da destra a sinistra. Nel rendering bidirezionale dell'arabo, ad esempio, la direzione di lettura predefinita per il testo è da destra a sinistra, ma è da sinistra a destra per alcuni numeri. L'elaborazione di uno script complesso deve tenere conto della differenza tra l'ordine logico (sequenza di tasti) e l'ordine visivo dei glifi. Inoltre, l'elaborazione deve gestire correttamente il movimento del cursore e l'hit testing. Il mapping tra la posizione dello schermo e un indice dei caratteri richiede la comprensione degli algoritmi di layout per la visualizzazione specifica, ad esempio la selezione del testo o la visualizzazione del cursore.

## <a name="contextual-shaping"></a>Definizione del contesto

In shaping contestuale, i caratteri script cambiano forma a seconda dei caratteri che li racchiudono. Tale data shaping viene eseguita nella scrittura corsiva in lingua inglese quando una "l" minuscola cambia a seconda del carattere che la precede, ad esempio un "a" (si connette in basso a "l") o "o" (si connette in alto). Ad esempio, l'arabo è uno script che mostra il Shaping contestuale.

## <a name="combining-characters"></a>Combinazione di caratteri

La combinazione di caratteri, detti anche "legature", sono caratteri che si uniscono a un carattere quando vengono posizionati insieme. L'arabo è uno script con molti caratteri combinati. Un esempio di utilizzo dei caratteri combinati è "a" seguito da "combinando grave", per il quale la rappresentazione di cui è stato eseguito il rendering è "à". Il flusso Unicode "U + 0061 U + 0300" richiede una certa elaborazione per assicurarsi che la "combinazione di tombe" sia posizionata correttamente sopra "a".

## <a name="specialized-word-break-and-justification"></a>Pausa e giustificazione di parole specializzate

Alcuni script, ad esempio Thai, presentano regole complesse per dividere le parole tra le righe o giustificare il testo su una riga.

## <a name="filtering-for-illegal-character-combinations"></a>Filtro per combinazioni di caratteri non valide

Uno script complesso, ad esempio tailandese, può filtrare le combinazioni di caratteri non valide quando un linguaggio non consente determinate combinazioni di caratteri.

## <a name="font-fallback"></a>Fallback del tipo di carattere

Il fallback del tipo di carattere è la selezione automatica di un tipo di carattere diverso dal tipo di carattere selezionato dall'utente. In Uniscribe il fallback del tipo di carattere viene applicato dalla funzione [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) quando tutto o parte del testo è in uno script che non è supportato dal tipo di carattere selezionato dall'utente. Per ulteriori informazioni, vedere [utilizzo del fallback dei tipi di carattere](using-font-fallback.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Uniscribe](about-uniscribe.md)
</dt> </dl>

 

 



