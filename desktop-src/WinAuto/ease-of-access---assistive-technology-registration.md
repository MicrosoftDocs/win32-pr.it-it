---
title: Registrazione facilitata della tecnologia di accesso facilitato
description: Questo articolo illustra come registrare un'applicazione di accessibilità con la facilità di accesso al centro. Viene inoltre illustrato come adattare l'applicazione di accessibilità in modo che funzioni correttamente con il desktop protetto.
ms.assetid: 6F1F2AAE-B2E4-4F26-8BDF-A3DE8F5C5460
ms.topic: article
ms.date: 04/02/2019
ms.openlocfilehash: 66901cd899fc578b032f86e3752fcdcac0788ba1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300183"
---
# <a name="ease-of-access---assistive-technology-registration"></a>Registrazione facilitata della tecnologia di accesso facilitato

Questo articolo illustra come registrare un'applicazione di accessibilità con la facilità di accesso al centro. Viene inoltre illustrato come adattare l'applicazione di accessibilità in modo che funzioni correttamente con il desktop protetto.

Il Centro accesso facilitato è un'applicazione del pannello di controllo per Microsoft Windows che riunisce le funzionalità per l'accessibilità e la semplicità d'uso. Grazie alla facilità di accesso al centro, gli utenti possono configurare i computer in base alle proprie esigenze fisiche e cognitive.

Una funzione del Centro accesso facilitato è aiutare gli utenti a avviare applicazioni di accessibilità, tra cui Assistente vocale, tastiera su schermo e lente di ingrandimento. Le applicazioni registrate di terze parti vengono visualizzate anche nel centro di accesso facilitato e possono essere avviate direttamente da questa posizione.

Le applicazioni di accessibilità devono funzionare senza problemi con il desktop protetto. Il desktop sicuro è l'interfaccia utente visualizzata quando il computer è bloccato (al momento dell'accesso o quando l'utente ha bloccato il desktop) e quando all'utente viene richiesto di consentire un'azione potenzialmente non sicura. Per motivi di sicurezza, Windows pone limiti a software di terze parti in esecuzione sul desktop sicuro. Se si vuole che l'applicazione di accessibilità venga eseguita sul desktop protetto, è necessario registrare l'applicazione con la facilità di accesso al centro.

## <a name="registering-with-the-ease-of-access-center"></a>Registrazione con la facilità di accesso al centro

Le applicazioni di accessibilità si registrano con la facilità di accesso al centro creando una o più chiavi del registro di sistema durante l'installazione dell'applicazione. Nella tabella seguente sono elencate le informazioni contenute nelle chiavi del registro di sistema.



