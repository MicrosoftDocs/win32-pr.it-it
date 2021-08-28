---
description: Questa sezione illustra come creare un dizionario personalizzato per il riconoscimento della grafia.
ms.assetid: 83abf534-740c-44a3-bbd4-babb54f2930e
title: Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46c7b27fbb03897b406609590420bd8b69b7ceee
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122631196"
---
# <a name="creating-custom-dictionaries-for-handwriting-recognition-in-windows-7-and-windows-server-2008-r2"></a>Creazione di dizionari personalizzati per il riconoscimento della grafia in Windows 7 e Windows Server 2008 R2

Questa sezione illustra come creare un dizionario personalizzato per il riconoscimento della grafia.

Nel sistema operativo Windows 7 e nel sistema operativo Windows Server 2008 R2, l'accuratezza del riconoscimento della grafia può essere notevolmente migliorata tramite l'uso di dizionari personalizzati. Questi dizionari integrano o sostituiscono i dizionari di sistema usati per la scrittura manuale. Il supporto per il riconoscimento della grafia viene fornito tramite Servizi di riconoscimento della grafia funzionalità che deve essere abilitata tramite Server Manager.

> [!Note]  
> I dizionari personalizzati possono essere installati per una lingua solo se è installato il riconoscimento della grafia per tale lingua.

 

Per configurare un dizionario personalizzato per la scrittura manuale, è necessario eseguire due passaggi di base:

-   Compilare un elenco di parole. La compilazione crea un file di dizionario personalizzato compilato (con estensione hwrdict).
-   Installare il dizionario personalizzato compilato.

## <a name="compiling-a-word-list"></a>Compilazione di un elenco di parole

L'elenco di parole da compilare deve essere in formato testo normale e deve essere salvato usando una codifica Unicode. Altre codifiche non funzionano. Ogni riga del file di testo viene presa come singola voce nel dizionario. Sono consentite voci di unità multiword contenenti uno o più spazi. Gli spazi all'inizio o alla fine di una riga vengono ignorati.

