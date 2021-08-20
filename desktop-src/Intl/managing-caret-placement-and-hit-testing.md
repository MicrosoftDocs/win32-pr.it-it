---
description: I linguaggi di script complessi vengono suddivisi in cluster da ScriptShape. Il riordinamento dei caratteri avviene sempre entro i limiti del cluster. È garantito che i cluster stessi avanzano nella direzione dell'ordine di lettura.
ms.assetid: 50b4b643-af96-4a6f-80f9-27a71ce16b0e
title: Gestione del posizionamento del caret e dell'hit testing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e1c6d3b9dbd54f3df2b458a3f7473d1021dceafd6772730b8482b06c4e1c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788401"
---
# <a name="managing-caret-placement-and-hit-testing"></a>Gestione del posizionamento del caret e dell'hit testing

I linguaggi di script complessi vengono [suddivisi in cluster](uniscribe-glossary.md) [**da ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Il riordinamento dei caratteri avviene sempre entro i limiti del cluster. È garantito che i cluster stessi avanzano nella direzione dell'ordine di lettura.

Le informazioni sui cluster nella matrice di cluster logici vengono usate per condividere in modo uniforme la larghezza di un cluster di glifi tra i caratteri logici che rappresentano. Ad esempio, il glifo lam alef è suddiviso in quattro aree:

-   Metà iniziale del lam.
-   Metà finale del lam.
-   Metà iniziale dell'alef.
-   Metà finale dell'alef.

Le convenzioni per il posizionamento del caret all'interno dei cluster dipendono dagli script. Per lo script arabo, se la posizione del cursore è impostata tra un carattere di base e il segno di combinazione, il cursore viene visualizzato a metà del carattere di base. Per lo script tailandese, il cursore non può essere posizionato all'interno di un cluster. Pertanto, quando l'utente fa avanzare il caret, l'applicazione deve superare tutti i glifi che costituiscono il cluster.

Le [**funzioni ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) traslano tra le posizioni del cursore (negli offset del punto di codice) e le posizioni x (in pixel). La **funzione ScriptXtoCP** è a conoscenza delle convenzioni di posizione del cursore di ogni script:

-   Per india e tailandese, le posizioni del cursore vengono bloccate ai limiti del cluster.
-   Per l'arabo, le posizioni del cursore sono interpolate con cluster.
-   Per l'ebraico, nelle versioni precedenti Usp10.dll, versione 1.420, le posizioni del cursore sono interpolate con cluster. A partire Usp10.dll, versione 1.420, le posizioni del cursore vengono bloccate ai limiti del cluster.

Sia [**ScriptXtoCP che**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) operano solo all'interno delle esecuzioni. Le funzioni richiedono che determinati parametri provengono da chiamate Uniscribe precedenti, come illustrato nella tabella seguente.



| Parametro                                        | Source (Sorgente)                                                 |
|--------------------------------------------------|--------------------------------------------------------|
| *Psa*                                            | Come restituito da [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize). |
| *cGlyphspwLogClust*<br/> *psva*<br/> | Come restituito da [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).     |
| *piAdvance*                                      | Come restituito da [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace).     |



 

L'applicazione deve stabilire l'esecuzione in cui si trova un offset del cursore specificato o una posizione x prima di passare le informazioni a [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) [**o ScriptXtoCP.**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) Se l'applicazione non salva le informazioni sulla larghezza, può eseguire hit testing e posizionamento del caret dopo la visualizzazione di ogni esecuzione. In alternativa, l'applicazione può memorizzare nella cache informazioni sufficienti per eseguire hit testing e posizionamento del punto di inserimento nella riga corrente senza richiedere la rielaborazione del paragrafo.

[**ScriptXtoCP restituisce**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) un valore di bordo finale in modo che l'applicazione conosca il lato del carattere o del cluster su cui l'utente ha fatto clic. Il valore è 0 o la larghezza del carattere o del cluster nei punti di codice. La posizione del carattere restituita è la posizione del carattere su cui l'utente ha fatto clic. Per altre informazioni, vedere [Visualizzazione del caret nelle stringhe bidirezionali.](displaying-the-caret-in-bidirectional-strings.md)

Per lingue come il tailandese, per cui l'utente convenzionalmente non vuole inserire il punto di caret in un cluster, [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) imposta il flag laterale finale su 0 o sulla larghezza del cluster. Per lingue come l'arabo, per cui l'utente prevede di poter modificare all'interno di un cluster, **ScriptXtoCP** imposta il flag laterale finale su 0 o su 1.

Per consentire all'applicazione di stabilire posizioni valide per il cursore durante la gestione dei tasti di direzione, Uniscribe fornisce informazioni sulle posizioni valide del cursore nel membro **fCharStop** negli attributi logici restituiti da [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak). **Viene** restituito TRUE per la maggior parte dei caratteri e **FALSE** per i caratteri intercluster negli script, ad esempio tailandese. L'applicazione deve controllare il valore **fNeedsCaretInfo** nella struttura [**SCRIPT \_ PROPERTIES**](/windows/desktop/api/Usp10/ns-usp10-script_properties) per verificare se è necessario chiamare **ScriptBreak** per verificare la presenza di posizioni del cursore valide. Se il **valore fNeedsCaretInfo** **è FALSE,** tutti i punti di codice sono posizioni del cursore valide.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




