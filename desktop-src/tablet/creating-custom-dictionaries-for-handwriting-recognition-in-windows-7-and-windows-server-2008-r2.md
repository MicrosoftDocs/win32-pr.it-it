---
description: In questa sezione viene illustrato come creare un dizionario personalizzato per il riconoscimento della grafia.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80b9b7b5a1d9dfadddd83825aea7d6f676439999
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305683"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2

In questa sezione viene illustrato come creare un dizionario personalizzato per il riconoscimento della grafia.

Nel sistema operativo Windows 7 e nel sistema operativo Windows Server 2008 R2, l'accuratezza del riconoscimento della grafia può essere significativamente migliorata tramite l'uso di dizionari personalizzati. Questi dizionari integrano o sostituiscono i dizionari di sistema usati per la grafia. Il supporto per il riconoscimento della grafia viene fornito tramite la funzionalità Servizi di riconoscimento della grafia che deve essere abilitata tramite Server Manager.

> [!Note]  
> I dizionari personalizzati possono essere installati per un linguaggio solo se il riconoscimento della grafia per tale lingua è installato.

 

Per configurare un dizionario personalizzato per la grafia sono necessari due passaggi di base:

-   Compila un elenco di parole. La compilazione crea un file di dizionario personalizzato compilato (con estensione hwrdict).
-   Installare il dizionario personalizzato compilato.

## <a name="compiling-a-word-list"></a>Compilazione di un elenco di parole

L'elenco di parole da compilare deve essere in formato testo normale e deve essere salvato utilizzando una codifica Unicode. Altre codifiche non funzioneranno. Ogni riga del file di testo viene considerata come una singola voce nel dizionario. Sono consentite le voci di unità multiword contenenti uno o più spazi. Gli spazi all'inizio o alla fine di una riga vengono ignorati.

Un dizionario personalizzato viene compilato da una riga di comando. Per compilare un dizionario, aprire una finestra di comando, passare alla cartella contenente l'elenco di parole, quindi eseguire HwrComp.exe con le opzioni della riga di comando che si desidera utilizzare.

Nell'esempio seguente viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.

``` syntax
Usage: hwrcomp       [-lang <localename>] [-type <type>]
    [-comment <comment>]
    [-o <dictfile.hwrdict>]
    <inputfile>
     
```

### <a name="explanation-of-options"></a>Spiegazione delle opzioni



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>-lang <localename></td>
<td>Nome delle impostazioni locali specificato assegnato al file del dizionario personalizzato compilato. L'argomento <localename> ha il formato Language-Region. Un esempio è en-US, che indica la lingua inglese nell'area Stati Uniti. Per esempi di questo formato, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings). Le lingue seguenti sono supportate per Windows 7 e Windows Server 2008 R2 da questa funzionalità: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, NL-BE, PT-BR, PT-PT, da-DK, sv-SE, nb-NO, nn-NO, fi-FI, pl-PL, CS-CZ, ur-RU, RO-RO, Sr-Latn-CS, Sr-Cyrl-CS, ca-ES e HR-HR.<br/></td>
</tr>
<tr class="even">
<td>-tipo <type></td>
<td>L'argomento option <type> è una concatenazione a singola stringa dell'uso della risorsa come elenco di parole principale (primario) o come supplemento all'elenco di parole principale (secondario) seguito dal nome effettivo dell'elenco di parole a cui viene applicata la risorsa (ad esempio dizionario o cognome). Di seguito sono indicati i valori possibili:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>PRIMARY-DICTIONARY</li>
<li>PRIMARY-DATENAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-COGNOME-ELENCO</li>
<li>SECONDARY-CITYNAME-LIST</li>
<li>SECONDARY-COUNTRYNAME-LIST</li>
<li>SECONDARY-COUNTRYSHORTNAME-LIST</li>
<li>DIZIONARIO SECONDARIO</li>
<li>SECONDARY-EMAILSMTP-LIST</li>
<li>SECONDARY-EMAILUSERNAME-LIST</li>
<li>ELENCO SECONDARIO-SPECIFICATO</li>
<li>SECONDARY-STATEORPROVINCE-LIST</li>
<li>SECONDARY-VIA-ELENCO</li>
<li>SECONDARY-COGNOME-ELENCO</li>
<li>ELENCO SECONDARIO-URL</li>
</ul>
Se un valore di tipo inizia con il prefisso primario, il dizionario compilato, dopo l'installazione, sostituirà il dizionario di sistema per tale lingua. Il valore PRIMARY-DICTIONARY rappresenta il dizionario principale di sistema per una lingua.
<blockquote>
[!Note]<br />
La sostituzione di un dizionario di sistema non esegue alcuna operazione sul contenuto del dizionario di sistema originale, perché la sostituzione è attiva solo fino a quando il dizionario personalizzato non è stato rimosso.
</blockquote>
<br/> Se un valore di tipo inizia con il prefisso SECONDARY, il dizionario compilato completerà il dizionario di sistema senza sostituirlo.</td>
</tr>
<tr class="odd">
<td>-Commento <comment></td>
<td>Il commento specificato viene compilato nel file del dizionario. Il commento deve essere una singola stringa e non più di 64 caratteri.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>L'output viene scritto nel nome file specificato da <dictfile.hwrdict> .<br/> Se questa opzione è mancante, il nome del file di output viene derivato dal nome del file di input originale, con l'estensione del file di input sostituita da. hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Valori predefiniti

Se non viene specificato alcun parametro, i valori predefiniti dell'opzione sono

-lang <current input language> -Type-dizionario secondario

### <a name="examples"></a>Esempio

