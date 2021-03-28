---
description: Il menu Start di Windows XP e Windows Vista contiene slot riservati per i client Internet (browser) e di posta elettronica (posta) predefiniti, insieme comunemente noti come applicazioni Internet del menu Start.
ms.assetid: a3d7416f-0dbd-4af2-ab38-758f9cc8aec5
title: Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccdd8fb8efe32522947b30ab2ce1a50b7058e97
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "104234554"
---
# <a name="how-to-register-an-internet-browser-or-email-client-with-the-windows-start-menu"></a>Come registrare un browser Internet o un client di posta elettronica con il menu Start di Windows

> [!Note]  
> Questo argomento si applica a Windows XP, Windows Vista e Windows 7.

 

Il menu Start di Windows XP e Windows Vista contiene slot riservati per i client **Internet** (browser) e di **posta elettronica** (posta) predefiniti, insieme comunemente noti come *applicazioni Internet del menu Start*. Le applicazioni che si registrano come applicazioni Internet del menu Start eseguono questa operazione nell'intero sistema (per computer). In Windows Vista, l'utente può utilizzare la funzionalità **programmi predefiniti** per impostare un valore predefinito per singolo utente.

Quando le applicazioni si registrano come applicazioni Internet del menu Start, Windows XP e Windows Vista creano icone **Internet** e **posta elettronica** dal menu Start. Se si fa clic su queste icone, il menu Start controlla il sottoalbero del registro di sistema per utente (**HKEY \_ Current \_ User**). Se non viene trovata alcuna impostazione predefinita per utente, il menu Start Cerca la sottochiave predefinita per computer nel sottoalbero **del \_ \_ computer locale HKEY** .

> [!Note]  
> L'installazione predefinita di Windows non registra un programma Internet o di posta elettronica predefinito per ogni utente, ma solo un valore predefinito a livello di sistema. Questo fornisce un percorso di aggiornamento uniforme rispetto alle versioni precedenti del sistema operativo, in cui \_ \_ è supportato solo il sottoalbero del computer locale HKEY per le registrazioni client.

 

In questo argomento vengono illustrati gli elementi seguenti:

