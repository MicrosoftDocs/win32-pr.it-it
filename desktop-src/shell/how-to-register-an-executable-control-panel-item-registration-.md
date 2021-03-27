---
description: Per gli elementi del pannello di controllo implementati come file con estensione exe, non è necessaria alcuna esportazione o gestione dei messaggi speciale. Qualsiasi file con estensione exe può essere registrato come oggetto Command per essere visualizzato con un punto di ingresso nella cartella del pannello di controllo.
title: Come registrare gli elementi del pannello di controllo eseguibile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104050000"
---
# <a name="how-to-register-executable-control-panel-items"></a>Come registrare gli elementi del pannello di controllo eseguibile

Per gli elementi del pannello di controllo implementati come file con estensione exe, non è necessaria alcuna esportazione o gestione dei messaggi speciale. Qualsiasi file con estensione exe può essere registrato come oggetto Command per essere visualizzato con un punto di ingresso nella cartella del pannello di controllo.

Un esempio viene usato qui per illustrare i requisiti di registrazione. Nell'esempio viene illustrato come registrare un elemento del pannello di controllo denominato **impostazioni personali** come oggetto comando, in modo che venga visualizzato nella finestra del pannello di controllo. La finestra **impostazioni personali** viene visualizzata anche quando `MyApp.exe /settings` viene eseguito il comando.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Genera un GUID per l'elemento del pannello di controllo. Il GUID identifica in modo univoco l'elemento del pannello di controllo. In questo esempio, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` è il GUID dell'elemento del pannello di controllo.

### <a name="step-2"></a>Passaggio 2:

Utilizzando il GUID come nome, aggiungere una sottochiave al registro di sistema come indicato di seguito.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

I dati per la voce predefinita sono semplicemente il \_ nome di reg SZ dell'elemento del pannello di controllo. La voce predefinita può essere utile per identificare la voce del GUID, ma è facoltativa.

### <a name="step-3"></a>Passaggio 3:

Utilizzando il GUID come nome, aggiungere una sottochiave e le relative voci al registro di sistema come indicato di seguito.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Default**. REG \_ SZ. Nome visualizzato per l'elemento del pannello di controllo.
-   **LocalizedString**. facoltativo. REG \_ sz o reg \_ expand \_ SZ. Il nome del modulo e l'ID della tabella di stringhe del nome localizzato dell'elemento del pannello di controllo. Il formato è un segno di chiocciola (@) seguito dal nome del file con estensione exe o dll che contiene la tabella delle stringhe MUI (Multilingual User Interface). Le variabili di ambiente possono essere usate come sostituzioni per una parte del percorso. Il percorso e il nome del file sono seguiti da una virgola (,) e un trattino (-), seguiti dall'ID nella tabella di stringhe.

    Se il modulo non dispone di una tabella di stringhe, questa voce può essere semplicemente la stringa del nome visualizzato. Se si usa solo la stringa del nome visualizzato anziché una tabella di stringhe, il nome non si adatta alla lingua di visualizzazione corrente.

-   **Infotip**. REG \_ sz o reg \_ expand \_ SZ. Descrizione dell'elemento del pannello di controllo. Queste informazioni vengono visualizzate in un InfoTip visualizzato quando il mouse viene posizionato sull'icona dell'elemento. La sintassi è identica a quella usata per LocalizedString, inclusa la possibilità di fornire semplicemente una stringa anziché un riferimento a una tabella di stringhe.
-   **System. ApplicationName**. REG \_ SZ. Nome canonico dell'elemento. Il comando del modulo `control.exe /name System.ApplicationName` apre l'elemento, ad esempio `control.exe /name MyCorporation.MySettings` . Per ulteriori informazioni sull'utilizzo di Control.exe, vedere [esecuzione di elementi del pannello di controllo](executing-control-panel-items.md) .
-   **System. controlpanel. Category**. REG \_ SZ. Valore che dichiara le categorie del pannello di controllo in cui viene visualizzato l'elemento. Più categorie sono separate da virgole. Nel caso dell'esempio precedente, la voce specifica che l'elemento **impostazioni personali** dovrebbe essere visualizzato nelle categorie **aspetto e personalizzazione** e **programmi** . Vedere [assegnazione delle categorie del pannello di controllo](assigning-control-panel-categories.md) per i valori di categoria possibili.
-   **System. software. TasksFileUrl**. REG \_ sz o reg \_ expand \_ SZ. Percorso del file XML che definisce i [collegamenti alle attività](creating-searchable-task-links.md). Può trattarsi di un percorso di file diretto, come illustrato nell'esempio, oppure di una risorsa incorporata specificata come nome di modulo e ID di risorsa, ad esempio "% ProgramFiles% \\ \\ \\MyApp.exe MyApp,-31".

### <a name="step-4"></a>Passaggio 4:

Nella stessa sottochiave GUID aggiungere la sottochiave seguente al registro di sistema per specificare il percorso del file che contiene l'icona e l'ID risorsa dell'immagine all'interno del file.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Si noti che, mentre la sintassi è altrimenti simile alle voci LocalizedString e InfoTip descritte in precedenza, nessun carattere ' @' viene utilizzato come prefisso nella \_ voce reg SZ o reg \_ expand \_ SZ che specifica il percorso.

### <a name="step-5"></a>Passaggio 5:

Aggiungere al registro di sistema le informazioni seguenti per fornire il comando chiamato dal sistema quando l'utente apre il pannello di controllo.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Registrazione degli elementi del pannello di controllo](registering-control-panel-items.md)
</dt> <dt>

[Come registrare gli elementi del pannello di controllo DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