| Nome                        | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        | Obbligatorio/facoltativo | Linguaggio      |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------|---------------|
| Nome dell'applicazione            | Nome dell'applicazione, che si trova in un file di risorse. Questo valore del registro di sistema contiene una stringa in un formato specificato. Potrebbe trattarsi di una versione localizzata del nome dell'applicazione, se l'applicazione è localizzata in lingue diverse dall'inglese. Il nome viene visualizzato nel centro accesso facilitato.<br/>                                                                                                                                                                                                                                                                                       | Obbligatorio          | Localizzata     |
| ATEx                       | Nome del file eseguibile dell'applicazione o dell'immagine. Windows utilizza questo valore per determinare se l'applicazione di accessibilità è in esecuzione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obbligatorio          | Non localizzato |
| CopySettingsToLockedDesktop | Valore **DWORD** che indica se copiare le impostazioni dell'applicazione di accessibilità sul desktop bloccato.<br/> Se questo valore è 1, l'applicazione può scrivere le impostazioni in un percorso nel registro utenti e Windows copia le impostazioni nello stesso percorso nel registro utenti per il desktop bloccato. Ciò consente all'applicazione di salvare in modo permanente il proprio stato dal desktop "normale" al desktop bloccato.<br/>                                                                                                                                                             | Facoltativo           | Non localizzato |
| Descrizione                 | Breve descrizione dell'applicazione, da un file di risorse. Questo valore del registro di sistema contiene una stringa in un formato specificato. Potrebbe trattarsi di una versione localizzata della descrizione, se l'applicazione è localizzata in lingue diverse dall'inglese. La lunghezza di questa stringa deve essere inferiore a 512 caratteri.<br/> La descrizione viene visualizzata nel centro di accesso facilitato per fornire informazioni aggiuntive sull'applicazione di accessibilità all'utente.<br/> Questo valore può essere usato anche per notificare all'utente che l'applicazione non viene usata sul desktop sicuro.<br/>      | Obbligatorio          | Localizzata     |
| Profilo                     | Breve frammento di codice XML che specifica le sistemazioni fornite dall'applicazione. Garantisce che l'applicazione venga visualizzata sotto la categoria corretta nel centro accesso facilitato.<br/>                                                                                                                                                                                                                                                                                                                                                                                                  | Obbligatorio          | Non localizzato |
| PassiveAutoStartBehavior    | <p>Valore **DWORD** che indica se il comportamento di avvio automatico legacy è abilitato.</p><p>Il valore predefinito è 0, che indica che un oggetto AT richiede un comportamento di avvio automatico legacy. In questo modo, l'impostazione "avvia dopo l'accesso" per l'oggetto in verrà archiviata nella configurazione guidata e nel pannello di controllo (vedere **Pannello di controllo-> facilità di accesso-> facilità di accesso al centro-> modificare le impostazioni di accesso**) e avvia automaticamente il dopo UAC e la schermata di blocco.</p><p>Il valore 1 indica che in deve essere utilizzato il nuovo comportamento di avvio automatico in cui l'impostazione "avvia dopo l'accesso" in non viene archiviata nella configurazione guidata e nel pannello di controllo e viene automaticamente avviata una volta per ogni sessione utente (all'accesso) solo se viene selezionata l'impostazione "avvia dopo l'accesso".</p>                                                                                                                                                                                                                                                                                                                                                                                                  | Facoltativo          | Non localizzato |
| SecureDesktopAccommodation  | Nome di un'applicazione di accessibilità alternativa da eseguire sul desktop protetto al posto di questa applicazione. L'alternativa può essere un'applicazione diversa, una versione diversa della stessa applicazione, una delle applicazioni di accessibilità inclusa in Windows o "None" se non si desidera eseguire alcuna applicazione di accessibilità sul desktop protetto. <br/>                                                                                                                                                                                                               | Facoltativo           | Non localizzato |
| Profilo semplice              | Valore che descrive come classificare l'applicazione in una parola o due:, ad esempio, una tastiera a schermo, una lente di ingrandimento o una tastiera sullo schermo.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                  | Obbligatorio          | Non localizzato |
| StartExe                    | Percorso completo del file eseguibile. Questo valore viene utilizzato per avviare l'applicazione di accessibilità.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Obbligatorio          | Non localizzato |
| StartParams                 | Argomenti della riga di comando. Questi valori vengono usati insieme a StartExe per avviare l'applicazione.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Facoltativo           | Non localizzato |
| TerminateOnDesktopSwitch    | Valore **DWORD** che specifica il modo in cui l'applicazione di accessibilità risponde alle transizioni verso o dal desktop protetto.<br/> Se questo valore non esiste o è 1, Windows termina e riavvia l'applicazione a ogni transizione da o verso il desktop protetto. Comportamento predefinito.<br/> Se questo valore è 0, Windows non termina l'applicazione di accessibilità su una transizione desktop. L'applicazione continuerà a essere eseguita sul desktop precedente e Windows avvierà una nuova istanza sul nuovo desktop se un'istanza non è già in esecuzione.<br/> | Facoltativo           | Non localizzato |


 

### <a name="localization"></a>Localizzazione

I valori del registro di sistema del nome e della descrizione dell'applicazione devono essere localizzabili per supportare MUI (Multilingual User Interface).

