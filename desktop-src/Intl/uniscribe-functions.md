---
description: In questa sezione vengono descritte le funzioni per la tipografia e l'elaborazione di script complessi.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funzioni Uniscribe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f623c8da04f985f88d091f8e9e2b4cb724c0801
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319490"
---
# <a name="uniscribe-functions"></a>Funzioni Uniscribe

In questa sezione vengono descritte le funzioni per la tipografia e l'elaborazione di script complessi.



| Funzione                                                               | Descrizione                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Applica le impostazioni di sostituzione delle cifre specificate al controllo script specificato e alle strutture dello stato dello script.                                                                    |
| [**ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Accetta una matrice di larghezze di avanzamento per un'esecuzione e genera una matrice di larghezze del glifo di avanzamento modificate.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera le informazioni per determinare le interruzioni di riga.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera l'altezza del tipo di carattere attualmente memorizzato nella cache.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Genera l'offset x dall'estremità sinistra o dal bordo principale di un'esecuzione al bordo principale o finale di un cluster di caratteri logici.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera una cache di script.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera gli indici di glifo dei caratteri Unicode in una stringa in base alla tabella CMAP di TrueType o alla tabella CMAP standard implementata per i tipi di carattere obsoleti.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera un elenco di glifi alternativi per un carattere specificato a cui è possibile accedere tramite una caratteristica OpenType specificata.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera un elenco di funzionalità tipografiche per il sistema di scrittura definito per l'elaborazione OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera un elenco di tag di lingua disponibili per l'elemento specificato e supportati da un tag di script specificato per l'elaborazione OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera le informazioni dalla cache dei tipi di carattere nei glifi speciali utilizzati da un tipo di carattere.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera un elenco di script disponibili nel tipo di carattere per l'elaborazione OpenType.                                                                                                        |
| [**ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera la larghezza ABC di un glifo specificato.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Converte le larghezze di avanzamento del glifo per un tipo di carattere specifico in larghezze logiche.                                                                                                        |
| [**ScriptGetProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera le informazioni sugli script correnti.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina se una stringa Unicode richiede l'elaborazione di script complessi.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Suddivide una stringa Unicode in elementi formabili singolarmente.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Suddivide una stringa Unicode in elementi formabili singolarmente e fornisce una matrice di tag di funzionalità per ogni elemento formabile per l'elaborazione OpenType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Crea una tabella di larghezze avanzate per consentire la giustificazione del testo quando viene passata alla funzione [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout) .                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Converte una matrice di livelli di incorporamento dell'esecuzione in una mappa di posizione da Visual a logica e/o da una posizione logica a un oggetto visivo.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Genera la larghezza di avanzamento del glifo e le informazioni sull'offset bidimensionale dall'output di [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape).                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Genera glifi e attributi visivi per un'esecuzione Unicode con informazioni OpenType dall'output di [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype).                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Posiziona un singolo glifo con una singola regolazione utilizzando una funzionalità specificata nel tipo di carattere per l'elaborazione OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Legge le impostazioni di sostituzione delle cifre e delle cifre native del supporto tecnico nazionale (NLS) e le registra in una struttura [**\_ DIGITSUBSTITUTE dello script**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) . |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Genera glifi e attributi visivi per un'esecuzione Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Genera glifi e attributi visivi per un'esecuzione Unicode con informazioni OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analizza una stringa di testo normale.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera la coordinata x per il bordo principale o finale di una posizione del carattere.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera una struttura [**di \_ \_ analisi della stringa di script**](script-string-analysis.md) .                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Converte le larghezze visive in larghezze logiche.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Crea una matrice che esegue il mapping di una posizione del carattere originale a una posizione del glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Visualizza una stringa generata da una chiamata precedente a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) e, facoltativamente, aggiunge l'evidenziazione.                                               |
| [**\_PcOutChars scriptString**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Restituisce un puntatore alla lunghezza di una stringa dopo il ritaglio.                                                                                                                       |
| [**\_PLogAttr scriptString**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Restituisce un puntatore a un buffer di attributi logici per una stringa analizzata.                                                                                                          |
| [**\_PSize scriptString**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Restituisce un puntatore a una struttura di [**dimensioni**](/previous-versions//dd145106(v=vs.85)) per una stringa analizzata.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Verifica la presenza di sequenze non valide in una struttura di [**\_ \_ analisi della stringa di script**](script-string-analysis.md) .                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Converte una coordinata x in una posizione del carattere.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Consente la sostituzione di un singolo glifo con una forma alternativa dello stesso glifo per l'elaborazione OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Visualizza il testo per la forma di script specificata e inserisce le informazioni.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Genera il bordo principale o finale di un cluster di caratteri logici dall'offset x di un'esecuzione.                                                                                 |



 

 

 
