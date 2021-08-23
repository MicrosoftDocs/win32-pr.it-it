---
title: Giustificazione, crenatura e spaziatura
description: A partire da Windows 8, DirectWrite offre una serie di funzionalità che consentono di controllare le funzionalità tipografiche, di layout e di spaziatura di base, ad esempio la spaziatura dei caratteri, la crenatura delle coppie e la giustificazione.
ms.assetid: A5397132-0806-4842-8B82-E17925FBBBA9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fdd82e201429adb62e687021f003d7d5d6bedcd228c3102f448b04d1f079f71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632655"
---
# <a name="justification-kerning-and-spacing"></a>Giustificazione, crenatura e spaziatura

A partire da Windows 8, [DirectWrite](direct-write-portal.md) offre una serie di funzionalità che consentono di controllare le funzionalità tipografiche, di layout e di spaziatura di base, ad esempio la spaziatura dei caratteri, la crenatura delle coppie e la giustificazione.

## <a name="character-spacing"></a>Spaziatura caratteri

La spaziatura dei caratteri, nota anche come "rilevamento", è la spaziatura tra i caratteri in un'esecuzione di testo.

Di seguito è riportato un esempio di rilevamento. La prima riga non applica alcun rilevamento al testo. La seconda riga aumenta la spaziatura dei caratteri e la terza riga riduce la spaziatura dei caratteri.

![tre esempi dello stesso testo senza rilevamento, maggiore spaziatura e meno spaziatura.](images/spacing.png)

A partire Windows 8, [DirectWrite](direct-write-portal.md) questi metodi vengono aggiunti qui per controllare la spaziatura dei caratteri nel testo.

Se si usa il layout [DirectWrite,](direct-write-portal.md) è possibile usare i metodi [**IDWriteTextLayout1::GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) e [**IDWriteTextLayout1::SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) a questo scopo.

