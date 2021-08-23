---
description: Le applicazioni possono usare Unicode per rappresentare stringhe in più formati.
ms.assetid: 027c9ef5-4012-4d1c-b78c-a4d3f1ccbf35
title: Uso della normalizzazione Unicode per rappresentare stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62c6d091548d924919a18fe05fb9d98d2b82b13792df2facfe96489be2d7ff2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822491"
---
# <a name="using-unicode-normalization-to-represent-strings"></a>Uso della normalizzazione Unicode per rappresentare stringhe

Le applicazioni possono usare Unicode per rappresentare stringhe in più formati. Con l'aumentata accettazione di Unicode, in particolare tramite Internet, si è verificata la necessità di eliminare le differenze non essenziali nelle stringhe Unicode. Più rappresentazioni per una combinazione di caratteri complicano il software, ad esempio quando un server Web risponde a una richiesta di pagina o un linker cerca un identificatore specifico in una libreria.

> [!Caution]  
> Stringhe Unicode diverse possono sembrare visivamente identiche, generando problemi di sicurezza. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

In risposta a questo requisito, il consorzio Unicode ha definito un processo denominato "normalizzazione", che produce una rappresentazione binaria per una delle rappresentazioni binarie equivalenti di un carattere. Dopo la normalizzazione, due stringhe sono equivalenti se e solo se hanno rappresentazioni binarie identiche. La normalizzazione elimina alcune differenze, ma mantiene la distinzione tra maiuscole e minuscole.

Per usare la normalizzazione Unicode, un'applicazione può chiamare le funzioni [**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring) e [**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring) per ridisporre le stringhe che acccorde a Unicode 4.0 TR \# 15. La normalizzazione consente di migliorare la sicurezza riducendo le rappresentazioni di stringa alternative con lo stesso significato linguistico. Tenere presente, tuttavia, che la normalizzazione non può eliminare completamente le rappresentazioni alternative.

