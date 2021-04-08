---
description: In questo argomento vengono definiti i termini importanti quando si utilizza la funzionalità NLS.
ms.assetid: daf929b2-8ff9-4a17-b294-f2c0eaef5848
title: Terminologia NLS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a86808d31cb034e7ad29e4580b8f201ad3c9a6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760178"
---
# <a name="nls-terminology"></a>Terminologia NLS

In questo argomento vengono definiti i termini importanti quando si utilizza la funzionalità NLS.

## <a name="locale-and-language-terms"></a>Termini delle impostazioni locali e della lingua

Nella tabella seguente vengono riepilogati i termini delle impostazioni locali e della lingua. Vedere anche [impostazioni locali e lingue](locales-and-languages.md).



|                          | Gruppo di lingue                                                                                                                                                                                                                                                                   | lingua per programmi non Unicode                                                                                                                                                                                                                | Standard e formati                                                                                                                                                                                                                   |
|--------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scopo**              | Fornisce tutti i layout di tastiera, gli IME (Input Method Editor), i tipi di carattere TrueType, i collegamenti dei tipi di carattere, i file di pacchetto licenze (LPK), i tipi di carattere bitmap e le tabelle di conversione delle tabelle codici necessari per un gruppo di linguaggi. Quindi influiscono su tutte le altre impostazioni di questo elenco. | Determina quali tipi di carattere bitmap e tabelle codici OEM, ANSI e Macintosh sono valori predefiniti per il sistema operativo. Questo linguaggio influiscono solo sulle applicazioni che non sono completamente Unicode. Prima di Windows XP, questo linguaggio era denominato "impostazioni locali del sistema". | Determina quali impostazioni vengono utilizzate per la formattazione di date, ore, valute e numeri come valore predefinito per ogni utente. Determina anche il tipo di ordinamento per l'ordinamento del testo. Prima di Windows XP, gli standard e i formati venivano chiamati "impostazioni locali dell'utente". |
| **Primo set**            | Installazione                                                                                                                                                                                                                                                                     | Installazione                                                                                                                                                                                                                                     | Installazione                                                                                                                                                                                                                            |
| **Come gli utenti possono modificare** | Opzioni internazionali (elemento del pannello di controllo)<br/> **Windows XP:** Opzioni internazionali e della lingua<br/> (solo amministratori)<br/>                                                                                                                                       | Opzioni internazionali (elemento del pannello di controllo)<br/> **Windows XP:** Opzioni internazionali e della lingua<br/> (solo amministratori)<br/>                                                                                                       | Opzioni internazionali (elemento del pannello di controllo)<br/> **Windows XP:** Opzioni internazionali e della lingua<br/>                                                                                                                               |
| **Default**              | Europa occidentale e Stati Uniti e gruppo di lingue necessari per visualizzare la lingua di una versione localizzata.                                                                                                                                                                         | Lingua della versione localizzata.                                                                                                                                                                                                                   | Lingua del sistema operativo localizzato.                                                                                                                                                                                                 |
| **Funzione**             | [**EnumSystemLanguageGroups**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlanguagegroupsa)                                                                                                                                                                                                                     | [**GetSystemDefaultLangID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlangid)                                                                                                                                                                                         | [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid), [ **GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename)                                                                                                                          |



 



