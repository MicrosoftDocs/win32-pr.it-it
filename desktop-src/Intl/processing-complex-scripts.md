---
description: Per fornire la giustificazione del testo, un'applicazione può usare uno dei due metodi.
ms.assetid: 1190baed-5959-4f7a-8946-ac3b3da85821
title: Elaborazione di script complessi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87bea5b75e87afc4177b03c03f4263ba2592a0e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049447"
---
# <a name="processing-complex-scripts"></a>Elaborazione di script complessi

Per fornire la giustificazione del testo, un'applicazione può usare uno dei due metodi. Per una semplice implementazione di una giustificazione multilingue, l'applicazione deve chiamare [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify). Genera la matrice Delta DX considerando kashida, quindi la spaziatura tra le parole, quindi la spaziatura tra caratteri. Per una giustificazione più sofisticata, l'applicazione può generare una matrice Delta DX aggiornata usando la propria conoscenza della lingua e le informazioni recuperate da [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) nella matrice [**\_ VISATTR dello script**](/windows/win32/api/usp10/ns-usp10-script_visattr) .

È necessario inserire lo spazio di giustificazione o kashida se identificato dal membro **uJustification** dello [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr). Quando si esegue la giustificazione tra caratteri, l'applicazione deve inserire ulteriore spazio solo dopo i glifi contrassegnati con il \_ carattere di giustificazione dello script \_ .

L'applicazione esegue il posizionamento e l'hit testing del cursore usando [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp) e [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox). Per ulteriori informazioni, vedere [gestione del posizionamento del cursore e hit testing](managing-caret-placement-and-hit-testing.md).

Per ottenere larghezze in modo indipendente dal tipo di carattere, l'applicazione chiama [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths). Passando le larghezze logiche a [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth), un blocco di testo può essere rivisualizzato negli stessi limiti con una perdita accettabile di qualità anche quando il tipo di carattere originale non è disponibile. Genera una matrice di larghezze del glifo ([larghezze di avanzamento](uniscribe-glossary.md)) adatte per passare a [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout). La registrazione e la riapplicazione delle informazioni sulla larghezza avanzata in modo indipendente dal tipo di carattere possono essere utili in situazioni come la Metafiling in un formato definito dall'applicazione.

> [!Note]  
> I metafile non supportano gli indici di glifi. Per scrivere in un metafile avanzato, l'applicazione deve usare [**ExtTextOut**](/windows/win32/api/wingdi/nf-wingdi-exttextouta) e scrivere direttamente i caratteri logici. Con questo meccanismo, la generazione e la selezione del glifo non vengono eseguite fino a quando non viene riprodotto il testo.

 

Per recuperare i glifi specifici utilizzati per i valori predefiniti, Blank, Kashida e così via, per il tipo di carattere corrente, l'applicazione deve chiamare [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties). Per determinare quali caratteri in un'esecuzione sono supportati dal tipo di carattere selezionato, l'applicazione chiama [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap). I caratteri non disponibili hanno il glifo predefinito nel buffer del glifo. Si noti che questo metodo ha esito negativo se un tipo di carattere esegue il rendering di un carattere utilizzando una combinazione di glifi anziché un solo glifo. Ad esempio, 00C9; È possibile eseguire il rendering della lettera MAIUSCOLa Latina E con ACUTo usando un glifo e un glifo acuto. Per determinare il supporto del tipo di carattere per una stringa che contiene questi tipi di punti di codice, l'applicazione può chiamare [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape). Per altre informazioni, vedere [uso dei motori di shaping](using-shaping-engines.md).

La funzione [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight) restituisce l'altezza del tipo di carattere dalla cache dei tipi di carattere. [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties) fornisce informazioni sull'elaborazione speciale necessaria per tutti gli script, indicizzati per script. Ad esempio, include la lingua primaria associata allo script, i dati che indicano se lo script è numerico e i dati che indicano se lo script è uno script complesso.

[**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth) restituisce la [larghezza ABC](uniscribe-glossary.md) di un glifo specificato, che potrebbe essere utile per la creazione di grafici di glifi. Tuttavia, non deve essere usato per la normale formattazione del testo di script complessi.

## <a name="related-topics"></a>Argomenti correlati

[Uso di Uniscribe](using-uniscribe.md)


 

 
