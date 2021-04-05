---
title: Giustificazione, crenatura e spaziatura
description: A partire da Windows 8, DirectWrite offre una serie di funzionalità che consentono di controllare le funzionalità tipografiche, di layout e di spaziatura di base, ad esempio la spaziatura dei caratteri, la crenatura delle coppie e la giustificazione.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17cc915922d0dbadb45bf47f223df83a25414daf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729831"
---
# <a name="justification-kerning-and-spacing"></a>Giustificazione, crenatura e spaziatura

A partire da Windows 8, [DirectWrite](direct-write-portal.md) offre una serie di funzionalità che consentono di controllare le funzionalità tipografiche, di layout e di spaziatura di base, ad esempio la spaziatura dei caratteri, la crenatura delle coppie e la giustificazione.

## <a name="character-spacing"></a>Spaziatura caratteri

La spaziatura dei caratteri, nota anche come "rilevamento", è la spaziatura tra i caratteri in un'esecuzione di testo.

Di seguito è riportato un esempio di rilevamento. La prima riga non applica alcun rilevamento al testo. La seconda riga aumenta la spaziatura dei caratteri e la terza riga riduce la spaziatura dei caratteri.

![tre esempi dello stesso testo senza rilevamento, maggiore spaziatura e minore spaziatura.](images/spacing.png)

A partire da Windows 8, [DirectWrite](direct-write-portal.md) aggiunge questi metodi per controllare la spaziatura dei caratteri nel testo.

Se si usa il layout [DirectWrite](direct-write-portal.md) , è possibile usare i metodi [**IDWriteTextLayout1:: GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) e [**IDWriteTextLayout1:: SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) per questo scopo.

