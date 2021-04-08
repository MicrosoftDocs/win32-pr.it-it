---
description: Le applicazioni possono utilizzare Unicode per rappresentare stringhe in più formati.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Uso della normalizzazione Unicode per rappresentare le stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad452db3bc20518320afcf77e5f6483e010cd144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885717"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Uso della normalizzazione Unicode per rappresentare le stringhe

Le applicazioni possono utilizzare Unicode per rappresentare stringhe in più formati. Poiché l'accettazione Unicode è cresciuta, in particolare tramite Internet, è stata creata la necessità di eliminare le differenze non essenziali nelle stringhe Unicode. Più rappresentazioni per una combinazione di caratteri complicano il software, ad esempio quando un server Web risponde a una richiesta di pagina o un linker cerca un identificatore specifico in una libreria.

> [!Caution]  
> Diverse stringhe Unicode possono sembrare visivamente identiche, aumentando i problemi di sicurezza. Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

In risposta a questo requisito, il Consorzio Unicode ha definito un processo denominato "normalizzazione", che produce una rappresentazione binaria per le rappresentazioni binarie equivalenti di un carattere. Una volta normalizzate, due stringhe sono equivalenti se e solo se hanno rappresentazioni binarie identiche. La normalizzazione Elimina alcune differenze, ma conserva le maiuscole e minuscole.

Per utilizzare la normalizzazione Unicode, un'applicazione può chiamare le funzioni [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) per la ridisposizione delle stringhe ACCCORDING a Unicode 4,0 TR \# 15. La normalizzazione può contribuire a migliorare la sicurezza riducendo le rappresentazioni di stringa alternative con lo stesso significato linguistico. Tenere presente, tuttavia, che la normalizzazione non può eliminare completamente rappresentazioni alternative.