|                          | Impostazioni locali del thread                                                                                                                                                 | Lingua di input                                                                                            | Lingua dell'interfaccia utente predefinita del sistema                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scopo**              | Determina le impostazioni utilizzate per la formattazione di date, ore, valute e numeri elevati per un thread. Determina anche il tipo di ordinamento per l'ordinamento del testo. | È costituito da un linguaggio e da un metodo di input.                                                             | Determina la lingua predefinita di menu e finestre di dialogo, messaggi, file di informazioni di installazione (INF) e file della guida.<br/> **Windows Vista e versioni successive:** Noto come lingua di installazione. Gioca un ruolo più limitato, ampiamente sostituito dalle lingue dell'interfaccia utente preferite dal sistema.<br/> Per ulteriori informazioni, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md) .<br/> |
| **Primo set**            | Per impostazione predefinita, standard e formati                                                                                                                              | Installazione                                                                                              | Installazione                                                                                                                                                                                                                                                                                                                                                                                   |
| **Come gli utenti possono modificare** | [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)                                                                                                                    | Opzioni internazionali (elemento del pannello di controllo)<br/> **Windows XP:** Opzioni internazionali e della lingua<br/> | No                                                                                                                                                                                                                                                                                                                                                                                             |
| **Default**              | Standard e formati                                                                                                                                         | Lingua della versione localizzata con il metodo di input predefinito.                                                  | Lingua della versione localizzata.                                                                                                                                                                                                                                                                                                                                                                 |
| **Funzione**             | [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale)                                                                                                                    | [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout)                                                     | [**GetSystemDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultuilanguage)                                                                                                                                                                                                                                                                                                                               |



 



|                          | Lingua dell'interfaccia utente del sistema, lingue dell'interfaccia utente preferite del sistema                                                                                                                                                                  | Lingua dell'interfaccia utente, lingue dell'interfaccia utente preferite dall'utente                                                                                                                                               | Lingue dell'interfaccia utente preferite dai thread                                                                                                                                                                 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scopo**              | Determinare la lingua dei menu e delle finestre di dialogo, i messaggi, i file INF e i file della Guida per il sistema operativo. Per ulteriori informazioni, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md). | Determinare la lingua dei menu e delle finestre di dialogo, i messaggi e i file della Guida per l'utente. Per ulteriori informazioni, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md). | **Windows Vista e versioni successive:** Specificare le lingue preferite per i thread dell'applicazione. Per ulteriori informazioni, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md). |
| **Primo set**            | Il valore predefinito è NULL                                                                                                                                                                                                    | Il valore predefinito è NULL                                                                                                                                                                             | Il valore predefinito è NULL                                                                                                                                                                               |
| **Come gli utenti possono modificare** | Opzioni internazionali e della lingua<br/> (solo amministratori)<br/>                                                                                                                                          | Opzioni internazionali (elemento del pannello di controllo)<br/> **Windows XP:** Opzioni internazionali e della lingua<br/>                                                                                   | [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)                                                                                                                        |
| **Default**              | **Windows Vista e versioni successive:** Lingua della versione localizzata, seguita da eventuali fallback.                                                                                                                             | **Prima di Windows Vista:** Lingua della versione localizzata.<br/> **Windows Vista e versioni successive:** Lingua della versione localizzata, seguita da eventuali fallback.<br/>                     | Elenco di valori null                                                                                                                                                                                     |
| **Funzione**             | [**GetSystemPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getsystempreferreduilanguages)                                                                                                                                             | [**GetUserDefaultUILanguage**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultuilanguage), [ **GetUserPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getuserpreferreduilanguages)                                                            | [**GetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getthreadpreferreduilanguages)                                                                                                                        |



 