Usare il metodo [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) per determinare la spaziatura dei caratteri corrente e restituisce il carattere corrente, la spaziatura prima e dopo il carattere, la larghezza minima di avanzamento e una struttura di [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che contiene informazioni sulla posizione iniziale e la lunghezza del testo rimanente.

Usare [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) su un'interfaccia [**DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) per applicare la spaziatura dei caratteri al testo nel layout. Il metodo **SetCharacterSpacing** accetta la quantità di spazio desiderata prima e dopo il carattere, l'avanzamento minimo consentito e un [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che definisce l'intervallo per applicare la spaziatura.

Se si usa un layout personalizzato, [DirectWrite](direct-write-portal.md) dispone del supporto per l'impostazione della spaziatura dei caratteri con [**IDWriteTextAnalyzer1:: ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Utilizzare questo metodo se è necessario un layout di testo personalizzato per avere un controllo avanzato sul layout. Questo metodo consente di fornire **ApplyCharacterSpacing** con spazi iniziali e finali, larghezza minima di avanzamento, lunghezza della mappa del cluster, numero di glifi, mapping da intervalli di caratteri a glifi e larghezza di avanzamento di ogni glifo se si utilizza un layout personalizzato. Il metodo restituisce gli avanzamenti del glifo modificati e un'enumerazione di [**\_ \_ offset del glifo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) con i nuovi offset all'origine di ogni glifo.

## <a name="kerning"></a>Crenatura

La crenatura è la regolazione della spaziatura contestuale tra coppie o triplette di lettere. Una spaziatura specifica tra set di caratteri può migliorare la leggibilità e rendere il testo migliore. La differenza importante tra la crenatura e la spaziatura dei caratteri è costituita dal fatto che la spaziatura tra le lettere è indipendente dal testo it Spaces, mentre la crenatura viene utilizzata in determinate situazioni tra alcune coppie di caratteri come definito nel tipo di carattere.

L'immagine è un esempio di crenatura. Per rendere la parola più naturale, l'AVATAR di Word sulla riga superiore è stato kernato. Come è possibile osservare dalle caselle rosse attorno ai caratteri, viene applicata una maggiore spaziatura tra le prime quattro lettere, mentre la R alla fine ha più spazio prima di esso. Il testo originale senza crenatura si trova nella seconda riga. La crenatura in questo esempio rende la parola più leggibile e più naturale.

![un esempio della stessa parola con e senza la crenatura applicata.](images/kerning.png)

Il carattere avanza tra le coppie di caratteri che il carattere Kerns viene archiviato nella tabella Kern e [DirectWrite](direct-write-portal.md) analizza la tabella e restituisce le informazioni tramite le API di crenatura.

Se si vuole sapere se un tipo di carattere supporta la crenatura delle coppie, è possibile usare il metodo [**IDWriteFontFace1:: HasKerningPairs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) . Questo metodo restituisce un valore bool pari a 1 se il tipo di carattere supporta le coppie di crenatura.

Il [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) dispone anche di un metodo che consente di ottenere l'accesso alle regolazioni della coppia di crenatura per gli indici di glifi. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) consente di inserire una matrice di indici di glifi e [DirectWrite](direct-write-portal.md) restituisce una matrice di modifiche di avanzamento dei glifi. Se un tipo di carattere non supporta la tabella Kern, il metodo restituisce zeri per le regolazioni di avanzamento dell'icona.

Se si usa il layout [DirectWrite](direct-write-portal.md) , sono disponibili due metodi sull'interfaccia [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) che consentono di impostare la crenatura delle coppie e altre informazioni sulla crenatura delle coppie nel layout. Il metodo [**SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) accetta una rappresentazione booleana che indica se si vuole che la crenatura delle coppie sia abilitata e un [**\_ \_ intervallo di testo DWrite**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che definisce l'intervallo di testo a cui applicare l'oggetto. Per sapere se la crenatura delle coppie è abilitata o meno in un intervallo di testo, è possibile usare il metodo [**GetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) , che accetta la posizione corrente e restituisce un valore bool corrispondente a se è abilitata o meno la crenatura delle coppie e l'intervallo di testo a cui si applica l'impostazione di crenatura.

## <a name="justification"></a>Giustificazione

La giustificazione è il processo di allineamento del testo in modo che riempia tutto lo spazio all'interno di una colonna aumentando i progressi tra i caratteri o i cluster di glifi oppure aggiungendo caratteri di giustificazione per ottenere lo stesso effetto. In generale, questa operazione viene eseguita determinando la posizione in cui deve essere aggiunto lo spazio a una riga di testo e inserendo caratteri di spaziatura in tali opportunità. Questi elementi di spaziatura possono variare anche in alfabeto latino. il testo è giustificato dall'aumento delle larghezze di avanzamento tra gli elementi, mentre in arabo il testo è giustificato da un Kashida. Di seguito è riportato un esempio di script arabo e latino sia giustificato che non giustificato.

![un esempio di script arabo e latino è giustificato e non giustificato.](images/justification.png)

A partire da Windows 8, [DirectWrite](direct-write-portal.md) dispone di una serie di metodi che consentono di giustificare il testo nelle app.

È presente un valore aggiuntivo nell'enumerazione [**dell' \_ \_ allineamento del testo DWrite**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) . È possibile utilizzare il metodo [**SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e passare la costante **\_ \_ \_ giustificata dell'allineamento del testo DWrite** e [DirectWrite](direct-write-portal.md) giustifica il testo e inserisce il carattere di giustificazione appropriato per lo script.

Se si usa un layout personalizzato, sono disponibili diversi metodi per poter sfruttare la giustificazione. [DirectWrite](direct-write-portal.md) dispone di tre metodi sull'interfaccia [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) che è possibile usare per aggiungere la giustificazione a un layout personalizzato.

Il primo metodo è [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities), che accetta il testo che si desidera giustificare e restituisce una struttura [**di \_ \_ opportunità di giustificazione DWrite**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) che delinea dove è possibile aggiungere i caratteri giustificativi per giustificare il testo.

La seconda funzione è [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances), che giustifica una matrice di avanzamenti del glifo in modo che corrispondano alla lunghezza della linea. Questo metodo accetta la struttura [**di \_ \_ opportunità di giustificazione DWrite**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) generata da [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) , il glifo avanza e gli offset del glifo. Genera quindi gli avanzamenti del glifo giustificati e un'enumerazione dell' [**\_ \_ offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) del glifo DWrite che contiene gli offset del glifo giustificati.

La terza funzione è [**GetJustifiedGlyphs**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs), che compila i nuovi glifi per gli script complessi in cui la giustificazione ha aumentato i progressi per i glifi. **GetJustifiedGlyphs** deve essere chiamato solo se lo script ha un carattere di giustificazione specifico come restituito da [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Questo metodo accetta informazioni sul tipo di carattere, sulla lunghezza del testo, sulle dimensioni em dei glifi, sullo script del testo, sul numero di glifi, sulla mappa del cluster, sugli spostamenti/offset del glifo originale, sugli spostamenti/offset del glifo giustificati e sulle proprietà del glifo. Il metodo restituisce il numero effettivo di glifi, mappa del cluster aggiornata, indici di glifi aggiornati con glifi di giustificazione inseriti, offset del glifo aggiornati e avanzamenti del glifo aggiornati.

 

 