Queste stringhe hanno il formato seguente, dove le parentesi angolari indicano gli elementi obbligatori e le parentesi quadre indicano un elemento facoltativo.

*@ <ResDllPath \\ ResDLLFilename>,- <resID> \[ ;<comment>\]*

*<ResDllPath \\ ResDLLFilename>* è il percorso della dll della risorsa. Il percorso può contenere variabili di ambiente.

*<resID>* ID di risorsa della stringa.

il *\[ Commento \]* contiene commenti facoltativi.

Ecco un esempio:


```
@%SystemRoot%\system32\anyAT.dll,-5020
```



Per ulteriori informazioni su MUI, vedere [Windows MUI Knowledge Center](../intl/about-multilingual-user-interface.md).

### <a name="hci-profile"></a>Profilo HCI

Il profilo di interazione human computer (HCI) è un modo per determinare quali sistemazioni fornire in base alle esigenze dell'utente. Le applicazioni per l'accessibilità dovrebbero registrare informazioni sul tipo di disabilità che l'applicazione può supportare.

Il valore del registro di sistema del profilo contiene codice XML che descrive il tipo di disabilità di destinazione dell'applicazione di accessibilità. Questo XML ha il formato seguente:


```XML
<HCIModel>
<Accommodation type="disability"/>
</HCIModel>
```



I valori validi per l'attributo **tipo di alloggio** sono i seguenti:

-   visione lieve
-   visione grave
-   cognitive lieve
-   cognitivo grave
-   destrezza lieve
-   destrezza grave
-   udito lieve
-   udito grave
-   riconoscimento vocale lieve
-   riconoscimento vocale grave

> [!Note]  
> Per tali valori viene applicata la distinzione tra maiuscole e minuscole.

 

Se un'applicazione di accessibilità supporta più alloggi, il valore del registro di sistema del profilo deve includere un attributo del **tipo di alloggio** per ogni alloggio.

### <a name="ease-of-access-registry-details"></a>Dettagli del registro di sistema di accesso facilitato

Per registrare l'applicazione di accessibilità, è necessario creare una chiave per l'applicazione nel seguente percorso del registro di sistema e popolarla con coppie nome-valore.

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ accessibilità \\ ATS\\**

Assegnare un nome alla chiave del registro di sistema dell'applicazione usando il formato seguente:

*"CompanyName \_ ProductName \_ v \# "*

Ad esempio, "Contoso \_ Magnifier \_ v 2.0".

Per aggiungere i valori del registro di sistema, è necessario che il programma di installazione sia in esecuzione con privilegi elevati.

### <a name="secure-desktop-accommodation"></a>Secure Desktop accommodation

La chiave del registro di sistema **SecureDesktopAccommodation** consente di specificare il modo in cui l'applicazione di accessibilità risponde al desktop protetto. Per impostazione predefinita, la facilità di accesso al centro avvia l'applicazione sul desktop protetto se è già in esecuzione sul desktop normale o se è configurata per l'esecuzione sul desktop di accesso. Utilizzando la chiave **SecureDesktopAccommodation** , è possibile:

-   Specificare una versione alternativa dell'applicazione da usare sul desktop sicuro. Ad esempio, si potrebbe avere una versione alternativa che disabilita le funzionalità non protette o è ottimizzata per usare meno memoria e avviare più velocemente.

    Per specificare la versione alternativa, impostare la chiave **SecureDesktopAccommodation** sul nome della versione alternativa. Ad esempio, se l'applicazione è stata registrata nella \_ chiave di lettura dello schermo di Contoso \_ v 1.0, è possibile registrare la versione alternativa nella schermata di Contoso \_ ReaderSecure \_ v 1.0. Impostare quindi la chiave **SecureDesktopAccommodation** di Contoso \_ Screen Reader \_ v 1.0 su "Contoso \_ Screen ReaderSecure \_ v 1.0".