Il codice seguente compila il file di input mylist1.txt, applica i valori di opzione predefiniti e crea il file di output mylist1. hwrdict.

``` syntax
hwrcomp mylist1.txt
```

Il codice seguente, invece, compila mylist1.txt in myrsrc1. hwrdict, ma assegna "English (US)" (en-US) come Language e SECONDARY-DICTIONARY come tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Installazione di un dizionario personalizzato compilato

HwrComp.exe crea un file con estensione hwrdict, che è in un formato binario utilizzabile da un riconoscimento della grafia. Questo file può essere installato in qualsiasi computer che esegue Windows 7 o Windows Server 2008 R2 che supporta il riconoscimento della grafia. Un dizionario viene installato solo per l'utente corrente o per tutti gli utenti di un computer.

Un file di dizionario personalizzato compilato può essere installato dalla riga di comando utilizzando lo strumento HwrReg.exe. Questo strumento è utile se si desidera eseguire l'override di alcuni valori di configurazione che vengono compilati nel file o sono i valori predefiniti. Esistono due modi per eseguire HwrReg.exe: in modalità di controllo/installazione e in modalità elenco/rimozione.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Esecuzione di HwrReg.exe in modalità di controllo/installazione

Questa modalità è per i file di dizionario personalizzati che non sono stati ancora installati. Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.

``` syntax
Usage: hwrreg        [-check]
    [-lang <localename>] 
    [-scope {all|me}]
    [-noprompt] 
    <dictfile.hwrdict>
```

### <a name="explanation-of-options"></a>Spiegazione delle opzioni



| Parametro                | Descrizione                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -controllo                   | Il file del dizionario viene verificato senza essere installato. L'opzione check Visualizza il commento del file, più le informazioni di registrazione che verrebbero usate per installare il file. Questa opzione è utile per verificare le informazioni di registrazione prima di eseguire l'installazione. <br/> Se questa opzione è mancante, HwrReg.exe installa il dizionario personalizzato.<br/>  |
|  lang <localename> | Il file del dizionario viene verificato senza essere installato. L'opzione check Visualizza il commento del file, più le informazioni di registrazione che verrebbero usate per installare il file. Questa opzione è utile per verificare le informazioni di registrazione prima di eseguire l'installazione. <br/> Se questa opzione è mancante, HwrReg.exe installa il dizionario personalizzato. <br/> |
|  ambito {All \| me}         | Il dizionario personalizzato è installato per tutti gli utenti (ambito tutti) o solo per l'utente corrente (ambito me). Per l'installazione di con ambito, è necessario che il comando venga eseguito in un prompt dei comandi con privilegi elevati. in caso contrario, verrà restituito un codice di errore. <br/> Se questa opzione non è presente, l'ambito dell'installazione è solo l'utente corrente.<br/>                          |
|  noprompt                | HwrReg.exe non richiede la conferma. Questa operazione può essere utile quando si esegue hwrReg.exe da uno script. <br/>                                                                                                                                                                                                                                                                 |



 

Nell'esempio seguente viene installato il dizionario personalizzato myrsrc1. hwrdict per la lingua "danese (Danimarca)" (da DK), con l'ambito predefinito solo dell'utente corrente.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Esecuzione di HwrReg.exe in modalità elenco/rimozione

In questa modalità è possibile elencare o rimuovere i dizionari personalizzati installati. Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Spiegazione delle opzioni



| Parametro                | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang <localename> | I dizionari registrati solo per questo nome delle impostazioni locali vengono elencati o rimossi. L'argomento <localename> ha l'area della lingua del modulo. Per esempi di questo formato, vedere [costanti e stringhe degli identificatori di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Se questa opzione è mancante, i dizionari per tutte le lingue vengono elencati o rimossi.<br/> |
|  ambito {All \| me}         | Il dizionario personalizzato è installato per tutti gli utenti (ambito tutti) o solo per l'utente corrente (ambito me). Per l'installazione di con ambito, è necessario che il comando venga eseguito in un prompt dei comandi con privilegi elevati. in caso contrario, verrà restituito un codice di errore. <br/> Se questa opzione non è presente, l'ambito dell'installazione è solo l'utente corrente.<br/>                      |
|  tipo <type>       | Elenca o rimuove solo i dizionari registrati con il tipo specificato.<br/> Se questa opzione è mancante, tutti i tipi di dizionario vengono elencati o rimossi. L'installazione o la rimozione di un dizionario personalizzato di un altro tipo, ad esempio PRIMARY-COUNTRYname-LIST, può influire sul riconoscimento della grafia in altri contesti. <br/>                                              |
|  list                    | Elenca tutti i dizionari installati che corrispondono alle altre opzioni.<br/> Se questa opzione è mancante, è necessario specificare l'opzione Remove.<br/>                                                                                                                                                                                                                          |
|  remove                  | Richiede la rimozione di qualsiasi dizionario corrispondente alle altre opzioni.<br/> Se questa opzione è mancante, è necessario specificare l'elenco di opzioni.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Esempio

Di seguito sono elencati i dizionari con lingua "inglese (Stati Uniti)" (en US) e tipo dizionario primario e installati solo per l'utente corrente.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Analogamente, di seguito vengono rimossi i dizionari che corrispondono agli stessi criteri.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Note generali sui dizionari personalizzati

-   Se si installano due dizionari personalizzati con lo stesso tipo, lingua e ambito, la seconda operazione sovrascriverà la prima.
-   Se si installano due dizionari personalizzati con lo stesso tipo e la stessa lingua, ma con ambiti diversi (uno per tutti gli utenti e uno per l'utente corrente), il dizionario installato per l'utente corrente ha la precedenza e il dizionario installato per tutti gli utenti viene ignorato.

 

