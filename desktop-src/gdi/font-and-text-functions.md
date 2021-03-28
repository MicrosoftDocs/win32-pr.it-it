---
description: Le funzioni seguenti vengono usate con i tipi di carattere e il testo.
ms.assetid: 69c04ed7-52da-4cb6-9fd2-f2a8c044df8b
title: Funzioni di tipo carattere e testo (Windows GDI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1a4dd6f000356dfb0e52c34fadef81bd6e8843e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528351"
---
# <a name="font-and-text-functions-windows-gdi"></a>Funzioni di tipo carattere e testo (Windows GDI)

Le funzioni seguenti vengono usate con i tipi di carattere e il testo.



| Funzione                                                   | Descrizione                                                                                                          |
|------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**AddFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontmemresourceex)       | Aggiunge un tipo di carattere incorporato alla tabella dei tipi di carattere di sistema.                                                                      |
| [**AddFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourcea)                 | Aggiunge una risorsa del tipo di carattere alla tabella dei tipi di carattere di sistema.                                                                       |
| [**AddFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-addfontresourceexa)             | Aggiunge un tipo di carattere privato o non enumerabile alla tabella dei tipi di carattere di sistema.                                                      |
| [**CreateFont**](/windows/desktop/api/Wingdi/nf-wingdi-createfonta)                           | Crea un tipo di carattere logico.                                                                                              |
| [**CreateFontIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirecta)           | Crea un tipo di carattere logico da una struttura.                                                                             |
| [**CreateFontIndirectEx**](/windows/desktop/api/Wingdi/nf-wingdi-createfontindirectexa)       | Crea un tipo di carattere logico da una struttura.                                                                             |
| [**DrawText**](/windows/desktop/api/Winuser/nf-winuser-drawtext)                               | Disegna il testo formattato in un rettangolo.                                                                                 |
| [**DrawTextEx**](/windows/desktop/api/Winuser/nf-winuser-drawtextexa)                           | Disegna il testo formattato nel rettangolo.                                                                                   |
| [**EnumFontFamExProc**](/previous-versions//dd162618(v=vs.85))             | Funzione definedcallback dell'applicazione usata con [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa) per elaborare i tipi di carattere. |
| [**EnumFontFamiliesEx**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesexa)           | Enumera tutti i tipi di carattere del sistema con determinate caratteristiche.                                                     |
| [**ExtTextOut**](/windows/desktop/api/Wingdi/nf-wingdi-exttextouta)                           | Disegna una stringa di caratteri.                                                                                            |
| [**GetAspectRatioFilterEx**](/windows/desktop/api/Wingdi/nf-wingdi-getaspectratiofilterex)   | Ottiene l'impostazione per il filtro proporzioni.                                                                        |
| [**GetCharABCWidths**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsa)               | Ottiene le larghezze dei caratteri consecutivi dal tipo di carattere TrueType.                                                    |
| [**GetCharABCWidthsFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsfloata)     | Ottiene le larghezze dei caratteri consecutivi dal tipo di carattere corrente.                                                     |
| [**GetCharABCWidthsI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharabcwidthsi)             | Ottiene le larghezze degli indici di glifi consecutivi o da una matrice di indici di glifi dal tipo di carattere TrueType.               |
| [**GetCharacterPlacement**](/windows/desktop/api/Wingdi/nf-wingdi-getcharacterplacementa)     | Ottiene informazioni su una stringa di caratteri.                                                                           |
| [**GetCharWidth32**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidth32a)                   | Ottiene le larghezze dei caratteri consecutivi dal tipo di carattere corrente.                                                     |
| [**GetCharWidthFloat**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthfloata)             | Ottiene le larghezze frazionarie dei caratteri consecutivi dal tipo di carattere corrente.                                          |
| [**GetCharWidthI**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidthi)                     | Ottiene le larghezze degli indici di glifi consecutivi o una matrice di indici di glifi dal tipo di carattere corrente.                     |
| [**GetFontData**](/windows/desktop/api/Wingdi/nf-wingdi-getfontdata)                         | Ottiene i dati della metrica per un tipo di carattere TrueType.                                                                                |
| [**GetFontLanguageInfo**](/windows/desktop/api/Wingdi/nf-wingdi-getfontlanguageinfo)         | Restituisce informazioni sul tipo di carattere selezionato per un contesto di visualizzazione.                                                   |
| [**GetFontUnicodeRanges**](/windows/desktop/api/Wingdi/nf-wingdi-getfontunicoderanges)       | Indica quali caratteri Unicode sono supportati da un tipo di carattere.                                                              |
| [**GetGlyphIndices**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphindicesa)                 | Converte una stringa in una matrice di indici di glifi.                                                                  |
| [**GetGlyphOutline**](/windows/desktop/api/Wingdi/nf-wingdi-getglyphoutlinea)                 | Ottiene la struttura o la bitmap per un carattere nel tipo di carattere TrueType.                                                     |
| [**GetKerningPairs**](/windows/desktop/api/WinGdi/nf-wingdi-getkerningpairsa)                 | Ottiene le coppie di caratteri di crenatura per un tipo di carattere.                                                                         |
| [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)     | Ottiene la metrica del testo per i tipi di carattere TrueType.                                                                                |
| [**GetRasterizerCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getrasterizercaps)             | Indica se i tipi di carattere TrueType sono installati.                                                                          |
| [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta)         | Calcola la larghezza e l'altezza di una stringa di caratteri, incluse le schede.                                                 |
| [**GetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-gettextalign)                       | Ottiene l'impostazione di allineamento del testo per un contesto di dispositivo.                                                                |
| [**GetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharacterextra)     | Ottiene la spaziatura tra i caratteri corrente per un contesto di dispositivo.                                                        |
| [**GetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcolor)                       | Ottiene il colore del testo per un contesto di dispositivo.                                                                            |
| [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa)       | Ottiene il numero di caratteri in una stringa che rientrerà in uno spazio.                                              |
| [**GetTextExtentExPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointi)     | Ottiene il numero di indici di glifi che rientreranno in uno spazio.                                                       |
| [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)       | Calcola la larghezza e l'altezza di una stringa di testo.                                                                   |
| [**GetTextExtentPointI**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpointi)         | Calcola la larghezza e l'altezza di una matrice di indici di glifi.                                                          |
| [**GetTextFace**](/windows/desktop/api/Wingdi/nf-wingdi-gettextfacea)                         | Ottiene il nome del tipo di carattere selezionato in un contesto di dispositivo.                                                    |
| [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics)                   | Riempie un buffer con le metriche per un tipo di carattere.                                                                          |
| [**Sottotesto**](/windows/desktop/api/Wingdi/nf-wingdi-polytextouta)                         | Disegna diverse stringhe usando il tipo di carattere e i colori del testo in un contesto di dispositivo.                                            |
| [**RemoveFontMemResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontmemresourceex) | Rimuove un tipo di carattere la cui origine è incorporata in un documento della tabella dei tipi di carattere di sistema.                                   |
| [**RemoveFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourcea)           | Rimuove i tipi di carattere in un file dalla tabella dei tipi di carattere di sistema.                                                              |
| [**RemoveFontResourceEx**](/windows/desktop/api/Wingdi/nf-wingdi-removefontresourceexa)       | Rimuove un tipo di carattere privato o non enumerabile dalla tabella dei tipi di carattere di sistema.                                                 |
| [**SetMapperFlags**](/windows/desktop/api/Wingdi/nf-wingdi-setmapperflags)                   | Modifica l'algoritmo utilizzato per eseguire il mapping di tipi di carattere logici a tipi di carattere fisici.                                                    |
| [**SetTextAlign**](/windows/desktop/api/Wingdi/nf-wingdi-settextalign)                       | Imposta i flag di allineamento del testo per un contesto di dispositivo.                                                                  |
| [**SetTextCharacterExtra**](/windows/desktop/api/Wingdi/nf-wingdi-settextcharacterextra)     | Imposta la spaziatura tra caratteri.                                                                                     |
| [**SetTextColor**](/windows/desktop/api/Wingdi/nf-wingdi-settextcolor)                       | Imposta il colore del testo per un contesto di dispositivo.                                                                            |
| [**SetTextJustification**](/windows/desktop/api/Wingdi/nf-wingdi-settextjustification)       | Specifica la quantità di spazio che il sistema deve aggiungere ai caratteri di pausa in una stringa.                             |
| [**TabbedTextOut**](/windows/desktop/api/Winuser/nf-winuser-tabbedtextouta)                     | Scrive una stringa di caratteri in una posizione, espandendo le schede ai valori specificati.                                         |
| [**TextOut**](/windows/desktop/api/Wingdi/nf-wingdi-textouta)                                 | Scrive una stringa di caratteri in una posizione.                                                                             |



 

## <a name="obsolete-functions"></a>Funzioni obsolete

Queste funzioni vengono fornite solo per la compatibilità con le versioni di Windows a 16 bit.

-   [**CreateScalableFontResource**](/windows/desktop/api/Wingdi/nf-wingdi-createscalablefontresourcea)
-   [**EnumFontFamilies**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontfamiliesa)
-   [**EnumFontFamProc**](/previous-versions//dd162621(v=vs.85))
-   [**EnumFonts**](/windows/desktop/api/Wingdi/nf-wingdi-enumfontsa)
-   [**EnumFontsProc**](/previous-versions//dd162623(v=vs.85))
-   [**GetCharWidth**](/windows/desktop/api/Wingdi/nf-wingdi-getcharwidtha)
-   [**GetTextExtentPoint**](/windows/desktop/api/WinGdi/nf-wingdi-gettextextentpointa)

 

 