-   Specificare un'applicazione Microsoft Accessibility da usare sul desktop sicuro al posto dell'applicazione. Per questa opzione, impostare **SecureDesktopAccommodation** sul nome dell'applicazione di accessibilità Microsoft specifica: "OSK", "magnifierpane" o "Assistente vocale".
-   Specificare che l'applicazione non deve essere eseguita sul desktop protetto e nessuna applicazione alternativa. Per questa opzione, impostare **SecureDesktopAccommodation** su "None" (consigliato) o il nome di un'applicazione inesistente.

Se la chiave del registro di sistema **SecureDesktopAccommodation** per l'applicazione di accessibilità specifica un'applicazione Microsoft Accessibility da eseguire sul desktop protetto al posto dell'applicazione, Windows invia una notifica all'utente quando effettua la transizione al desktop sicuro. Per inviare una notifica all'utente, Windows Visualizza la stringa specificata nella chiave del registro di sistema Description per l'applicazione. Se, ad esempio, l'applicazione ScreenReader Deluxe 1,0 utilizza l'Assistente vocale Microsoft sul desktop protetto, includerà una stringa di descrizione, ad esempio, "l'Assistente vocale Microsoft verrà usato per i desktop protetti, di accesso e di altro tipo, al posto di ScreenReader Deluxe 1,0".

Se la chiave **SecureDesktopAccommodation** dell'applicazione è impostata su "None", usare la chiave **Description** per indicare all'utente che l'applicazione non è disponibile sul desktop protetto e non è disponibile alcuna alternativa.

Windows Visualizza il testo della descrizione nelle posizioni pertinenti nel centro di accesso facilitato.

### <a name="running-at-installation-and-on-the-logon-desktop"></a>Esecuzione al momento dell'installazione e sul desktop di accesso

Se si aggiunge il nome della chiave registrata dell'applicazione di accessibilità alla stringa nel seguente percorso del registro di sistema, Windows avvierà l'applicazione subito dopo l'installazione. Inoltre, Windows eseguirà automaticamente l'applicazione ogni volta che il desktop di accesso è attivo.

**\\Configurazione di \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ per HKCU Software**

La chiave di configurazione è una stringa delimitata da virgole. Per aggiungere l'applicazione, aggiungere una stringa identica alla chiave del registro di sistema dell'applicazione in HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ .

### <a name="running-in-a-job"></a>Esecuzione in un processo

Se la chiave del registro di sistema **TerminateOnDesktopSwitch** non è presente o è impostata su un valore diverso da zero, Windows esegue l'applicazione nel contesto di un processo, terminando e riavviando l'applicazione con ogni transizione desktop. L'esecuzione in un processo garantisce che venga eseguita una sola istanza dell'applicazione in un determinato momento e che l'applicazione non debba monitorare lo stato del desktop. Gli svantaggi dell'esecuzione in un processo includono:

-   L'applicazione comporta un costo di avvio per ogni transizione del desktop.
-   L'applicazione può essere avviata solo tramite il Centro accesso facilitato.
-   L'applicazione deve salvare continuamente le impostazioni perché può essere terminata in qualsiasi momento da una transizione desktop.

Se la chiave **TerminateOnDesktopSwitch** esiste ed è impostata su 0, Windows non esegue l'applicazione di accessibilità in un processo. I vantaggi di questo approccio sono i seguenti:

-   Nessun costo di avvio è associato a transizioni desktop.
-   L'applicazione può essere avviata al di fuori della facilità di accesso al centro.

Gli svantaggi di non in esecuzione in un processo includono:

-   Poiché l'applicazione non viene riavviata sulle transizioni desktop, deve rilevare quando il desktop corrente è inattivo e rispondere in modo appropriato. Ad esempio, l'applicazione deve cedere il controllo dell'hardware, in modo che la versione desktop protetta dell'applicazione possa utilizzarla e l'applicazione deve passare alla modalità sospensione per evitare di utilizzare le risorse del processore.
-   Se l'applicazione può essere avviata tramite il menu Start, Esplora risorse o la riga di comando, è necessario informare il Centro accesso facilitato. Per ulteriori informazioni, vedere **tasto logo Windows + U**.
-   Poiché più copie dell'applicazione possono essere eseguite contemporaneamente su diversi desktop, l'applicazione deve essere scritta per supportare più copie in esecuzione.