|                          | Elabora le lingue dell'interfaccia utente preferite                                                                                                                                                                 |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Scopo**              | **Windows 7 e versioni successive:** Determinare le lingue preferite per un processo dell'applicazione. Per ulteriori informazioni, vedere [gestione della lingua dell'interfaccia utente](user-interface-language-management.md). |
| **Primo set**            | Il valore predefinito è NULL                                                                                                                                                                                |
| **Come gli utenti possono modificare** | Opzioni internazionali e della lingua (solo amministratori)                                                                                                                                            |
| **Default**              | **Windows 7 e versioni successive:** Lingua della versione localizzata, seguita da eventuali fallback.                                                                                                             |
| **Funzione**             | [**GetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-getprocesspreferreduilanguages), [ **SetProcessPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setprocesspreferreduilanguages)                                             |



 

## <a name="code-page"></a>Tabella codici

L'impossibilità di 256-tabelle codici di punti di codice per supportare la combinazione di script in un unico testo è stato uno dei motivi principali per l'incremento di Unicode. Le tabelle codici rimangono importanti per la scrittura di codice della console, per la gestione di applicazioni legacy o per l'esecuzione in versioni precedenti di Windows e per l'interazione con un software non Microsoft non abilitato per Unicode.

## <a name="input-language"></a>Lingua di input

La lingua di input è rappresentata da una variabile di dati per processo che descrive un linguaggio (ad esempio, greco) e un metodo di input (ad esempio, la tastiera). È possibile installare più lingue di input e l'utente può spostarsi tra loro.

Per impostare e recuperare il valore della lingua di input, l'applicazione chiama rispettivamente [**LoadKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-loadkeyboardlayouta) e [**GetKeyboardLayout**](/windows/win32/api/winuser/nf-winuser-getkeyboardlayout). Gli utenti possono aggiungere e rimuovere le lingue di input tramite la scheda **lingue** della parte opzioni internazionali e della lingua del pannello di controllo.

La lingua di input predefinita è la lingua localizzata del sistema operativo ed è l'impostazione attiva quando viene avviata una nuova applicazione (o quando viene aperta una nuova finestra per alcune applicazioni). Il passare a una lingua di input diversa viene eseguito in base alle singole applicazioni. In altre parole, è possibile usare due lingue di input diverse in due applicazioni diverse. Un utente può, ad esempio, digitare il tedesco utilizzando il layout di tastiera internazionale di Stati Uniti, l'inglese utilizzando l'input vocale (con software non Microsoft) e lo spagnolo utilizzando un IME in tre applicazioni diverse.

## <a name="language-for-non-unicode-programs"></a>Lingua per programmi non Unicode

Il linguaggio per i programmi non Unicode (denominato in precedenza "impostazioni locali di sistema") determina la tabella codici utilizzata per impostazione predefinita nel sistema operativo. L'impostazione lingua per programmi non Unicode ha effetto solo su applicazioni non Unicode, ovvero applicazioni ANSI. L'impostazione della lingua indica a Windows di emulare un sistema operativo non basato su Unicode, localizzato in questa lingua. La modifica della lingua per i programmi non Unicode consente di installare i file del tipo di carattere bitmap necessari per supportare le applicazioni non Unicode nella lingua specificata. Per consentire all'utente di selezionare una lingua per i programmi non Unicode, è necessario installare il gruppo di lingue appropriato. Per l'applicazione è necessario il supporto dello script per selezionare una lingua per i programmi non Unicode. Il linguaggio per i programmi non Unicode è un'impostazione per sistema ed è necessario implementare un riavvio.

In alcuni casi non vi è alcuna differenza evidente tra due lingue per i programmi non Unicode. Ad esempio, questo è il caso delle impostazioni locali tedesche (neutre) e tedesche (Austria). In generale, le impostazioni di un gruppo di lingue sono molto simili e sono diverse solo nella tabella codici OEM o MAC.

Un'applicazione ANSI deve controllare l'impostazione della lingua per i programmi non Unicode durante l'installazione. USA [**GetACP**](/windows/desktop/api/Winnls/nf-winnls-getacp) o [**GetOEMCP**](/windows/desktop/api/Winnls/nf-winnls-getoemcp) per recuperare il valore. Non è supportata alcuna funzione per impostare la lingua per i programmi non Unicode. Tuttavia, gli utenti possono modificarla utilizzando la scheda **Avanzate** nella parte opzioni internazionali e della lingua del pannello di controllo. Di seguito sono riportati alcuni esempi di linguaggio per le impostazioni dei programmi non Unicode:

1.  Un utente tedesco che desidera eseguire un'applicazione giapponese progettata per il giapponese Windows 95 deve selezionare il giapponese come lingua per i programmi non Unicode. Dopo questa selezione, le applicazioni in lingua tedesca non Unicode presentano problemi. Ad esempio, le diereszioni tedesche (̈) non vengono visualizzate correttamente.
2.  Un utente tedesco che desidera digitare testo in giapponese in un'applicazione non Unicode in tedesco deve selezionare giapponese come lingua per i programmi non Unicode. Come nel primo esempio, ciò causa problemi nell'immissione del testo tedesco in applicazioni non Unicode.
3.  Un utente arabo che desidera digitare arabo, francese e inglese in un'applicazione araba non Unicode deve selezionare arabo come lingua per i programmi non Unicode, perché la tabella codici ANSI araba contiene la maggior parte dei caratteri in francese e tutti i caratteri inglesi.

## <a name="language-group"></a>Gruppo di lingue

Il gruppo di lingue controlla la lingua dei programmi, standard e formati, le lingue di input e le lingue dell'interfaccia utente che possono essere selezionati non Unicode. Per ogni versione localizzata, il gruppo di lingue specificato è il valore predefinito e non può essere rimosso. Per impostazione predefinita, Windows installa ad esempio il gruppo di lingue Europa occidentale e Stati Uniti. Pertanto, se la versione in lingua inglese di Windows è installata in un paese o in un'area geografica non in lingua inglese, l'utente installerà in genere un altro gruppo di lingue.

Quando si aggiunge un gruppo di lingue, in Windows vengono copiati (ma non attivati) i file di tastiera necessari, gli IME (Input Method Editor), i file dei tipi di carattere TrueType, i file di caratteri bitmap e i file NLS (National Language Support). L'aggiunta di un gruppo di lingue aggiunge anche valori del registro di sistema per il collegamento dei tipi di carattere e installa i motori di scripting per linguaggi di script complessi (arabo, ebraico, indiano e Thai).

Oltre al gruppo di lingue Europa occidentale e Stati Uniti, sono disponibili 16 altri gruppi di lingue:



<table>
<tbody>
<tr class="odd">
<td><dl> Arabo<br />
Armeno<br />
Baltico<br />
Europa centrale<br />
Cirillico<br />
Georgiano<br />
Greco<br />
Ebraico<br />
</dl></td>
<td><dl> Delle lingue indiane<br />
Giapponese<br />
Coreano<br />
Cinese semplificato<br />
Cinese tradizionale<br />
Thai<br />
Turco<br />
Vietnamita<br />
</dl></td>
</tr>
</tbody>
</table>



 

Qualsiasi numero e combinazione di gruppi di lingue può essere installato in qualsiasi sistema operativo. Ad esempio, un utente spagnolo può installare il gruppo di lingue cirillico per lavorare su testi russi. In questo caso, un'applicazione di elaborazione di testo deve supportare anche il gruppo di lingue cirillici.

> [!Note]  
> L'aggiunta del gruppo di lingue appropriato non consente automaticamente a un'applicazione di accettare testo. È consigliabile eseguire il test. Ad esempio, le applicazioni non Unicode potrebbero richiedere la modifica della lingua per i programmi non Unicode.

 

## <a name="location"></a>Location

**Windows XP:** Un percorso è un identificatore geografico. È rappresentato da una variabile di dati per utente che definisce il paese/area geografica in cui si trova l'utente.

Per impostare il valore, l'applicazione chiama [**SetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-setusergeoid). Per recuperare il valore, l'applicazione chiama [**GetUserGeoID**](/windows/desktop/api/Winnls/nf-winnls-getusergeoid).

## <a name="standards-and-formats"></a>Standard e formati

Standard e formati (in precedenza "impostazioni locali dell'utente") è una variabile per singolo utente che determina l'ordinamento predefinito e le impostazioni predefinite per la formattazione di date, ore, valute e numeri. La variabile viene presentata come linguaggio (a volte in combinazione con un paese/area geografica), ma non si tratta di un linguaggio. Se ad esempio si imposta la variabile Standards e formats su ebraico, l'utente desidera utilizzare le convenzioni di formattazione dell'ebraico, non necessariamente la lingua ebraica. Inoltre, la variabile Standards and formats determina la stringa utilizzata per i nomi di giorni e mesi. Se, ad esempio, un utente Visualizza "25 novembre 1998", la stringa "novembre" può variare in base alla variabile Standards e formats. La modifica della variabile aggiunge automaticamente le impostazioni locali di input con le impostazioni predefinite per la lingua.

Per ottenere l'impostazione della variabile Standards e formats, l'applicazione chiama [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) o [**GetUserDefaultLocaleName**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlocalename). Non è disponibile alcuna funzione NLS per impostare la variabile. Tuttavia, gli utenti possono modificarla tramite la scheda **Opzioni area** della parte opzioni internazionali e della lingua del pannello di controllo.

In genere, un'applicazione deve usare gli standard e formatta le impostazioni delle variabili per visualizzare i dati. Tuttavia, un'applicazione che Usa impostazioni locali fisse per visualizzare i dati deve passare un identificatore delle impostazioni locali specifico anziché usare impostazioni locali \_ dell'utente \_ .

## <a name="thread-locale"></a>Impostazioni locali del thread

Le impostazioni locali del thread sono rappresentate da una variabile di dati delle impostazioni locali per thread che determina la formattazione di date, ore, valute e numeri elevati per il thread. Per impostazione predefinita viene impostato il valore per le impostazioni locali attualmente selezionate per gli standard e i formati. Per impostare le impostazioni locali del thread, l'applicazione chiama [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale). Per recuperare le impostazioni locali del thread, l'applicazione chiama [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).

Nella maggior parte dei casi le impostazioni locali del thread non devono essere sovrascritte. Normalmente è consigliabile usarla solo per sincronizzare le impostazioni locali del thread di un'applicazione server con la variabile Standards e formats di un computer client. Ad esempio, un'applicazione di trading finanziario per il New York Stock Exchange, che viene usata nelle banche di tutto il mondo, deve visualizzare i prezzi di ora, data e magazzino nei formati Stati Uniti. Questa applicazione usa [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) per impostare le impostazioni locali del thread sulla lingua inglese (Stati Uniti), quindi usa le funzioni NLS per formattare le date, le ore e i prezzi delle scorte.

La modifica delle impostazioni locali del thread non influisce su tutte le funzioni API. Pertanto non è sempre un metodo affidabile per eseguire l'override della variabile Standards e formats. Al contrario, le applicazioni che controllano standard e formati devono usare impostazioni locali fisse per visualizzare i dati, passando un identificatore delle impostazioni locali specifico anziché usare impostazioni locali \_ dell'utente \_ .

## <a name="nls-example"></a>Esempio NLS

Nell'esempio seguente viene illustrata l'interazione tra standard e formati, il linguaggio per i programmi non Unicode, la posizione e la lingua dell'interfaccia utente.

Un utente che è nativo del Cile, ma che vive nel Stati Uniti dispone di un computer che esegue Windows XP English. L'utente imposta il percorso su Stati Uniti per utilizzare un provider di servizi Internet (ISP) per ottenere il meteo per il Stati Uniti. Tuttavia, la variabile Standards and formats è impostata su Spanish (Chile), in modo che le informazioni vengano formattate in base agli standard cileni. Inoltre, l'utente utilizza un elaboratore di testo coreano, ovvero un'applicazione ANSI, in modo che la lingua per i programmi non Unicode sia impostata su coreano (Corea). Per utilizzare l'applicazione, l'utente dispone di una tastiera in lingua inglese e installa anche un IME coreano per supportare una seconda lingua di input. Il collaboratore dell'utente, che condivide il computer, ma non è a conoscenza della lingua inglese, può impostare la lingua dell'interfaccia utente in spagnolo (Spagna) quando si usa il computer.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul supporto linguistico nazionale](about-national-language-support.md)
</dt> <dt>

[Impostazioni locali e lingue](locales-and-languages.md)
</dt> <dt>

[Interfaccia utente multilingue](multilingual-user-interface.md)
</dt> </dl>

 

 
