---
description: Per fornire la giustificazione del testo, un'applicazione può usare uno dei due metodi seguenti.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Elaborazione di script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 987c58cd1d6e8979573b47bbf3e2e7ff248617b12907f81ef70761c08403a067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118390425"
---
# <a name="processing-complex-scripts"></a>Elaborazione di script complessi

Per fornire la giustificazione del testo, un'applicazione può usare uno dei due metodi seguenti. Per una semplice implementazione della giustificazione multilingue, l'applicazione deve chiamare [**ScriptJustify.**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify) Genera la matrice delta dx considerando kashida, quindi la spaziatura tra parole e infine la spaziatura tra caratteri. Per una giustificazione più sofisticata, l'applicazione può generare una matrice delta dx aggiornata usando le proprie conoscenze del linguaggio e le informazioni recuperate da [**ScriptShape nella**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) [**matrice SCRIPT \_ VISATTR.**](/windows/win32/api/usp10/ns-usp10-script_visattr)

Lo spazio di giustificazione o kashida deve essere inserito dove identificato dal **membro uJustification** di [**SCRIPT \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr). Quando si esegue la giustificazione tra caratteri, l'applicazione deve inserire spazio aggiuntivo solo dopo i glifi contrassegnati con SCRIPT \_ JUSTIFY \_ CHARACTER.

L'applicazione esegue il posizionamento del punto di inserimento e l'hit testing [**usando ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) [**e ScriptCPtoX.**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox) Per altre informazioni, vedere Gestione [del posizionamento del caret e hit testing.](managing-caret-placement-and-hit-testing.md)

Per ottenere larghezze in modo indipendente dal tipo di carattere, l'applicazione chiama [**ScriptGetLogicalWidths.**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths) Passando le larghezze logiche a [**ScriptApplyLogicalWidth,**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)è possibile visualizzare nuovamente un blocco di testo negli stessi limiti con una perdita accettabile di qualità anche quando il tipo di carattere originale non è disponibile. Genera una matrice di larghezze di glifi [(larghezze di avanzamento](uniscribe-glossary.md)) adatte per il passaggio [**a ScriptTextOut.**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) Tale registrazione e riapplicazione delle informazioni sulla larghezza di avanzamento in modo indipendente dal tipo di carattere può essere utile in situazioni come la metafiling in un formato definito dall'applicazione.

> [!Note]  
> I metafile non supportano gli indici dei glifi. Per scrivere in un metafile avanzato, l'applicazione deve usare [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e scrivere direttamente i caratteri logici. Usando questo meccanismo, la generazione e la posizione del glifo non si verificano fino a quando il testo non viene riprodotto.

 

Per recuperare i glifi specifici usati per impostazione predefinita, spazi vuoti, kashida e così via, per il tipo di carattere corrente, l'applicazione deve chiamare [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Per determinare quali caratteri in un'esecuzione sono supportati dal tipo di carattere selezionato, l'applicazione [**chiama ScriptGetCMap.**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap) I caratteri non disponibili hanno il glifo predefinito nel buffer del glifo. Si noti che questo metodo ha esito negativo se un tipo di carattere esegue il rendering di un carattere usando una combinazione di glifi anziché un singolo glifo. Ad esempio, 00C9; È possibile eseguire il rendering di LATIN CAPITAL LETTER E WITH ACUTE usando un glifo maiuscolo e un glifo acuto. Per determinare il supporto del tipo di carattere per una stringa che contiene questi tipi di punti di codice, l'applicazione può [**chiamare ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) Per altre informazioni, vedere [Uso dei motori di data shaping.](using-shaping-engines.md)

La [**funzione ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) restituisce l'altezza del tipo di carattere dalla cache dei tipi di carattere. [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) fornisce informazioni sull'elaborazione speciale necessaria per tutti gli script, indicizzati da script. Ad esempio, include la lingua principale associata allo script, i dati che indicano se lo script è numerico e i dati che indicano se lo script è uno script complesso.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) restituisce la larghezza [ABC](uniscribe-glossary.md) di un glifo specificato, che potrebbe essere utile per disegnare grafici di glifi. Tuttavia, non deve essere usato per la normale formattazione complessa del testo dello script.

## <a name="related-topics"></a>Argomenti correlati

[Uso di Uniscribe](using-uniscribe.md)


 

 