### <a name="windows-logo-key--u"></a>Tasto logo Windows + U

Se l'applicazione di accessibilità è configurata per l'esecuzione in un processo, il codice di avvio dell'applicazione deve includere una chiamata alla funzione [**IsProcessInJob**](/windows/desktop/api/jobapi/nf-jobapi-isprocessinjob) per determinare se l'applicazione viene avviata in un processo. In tal caso, l'applicazione deve avviare il Centro accesso facilitato e quindi uscire. Nell'esempio seguente viene illustrato come chiamare **IsProcessInJob**.


```C++
BOOL fAlreadyInJob;
BOOL fSuccess = IsProcessInJob(GetCurrentProcess(), NULL, &fAlreadyInJob); 
```



Se l'applicazione di accessibilità è configurata per essere eseguita all'esterno di un processo, deve notificare al centro accesso facilitato l'avvio dell'applicazione e continuare normalmente.

Indipendentemente dal modo in cui è configurata l'applicazione, se fornisce un modo per uscire dall'applicazione, ad esempio un pulsante Chiudi, l'applicazione deve notificare al centro accessi la facilità di uscita.

Un'applicazione notifica la facilità di accesso al centro impostando una chiave del registro di sistema temporanea e inserendo quindi la combinazione di tasti logo Windows + U nel flusso di input.

L'applicazione deve creare la chiave temporanea nel percorso seguente.

**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ AccessibilityTemp**

La chiave temporanea deve avere lo stesso nome del nome dell'applicazione registrata, ad esempio "Contoso \_ Screen Reader \_ v 1.0". Il valore della chiave è un **DWORD** impostato su 0x0003 all'avvio oppure 0x0002 quando l'applicazione viene chiusa.


```C++
INPUT input[4] = {0};

input[0].type = INPUT_KEYBOARD;
input[0].ki.wVk = VK_LWIN;
input[0].ki.dwFlags = 0;

input[1].type = INPUT_KEYBOARD;
input[1].ki.wVk = 0x55; // U key
input[1].ki.dwFlags = 0;

input[2].type = INPUT_KEYBOARD;
input[2].ki.wVk = 0x55; // U key
input[2].ki.dwFlags = KEYEVENTF_KEYUP;

input[3].type = INPUT_KEYBOARD;
input[3].ki.wVk = VK_LWIN;
input[3].ki.dwFlags = KEYEVENTF_KEYUP;

SendInput(ARRAYSIZE(input), input, sizeof(input[0]));
```



### <a name="windows-logo-key--volume-up"></a>Tasto logo Windows + volume su

Quando l'utente avvia l'applicazione di accessibilità premendo la combinazione di tasti con il tasto logo Windows + volume su, ad esempio in un dispositivo tablet, il Centro accesso facilitato passa l'argomento della riga di comando seguente all'applicazione:

**/hardwarebuttonlaunch**

L'applicazione può utilizzare questo argomento per determinare se avviare normalmente o per modificare di conseguenza il comportamento.

### <a name="transferring-secure-desktop-settings"></a>Trasferimento delle impostazioni desktop protette

Se l'applicazione di accessibilità supporta il desktop protetto, è possibile usare il registro di sistema per copiare le impostazioni quando l'applicazione esegue la transizione al desktop protetto. La copia delle impostazioni contribuisce a semplificare la transizione al desktop sicuro per l'utente.

Per copiare le impostazioni, impostare la chiave del registro di sistema CopySettingsToLockedDesktop dell'applicazione su 1 e archiviare le impostazioni nel seguente percorso del registro di sistema.

**HKCU \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATConfig\\<AT Key Name>**

