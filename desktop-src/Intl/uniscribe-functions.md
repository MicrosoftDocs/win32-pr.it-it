---
description: Questa sezione descrive le funzioni per la tipografia e per l'elaborazione di script complessi.
ms.assetid: 876e36f5-a91c-490b-87bd-b7cb4993f8c4
title: Funzioni di annullamento della sottoscrizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 547bdd2179e734120fe07c2ae774c8a066d9fd5d9db2be1262e67b505cbb04ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582191"
---
# <a name="uniscribe-functions"></a>Funzioni di annullamento della sottoscrizione

Questa sezione descrive le funzioni per la tipografia e per l'elaborazione di script complessi.



| Funzione                                                               | Descrizione                                                                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution)   | Applica le impostazioni di sostituzione delle cifre specificate alle strutture di stato dello script e del controllo script specificate.                                                                    |
| [**Proprietà ScriptApplyLogicalWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptapplylogicalwidth)             | Accetta una matrice di larghezze di avanzamento per un'esecuzione e genera una matrice di larghezze del glifo di avanzamento regolate.                                                                               |
| [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak)                                     | Recupera informazioni per determinare le interruzioni di riga.                                                                                                                                |
| [**ScriptCacheGetHeight**](/windows/desktop/api/Usp10/nf-usp10-scriptcachegetheight)                   | Recupera l'altezza del tipo di carattere attualmente memorizzato nella cache.                                                                                                                                |
| [**ScriptCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptcptox)                                     | Genera l'offset x dall'estremità sinistra o dal bordo iniziale di un'esecuzione al bordo iniziale o finale di un cluster di caratteri logici.                                          |
| [**ScriptFreeCache**](/windows/desktop/api/Usp10/nf-usp10-scriptfreecache)                             | Libera una cache di script.                                                                                                                                                             |
| [**ScriptGetCMap**](/windows/desktop/api/Usp10/nf-usp10-scriptgetcmap)                                 | Recupera gli indici dei glifi dei caratteri Unicode in una stringa in base alla tabella cmap TrueType o alla tabella cmap standard implementata per i tipi di carattere di tipo precedente.         |
| [**ScriptGetFontAlternateGlyphs**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontalternateglyphs)   | Recupera un elenco di glifi alternativi per un carattere specificato a cui è possibile accedere tramite una funzionalità OpenType specificata.                                                         |
| [**ScriptGetFontFeatureTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontfeaturetags)           | Recupera un elenco di funzionalità tipografiche per il sistema di scrittura definito per l'elaborazione OpenType.                                                                                  |
| [**ScriptGetFontLanguageTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontlanguagetags)         | Recupera un elenco di tag di lingua disponibili per l'elemento specificato e supportati da un tag di script specificato per l'elaborazione OpenType.                                  |
| [**ScriptGetFontProperties**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontproperties)             | Recupera informazioni dalla cache dei tipi di carattere sui glifi speciali utilizzati da un tipo di carattere.                                                                                                   |
| [**ScriptGetFontScriptTags**](/windows/desktop/api/Usp10/nf-usp10-scriptgetfontscripttags)             | Recupera un elenco di script disponibili nel tipo di carattere per l'elaborazione OpenType.                                                                                                        |
| [**Proprietà ScriptGetGlyphABCWidth**](/windows/desktop/api/Usp10/nf-usp10-scriptgetglyphabcwidth)               | Recupera la larghezza ABC di un glifo specificato.                                                                                                                                         |
| [**ScriptGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptgetlogicalwidths)               | Converte le larghezze di avanzamento del glifo per un tipo di carattere specifico in larghezze logiche.                                                                                                        |
| [**Proprietà ScriptGet**](/windows/desktop/api/Usp10/nf-usp10-scriptgetproperties)                     | Recupera informazioni sugli script correnti.                                                                                                                                  |
| [**ScriptIsComplex**](/windows/desktop/api/Usp10/nf-usp10-scriptiscomplex)                             | Determina se una stringa Unicode richiede un'elaborazione di script complessa.                                                                                                           |
| [**ScriptItemize**](/windows/desktop/api/Usp10/nf-usp10-scriptitemize)                                 | Suddivide una stringa Unicode in elementi modellabili singolarmente.                                                                                                                        |
| [**ScriptItemizeOpenType**](/windows/desktop/api/usp10/nf-usp10-scriptitemizeopentype)                 | Suddivide una stringa Unicode in elementi modellabili singolarmente e fornisce una matrice di tag di funzionalità per ogni elemento con forme per l'elaborazione OpenType.                                  |
| [**ScriptJustify**](/windows/desktop/api/Usp10/nf-usp10-scriptjustify)                                 | Crea una tabella di larghezze di avanzamento per consentire la giustificazione del testo quando viene passata alla [**funzione ScriptTextOut.**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                                   |
| [**ScriptLayout**](/windows/desktop/api/Usp10/nf-usp10-scriptlayout)                                   | Converte una matrice di livelli di incorporamento di esecuzione in una mappa di posizione da oggetto visivo a posizione logica e/o da logica a visualizzazione.                                                               |
| [**ScriptPlace**](/windows/desktop/api/Usp10/nf-usp10-scriptplace)                                     | Genera informazioni sulla larghezza di avanzamento del glifo e sull'offset bidimensionale dall'output di [**ScriptShape.**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                                       |
| [**ScriptPlaceOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptplaceopentype)                     | Genera glifi e attributi visivi per un'esecuzione Unicode con informazioni OpenType dall'output [**di ScriptShapeOpenType.**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                         |
| [**ScriptPositionSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptpositionsingleglyph)         | Posiziona un singolo glifo con una singola regolazione usando una funzionalità specificata fornita nel tipo di carattere per l'elaborazione OpenType.                                                         |
| [**ScriptRecordDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptrecorddigitsubstitution) | Legge le impostazioni di sostituzione di cifra e cifra native NLS (National Language Support) e le registra in [**una struttura SCRIPT \_ DIGITSUBSTITUTE.**](/windows/win32/api/usp10/ns-usp10-script_digitsubstitute) |
| [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape)                                     | Genera glifi e attributi visivi per un'esecuzione Unicode.                                                                                                                         |
| [**ScriptShapeOpenType**](/windows/desktop/api/Usp10/nf-usp10-scriptshapeopentype)                     | Genera glifi e attributi visivi per un'esecuzione Unicode con informazioni OpenType.                                                                                               |
| [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse)                     | Analizza una stringa di testo normale.                                                                                                                                                     |
| [**ScriptStringCPtoX**](/windows/desktop/api/Usp10/nf-usp10-scriptstringcptox)                         | Recupera la coordinata x per il bordo iniziale o finale di una posizione del carattere.                                                                                              |
| [**ScriptStringFree**](/windows/desktop/api/Usp10/nf-usp10-scriptstringfree)                           | Libera una struttura [**SCRIPT \_ STRING \_ ANALYSIS.**](script-string-analysis.md)                                                                                                     |
| [**ScriptStringGetLogicalWidths**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetlogicalwidths)   | Converte larghezze degli oggetti visivi in larghezze logiche.                                                                                                                                       |
| [**ScriptStringGetOrder**](/windows/desktop/api/Usp10/nf-usp10-scriptstringgetorder)                   | Crea una matrice che esegue il mapping di una posizione del carattere originale a una posizione del glifo.                                                                                                    |
| [**ScriptStringOut**](/windows/desktop/api/Usp10/nf-usp10-scriptstringout)                             | Visualizza una stringa generata da una chiamata precedente a [**ScriptStringAnalyse**](/windows/desktop/api/Usp10/nf-usp10-scriptstringanalyse) e, facoltativamente, aggiunge l'evidenziazione.                                               |
| [**ScriptString \_ pcOutChars**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_pcoutchars)            | Restituisce un puntatore alla lunghezza di una stringa dopo il ritaglio.                                                                                                                       |
| [**ScriptString \_ pLogAttr**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_plogattr)                | Restituisce un puntatore a un buffer di attributi logici per una stringa analizzata.                                                                                                          |
| [**ScriptString \_ pSize**](/windows/desktop/api/Usp10/nf-usp10-scriptstring_psize)                      | Restituisce un puntatore a [**una struttura SIZE**](/previous-versions//dd145106(v=vs.85)) per una stringa analizzata.                                                                                                     |
| [**ScriptStringValidate**](/windows/desktop/api/Usp10/nf-usp10-scriptstringvalidate)                   | Verifica la presenza di sequenze non valide in una struttura SCRIPT [**\_ STRING \_ ANALYSIS.**](script-string-analysis.md)                                                                              |
| [**ScriptStringXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptstringxtocp)                         | Converte una coordinata x in una posizione di carattere.                                                                                                                                 |
| [**ScriptSubstituteSingleGlyph**](/windows/desktop/api/Usp10/nf-usp10-scriptsubstitutesingleglyph)     | Consente la sostituzione di un singolo glifo con un formato alternativo dello stesso glifo per l'elaborazione OpenType.                                                                         |
| [**ScriptTextOut**](/windows/desktop/api/Usp10/nf-usp10-scripttextout)                                 | Visualizza il testo per la forma e le informazioni sulla posizione dello script specificate.                                                                                                               |
| [**ScriptXtoCP**](/windows/desktop/api/Usp10/nf-usp10-scriptxtocp)                                     | Genera il bordo iniziale o finale di un cluster di caratteri logici dall'offset x di un'esecuzione.                                                                                 |



 

 

 
