---
description: I linguaggi di script complessi vengono suddivisi in cluster per ScriptShape. Il riordinamento dei caratteri si verifica sempre all'interno dei limiti del cluster. I cluster stessi sono garantiti per avanzare nella direzione dell'ordine di lettura.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Gestione della selezione host e hit testing del cursore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60396a668c89f7392b28adde0bb123060bf50348
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308699"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Gestione della selezione host e hit testing del cursore

I linguaggi di script complessi vengono suddivisi in [cluster](uniscribe-glossary.md) per [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Il riordinamento dei caratteri si verifica sempre all'interno dei limiti del cluster. I cluster stessi sono garantiti per avanzare nella direzione dell'ordine di lettura.

Le informazioni sul cluster nella matrice del cluster logico vengono utilizzate per condividere equamente la larghezza di un cluster di glifi tra i caratteri logici che rappresentano. Il glifo di lam Alef, ad esempio, è suddiviso in quattro aree:

-   Metà principale del Lam.
-   Metà finale della lam.
-   Metà principale del Alef.
-   Metà finale dell'oggetto Alef.

Le convenzioni per la posizione del punto di inserimento all'interno dei cluster dipendono dallo script. Per lo script arabo, se la posizione del punto di inserimento è impostata tra un carattere di base e il contrassegno di combinazione, il cursore viene visualizzato a metà del carattere di base. Per lo script tailandese, il punto di inserimento non può essere posizionato all'interno di un cluster. Quindi, quando l'utente sposta il cursore, l'applicazione deve superare tutti i glifi che compongono il cluster.

Le funzioni [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) si traducono tra le posizioni del cursore (negli offset dei punti di codice) e le posizioni x (in pixel). La funzione **ScriptXtoCP** conosce le convenzioni di posizione del punto di inserimento di ogni script:

-   Per Indian e Thai, le posizioni del punto di inserimento vengono bloccate ai limiti del cluster.
-   Per l'arabo, le posizioni del punto di inserimento vengono interpolate con i cluster.
-   Per l'ebraico, nelle versioni precedenti Usp10.dll, la versione 1,420, le posizioni del punto di inserimento vengono interpolate con i cluster. A partire da Usp10.dll, la versione 1,420, le posizioni del punto di inserimento vengono bloccate ai limiti del cluster.

Sia [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) che [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) funzionano solo all'interno delle esecuzioni. Per le funzioni è necessario che determinati parametri provengano dalle chiamate Uniscribe precedenti, come illustrato nella tabella seguente.



| Parametro                                        | Source (Sorgente)                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *nei*                                            | Come restituito da [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Come restituito da [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).     |
| *piAdvance*                                      | Come restituito da [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

L'applicazione deve stabilire l'esecuzione in cui un determinato offset del cursore o una posizione x è prima di passare le informazioni a [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) o [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp). Se l'applicazione non salva le informazioni sulla larghezza, può eseguire l'hit testing e il posizionamento del punto di inserimento dopo la visualizzazione di ogni esecuzione. In alternativa, l'applicazione può memorizzare nella cache informazioni sufficienti per eseguire l'hit testing e il posizionamento del punto di inserimento nella riga corrente senza richiedere la rielaborazione del paragrafo.

[**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) restituisce un valore perimetrale finale in modo che l'applicazione conosca il lato del carattere o del cluster su cui l'utente ha fatto clic. Il valore è 0 o la larghezza del carattere o del cluster nei punti di codice. La posizione del carattere restituita è la posizione del carattere su cui l'utente ha fatto clic. Per altre informazioni, vedere [visualizzazione del cursore nelle stringhe bidirezionali](displaying-the-caret-in-bidirectional-strings.md).

Per i linguaggi come Thai, per i quali l'utente non vuole inserire il punto di inserimento in un cluster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) imposta il flag del lato finale su 0 o sulla larghezza del cluster. Per lingue quali l'arabo, per le quali l'utente si aspetta di poter modificare all'interno di un cluster, **ScriptXtoCP** imposta il flag del lato finale su 0 o su 1.

Per consentire all'applicazione di definire percorsi validi per il punto di inserimento quando si gestiscono i tasti di direzione, Uniscribe fornisce informazioni sulle posizioni del punto di inserimento valide nel membro **fCharStop** negli attributi logici restituiti da [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak). Viene restituito **true** per la maggior parte dei caratteri e **false** per i caratteri Intercluster negli script, ad esempio Thai. L'applicazione deve controllare il valore **fNeedsCaretInfo** nella struttura [**delle \_ proprietà dello script**](/windows/desktop/api/Usp10/ns-usp10-script_properties) per un elemento per vedere se è necessario chiamare **ScriptBreak** per verificare la presenza di posizioni di cursore valide. Se il valore **fNeedsCaretInfo** è **false**, tutti i punti di codice sono posizioni di cursore valide.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