Il Centro accesso facilita il monitoraggio di questo percorso del registro di sistema mentre l'applicazione è in esecuzione. Quando si verifica una transizione al desktop protetto, la facilità di accesso al centro copia le impostazioni nello stesso percorso dell'hive HKCU del desktop protetto. L'applicazione può quindi leggere le impostazioni e riprendere il proprio stato.

L'applicazione di accessibilità deve scrivere le impostazioni a intervalli regolari o ogni volta che i valori cambiano. La scrittura delle impostazioni all'uscita dell'applicazione non funzionerà. Se l'applicazione è in esecuzione in un processo, viene terminata in fase di transizione dal desktop protetto, prima che sia possibile eseguire il codice di uscita. Se l'applicazione non è in esecuzione in un processo, l'applicazione non viene terminata in fase di transizione dal desktop protetto.

### <a name="caution"></a>Attenzione

Poiché le chiavi del registro di sistema descritte di seguito sono scritte in modalità utente, non sono sicure. Se l'applicazione di accessibilità legge il contenuto di queste chiavi, deve controllare attentamente i dati e usarli con cautela. In particolare, l'applicazione deve eseguire un controllo dei limiti sui valori **DWORD** , prestare attenzione con le lunghezze di stringa, non deve leggere i nomi di DLL plug-in e non deve eseguire alcun comando trovato in stringhe.

## <a name="registry-examples"></a>Esempi di registro

Nell'esempio seguente vengono illustrati i possibili valori del registro di sistema per un prodotto fittizio denominato contoso ScreenReader versione 2,0, il cui nome localizzato è archiviato come risorsa.

I valori nella tabella si trovano sotto la chiave seguente:

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Accessibility \\ ATS \\ Contoso \_ Screen Reader \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Data</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5020</td>
</tr>
<tr class="even">
<td>Descrizione</td>
<td>REG_SZ</td>
<td>@% SystemRoot% \system32\ContosoRes.dll,-5040</td>
</tr>
<tr class="odd">
<td>Profilo</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\ContosoTools\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>

</tr>
<tr class="odd">
<td>SecureDesktopAccommodation</td>
<td>REG_SZ</td>
<td>Assistente vocale</td>
</tr>
</tbody>
</table>



 

Se l'applicazione fornisce sia un'applicazione per la lettura dello schermo che una lente di ingrandimento dello schermo in un singolo eseguibile, i valori per il componente Visualizzatore schermo potrebbero essere simili ai seguenti:



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Data</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-30</td>
</tr>
<tr class="even">
<td>Descrizione</td>
<td>REG_SZ</td>
<td>@C:\Program Files\Contoso\Contosores.dll,-32</td>
</tr>
<tr class="odd">
<td>Profilo</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;low vision&quot; />
   <Accommodation type=&quot;severe vision&quot; />
   <Accommodation type=&quot;mild cognitive&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>ScreenReader</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>C:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/r</td>
</tr>
</tbody>
</table>



 

I valori per il componente Magnifier si trovino nella chiave seguente:

**HKLM \\ software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ Contosoibility \\ ATS \\ Contoso \_ Magnifier \_ v 2.0**



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Nome</th>
<th>Tipo</th>
<th>Data</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ApplicationName</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-31</td>
</tr>
<tr class="even">
<td>Descrizione</td>
<td>REG_SZ</td>
<td>@c:\Program Files\Contoso\Contosores.dll,-42</td>
</tr>
<tr class="odd">
<td>Profilo</td>
<td>REG_SZ</td>
<td><span data-codelanguage="XML"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>XML</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code><HCIModel>
   <Accommodation type=&quot;mild vision&quot; />
</HCIModel></code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>SimpleProfile</td>
<td>REG_SZ</td>
<td>Ingrandimento</td>
</tr>
<tr class="odd">
<td>StartExe</td>
<td>REG_SZ</td>
<td>c:\Program Files\Contoso\Bin\ContosoSR.exe</td>
</tr>
<tr class="even">
<td>StartParams</td>
<td>REG_SZ</td>
<td>/m</td>
</tr>
</tbody>
</table>



 

 

