---
description: Pannello di controllo elementi implementati in una DLL che esporta la funzione CPlApplet hanno requisiti di registrazione diversi rispetto ai .exe file.
title: Come registrare gli elementi di Pannello di controllo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b25fffb3b06f93640c5ca8623fb24ffb53c6fd3ecae0b9e23cabafacdceba8f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593191"
---
# <a name="how-to-register-dll-control-panel-items"></a>Come registrare gli elementi di Pannello di controllo DLL

> [!Note]  
> Le linee guida di implementazione correnti Pannello di controllo che i nuovi elementi devono essere implementati come .exe anziché .cpl file. Le informazioni seguenti sono incluse principalmente per scopi legacy.

 

Pannello di controllo elementi implementati in una DLL che esporta la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) hanno requisiti di registrazione diversi da quelli .exe file. A Windows XP, le nuove DLL Pannello di controllo elemento devono essere installate nella cartella dell'applicazione associata nella cartella Programmi. Non è necessario registrare gli elementi archiviati nella directory System32 .cpl'estensione . vengono visualizzati automaticamente nel Pannello di controllo. Tutti gli Pannello di controllo che usano **CPlApplet** devono essere registrati in uno dei due modi seguenti:

-   Se l'elemento Pannello di controllo deve essere disponibile per tutti gli utenti, registrare il percorso in base al computer aggiungendo un valore **REG \_ EXPAND \_ SZ** alla sottochiave **HKEY LOCAL \_ \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Pannello di controllo** \\ **Cpls,** impostare sul percorso DLL.
-   Se l Pannello di controllo'elemento deve essere disponibile per ogni utente, usare **HKEY \_ CURRENT \_ USER** come chiave radice anziché **HKEY \_ LOCAL \_ MACHINE.**

I due esempi seguenti registrano *l'elemento Pannello di controllo MyCplApp.* La DLL è denominata MyCpl.cpl e si trova nella directory *dell'applicazione \\ MyCorp MyApp.* Questo primo esempio illustra la registrazione per computer.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere queste informazioni al Registro di sistema per registrare l'esistenza .cpl file.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a>Passaggio 2:

**Windows Vista e versioni successive:** Aggiungere queste informazioni aggiuntive al Registro di sistema per fornire un GUID per l Pannello di controllo seguente.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

Generando un GUID per identificare in modo univoco l'elemento Pannello di controllo, è possibile aggiungere collegamenti di attività al Pannello di controllo. Senza questo GUID, non è possibile associare i collegamenti di attività all'elemento Pannello di controllo attività. Vedere [Creating Searchable Task Links for a Pannello di controllo Item](creating-searchable-task-links.md).

### <a name="step-3"></a>Passaggio 3:

**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al Registro di sistema per creare un nome canonico per l'elemento.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

Aggiungendo un nome canonico, gli utenti possono avviare l Pannello di controllo comando da una riga di comando immettendo `control.exe /name MyCorporation.MyCpl` . In questo modo è anche possibile modificare un'implementazione da un file .cpl a un file .exe in un secondo momento, senza dover chiamare programmi per apportare modifiche perché possono continuare ad aprire l'elemento tramite il nome canonico. Per altre informazioni sui nomi canonici, vedere [Executing Pannello di controllo Items](executing-control-panel-items.md).

### <a name="step-4"></a>Passaggio 4:

**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al Registro di sistema per assegnare un Pannello di controllo a una o più categorie.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

**Windows XP:** Aggiungere le informazioni seguenti al Registro di sistema per assegnare un Pannello di controllo a una o più categorie.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

Questo esempio assegna l'elemento alla categoria 3, ovvero Rete e Internet. Per aggiungere un elemento a più categorie, specificare l'elenco come valore REG SZ separato da virgole, ad esempio \_ "3,8". I valori possono essere specificati come decimali o esadecimali. Si noti che la possibilità di aggiungere un elemento a più categorie è possibile solo in Windows XP Service Pack 2 (SP2) e versioni successive. Vedere [Assegnazione Pannello di controllo categorie per](assigning-control-panel-categories.md) tutti i valori possibili.

### <a name="step-5"></a>Passaggio 5:

**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al Registro di sistema per creare e puntare a un file XML per contenere i collegamenti alle attività per l'elemento. Il valore deve essere un percorso REG SZ come illustrato qui o un modulo e un ID risorsa \_ (ad esempio, "C: Programmi \\ \\ \\ MyCorp MyAppMyApp.exe,-31") se si tratta di una risorsa \\ incorporata. Il percorso del file XML deve essere specificato completamente. Non può usare una variabile di ambiente, ad esempio %ProgramFiles%.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

Per altre informazioni sui collegamenti alle attività e su come creare il file XML per contenerli, vedere Creazione di collegamenti attività ricercabili per un [Pannello di controllo elemento](creating-searchable-task-links.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Come registrare elementi Pannello di controllo eseguibili](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