Un dizionario personalizzato viene compilato da una riga di comando. Per compilare un dizionario, aprire una finestra di comando, passare alla cartella contenente l'elenco di parole e quindi eseguire HwrComp.exe con le opzioni della riga di comando da usare.

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
<col  />
<col  />
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
<td>Nome delle impostazioni locali specificato assegnato al file del dizionario personalizzato compilato. <localename>L'argomento ha il formato language-REGION. Un esempio è en-US, che indica la lingua inglese nell'area Stati Uniti locale. Per esempi di questo formato, vedere Costanti e stringhe [dell'identificatore di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings). Le lingue seguenti sono supportate per Windows 7 e Windows Server 2008 R2 da questa funzionalità: en-US, en-GB, en-CA, en-AU, de-DE, de-CH, fr-FR, es-ES, es-MX, es-AR, it-IT, nl-NL, nl-BE, pt-BR, pt-PT, da-DK, sv-edizione Standard, nb-NO, nn-NO, fi-FI, pl-PL, cs-CZ, ru-RU, ro-RO, sr-Latn-CS, sr-Cyrl-CS, ca-ES e hr-HR.<br/></td>
</tr>
<tr class="even">
<td>-type <type></td>
<td>L'argomento option è una concatenazione a stringa singola dell'uso della risorsa come elenco di parole principale (PRIMARY) o come supplemento all'elenco di parole principale (SECONDARY) seguito dal nome effettivo dell'elenco di parole a cui viene applicata la risorsa (ad esempio DICTIONARY o <type> SURNAME). Di seguito sono indicati i valori possibili:
<ul>
<li>PRIMARY-CITYNAME-LIST</li>
<li>PRIMARY-COUNTRYNAME-LIST</li>
<li>PRIMARY-COUNTRYSHORTNAME-LIST</li>
<li>PRIMARY-DICTIONARY</li>
<li>PRIMARY-GIVENNAME-LIST</li>
<li>PRIMARY-STATEORPROVINCE-LIST</li>
<li>PRIMARY-STREETNAME-LIST</li>
<li>PRIMARY-SURNAME-LIST</li>
<li>SECONDARY-CITYNAME-LIST</li>
<li>SECONDARY-COUNTRYNAME-LIST</li>
<li>SECONDARY-COUNTRYSHORTNAME-LIST</li>
<li>SECONDARY-DICTIONARY</li>
<li>SECONDARY-EMAILSMTP-LIST</li>
<li>SECONDARY-EMAILUSERNAME-LIST</li>
<li>SECONDARY-GIVENNAME-LIST</li>
<li>SECONDARY-STATEORPROVINCE-LIST</li>
<li>SECONDARY-STREETNAME-LIST</li>
<li>SECONDARY-SURNAME-LIST</li>
<li>SECONDARY-URL-LIST</li>
</ul>
Se un valore di tipo inizia con il prefisso PRIMARY, il dizionario compilato, dopo l'installazione, sostituirà il dizionario di sistema per tale lingua. Il valore PRIMARY-DICTIONARY rappresenta il dizionario di sistema principale per una lingua.
<blockquote>
[!Note]<br />
La sostituzione di un dizionario di sistema non esegue alcuna operazione nel contenuto del dizionario di sistema originale, in quanto la sostituzione è effettiva solo fino a quando il dizionario personalizzato non è stato rimosso.
</blockquote>
<br/> Se un valore di tipo inizia con il prefisso SECONDARY, il dizionario compilato integra il dizionario di sistema senza sostituirlo.</td>
</tr>
<tr class="odd">
<td>-comment <comment></td>
<td>Il commento specificato viene compilato nel file del dizionario. Il commento deve essere una singola stringa e non più di 64 caratteri.</td>
</tr>
<tr class="even">
<td>-o <dictfile.hwrdict></td>
<td>L'output viene scritto nel nome file specificato da <dictfile.hwrdict> .<br/> Se questa opzione non è presente, il nome del file di output viene derivato dal nome del file di input originale, con l'estensione del file di input sostituita da hwrdict.<br/></td>
</tr>
</tbody>
</table>



 

### <a name="defaults"></a>Valori predefiniti

Se non viene specificato alcun parametro, i valori predefiniti dell'opzione sono

-lang <current input language> -type SECONDARY-DICTIONARY

### <a name="examples"></a>Esempio

Di seguito viene compilato il file di input mylist1.txt, vengono applicate le opzioni predefinite e viene creato il file di output mylist1.hwrdict.

``` syntax
hwrcomp mylist1.txt
```

Al contrario, il codice seguente mylist1.txt in myrsrc1.hwrdict, ma assegna "English (US)" (en-US) come lingua e SECONDARY-DICTIONARY come tipo.

``` syntax
hwrcomp -lang en-US -type SECONDARY-DICTIONARY -o myrsrc1 mylist1.txt 
```

## <a name="installing-a-compiled-custom-dictionary"></a>Installazione di un dizionario personalizzato compilato

HwrComp.exe crea un file con estensione hwrdict, che è in formato binario utilizzabile da un sistema di riconoscimento della grafia. Questo file può essere installato in qualsiasi computer che esegue Windows 7 o Windows Server 2008 R2 che supporta il riconoscimento della grafia. Un dizionario viene installato solo per l'utente corrente o per tutti gli utenti in un computer.

Un file di dizionario personalizzato compilato può essere installato dalla riga di comando usando lo strumento HwrReg.exe. Questo strumento è utile se si desidera eseguire l'override di alcuni valori di configurazione compilati nel file o che sono i valori predefiniti. Esistono due modi per eseguire HwrReg.exe: in modalità di controllo/installazione e in modalità elenco/rimozione.

### <a name="running-hwrregexe-in-checkinstall-mode"></a>Esecuzione HwrReg.exe in modalità di controllo/installazione

Questa modalità è per i file di dizionario personalizzati che non sono ancora stati installati. Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.

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
| -check                   | Il file del dizionario viene verificato senza essere installato. L'opzione check visualizza il commento del file, oltre alle informazioni di registrazione che verranno usate per installare il file. Questa opzione è utile per verificare le informazioni di registrazione prima che venga eseguita l'installazione. <br/> Se questa opzione non è presente, HwrReg.exe installa il dizionario personalizzato.<br/>  |
|  lang <localename> | Il file del dizionario viene verificato senza essere installato. L'opzione check visualizza il commento del file, oltre alle informazioni di registrazione che verranno usate per installare il file. Questa opzione è utile per verificare le informazioni di registrazione prima che venga eseguita l'installazione. <br/> Se questa opzione non è presente, HwrReg.exe installa il dizionario personalizzato. <br/> |
|  scope {all \| me}         | Il dizionario personalizzato viene installato per tutti gli utenti (ambito all) o solo per l'utente corrente (ambito me). L'installazione con ambito richiede l'esecuzione del comando in un prompt dei comandi con privilegi elevati. In caso contrario, verrà restituito un codice di errore. <br/> Se questa opzione non è presente, l'installazione ha come ambito solo l'utente corrente.<br/>                          |
|  noprompt                | HwrReg.exe non richiede conferma. Ciò può essere utile quando si esegue hwrReg.exe da uno script. <br/>                                                                                                                                                                                                                                                                 |



 

Nell'esempio seguente viene installato il dizionario personalizzato myrsrc1.hwrdict per la lingua "Danese (Danimarca)" (da DK), con l'ambito predefinito solo dell'utente corrente.

``` syntax
hwrreg -lang da-DK myrsrc1.hwrdict 
```

### <a name="running-hwrregexe-in-listremove-mode"></a>Esecuzione HwrReg.exe in modalità elenco/rimozione

Questa modalità elenca o rimuove i dizionari personalizzati installati. Di seguito viene illustrata la sintassi di utilizzo per le opzioni della riga di comando.

``` syntax
Usage: hwrreg        [-lang <localename>] 
    [-scope {all|me}] 
    [-type <type>]
    -list | -remove
```

### <a name="explanation-of-options"></a>Spiegazione delle opzioni



| Parametro                | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  lang <localename> | I dizionari registrati solo per questo nome di impostazioni locali vengono elencati o rimossi. L'argomento <localename> ha la lingua del formato REGION. Per esempi di questo formato, vedere Costanti e stringhe [dell'identificatore di lingua](/windows/desktop/Intl/language-identifier-constants-and-strings). <br/> Se questa opzione non è presente, i dizionari per tutte le lingue vengono elencati o rimossi.<br/> |
|  scope {all \| me}         | Il dizionario personalizzato viene installato per tutti gli utenti (ambito all) o solo per l'utente corrente (ambito me). L'installazione con ambito richiede l'esecuzione del comando in un prompt dei comandi con privilegi elevati. In caso contrario, verrà restituito un codice di errore. <br/> Se questa opzione non è presente, l'installazione ha come ambito solo l'utente corrente.<br/>                      |
|  digitare <type>       | Elenca o rimuove solo i dizionari registrati con il tipo specificato.<br/> Se questa opzione non è presente, vengono elencati o rimossi tutti i tipi di dizionario. L'installazione o la rimozione di un dizionario personalizzato di un altro tipo, ad esempio PRIMARY-COUNTRYNAME-LIST, può influire sul riconoscimento della grafia in altri contesti. <br/>                                              |
|  list                    | Elenca tutti i dizionari installati che corrispondono alle altre opzioni.<br/> Se questa opzione non è presente, è necessario specificare l'opzione remove.<br/>                                                                                                                                                                                                                          |
|  remove                  | Richiede la rimozione di qualsiasi dizionario che corrisponde alle altre opzioni.<br/> Se questa opzione non è presente, è necessario specificare l'elenco di opzioni.<br/>                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Esempio

Di seguito sono elencati i dizionari con la lingua "English (US)" (en US) e il tipo PRIMARY DICTIONARY e che vengono installati solo per l'utente corrente.

``` syntax
hwrreg -list -lang en-US -type PRIMARY-DICTIONARY
                  
```

Analogamente, il comando seguente rimuove i dizionari che corrispondono allo stesso criterio.

``` syntax
hwrreg -remove -lang en-US -type PRIMARY-DICTIONARY
                  
```

## <a name="general-notes-on-custom-dictionaries"></a>Note generali sui dizionari personalizzati

-   Se si installano due dizionari personalizzati con lo stesso tipo, lingua e ambito, la seconda installazione sovrascriverà il primo.
-   Se si installano due dizionari personalizzati con lo stesso tipo e lingua, ma con ambiti diversi (uno per tutti gli utenti e uno per l'utente corrente), il dizionario installato per l'utente corrente ha la precedenza e il dizionario installato per tutti gli utenti viene ignorato.

 