Per una descrizione dettagliata degli standard Unicode per la normalizzazione, vedere Unicode [Standard Annex \# 15: Unicode Normalizzation Forms](https://www.unicode.org/reports/tr15) (UAX \# 15).

> [!Caution]  
> Poiché la normalizzazione può modificare il formato di una stringa, i meccanismi di sicurezza o gli algoritmi di convalida dei caratteri devono essere implementati in genere dopo la normalizzazione. Per ulteriori informazioni, vedere [considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Fornire più rappresentazioni della stessa stringa

In molti casi, Unicode consente più rappresentazioni di ciò che è linguisticamente la stessa stringa. Ad esempio:

-   La lettera maiuscola con dieresis (dieresi) può essere rappresentata come un singolo punto di codice Unicode "Ä" (U + 00C4) o con la combinazione di maiuscole e minuscole ("A" + "̈", ovvero U + 0041 U + 0308). Considerazioni simili sono valide per molti altri caratteri con segni diacritici.
-   La lettera maiuscola a se stessa può essere rappresentata nel modo consueto (Latin capital letter A, U + 0041) o fullwidth Latin capital lettera A (U + FF21). Considerazioni simili sono valide per le altre semplici lettere latine (sia maiuscole che minuscole) e per i caratteri katakana usati per la scrittura in giapponese.
-   La stringa "Fi" può essere rappresentata dai caratteri "f" e "i" (U + 0066 U + 0069) o dalla legatura "Fi" (U + FB01). Considerazioni simili si applicano a molte altre combinazioni di caratteri per le quali Unicode definisce legature.

## <a name="use-the-four-defined-normalization-forms"></a>Usare i quattro formati di normalizzazione definiti

Le applicazioni possono eseguire la normalizzazione Unicode usando diversi algoritmi, detti "forme di normalizzazione", che rispettano diverse regole. Unicode Consortium ha definito quattro forme di normalizzazione: NFC (form C), NFD (form D), NFKC (form KC) e NFKD (form KD). Ogni modulo Elimina alcune differenze, ma conserva i casi. Win32 e il .NET Framework supportano tutti e quattro i form di normalizzazione.

Il [**\_ modulo**](/windows/desktop/api/Winnls/ne-winnls-norm_form) NLS Enumeration Type Norm supporta i quattro formati standard di normalizzazione Unicode. I form C e D forniscono forme canoniche per le stringhe. Le forme non canoniche KC e KD forniscono una maggiore compatibilità e possono rivelare determinate equivalenze semantiche che non sono evidenti nei moduli C e D. Tuttavia, lo fanno a scapito di una certa perdita di informazioni e in genere non devono essere usate come metodo canonico per archiviare le stringhe.

Tra le due forme canoniche, il form C è un formato "composto" e il form D è un formato "decomposto". Ad esempio, il form C usa il singolo punto di codice Unicode "Ä" (U + 00C4), mentre il form D USA ("A" + "̈", ovvero U + 0041 U + 0308). Questi rendering sono identici, perché "̈" (U + 0308) è un carattere di combinazione. Il form D può utilizzare un numero qualsiasi di punti di codice per rappresentare un singolo punto di codice utilizzato dal form C.

Se due stringhe sono identiche in entrambi i form C o form D, sono identiche nell'altro form. Inoltre, quando il rendering viene eseguito correttamente, vengono visualizzati in modo indistinguibile l'uno dall'altro e dalla stringa originale non normalizzata.

Una volta normalizzate, le stringhe non possono essere restituite in modo coerente alla relativa rappresentazione originale. Se, ad esempio, una stringa con una combinazione di rappresentazioni di caratteri composti e scomposti viene convertita in un formato normalizzato, non è possibile denormalizzarla nella stringa mista originale. Pertanto, se un'applicazione richiede la rappresentazione originale della stringa, deve archiviare in modo esplicito tale rappresentazione. Tuttavia, la conversione tra le due forme canoniche è reversibile. Una stringa nel formato C può essere convertita in forma D, quindi di nuovo nel form C e il risultato è identico alla stringa C del formato originale.

I moduli KC e KD sono simili rispettivamente ai form C e D, ma questi "moduli di compatibilità" hanno mapping aggiuntivi di caratteri compatibili alla forma di base di ogni carattere. Tali mapping possono causare la perdita delle variazioni dei caratteri secondari. Combinano alcuni caratteri visivamente distinti. Ad esempio, combinano caratteri a larghezza intera e a metà larghezza con lo stesso significato semantico, o forme diverse della stessa lettera araba, o la legatura "Fi" (U + FB01) e la coppia di caratteri "Fi" (U + 0066 U + 0069). Combinano anche alcuni caratteri che talvolta possono avere un significato semantico diverso, ad esempio una cifra scritta come apice, come indice o racchiuso in un cerchio. A causa di questa perdita di informazioni, i moduli KC e KD in genere non devono essere usati come forme canoniche di stringhe, ma sono utili per alcune applicazioni.

Il formato KC è un formato composto e il formato KD è un formato decomposto. L'applicazione può andare avanti e indietro tra i form KC e KD, ma non esiste un modo coerente per passare dal formato KC o KD alla stringa originale, anche se la stringa originale è nel formato C o D.

Windows, le applicazioni Microsoft e i .NET Framework in genere generano caratteri nel form C utilizzando i normali metodi di input. Per la maggior parte degli scopi di Windows, form C è il formato preferito. Ad esempio, i caratteri nel formato C sono prodotti da input da tastiera di Windows. Tuttavia, i caratteri importati dal Web e da altre piattaforme possono introdurre altri moduli di normalizzazione nel flusso di dati.

Gli esempi seguenti sono tratti da UAX \# 15 e illustrano le differenze tra i quattro moduli di normalizzazione.



<table>
<thead>
<tr class="header">
<th>Originale</th>
<th>Form D</th>
<th>Form C</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Il ffi_ligature (U + FB03) non è scomposto, perché include un mapping di compatibilità, non un mapping canonico. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä \ uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Il numero romano IV (U + 2163) non è scomposto. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dieci</td>
<td>ga</td>
<td rowspan="5">Diversi equivalenti di compatibilità di un singolo carattere giapponese non comportano la stessa stringa nel formato C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dieci</td>
<td>Ka + dieci</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>
<td>hw_ka + hw_ten</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>
<td>Ka + hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka + dieci</td>
<td>hw_ka + dieci</td>
<td>hw_ka + dieci</td>

</tr>
<tr class="even">
<td>Mario</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>Mario</td>
<td>Le sillabe hangul vengono mantenute in normalizzazione.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Originale</th>
<th>Modulo KD</th>
<th>Formato KC</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Il ffi_ligature (U + FB03) viene scomposto nel formato KC, ma non nel formato C. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä \ uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td rowspan="2">Le stringhe risultanti sono identiche nel formato KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry IV&quot;</td>
<td>&quot;Henry IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>Ka + dieci</td>
<td>ga</td>
<td rowspan="5">Diversi equivalenti di compatibilità di un singolo carattere giapponese risultano nella stessa stringa nel formato KC. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>Ka + dieci</td>
<td>Ka + dieci</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + hw_ten</td>
<td>Ka + dieci</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Ka + hw_ten</td>
<td>Ka + dieci</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka + dieci</td>
<td>Ka + dieci</td>
<td>ga</td>

</tr>
<tr class="even">
<td>Mario</td>
<td>k <sub>i</sub> + a m + KS <sub>f</sub></td>
<td>Mario</td>
<td>Le sillabe hangul vengono mantenute in normalizzazione. Nelle versioni Unicode precedenti, i caratteri Jamo come KS <sub>f</sub> avevano mapping di compatibilità a k <sub>f</sub> + s <sub>f</sub>. Questi mapping sono stati rimossi in 2.1.9 Unicode per garantire la conservazione delle sillabe hangul.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Le due tabelle precedenti hanno un copyright di © 1998-2006 Unicode, Inc. Tutti i diritti riservati.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Usare i moduli composti per i singoli glifi

Molte sequenze di caratteri che corrispondono a un singolo glifo non hanno forme composte. Anche se normalizzato in base al form C, un singolo glifo visivo o elemento di testo logico può essere composto da più punti di codice Unicode. Ad esempio, diversi caratteri utilizzati per la scrittura in lituano hanno segni diacritici doppi, perché hanno solo moduli decomposti. Un esempio è U minuscolo con Macron e tilde ("ū̃", U + 016B U + 0303, dove il primo punto di codice è un U minuscolo con Macron e il secondo è un accento acuto combinato).

## <a name="example"></a>Esempio

Un esempio pertinente è disponibile nell' [esempio di normalizzazione NLS: Unicode](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto per le lingue nazionali](using-national-language-support.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