Per una descrizione dettagliata degli standard Unicode per la normalizzazione, vedere [Unicode Standard Annex \# 15: Unicode Normalization Forms](https://www.unicode.org/reports/tr15) (UAX \# 15).

> [!Caution]  
> Poiché la normalizzazione può modificare la forma di una stringa, i meccanismi di sicurezza o gli algoritmi di convalida dei caratteri devono in genere essere implementati dopo la normalizzazione. Per altre informazioni, vedere [Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md).

 

## <a name="provide-multiple-representations-of-the-same-string"></a>Fornire più rappresentazioni della stessa stringa

In molti casi, Unicode consente più rappresentazioni di ciò che è, linguisticamente, la stessa stringa. Esempio:

-   La lettera A maiuscola con dieresi (umlaut) può essere rappresentata come singolo punto di codice Unicode "Ä" (U+00C4) o come combinazione di maiuscolo A e carattere dieresi combinato ("A" + "È", ovvero U+0041 U+0308). Considerazioni simili si applicano a molti altri caratteri con segni diacritici.
-   La lettera A maiuscola può essere rappresentata nel modo consueto (lettera maiuscola A, U+0041) o in maiuscolo fullwidth A (U+FF21). Considerazioni simili si applicano alle altre semplici lettere latini (maiuscole e minuscole) e ai caratteri katakana usati per scrivere il giapponese.
-   La stringa "fi" può essere rappresentata dai caratteri "f" e "i" (U+0066 U+0069) o dalla legatura "fi" (U+FB01). Considerazioni simili si applicano a molte altre combinazioni di caratteri per cui Unicode definisce le legature.

## <a name="use-the-four-defined-normalization-forms"></a>Usare i quattro moduli di normalizzazione definiti

Le applicazioni possono eseguire la normalizzazione Unicode usando diversi algoritmi, denominati "moduli di normalizzazione", che rispettano regole diverse. Il consorzio Unicode ha definito quattro forme di normalizzazione: NFC (modulo C), NFD (modulo D), NFKC (modulo KC) e NFKD (modulo KD). Ogni modulo elimina alcune differenze, ma mantiene la distinzione tra maiuscole e minuscole. Win32 e il .NET Framework supportano tutti e quattro i moduli di normalizzazione.

Il tipo di enumerazione NLS [**NORM \_ FORM**](/windows/desktop/api/Winnls/ne-winnls-norm_form) supporta i quattro formati di normalizzazione Unicode standard. I moduli C e D forniscono forme canoniche per le stringhe. Le forme non canoniche KC e KD offrono ulteriore compatibilità e possono rivelare alcune equivalenze semantiche che non sono evidenti nelle forme C e D. Tuttavia, lo fanno a scapito di una certa perdita di informazioni e in genere non devono essere usate come modo canonico per archiviare le stringhe.

Delle due forme canoniche, la forma C è una forma "composta" e la forma D è una forma "scomposta". Ad esempio, il modulo C usa il singolo punto di codice Unicode "Ä" (U+00C4), mentre il modulo D usa ("A" + "è", ovvero U+0041 U+0308). Il rendering viene eseguito in modo identico, perché "è" (U+0308) è un carattere combinato. Il modulo D può usare qualsiasi numero di punti di codice per rappresentare un singolo punto di codice usato dal modulo C.

Se due stringhe sono identiche nel formato C o D, sono identiche nell'altra forma. Inoltre, quando viene eseguito correttamente il rendering, vengono visualizzati in modo indistinguibile l'uno dall'altro e dalla stringa originale non normalizzata.

Dopo la normalizzazione, le stringhe non possono essere restituite in modo coerente alla rappresentazione originale. Ad esempio, se una stringa con una combinazione di rappresentazioni di caratteri composte e scomposte viene convertita in un formato normalizzato, non è possibile annullarla alla stringa mista originale. Pertanto, se un'applicazione richiede la rappresentazione originale della stringa, deve archiviare tale rappresentazione in modo esplicito. Tuttavia, la conversione tra le due forme canoniche è reversibile. Una stringa nel formato C può essere convertita nel formato D e quindi nel formato C e il risultato è identico alla stringa C originale.

Le forme KC e KD sono simili alle forme C e D, rispettivamente, ma queste "forme di compatibilità" hanno mapping aggiuntivi di caratteri compatibili alla forma di base di ogni carattere. Questi mapping possono causare la perdita di variazioni di caratteri secondarie. Combinano determinati caratteri visivamente distinti. Ad esempio, combinano caratteri a larghezza intera e a metà larghezza con lo stesso significato semantico o forme diverse della stessa lettera araba o la legatura "fi" (U+FB01) e la coppia di caratteri "fi" (U+0066 U+0069). Combinano anche alcuni caratteri che talvolta possono avere un significato semantico diverso, ad esempio una cifra scritta come apice, come pedice o racchiusa in un cerchio. A causa di questa perdita di informazioni, i moduli KC e KD in genere non devono essere usati come forme canoniche di stringhe, ma sono utili per determinate applicazioni.

La forma KC è una forma composta e la forma KD è una forma scomposta. L'applicazione può andare avanti e indietro tra i formati KC e KD, ma non è possibile passare dal formato KC o KD alla stringa originale, anche se la stringa originale è nel formato C o D.

Windows, le applicazioni Microsoft e il .NET Framework genereranno caratteri nel formato C usando i normali metodi di input. Per la maggior parte degli Windows, il modulo C è il formato preferito. Ad esempio, i caratteri nel formato C vengono prodotti dall Windows input da tastiera. Tuttavia, i caratteri importati dal Web e da altre piattaforme possono introdurre altri moduli di normalizzazione nel flusso di dati.

Gli esempi seguenti sono tratti da UAX \# 15 e illustrano le differenze tra le quattro forme di normalizzazione.



<table>
<thead>
<tr class="header">
<th>Originale</th>
<th>Modulo D</th>
<th>Modulo C</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Il ffi_ligature (U+FB03) non è scomposto, perché ha un mapping di compatibilità, non un mapping canonico.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä\uFB03n&quot;</td>
<td>&quot;A\u0308\uFB03n&quot;</td>
<td>&quot;Ä\uFB03n&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Enrico IV&quot;</td>
<td>&quot;Enrico IV&quot;</td>
<td>&quot;Enrico IV&quot;</td>
<td rowspan="2">Il numero IV ROMAN (U+2163) non è scomposto.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Henry \u2163&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +10</td>
<td>ga</td>
<td rowspan="5">Equivalenti di compatibilità diversi di un singolo carattere giapponese non comportano la stessa stringa nel formato C.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +10</td>
<td>ka +10</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>
<td>hw_ka +hw_ten</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>
<td>ka +hw_ten</td>

</tr>
<tr class="odd">
<td>hw_ka +10</td>
<td>hw_ka +10</td>
<td>hw_ka +10</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>Le sillabe Hangul vengono mantenute in condizioni di normalizzazione.<br/></td>
</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Originale</th>
<th>Modulo KD</th>
<th>Modulo KC</th>
<th>Note</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>&quot;Äffin&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>
<td rowspan="2">Il ffi_ligature (U+FB03) viene scomposto nel formato KC, ma non nel formato C.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Ä\uFB03n&quot;</td>
<td>&quot;A\u0308ffin&quot;</td>
<td>&quot;Äffin&quot;</td>

</tr>
<tr class="odd">
<td>&quot;Enrico IV&quot;</td>
<td>&quot;Enrico IV&quot;</td>
<td>&quot;Enrico IV&quot;</td>
<td rowspan="2">Le stringhe risultanti sono identiche nel formato KC.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>&quot;Henry \u2163&quot;</td>
<td>&quot;Enrico IV&quot;</td>
<td>&quot;Enrico IV&quot;</td>

</tr>
<tr class="odd">
<td>ga</td>
<td>ka +10</td>
<td>ga</td>
<td rowspan="5">Equivalenti di compatibilità diversi di un singolo carattere giapponese comportano la stessa stringa nel formato KC.${REMOVE}$<br />
</td>
</tr>
<tr class="even">
<td>ka +10</td>
<td>ka +10</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +hw_ten</td>
<td>ka +10</td>
<td>ga</td>

</tr>
<tr class="even">
<td>ka +hw_ten</td>
<td>ka +10</td>
<td>ga</td>

</tr>
<tr class="odd">
<td>hw_ka +10</td>
<td>ka +10</td>
<td>ga</td>

</tr>
<tr class="even">
<td>kaks</td>
<td>k <sub>i</sub> + a m + ks <sub>f</sub></td>
<td>kaks</td>
<td>Le sillabe Hangul vengono mantenute in condizioni di normalizzazione. Nelle versioni Unicode precedenti, i caratteri jamo come ks <sub>f</sub> avevano mapping di compatibilità a k <sub>f</sub> + s <sub>f</sub>. Questi mapping sono stati rimossi in Unicode 2.1.9 per garantire che le sillabe Hangul siano mantenute.<br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Le due tabelle precedenti hanno un copyright di © 1998-2006 Unicode, Inc. Tutti i diritti riservati.

 

## <a name="use-composed-forms-for-single-glyphs"></a>Usare forme composte per singoli glifi

Molte sequenze di caratteri che corrispondono a un singolo glifo non hanno forme composte. Anche quando viene normalizzato dal formato C, un singolo glifo visivo o un elemento di testo logico può essere costituito da più punti di codice Unicode. Ad esempio, diversi caratteri usati per scrivere lituano hanno segni diacritici doppi, perché hanno solo forme scomposte. Un esempio è U minuscolo con macron e tilde ("ẫ", U+016b U+0303, dove il primo punto di codice è un U minuscolo con macron e il secondo è un accento acuto combinato).

## <a name="example"></a>Esempio

Un esempio pertinente è disponibile in [NLS: Unicode Normalization Sample](nls--unicode-normalization-sample.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso del supporto linguistico nazionale](using-national-language-support.md)
</dt> <dt>

[Considerazioni sulla sicurezza: funzionalità internazionali](security-considerations--international-features.md)
</dt> <dt>

[**IsNormalizedString**](/windows/desktop/api/Winnls/nf-winnls-isnormalizedstring)
</dt> <dt>

[**NormalizeString**](/windows/desktop/api/Winnls/nf-winnls-normalizestring)
</dt> </dl>

 

 




