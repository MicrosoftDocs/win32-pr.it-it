---
description: 'In questo argomento viene illustrato come registrare un programma nel registro di sistema di Windows come uno dei seguenti tipi di client: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.'
title: Registrazione di programmi con tipi di client
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 33fcb63c-3db2-44df-acfe-8c88e2e634e4
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 71dd4e3192dc75821fd0a3e8c0d4742e1a8d571a
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "103886041"
---
# <a name="registering-programs-with-client-types"></a>Registrazione di programmi con tipi di client

In questo argomento viene illustrato come registrare un programma nel registro di sistema di Windows come uno dei seguenti tipi di client: browser, posta elettronica, riproduzione multimediale, messaggistica immediata o macchina virtuale per Java.

> [!Note]  
> Queste informazioni si applicano ai sistemi operativi seguenti:
> 
> -   Windows 2000 Service Pack 3 (SP3)
> -   Windows 2000 Service Pack 4 (SP4)
> -   Windows XP Service Pack 1 (SP1)
> -   Windows XP Service Pack 2 (SP2)
> -   Windows XP Service Pack 3 (SP3)
> -   Windows Server 2003
> -   Windows Vista
> -   Windows Vista Service Pack 1 (SP1)
> -   Windows 8

 

In questo argomento sono incluse le sezioni seguenti.

