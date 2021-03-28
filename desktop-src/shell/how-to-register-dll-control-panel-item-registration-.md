---
description: Gli elementi del pannello di controllo implementati in una DLL che esporta la funzione CPlApplet presentano requisiti di registrazione diversi rispetto ai file exe.
title: Come registrare gli elementi del pannello di controllo DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756506"
---
# <a name="how-to-register-dll-control-panel-items"></a>Come registrare gli elementi del pannello di controllo DLL

> [!Note]  
> Le linee guida di implementazione correnti affermano che i nuovi elementi del pannello di controllo devono essere implementati come file con estensione exe anziché come file con estensione CPL. Le informazioni seguenti sono incluse principalmente per finalità legacy.

 

Gli elementi del pannello di controllo implementati in una DLL che esporta la funzione [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) presentano requisiti di registrazione diversi rispetto ai file exe. A partire da Windows XP, è necessario installare nuove dll elemento del pannello di controllo nella cartella dell'applicazione associata nella cartella programmi. Gli elementi archiviati nella directory system32 con estensione CPL non devono essere registrati. vengono visualizzati automaticamente nel pannello di controllo. Tutti gli altri elementi del pannello di controllo che usano **CPlApplet** devono essere registrati in uno dei due modi seguenti:

-   Se l'elemento del pannello di controllo deve essere disponibile per tutti gli utenti, registrare il percorso in base al computer aggiungendo un valore **reg \_ expand \_ SZ** alla sottochiave CPLS del computer **\_ locale \_ HKEY** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Control Panel** \\  , impostata sul percorso della dll.
-   Se l'elemento del pannello di controllo deve essere disponibile per ogni utente, usare **HKEY \_ Current \_ User** come chiave radice anziché **HKEY \_ Local \_ computer**.

Nei due esempi seguenti viene registrato l'elemento del pannello di controllo *MyCplApp* . Il nome della DLL è MyCpl.cpl e si *trova nella directory dell' \\ applicazione MyApplication* . Nel primo esempio viene illustrata la registrazione per computer.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere queste informazioni al registro di sistema per registrare l'esistenza del file con estensione CPL.

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

**Windows Vista e versioni successive:** Aggiungere queste informazioni aggiuntive al registro di sistema per fornire un GUID per l'elemento del pannello di controllo.

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

Generando un GUID per identificare in modo univoco l'elemento del pannello di controllo, è possibile aggiungere collegamenti alle attività nel pannello di controllo. Senza questo GUID, non esiste alcun modo per associare i collegamenti dell'attività all'elemento del pannello di controllo. [Per un elemento del pannello di controllo, vedere Creazione di collegamenti alle attività ricercabili](creating-searchable-task-links.md).

### <a name="step-3"></a>Passaggio 3:

**Windows Vista e versioni successive:** Aggiungere al registro di sistema le informazioni seguenti per creare un nome canonico per l'elemento.

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

Aggiungendo un nome canonico, gli utenti possono avviare l'elemento del pannello di controllo da una riga di comando immettendo `control.exe /name MyCorporation.MyCpl` . In questo modo è possibile anche modificare un'implementazione da un file con estensione CPL in un file con estensione exe in un secondo momento, senza che sia necessario chiamare programmi per apportare modifiche, in quanto possono continuare ad aprire l'elemento tramite il nome canonico. Per ulteriori informazioni sui nomi canonici, vedere [esecuzione di elementi del pannello di controllo](executing-control-panel-items.md).

### <a name="step-4"></a>Passaggio 4:

**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al registro di sistema per assegnare un elemento del pannello di controllo a una o più categorie.

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

**Windows XP:** Aggiungere le informazioni seguenti al registro di sistema per assegnare un elemento del pannello di controllo a una o più categorie.

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

In questo esempio l'elemento viene assegnato alla categoria 3, ovvero rete e Internet. Per aggiungere un elemento a più categorie, fornire l'elenco come valore REG \_ SZ separato da virgole, ad esempio "3, 8". I valori possono essere specificati in formato decimale o esadecimale. Si noti che la possibilità di aggiungere un elemento a più categorie è possibile solo in Windows XP Service Pack 2 (SP2) e versioni successive. Vedere [assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md) per tutti i valori possibili.

### <a name="step-5"></a>Passaggio 5:

**Windows Vista e versioni successive:** Aggiungere le informazioni seguenti al registro di sistema per creare e puntare a un file XML per archiviare i collegamenti alle attività per l'elemento. Il valore deve essere un \_ percorso reg SZ, come illustrato qui, o un modulo e un ID di risorsa (ad esempio, "C: \\ Program Files \\ Corp \\ MyApp \\MyApp.exe,-31") se si tratta di una risorsa incorporata. Il percorso del file XML deve essere specificato in modo completo. Non può usare una variabile di ambiente, ad esempio% ProgramFiles%.

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

Per altri dettagli sui collegamenti alle attività e su come creare il file XML in cui tenerli, vedere [creazione di collegamenti alle attività ricercabili per un elemento del pannello di controllo](creating-searchable-task-links.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Come registrare gli elementi del pannello di controllo eseguibile](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