Usare il metodo [**GetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getcharacterspacing) per determinare la spaziatura dei caratteri corrente e restituisce il carattere corrente, la spaziatura prima e dopo il carattere, la larghezza minima di avanzamento e una struttura [**DWRITE \_ TEXT \_ RANGE**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che contiene informazioni sulla posizione iniziale e sulla lunghezza del testo rimanente.

Usare [**SetCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setcharacterspacing) in [**un'interfaccia DWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) per applicare la spaziatura dei caratteri personalizzata al testo nel layout. Il **metodo SetCharacterSpacing** accetta la quantità di spazio desiderata prima e dopo il carattere, l'avanzamento minimo consentito e un intervallo di testo [**DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che definisce l'intervallo per applicare la spaziatura.

Se si usa un layout [personalizzato,](direct-write-portal.md) DirectWrite il supporto per l'impostazione della spaziatura dei caratteri [**con IDWriteTextAnalyzer1::ApplyCharacterSpacing**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-applycharacterspacing). Usare questo metodo se è necessario un layout di testo personalizzato per avere un controllo avanzato sul layout. Questo metodo consente di specificare **ApplyCharacterSpacing** con la spaziatura iniziale e finale, la larghezza minima di avanzamento, la lunghezza della mappa cluster, il numero di glifi, il mapping dagli intervalli di caratteri ai glifi e la larghezza di avanzamento di ogni glifo se si usa un layout personalizzato. Il metodo restituisce gli avanzamenti del glifo modificato e un'enumerazione [**DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) con i nuovi offset all'origine di ogni glifo.

## <a name="kerning"></a>Crenatura

La crenatura è la regolazione della spaziatura contestuale tra coppie o triplette di lettere. La spaziatura specifica tra set di caratteri può aumentare la leggibilità e migliorare l'aspetto del testo. L'importante differenza tra la crenatura e la spaziatura dei caratteri è il fatto che la spaziatura tra lettere è indipendente dal testo spaziato, mentre la crenatura viene usata in determinate situazioni tra determinate coppie di caratteri come definito nel tipo di carattere.

L'immagine è un esempio di crenatura. La parola AVATAR nella riga superiore viene crenatura per rendere la parola più naturale. Come si può vedere dalle caselle rosse intorno ai caratteri, tra le prime quattro lettere viene applicata più spaziatura, mentre la R alla fine ha più spazio prima di essa. Il testo originale senza crenatura si trova nella seconda riga. La crenatura in questo esempio rende la parola più leggibile e naturale.

![un esempio della stessa parola con e senza crenatura applicata.](images/kerning.png)

Il carattere avanza tra coppie di caratteri in cui le crenatura dei caratteri vengono archiviate nella tabella kern e [DirectWrite](direct-write-portal.md) analizza la tabella e restituisce le informazioni tramite le API di crenatura.

Per sapere se un tipo di carattere supporta o meno la crenatura delle coppie, è possibile usare il metodo [**IDWriteFontFace1::HasKerningPairs.**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-haskerningpairs) Questo metodo restituisce un valore bool pari a 1 se il tipo di carattere supporta coppie di crenatura.

[**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) include anche un metodo che consente di ottenere l'accesso alle modifiche della coppia di crenatura per gli indici dei glifi. [**GetKerningPairAdjustments**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritefontface1-getkerningpairadjustments) consente di immettere una matrice di indici di glifi [e](direct-write-portal.md) DirectWrite una matrice di regolazioni di avanzamento degli glifi. Se un tipo di carattere non supporta la tabella kern, il metodo restituisce zeri per le regolazioni di avanzamento del glifo.

Se si usa il layout [DirectWrite,](direct-write-portal.md) nell'interfaccia [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) sono disponibili due metodi che consentono di impostare la crenatura delle coppie e di ottenere altre informazioni sulla crenatura delle coppie nel layout. Il [**metodo SetPairKerning**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-setpairkerning) accetta una rappresentazione booleana di se si vuole o meno la crenatura delle coppie abilitata e un intervallo di testo [**DWRITE \_ \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_text_range) che definisce l'intervallo di testo a cui applicarla. Se si vuole sapere se la crenatura delle coppie è abilitata o meno in un intervallo di testo, è possibile usare il metodo [**GetPairKerning,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextlayout1-getpairkerning) che accetta la posizione corrente e restituisce un valore bool corrispondente a se la crenatura della coppia è abilitata o meno e all'intervallo di testo a cui si applica l'impostazione di crenatura.

## <a name="justification"></a>Giustificazione

La giustificazione è il processo di allineamento del testo in modo che riempia tutto lo spazio all'interno di una colonna aumentando gli avanzamenti tra i caratteri o i cluster di glifi o aggiungendo caratteri di giustificazione per ottenere lo stesso effetto. In generale, questa operazione viene eseguita determinando dove deve essere aggiunto spazio a una riga di testo e inserendo caratteri di spaziatura nelle opportunità di interruzione. Anche questi elementi di spaziatura possono differire, negli script latini il testo è giustificato aumentando la larghezza di avanzamento tra gli elementi, mentre in arabo il testo è giustificato con un kashida. Ecco un esempio di alfabeto arabo e latino sia giustificato che non giustificato.

![un esempio di alfabeto arabo e latino sia giustificato che non giustificato.](images/justification.png)

A partire Windows 8, [DirectWrite](direct-write-portal.md) diversi metodi che consentono di giustificare il testo nelle app.

È presente un valore aggiuntivo [**nell'enumerazione DWRITE \_ TEXT \_ ALIGNMENT.**](/windows/win32/api/dwrite/ne-dwrite-dwrite_text_alignment) È possibile usare il [**metodo SetTextAlignment**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-settextalignment) e passare la costante **DWRITE \_ TEXT ALIGNMENT \_ \_ JUSTIFIED** e [DirectWrite](direct-write-portal.md) giustifica il testo e inserisce il carattere di giustificazione appropriato per lo script.

Se si usa un layout personalizzato, sono disponibili diversi metodi per poter sfruttare la giustificazione. [DirectWrite](direct-write-portal.md) dispone di tre metodi [**sull'interfaccia IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) che è possibile usare per aggiungere giustificazione a un layout personalizzato.

Il primo metodo è [**GetJustificationOpportunities**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities), che accetta il testo da giustificare e restituisce una struttura [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) che indica dove è possibile aggiungere caratteri di giustificazione per giustificare il testo.

La seconda funzione è [**JustifyGlyphAdvances**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-justifyglyphadvances), che giustifica l'avanzamento di una matrice di glifi in modo che si adattino alla larghezza della riga. Questo metodo accetta la struttura [**DWRITE \_ JUSTIFICATION \_ OPPORTUNITY**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_justification_opportunity) generata da [**GetJustificationOpportunities,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustificationopportunities) il glifo avanza e gli offset del glifo. Genera quindi gli avanzamenti giustificati del glifo e un'enumerazione [**DWRITE \_ GLYPH \_ OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset) che contiene gli offset giustificati del glifo.

La terza funzione è [**GetJustifiedGlyphs,**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getjustifiedglyphs)che compila i nuovi glifi per gli script complessi in cui la giustificazione ha aumentato i progressi per i glifi. **GetJustifiedGlyphs** deve essere chiamato solo se lo script ha un carattere di giustificazione specifico come restituito da [**GetScriptProperties**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties). Questo metodo accetta informazioni sul tipo di carattere, la lunghezza del testo, le dimensioni em dei glifi, lo script del testo, il numero di glifi, la mappa del cluster, gli avanzamenti/offset del glifo originale, gli avanzamenti/offset giustificati del glifo e le proprietà del glifo. Il metodo restituisce il conteggio effettivo dei glifi, la mappa cluster aggiornata, gli indici dei glifi aggiornati con i glifi di giustificazione inseriti, gli offset aggiornati dei glifi e gli avanzamenti dei glifi aggiornati.

 

 