-   [Elementi di registrazione comuni per tutti i tipi di client](#common-registration-elements-for-all-client-types)
    -   [Selezione di un nome canonico](#selecting-a-canonical-name)
    -   [Registrazione del nome visualizzato di un programma](#registering-a-programs-display-name)
    -   [Registrazione dell'icona di un programma](#registering-a-programs-icon)
    -   [Registrazione di un verbo aperto](#registering-an-open-verb)
    -   [Registrazione delle informazioni di installazione](#registering-installation-information)
-   [Elementi di registrazione per tipi client specifici](#registration-elements-for-specific-client-types)
    -   [Registrazione del menu Start](#start-menu-registration)
    -   [Registrazione client di posta elettronica](#mail-client-registration)
-   [Completa registrazioni di esempio](#complete-sample-registrations)
    -   [Un browser di esempio](#a-sample-browser)
    -   [Un browser di posta elettronica di esempio](#a-sample-mail-browser)
    -   [Media Player di esempio](#a-sample-media-player)
    -   [Programma Instant Messenger di esempio](#a-sample-instant-messenger-program)
    -   [Una macchina virtuale di esempio per Java](#a-sample-virtual-machine-for-java)
-   [Argomenti correlati](#related-topics)

In questo argomento viene estesa la documentazione esistente sulla registrazione di un programma come tipo di client specifico. Per i collegamenti alla documentazione, vedere la sezione Argomenti correlati.

## <a name="common-registration-elements-for-all-client-types"></a>Elementi di registrazione comuni per tutti i tipi di client

Quando si registra un programma come tipo di client, la maggior parte delle voci del registro di sistema sono le stesse indipendentemente dal tipo di client. Alcune voci del registro di sistema, tuttavia, sono specifiche del tipo di client e sono indicate nella sezione [elementi di registrazione per tipi di client specifici](#registration-elements-for-specific-client-types) .

In questa sezione vengono illustrati gli argomenti seguenti:

-   [Selezione di un nome canonico](#selecting-a-canonical-name)
-   [Registrazione del nome visualizzato di un programma](#registering-a-programs-display-name)
-   [Registrazione dell'icona di un programma](#registering-a-programs-icon)
-   [Registrazione di un verbo aperto](#registering-an-open-verb)
-   [Registrazione delle informazioni di installazione](#registering-installation-information)

> [!Note]  
> I nomi delle sottochiavi indicati in corsivo in questo argomento sono segnaposto per i nomi di sottochiavi definiti dall'utente o per un set di valori possibili. Gli esempi completi con i nomi di esempio sono disponibili nella sezione [completa registrazioni di esempio](#complete-sample-registrations) .

 

Tutte le informazioni di registrazione del tipo di client vengono archiviate con la sottochiave seguente:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
```

*ClientTypeName* è uno dei seguenti nomi di sottochiavi:

-   StartMenuInternet (per i browser)
-   Posta elettronica (per la posta elettronica)
-   Supporti (per la riproduzione di contenuti multimediali)
-   Messaggistica immediata (per la messaggistica istantanea)
-   JavaVM (per la macchina virtuale per Java)

In questo argomento si noteranno i riferimenti a un programma per computer fittizio denominato "Lit View" di Litware Inc., con un file eseguibile denominato Litview.exe. Questo ipotetico programma viene usato in modo intercambiabile come Instant Messenger, browser o un altro tipo di programma client, in base alle esigenze a scopo illustrativo.

### <a name="selecting-a-canonical-name"></a>Selezione di un nome canonico

Il fornitore deve scegliere un *nome canonico* per il programma. Il nome canonico non viene mai visualizzato all'utente, pertanto non è necessario localizzarlo. Il suo unico scopo è fornire una stringa univoca che può essere usata per identificare il programma. Corrisponde in genere al nome in lingua inglese del programma, ma si tratta semplicemente di una convenzione.

Per i tipi di client diversi dai browser, il nome canonico può essere una stringa qualsiasi. Scegliere un nome univoco, che probabilmente non verrà usato da un altro fornitore.

Per i client del browser, il nome canonico deve essere il nome, inclusa l'estensione, del file eseguibile associato. ad esempio, "Litview.exe".

Di seguito sono riportati alcuni esempi di nomi canonici.

-   Iexplore.exe (browser)
-   Windows Mail (posta elettronica)
-   Media Player Windows (supporto)
-   Windows Messenger (messaggistica istantanea)

Registrare il nome canonico creando una sottochiave come illustrato di seguito. Il nome della sottochiave è il nome canonico. Tutte le informazioni relative alla registrazione di tale programma sono disponibili in questa sottochiave.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
```

### <a name="registering-a-programs-display-name"></a>Registrazione del nome visualizzato di un programma

Il passaggio successivo della registrazione consiste nel specificare il nome visualizzato del programma. Viene specificato come valore sotto la chiave del nome canonico, come illustrato di seguito. Si noti che *CanonicalName* e *ClientTypeName* non sono i nomi effettivi delle chiavi, ma solo i segnaposto per i nomi veri, ad esempio la *visualizzazione illuminata*.

> [!Note]  
> A partire da Windows 8, il nome usato per registrare l' [accesso al programma set e le impostazioni predefinite del computer (SPAD)](cpl-setprogramaccess.md) e per i [programmi predefiniti](default-programs.md) deve corrispondere affinché le modifiche apportate da SPAD per attivare le registrazioni dei programmi predefiniti.

 

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               LocalizedString = @FilePath,-StringID
```

Il valore **LocalizedString** è una \_ stringa reg SZ ed è costituito da un segno di chiocciola (@), dal percorso completo di un file con estensione dll o exe, da una virgola, da un segno meno e da un numero intero decimale. Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno del file con estensione dll o exe, il cui valore deve essere visualizzato all'utente come nome del client. Si noti che il percorso del file non richiede virgolette, anche se contiene spazi.

La registrazione della stringa del nome visualizzato in questo modo consente di usare la stessa registrazione per più lingue. Ogni installazione della lingua fornisce un file di risorse diverso con il nome visualizzato archiviato con lo stesso ID di risorsa.

Nell'esempio riportato di seguito viene illustrata la registrazione di un programma di messaggistica istantanea di visualizzazione. Poiché si tratta di un programma di messaggistica immediata, la sottochiave *CanonicalName* (in questo caso la *visualizzazione illuminata*) viene archiviata nella sottochiave **im** .

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

Si noti l'uso della voce (impostazione predefinita) come dichiarazione secondaria del nome visualizzato del client. Se **LocalizedString** non è presente, viene invece utilizzato il valore (predefinito). Funziona con tutti i tipi di client (browser Internet, browser di posta elettronica, messaggeri istantanei e lettori multimediali). Per garantire la compatibilità con il [layout del registro di sistema del client di Internet Explorer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85)), i programmi di posta elettronica devono impostare il valore (predefinito) della sottochiave *CanonicalName* sul nome visualizzato del client nella lingua attualmente installata.

### <a name="registering-a-programs-icon"></a>Registrazione dell'icona di un programma

> [!Note]  
> Questa sezione non si applica a Windows 2000.

 

Per impostazione predefinita, la sezione superiore del menu **Start** di Windows XP e Windows Vista contiene le icone **Internet** e **posta elettronica** . Queste icone non sono presenti in Windows 7 e versioni successive. Per i client del browser e della posta elettronica, quando un programma viene assegnato come valore predefinito per il tipo di client, viene visualizzata l'icona registrata del programma per le voci del menu **Start** .

La registrazione dell'icona di un programma è obbligatoria per i client del browser e della posta elettronica. La registrazione di un'icona per la riproduzione multimediale, la messaggistica immediata o la macchina virtuale per i tipi di client Java è facoltativa e le icone registrate per tali tipi di client non sono attualmente utilizzate da Windows e non vengono visualizzate nella sezione superiore dei menu di **avvio** di Windows XP o Windows Vista.

Per registrare un'icona per un programma client, aggiungere una sottochiave **DefaultIcon** con un valore predefinito, come illustrato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               DefaultIcon
                  (Default) = FilePath,IconIndex
```

Il valore **filePath** è il percorso completo del file che contiene l'icona. Questo percorso non richiede virgolette, anche se contiene spazi.

Il valore **IconIndex** viene interpretato nel modo seguente:

-   Se **IconIndex** è un numero positivo, il numero viene usato come indice della matrice in *base zero* delle icone archiviate nel file. Se, ad esempio, **IconIndex** è 1, la seconda icona viene caricata dal file.
-   Se **IconIndex** è un numero negativo, il valore assoluto di **IconIndex** viene usato come identificatore di risorsa (anziché come indice) per l'icona. Ad esempio, se **IconIndex** è-3, l'icona con l'identificatore di risorsa 3 viene caricata dal file.

Nell'esempio seguente viene illustrata la registrazione di un ipotetico browser di visualizzazione illuminato. La seconda icona archiviata nel file di Litview.exe viene utilizzata come impostazione predefinita.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\Litview.exe,1
```

### <a name="registering-an-open-verb"></a>Registrazione di un verbo aperto

> [!Note]  
> Questa sezione non si applica a Windows 2000. Il passaggio seguente è necessario solo per i client di posta elettronica e browser.

 

Si supponga che un utente abbia selezionato il programma come Internet o programma di posta elettronica predefinito. Tale utente fa clic sull'icona **Internet** o **posta elettronica** nel menu **Start** di Windows XP o Windows Vista per aprire il programma. A questo punto, viene eseguita la riga di comando registrata come illustrato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               shell
                  open
                     command
                        (Default) = command line
```

La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando. Se il tipo di voce è REG \_ expand \_ SZ, le variabili di ambiente possono essere usate nel percorso. Utilizzare le virgolette appropriate per assicurarsi che gli spazi nella riga di comando non vengano interpretati erroneamente. La riga di comando deve eseguire il programma con le impostazioni predefinite appropriate. Per impostazione predefinita, i browser vengono generalmente predefiniti per l'home page dell'utente. I programmi di posta elettronica aprono generalmente la **posta in arrivo** dell'utente.

Nell'esempio seguente viene illustrata la registrazione di un `open` verbo per un browser di visualizzazione illuminato ipotetico. Non specifica alcuna opzione della riga di comando.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\Litview.exe"
```

Si noti che in questo valore le virgolette vengono posizionate intorno al tracciato perché contiene spazi incorporati. Se si ometteno queste virgolette, la riga di comando potrebbe essere interpretata erroneamente.

### <a name="registering-installation-information"></a>Registrazione delle informazioni di installazione

> [!Note]  
> Questa sezione non si applica a Windows Server 2003.

 

-   [Comando reinstalla](#the-reinstall-command)
-   [Comando Nascondi icone](#the-hide-icons-command)
-   [Comando Mostra icone](#the-show-icons-command)
-   [Configurazione del programma di gruppo](#group-program-configuration)
-   [Esempio di registrazione del browser](#browser-registration-example)

La funzionalità con cui l'utente seleziona programmi predefiniti per computer viene denominata e accessibile come illustrato nella tabella seguente. In Windows Vista è stata introdotta una nuova funzionalità, che consente di **impostare i programmi predefiniti** in base ai quali un utente può impostare le impostazioni predefinite per utente.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Sistema operativo</th>
<th>Titolo</th>
<th>Percorso di accesso</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows 7</td>
<td>Impostare l'accesso al programma e le impostazioni predefinite del computer</td>
<td><ul>
<li>Opzione <strong>programmi predefiniti</strong> menu <strong>Start</strong></li>
<li><strong>Programmi predefiniti</strong> Elemento del pannello di controllo</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows Vista</td>
<td>Impostare l'accesso al programma e le impostazioni predefinite del computer</td>
<td><ul>
<li>Opzione <strong>programmi predefiniti</strong> menu <strong>Start</strong></li>
<li><strong>Programmi predefiniti</strong> Elemento del pannello di controllo</li>
</ul></td>
</tr>
<tr class="odd">
<td>Windows XP SP2</td>
<td>Impostare l'accesso al programma e le impostazioni predefinite</td>
<td><ul>
<li>Menu <strong>Start</strong></li>
<li><strong>Installazione applicazioni</strong> Elemento del pannello di controllo</li>
</ul></td>
</tr>
<tr class="even">
<td>Windows XP SP1</td>
<td>Configura programmi</td>
<td><ul>
<li><strong>Installazione applicazioni</strong> Elemento del pannello di controllo</li>
</ul></td>
</tr>
</tbody>
</table>



 

Per semplicità, in questo argomento viene usato il titolo di Windows 7 della funzionalità. Tutte le versioni della funzionalità sono comunemente denominate SPAD.

> [!Note]  
> Se si esegue Windows 2000 o Windows XP, è necessario che sia installato almeno Windows 2000 SP3 o Windows XP SP1 per visualizzare la pagina **Imposta accesso al programma e impostazioni predefinite** . In Windows Vista e versioni successive, l'accesso alla pagina **Imposta accesso al programma e impostazioni predefinite computer** richiede privilegi di amministratore. Per questo motivo, gli sviluppatori sono invitati a eseguire la registrazione per l'elemento [impostare i programmi predefiniti](default-programs.md) del pannello di controllo in modo che tutti gli utenti possano gestire le impostazioni predefinite dell'applicazione.

 

Nell'albero del registro di sistema seguente viene illustrata la varietà di informazioni che devono essere registrate nella chiave **InstallInfo** del programma affinché il programma venga visualizzato nella pagina **Imposta accesso al programma e impostazioni predefinite computer** come opzione per il tipo di client. Ognuno di questi valori viene descritto in dettaglio nelle sezioni seguenti.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  HideIconsCommand = command line
                  ReinstallCommand = command line
                  ShowIconsCommand = command line
                  IconsVisible = 1
```

La riga di comando deve specificare un percorso assoluto completo del file, seguito da opzioni facoltative della riga di comando. Utilizzare le virgolette appropriate per assicurarsi che gli spazi nella riga di comando non vengano interpretati erroneamente.

### <a name="the-reinstall-command"></a>Comando reinstalla

La riga di comando reinstalla dichiarata nel valore ReinstallCommand viene eseguita quando l'utente utilizza la pagina impostazione **impostazioni predefinite computer e accesso** al programma per selezionare il programma come predefinito per il tipo di client. In Windows Vista e versioni successive, per accedere a questa pagina è necessario un livello di privilegi di amministratore. In Windows 8, se l'applicazione è stata registrata con lo stesso nome sia per l'accesso al programma sia per le **impostazioni predefinite del computer** e per i **programmi predefiniti**, le impostazioni predefinite specificate nei **programmi predefiniti** per l'applicazione verranno applicate per l'utente corrente, nonché per l'esecuzione del comando reinstalla.

Il programma avviato dalla riga di comando REINSTALL deve associare l'applicazione al set completo dei tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) che l'applicazione è in grado di gestire. Tutte le applicazioni devono stabilire la funzionalità del gestore nel comando reinstalla. Le applicazioni possono utilizzare il comando reinstalla per registrare la funzionalità e, facoltativamente, definire lo stato predefinito. Quando un'applicazione sceglie di implementare sia la funzionalità che lo stato predefinito del gestore nel comando reinstalla, deve anche ripristinare eventuali collegamenti visibili o scelte rapide desiderate. I punti di ingresso visibili scelti dalla maggior parte delle applicazioni sono elencati nel [comando Nascondi icone](#the-hide-icons-command).

> [!Note]  
> È consigliabile che le applicazioni implementino la funzionalità di gestione nel comando reinstalla.

 

Una volta completato il processo di reinstallazione, il programma avviato dalla riga di comando REINSTALL dovrebbe uscire. Non deve avviare il programma corrispondente. deve semplicemente registrare i valori predefiniti. Ad esempio, il comando reinstalla per un browser non deve aprire il home page dell'utente.

> [!Note]  
> Per i client del browser e della posta elettronica in Windows XP e Windows Vista, le applicazioni che scelgono di stabilire la funzionalità di gestione e lo stato predefinito nel comando reinstalla devono registrarsi per l'icona corrispondente nella parte superiore del menu Start. Per ulteriori informazioni, vedere la pagina relativa alla [registrazione del menu Start](#start-menu-registration) .

 

### <a name="the-hide-icons-command"></a>Comando Nascondi icone

La riga di comando dichiarata nel valore HideIconsCommand viene eseguita quando l'utente cancella la casella **Abilita accesso a questo programma** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** . Questa riga di comando deve nascondere tutti i punti di accesso del programma visibili nell'interfaccia utente. Le linee guida specifiche sono la rimozione di collegamenti e icone dalle posizioni seguenti:

-   Icone del desktop
-   Collegamenti al menu Start, incluso il gruppo di **avvio**
-   Collegamenti alla barra di avvio veloce
-   Area delle notifiche
-   Menu di scelta rapida
-   Gruppo di attività cartella

Questa riga di comando deve anche impedire chiamate automatiche del programma, ad esempio quelle specificate nella chiave **Run** del registro di sistema. I fornitori sono invitati a implementare queste linee guida nel callback Nascondi accesso dell'applicazione.

Non è necessario abbandonare la registrazione, ovvero la funzionalità dell'applicazione, dei tipi di file quando le icone sono nascoste. Non è inoltre necessario abbandonare lo stato predefinito dell'applicazione per i tipi di file e di protocollo. Questa operazione può causare un'esperienza utente errata quando questi tipi vengono rilevati nell'interfaccia utente.

Dopo aver nascosto le icone, è necessario aggiornare il valore del registro di sistema IconsVisible su 0, come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 0
```

La voce IconsVisible è di tipo **reg \_ DWORD**.

### <a name="an-alternate-hide-icons-method-in-spad"></a>Metodo Hide Icon alternativo in SPAD

Per alcune applicazioni legacy, un'implementazione completa di Hide Access potrebbe non essere pratica. Un metodo alternativo che ottiene lo stesso effetto è la disinstallazione dell'applicazione. La sezione seguente illustra il comportamento di esempio e il codice di esempio per implementare questa alternativa. In generale, i fornitori di software indipendenti (ISV) devono evitare questa alternativa, perché sarà:

-   Disinstallare completamente l'applicazione dal sistema.
-   Rimuovere le impostazioni predefinite selezionate in precedenza.
-   Non lasciare alcuna opzione dell'interfaccia utente per reinstallare l'applicazione.
-   Rendere la funzionalità Abilita accesso non più disponibile perché una disinstallazione rimuove completamente l'applicazione da SPAD.

L'esperienza utente consigliata è la seguente:

-   Quando l'utente deseleziona la casella **Abilita l'accesso a questo programma** in SPAD, viene visualizzata l'interfaccia utente seguente.

    ![finestra di dialogo per nascondere l'accesso al programma](images/hideaccessvista.png)

-   Quando l'utente seleziona **OK**, viene avviato l'elemento **programmi e funzionalità** del pannello di controllo per consentire all'utente di disinstallare l'applicazione.
-   Gli utenti di Windows XP devono essere visualizzati con questa finestra di dialogo.

    ![finestra di dialogo Windows XP equivalente](images/hideaccessxp.png)

-   Quando l'utente di Windows XP seleziona **OK**, viene avviato l'elemento del pannello di controllo **Installazione applicazioni** per consentire all'utente di disinstallare l'applicazione.

Il codice seguente fornisce un'implementazione riutilizzabile per la funzionalità Nascondi accesso, come illustrato in precedenza. Può essere utilizzato in Windows XP, Windows Vista e Windows 7.


```
#include <windows.h>
#include <shlwapi.h>
#include <strsafe.h>

PCWSTR c_pszMessage1 = L"To hide access to this program, you need to uninstall it by ";
PCWSTR c_pszMessage2 = L"using\n%s in Control Panel.\n\nWould you like to start %s?";
PCWSTR c_pszApplicationName  = L"Sample App";

int _tmain(int argc, WCHAR* argv[])
{
    OSVERSIONINFO version;
    version.dwOSVersionInfoSize = sizeof(version);

    if (GetVersionEx(&version))
    {
        PCWSTR pszCPLName = NULL;

        if (version.dwMajorVersion >= 6)
        {
            // Windows Vista and later
            pszCPLName = L"Programs and Features";
        }
        else if (version.dwMajorVersion == 5 &&
                 version.dwMinorVersion == 1)
        {
            // Windows XP
            pszCPLName = L"Add/Remove Programs";
        }

        if (pszCPLName != NULL)
        {
            WCHAR szMessage[256], szScratch[256];
            if (SUCCEEDED(StringCchPrintf(szScratch, 
                                          ARRAYSIZE(szScratch), 
                                          c_pszMessage2, 
                                          pszCPLName, 
                                          pszCPLName)))
            {
                if (SUCCEEDED(StringCchCopy(szMessage, 
                                            ARRAYSIZE(szMessage), 
                                            c_pszMessage1)))
                {
                    if (SUCCEEDED(StringCchCat(szMessage, 
                                               ARRAYSIZE(szMessage), 
                                               szScratch)))
                    {
                        if (IDOK == MessageBox(NULL, 
                                               szMessage, 
                                               c_pszApplicationName, 
                                               MB_OKCANCEL))
                        {
                            ShellExecute(NULL, 
                                         NULL, 
                                         L"appwiz.cpl", 
                                         NULL, 
                                         NULL, 
                                         SW_SHOWNORMAL);
                        }
                    }
                }
            }
        }
    }
    return 0;
}
```



### <a name="the-show-icons-command"></a>Comando Mostra icone

La riga di comando dichiarata nella voce ShowIconsCommand viene eseguita quando l'utente seleziona la casella **Abilita l'accesso a questo programma** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** . Questa riga di comando può ripristinare i punti di accesso del programma, inclusi quelli nel menu **Start** , sul desktop e nel gruppo di **avvio** , nonché le normali chiamate automatiche, ad esempio quelle specificate nella chiave **Run** del registro di sistema. I punti di accesso visibili di interesse per la maggior parte delle applicazioni sono elencati nel [comando Nascondi icone](#the-hide-icons-command). L'applicazione non deve modificare le impostazioni predefinite per utente; tale modifica deve essere eseguita dall'utente tramite **programmi predefiniti**.

Una volta visualizzate correttamente le icone, è necessario aggiornare il valore del registro di sistema IconsVisible a 1, come illustrato:

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  IconsVisible = 1
```

Si noti che se è stata usata la voce HideIconsCommand per richiedere una disinstallazione dell'applicazione, la voce ShowIconsCommand non è usata. Deve essere rimosso dal registro di sistema con le informazioni rimanenti dell'applicazione durante il processo di disinstallazione.

### <a name="group-program-configuration"></a>Configurazione del programma di gruppo

> [!Note]  
> Questa sezione non si applica a Windows 2000.

 

Come parte della preparazione del sistema, un OEM può stabilire una configurazione che nasconda i punti di accesso per il browser Microsoft, la posta elettronica, la riproduzione multimediale, la messaggistica istantanea o la macchina virtuale per i programmi client Java e specifica i propri programmi predefiniti. Gli OEM possono consentire agli utenti di reimpostare i computer in qualsiasi momento a questa configurazione predefinita impostando i valori del registro di sistema seguenti.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            CanonicalName
               InstallInfo
                  OEMShowIcons = 1
                  OEMDefault = 1
```

Se queste chiavi sono impostate, gli utenti possono ripristinare la configurazione OEM selezionando l'opzione **produttore computer** nella pagina **Imposta accesso al programma e impostazioni predefinite computer** . Se queste chiavi non sono impostate, l'opzione **produttore computer** non viene visualizzata.

La voce **OEMShowIcons** , se presente, imposta lo stato di visualizzazione dell'icona per il client specificato che viene applicato se l'utente seleziona **produttore computer**. Il valore 1 indica che le icone vengono visualizzate e il valore 0 indica che le icone non vengono visualizzate. Se **OEMShowIcons** è assente, la selezione del **produttore del computer** non ha alcun effetto sull'impostazione Mostra icona. **OEMShowIcons** è di tipo **reg \_ DWORD**.

La voce **OEMDefault** , se presente e impostata su 1, stabilisce la preferenza OEM per il client predefinito del tipo indicato. È possibile contrassegnare come predefinito OEM un solo client di un determinato tipo. Se più di una registrazione del client contiene la voce **OEMDefault** , verranno ignorate e il client corrente continuerà a essere usato come client predefinito. Se la voce **OEMDefault** non è presente o è impostata su 0, il client specifico non viene utilizzato come client predefinito se l'utente seleziona **produttore computer**. **OEMDefault** è di tipo **reg \_ DWORD**.

Oltre all'opzione per reimpostare i computer sulla configurazione predefinita stabilita dall'OEM, gli utenti dispongono di altre tre opzioni di configurazione:

-   Impostare il computer su una configurazione di Microsoft Windows. In questo caso, la pagina **set Program Access and computer defaults** consente l'accesso a tutti i software Microsoft e non Microsoft nel computer registrato nelle categorie di prodotti pertinenti. I programmi Microsoft Windows sono selezionati come opzione predefinita per ogni categoria.
-   Impostare il computer su una configurazione non Microsoft. Questa configurazione consente di nascondere i punti di accesso (ad esempio il menu **Start** ) a Windows Internet Explorer, Windows Media Player, Windows Messenger e Microsoft Outlook Express. Consente l'accesso al software non Microsoft nel computer in queste categorie. Inoltre, se in una categoria è disponibile un programma non Microsoft, viene impostato come predefinito per tale categoria. Se in una categoria è disponibile più di un programma non Microsoft, all'utente viene chiesto di scegliere il programma non Microsoft da usare come predefinito.
-   Definire una configurazione personalizzata. Gli utenti scelgono le proprie selezioni per abilitare o rimuovere l'accesso, combinando programmi Microsoft e non Microsoft nel modo appropriato. Gli utenti stabiliscono le opzioni predefinite in base alla categoria.

Gli utenti possono modificare una qualsiasi di queste opzioni in qualsiasi momento.

### <a name="browser-registration-example"></a>Esempio di registrazione del browser

Nell'esempio seguente viene illustrata la registrazione completa di **InstallInfo** per un browser di visualizzazione illuminato fittizio. In questo caso, le opzioni della riga di comando consentono al file Litview.exe di eseguire qualsiasi azione necessaria per ogni valore.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\Litview.exe" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\Litview.exe" /showicons
                  IconsVisible = 1
```

Si noti che le virgolette vengono posizionate intorno ai percorsi perché contengono spazi incorporati.

## <a name="registration-elements-for-specific-client-types"></a>Elementi di registrazione per tipi client specifici

Le informazioni seguenti sono reperibili anche nelle risorse elencate nella sezione Argomenti correlati alla fine di questo argomento.

-   [Registrazione del menu Start](#start-menu-registration)
-   [Registrazione client di posta elettronica](#mail-client-registration)

### <a name="start-menu-registration"></a>Registrazione del menu Start

In Windows XP le applicazioni sono in genere registrate per impostazione predefinita in un ambito a livello di computer (**HKEY \_ locale \_**) anziché un utente (**HKEY \_ Current \_ User**). Con l'introduzione di Windows Vista del controllo dell'account utente, le applicazioni che attestano gli slot **Internet** e di **posta elettronica** nel menu **Start** devono implementare il comando reinstalla nel contesto di esecuzione corretto.

> [!Note]  
> Il collegamento di **posta elettronica** del menu Start è stato rimosso a partire da Windows 7. Tuttavia, la registrazione descritta in questa sezione dovrebbe essere comunque eseguita perché assegna il client MAPI predefinito.

 

Un utente con limitazioni su Windows XP, Windows Vista o Windows 7 non può accedere a SPAD. Per questo motivo, gli sviluppatori sono invitati a eseguire la registrazione per l'elemento **impostare i programmi predefiniti** del pannello di controllo in modo che qualsiasi utente possa gestire le impostazioni predefinite dell'applicazione per utente.

Le selezioni effettuate in SPAD devono avere effetto solo sulle impostazioni per computer.

Impostare il valore del registro di sistema come indicato di seguito.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         ClientTypeName
            (Default) = CanonicalName
```

> [!Note]
> 
> **Le informazioni seguenti si applicano solo a Windows XP.**
> 
> Se la registrazione dell'impostazione predefinita a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito positivo, l'applicazione deve eliminare il valore assegnato alla voce predefinita nella sottochiave seguente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
> ```
> 
> Se la registrazione del valore predefinito a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito negativo, in genere perché l'utente non dispone dell'autorizzazione di scrittura per la sottochiave, l'applicazione deve impostare il valore seguente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          ClientTypeName
>             (Default) = CanonicalName
> ```
> 
> Il nome canonico viene registrato solo per l'utente corrente, non per tutti gli utenti.

 

Dopo l'aggiornamento delle chiavi del registro di sistema, il programma deve trasmettere il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con **wParam** = 0 e **lParam** che punta alla stringa con terminazione null "software \\ clients \\ **ClientTypeName**" per notificare al sistema operativo che il client predefinito è stato modificato.

### <a name="mail-client-registration"></a>Registrazione client di posta elettronica

Per un client di posta elettronica, è necessario che il programma disponga di impostazioni registrate sotto la chiave mailto **\_ \_ radice delle classi HKEY**, \\  in modo da soddisfare gli URL che utilizzano il `mailto` protocollo. Impostare i valori e le chiavi che rispecchiano tali impostazioni nella chiave seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
```

Questa gerarchia del registro di sistema sostituisce la `mailto` gerarchia esistente del registro di sistema disponibile in **HKEY \_ classi \_ radice** \\ **mailto**. La gerarchia rimane invariata, ma solo il percorso è stato modificato. Il formato di questa gerarchia è documentato in MSDN nelle panoramiche [e nelle esercitazioni del protocollo di collegamento asincrono](/previous-versions//aa767913(v=vs.85)). In genere, il `mailto` protocollo viene registrato in un programma anziché in un protocollo asincrono, nel qual caso viene applicata la documentazione relativa alla [registrazione di un'applicazione a uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85)) .

Nell'esempio seguente viene illustrata la `mailto` sezione della registrazione per un `mailto` gestore registrato in un programma.

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            CanonicalName
               Protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = %FilePath%,IconIndex
                     shell
                        open
                           command
                              (Default) = command line
```

Il valore del registro di sistema flag è documentato in [tipi di file](fa-file-types.md) nella sezione intitolata "definizione degli attributi dei tipi di file".

## <a name="complete-sample-registrations"></a>Completa registrazioni di esempio

Gli esempi seguenti sono forniti per mostrare i requisiti di registrazione completi per i vari tipi di client.

-   [Un browser di esempio](#a-sample-browser)
-   [Un browser di posta elettronica di esempio](#a-sample-mail-browser)
-   [Media Player di esempio](#a-sample-media-player)
-   [Programma Instant Messenger di esempio](#a-sample-instant-messenger-program)
-   [Una macchina virtuale di esempio per Java](#a-sample-virtual-machine-for-java)

### <a name="a-sample-browser"></a>Un browser di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         StartMenuInternet
            LITVIEW.EXE
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
                  shell
                     open
                        command
                           (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /homepage
```

### <a name="a-sample-mail-browser"></a>Un browser di posta elettronica di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Mail
            Lit View
               (Default) = Lit View
               DLLPath = @C:\Program Files\LItwareInc\LitwareMAPI.dll
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
               shell
                  open
                     command
                        (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /inbox
               protocols
                  mailto
                     (Default) = URL:MailTo Protocol
                     EditFlags = 02 00 00 00
                     URL Protocol
                     DefaultIcon
                        (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
                     shell
                        open
                           command
                              (Default) = "C:\Program Files\LitwareInc\LITVIEW.EXE" /mailto:%1
```

### <a name="a-sample-media-player"></a>Media Player di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         Media
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-instant-messenger-program"></a>Programma Instant Messenger di esempio

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         IM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

### <a name="a-sample-virtual-machine-for-java"></a>Una macchina virtuale di esempio per Java

```
HKEY_LOCAL_MACHINE
   Software
      Clients
         JavaVM
            Lit View
               (Default) = Lit View
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LITVIEW.EXE,1
               InstallInfo
                  ReinstallCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /reinstall
                  HideIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /hideicons
                  ShowIconsCommand = "C:\Program Files\LitwareInc\LITVIEW.EXE" /showicons
                  IconsVisible = 1
```

*Le società, le organizzazioni, i prodotti, i nomi di dominio, gli indirizzi di posta elettronica, i logo, le persone, i luoghi e gli eventi di esempio descritti nel presente documento sono fittizi. Nessuna associazione con nessuna società, organizzazione, prodotto, nome di dominio, indirizzo di posta elettronica, logo, persona, luogo o evento è intenzionale o può essere presupposta.*

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Programmi predefiniti](default-programs.md)
</dt> <dt>

[Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows](start-menu-reg.md)
</dt> <dt>

[Layout del registro di sistema del client di Internet Explorer (vedere la sezione "definizioni della chiave del registro di sistema")](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa753633(v=vs.85))
</dt> <dt>

[Panoramica ed esercitazioni sul protocollo di collegamento asincrono](/previous-versions//aa767913(v=vs.85))
</dt> <dt>

[Registrazione di un'applicazione in uno schema URI](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa767914(v=vs.85))
</dt> </dl>

 

 