-   [Registrazione per il collegamento Internet del menu Start](#registering-for-the-start-menu-internet-link)
    -   [Come registrarsi come client Internet predefinito](#how-to-register-as-the-default-internet-client)
-   [Registrazione per il collegamento di posta elettronica del menu Start](#registering-for-the-start-menu-email-link)
    -   [Visualizzazione del client di posta elettronica predefinito nel menu Start](#how-the-start-menu-displays-the-default-email-client)
    -   [Come registrarsi come client di posta elettronica predefinito](#how-to-register-as-the-default-email-client)
-   [Personalizzazione del menu di scelta rapida](#customizing-the-context-menu)

## <a name="registering-for-the-start-menu-internet-link"></a>Registrazione per il collegamento Internet del menu Start

> [!Note]  
> Questa registrazione è deprecata a partire da Windows 7, che non fornisce più un collegamento Internet del menu Start. Le registrazioni esistenti vengono ignorate in Windows 7 e versioni successive. La registrazione come applicazione Internet predefinita del menu Start non corrisponde a quella registrata come Web browser predefinito. Il Web browser predefinito viene utilizzato per avviare URL arbitrari da qualsiasi punto del sistema. L'applicazione Internet del menu Start controlla semplicemente il programma avviato quando l'utente fa clic sull'icona Internet nel menu Start.

 

Qualsiasi applicazione Web browser può essere registrata per essere visualizzata come client Internet nel menu Start. Questa visibilità, associata alla registrazione corretta per i tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) di un'applicazione, fornisce uno stato del browser predefinito dell'applicazione.

Le registrazioni effettuate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** hanno una precedenza maggiore per l'utente della console rispetto alle registrazioni corrispondenti effettuate nel **\_ \_ computer locale HKEY**. Per i nuovi utenti del sistema, vengono usate le impostazioni archiviate nel **\_ \_ computer locale HKEY** . A partire da Windows XP, le impostazioni Internet del menu Start vengono mantenute nelle voci predefinite dei due percorsi del registro di sistema:

-   **HKEY \_ Client \_ software utente corrente** \\  \\  \\ **StartMenuInternet**
-   **HKEY \_ Client software del \_ computer locale** \\  \\  \\ **StartMenuInternet**

La sottochiave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **StartMenuInternet** descrive il browser Internet che viene avviato quando l'utente fa clic sull'icona **Internet** nel menu Start. Se la sottochiave è vuota o mancante, l'icona **Internet** nel menu Start viene impostata sul valore predefinito di sistema archiviato nella seconda posizione in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **StartMenuInternet** , che descrive tutte le applicazioni del browser Internet installate nel sistema.

Quando un nuovo utente accede al sistema, nel menu Start viene usato il valore predefinito nella sottochiave in **HKEY \_ \_ computer locale** \\  \\ **client** software \\ **StartMenuInternet** per visualizzare il client Internet predefinito e avvia l'applicazione registrata quando si fa clic sull'icona.

### <a name="how-to-register-as-the-default-internet-client"></a>Come registrarsi come client Internet predefinito

Sotto la sottochiave **HKEY \_ \_ computer locale** \\  \\ **client** software \\ **StartMenuInternet** possono essere presenti zero o più sottochiavi, una per ogni applicazione Internet browser registrata. Ad esempio, un sistema ipotetico potrebbe avere questa disposizione:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            IEXPLORE.EXE
            BROWSER2.EXE
            BROWSER3.EXE
```

Vengono illustrate le voci del registro di sistema con un ipotetico browser denominato "Lit View" di una società fittizia denominata Litware Inc. si supponga che il nome dell'eseguibile per la visualizzazione illuminata sia Litview.exe. La registrazione della visualizzazione illuminata viene eseguita come indicato di seguito:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-123
```

I dati LocalizedString sono di tipo REG \_ SZ oppure reg \_ expand \_ SZ se vengono usate variabili di percorso come `%programfiles%` . LocalizedString fornisce il percorso di un file eseguibile (con estensione exe) o di una libreria (. dll). Si noti che la stringa di percorso inizia con un simbolo di chiocciola (@) e che non sono necessarie virgolette intorno al percorso indipendentemente dagli spazi al suo interno. Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno della DLL specificata, il cui valore deve essere visualizzato all'utente. In questo modo è possibile usare la stessa registrazione per più linguaggi. Ogni lingua fornisce un ResourceDLL.dll diverso. Ciò consente al sistema di visualizzare la stringa corretta in base alla lingua attualmente selezionata.

Il valore REG \_ sz o reg \_ expand \_ SZ seguente informa il menu Start dell'icona predefinita da visualizzare quando l'utente seleziona visualizzazione illuminata come browser Internet del menu Start.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitView.exe,1
```

La sottochiave del registro di sistema seguente consente di specificare una riga di comando da eseguire quando l'utente fa clic sul comando di menu Internet nel menu Start, supponendo che la visualizzazione illuminata sia il browser Internet selezionato dal menu Start. Ad esempio, il comando può aprire il browser con l'home page dell'utente oppure il comando può avviare un'interfaccia utente introduttiva che il fornitore di software indipendente (ISV) ritiene sia appropriato. I dati sono di tipo REG \_ sz o reg \_ expand \_ SZ, ma si noti che, dal momento che nel percorso della riga di comando è presente uno spazio, il percorso eseguibile è racchiuso tra virgolette.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            LITVIEW.EXE
               shell
                  open
                     (Default) = "C:\Program Files\LitwareInc\LitView.exe" -welcome
```

Quando l'utente specifica tramite [set Program Access e computer Defaults (SPAD)](cpl-setprogramaccess.md) che Lit View deve essere utilizzato come Web browser predefinito a livello di computer, l'applicazione deve impostare la seguente \_ voce reg SZ. Si noti che poiché SPAD viene eseguito con privilegi di amministratore, è consentito l'accesso a questa sottochiave.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         StartMenuInternet
            (Default) = LITVIEW.EXE
```

> [!Note]
> In Windows Vista, il Web browser predefinito a livello di utente deve essere impostato utilizzando lo strumento **programmi predefiniti** , non [SPAD](cpl-setprogramaccess.md).
> 
> **Le informazioni seguenti si applicano solo a Windows XP.**
> 
> Se la registrazione del Web browser predefinito a livello di computer nel computer \_ locale HKEY \_ come illustrato in precedenza ha esito positivo, l'applicazione deve eliminare la voce predefinita nella sottochiave seguente:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          StartMenuInternet
> ```
> 
> Se la registrazione del Web browser predefinito a livello di computer nel computer \_ locale HKEY ha \_ esito negativo, l'applicazione deve impostare i \_ dati reg SZ come illustrato in questo esempio per l'applicazione di visualizzazione illuminata:
> 
> ```
> HKEY_CURRENT_USER
>    SOFTWARE
>       Clients
>          (Default) = LITVIEW.EXE
> ```

 

Dopo aver aggiornato le sottochiavi appropriate, l'applicazione trasmette il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con il parametro *wParam* impostato su 0 e il parametro *lParam* che punta alla stringa con terminazione null `"Software\Clients\StartMenuInternet"` . Viene notificato al sistema operativo che il client predefinito è stato modificato.

L'impostazione di queste sottochiavi per il browser Internet predefinito del menu Start è necessaria per mantenere la compatibilità con le versioni precedenti di Web browser che non supportano le registrazioni per singolo utente.

## <a name="registering-for-the-start-menu-email-link"></a>Registrazione per il collegamento di posta elettronica del menu Start

> [!Note]  
> Il collegamento di posta elettronica del menu Start è stato rimosso a partire da Windows 7. Questa registrazione, tuttavia, descritta in questa sezione dovrebbe comunque essere eseguita per l'assegnazione del client MAPI predefinito.

 

### <a name="how-the-start-menu-displays-the-default-email-client"></a>Visualizzazione del client di posta elettronica predefinito nel menu Start

Qualsiasi applicazione di posta elettronica può essere registrata per essere visualizzata come client di posta elettronica nel menu Start. Questa visibilità, abbinata alla registrazione corretta per i tipi di [file](fa-intro.md) e di [protocollo](/previous-versions//aa767743(v=vs.85)) di un'applicazione, fornisce uno stato di posta predefinito per l'applicazione.

Le registrazioni effettuate nel sottoalbero dell' **\_ \_ utente corrente di HKEY** hanno una precedenza maggiore per l'utente della console rispetto alle registrazioni corrispondenti effettuate nel **\_ \_ computer locale HKEY**. Per i nuovi utenti del sistema, vengono usate le impostazioni archiviate nel **\_ \_ computer locale HKEY** . A partire da Windows XP, le impostazioni di posta elettronica del menu Start vengono mantenute nelle voci predefinite dei due percorsi del registro di sistema:

-   **HKEY \_ \_** \\  \\  \\ **Posta elettronica** client software utente corrente
-   **HKEY \_ \_** \\  \\  \\ **Posta elettronica** client del computer locale

La sottochiave **HKEY \_ Current \_ User** \\ **software** \\ **clients** \\ **mail** descrive il client di posta elettronica che viene avviato quando l'utente fa clic sull'icona del **messaggio di posta elettronica** nel menu Start.

La sottochiave **HKEY \_ Local \_ computer** \\ **software** \\ **clients** \\ **mail** descrive le applicazioni di posta elettronica installate nel sistema e l'applicazione di posta elettronica predefinita.

Se la posta elettronica client del software **\_ \_ utente corrente di HKEY** \\  \\  \\  è vuota o mancante, il valore predefinito definito in **HKEY \_ \_ computer locale** \\  \\ **client** software \\  viene usato per selezionare l'applicazione di posta elettronica che viene visualizzata nel menu Start.

Quando un nuovo utente accede al sistema, nel menu Start viene usato il valore predefinito nella sottochiave in **HKEY \_ Local \_ Machine** \\ **software** \\ **clients** \\ **mail** per visualizzare il client di posta elettronica predefinito e avvia l'applicazione registrata quando si fa clic sull'icona.

### <a name="how-to-register-as-the-default-email-client"></a>Come registrarsi come client di posta elettronica predefinito

**HKEY \_ I client software del \_ computer locale** \\  \\  \\  possono contenere zero o più sottochiavi, una per ogni applicazione di posta elettronica registrata. Un ipotetico sistema, ad esempio, può definire le sottochiavi seguenti:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            Eudora
            Windows Mail
```

In questo articolo vengono illustrate le voci del registro di sistema con un ipotetico client di posta elettronica denominato "Lit Mail" della società fittizia denominata Litware Inc. Litware Inc. decide di registrare il client di posta elettronica con il nome interno "LitMail". Come per un browser, il nome interno è una stringa univoca usata come nome della sottochiave, ma non viene mai visualizzata all'utente.

Per installare il client di posta elettronica per la posta illuminata come predefinita, usano la sottochiave e le voci seguenti:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               (Default) = Lit Mail
               LocalizedString = @C:\Program Files\LitwareInc\ResourceDLL.dll,-456
```

I dati LocalizedString sono di tipo REG \_ SZ oppure reg \_ expand \_ SZ se vengono usate variabili di percorso come `%programfiles%` . LocalizedString fornisce il percorso di un file eseguibile (con estensione exe) o di una libreria (. dll). Si noti che la stringa di percorso inizia con un simbolo di chiocciola (@) e che non sono necessarie virgolette intorno al percorso indipendentemente dagli spazi al suo interno. Il numero intero decimale è l'ID di una risorsa di tipo stringa, contenuto all'interno della DLL specificata, il cui valore deve essere visualizzato all'utente. In questo modo è possibile usare la stessa registrazione per più linguaggi. Ogni lingua fornisce un ResourceDLL.dll diverso. Ciò consente al sistema di visualizzare la stringa corretta in base alla lingua attualmente selezionata.

Dopo aver aggiornato le sottochiavi appropriate, l'applicazione trasmette il messaggio [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md) con il parametro *wParam* impostato su 0 e il parametro *lParam* che punta alla stringa con terminazione null `"Software\Clients\Mail"` . Viene notificato al sistema operativo che il client predefinito è stato modificato.

Per garantire la compatibilità con le applicazioni che non supportano le stringhe localizzate, il nome dell'applicazione nella lingua installata deve essere impostato anche come valore predefinito per la sottochiave.

Il valore **reg \_ SZ** o **reg \_ expand \_ SZ** seguente informa il menu Start dell'icona predefinita da visualizzare quando l'utente seleziona la posta illuminata come programma di posta elettronica del menu Start:

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               DefaultIcon
                  (Default) = C:\Program Files\LitwareInc\LitMail.exe,1
```

La voce seguente consente di specificare una riga di comando da eseguire quando l'utente fa clic sulla voce di menu della **posta elettronica** nel menu Start, supponendo che la posta elettronica sia il programma di posta elettronica del menu Start selezionato. Questa riga di comando viene eseguita anche se l'utente seleziona **Leggi messaggio di posta elettronica** dal menu **strumenti** di Windows Internet Explorer. I dati sono di tipo **reg \_ SZ** o **reg \_ expand \_ SZ**, ma si noti che, dal momento che nel percorso della riga di comando è presente uno spazio, il percorso eseguibile è racchiuso tra virgolette.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            shell
               open
                  command
                     (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -inbox
```

Se (e solo se) *l'utente* specifica che la posta elettronica è stata accesa come applicazione di posta elettronica predefinita del menu Start, l'applicazione di posta elettronica illuminata può scrivere il proprio nome interno nel seguente valore **reg \_ SZ** :

```
HKEY_CURRENT_USER
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

Se (e solo se) *l'utente* specifica la posta illuminata come applicazione di posta elettronica predefinita a livello di sistema, l'applicazione di posta elettronica illuminata può scrivere il proprio nome interno nel valore **reg \_ SZ** specificato di seguito. Si noti che l'accesso a questa sottochiave potrebbe essere limitato. Le applicazioni non devono presupporre che tutti gli utenti dispongano delle autorizzazioni per modificare l'applicazione di posta elettronica predefinita a livello di sistema.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            (Default) = LitMail
```

La registrazione come applicazione di posta elettronica predefinita del menu Start non equivale alla registrazione come client di posta elettronica predefinito del sistema o gestore *mailto* registrato.

-   Il client di posta elettronica predefinito del sistema viene avviato quando l'utente fa clic su **Leggi messaggio di posta elettronica** dal menu **strumenti** di Internet Explorer.
-   Il gestore *mailto* registrato viene avviato quando l'utente fa clic su un URL del modulo `mailto:someone@example.com` .
-   L'applicazione di posta elettronica del menu Start viene avviata quando l'utente fa clic sull'icona del **messaggio di posta elettronica** nel menu Start.

Se non viene specificata alcuna applicazione di posta elettronica predefinita del menu Start, l'icona del messaggio di posta elettronica nel menu Start avvia il client di posta elettronica predefinito del sistema.

In questo argomento non viene illustrata la registrazione dell'applicazione come gestore di protocollo *mailto* predefinito. Le applicazioni che si desidera registrare in questo modo devono continuare a seguire le specifiche esistenti in questo argomento.

## <a name="customizing-the-context-menu"></a>Personalizzazione del menu di scelta rapida

Un'applicazione può personalizzare le pagine delle proprietà visualizzate quando l'utente seleziona **Proprietà** dal menu di scelta rapida dell'icona del **messaggio di posta elettronica** (o **Internet**). Ad esempio, l'applicazione Litware email aggiunge i dati **reg \_ SZ** o **reg \_ expand \_ SZ** seguenti per visualizzare una finestra delle proprietà personalizzata per l'icona del **messaggio di posta elettronica** anziché la relativa finestra delle proprietà predefinita.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  properties
                     MUIVerb = @C:\Program Files\LitwareInc\ResourceDLL.dll,-789
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -properties
```

L'elemento di dati MUIVerb viene costruito a partire da un segno "at" (@), seguito dal percorso completo della DLL della risorsa, da una virgola, da un segno meno (-) e quindi dall'identificatore di risorsa della stringa decimale da visualizzare. Si noti che il percorso del programma LitMail.exe contiene spazi, quindi la stringa di percorso viene posizionata tra virgolette.

Un'applicazione può anche aggiungere altri comandi al menu di scelta rapida. Ad esempio, l'applicazione Litware email aggiunge un comando **Find** con i seguenti dati **reg \_ SZ** :

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Clients
         Mail
            LitMail
               shell
                  find
                     MUIVerb = @C:\Program File\LitwareInc\ResourceDLL.dll,-790
                     command
                        (Default) = "C:\Program Files\LitwareInc\LitMail.exe" -contacts
```

Il nome della sottochiave sottostante **Shell** , in questo caso "Find", è un nome arbitrario e non localizzato. Anche in questo caso i dati di MUIVerb contengono un segno di chiocciola (@) come primo elemento, seguito dal percorso di una DLL di risorse, da un separatore virgola e quindi da un segno meno che precede l'identificatore di risorsa della stringa decimale. Ad esempio, la risorsa stringa potrebbe essere "Apri rubrica". Si noti infine che la stringa della riga di comando contiene spazi, quindi è racchiusa tra virgolette.

 

 
