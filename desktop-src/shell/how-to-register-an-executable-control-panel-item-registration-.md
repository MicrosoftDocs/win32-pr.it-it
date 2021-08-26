---
description: Per Pannello di controllo elementi implementati come file .exe, non sono necessarie esportazioni speciali o gestione dei messaggi. Qualsiasi .exe file può essere registrato come oggetto comando per essere visualizzato con un punto di ingresso nella Pannello di controllo cartella.
title: Come registrare elementi Pannello di controllo eseguibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81e52e18bd2cd1c48d5d260b08844784a5286dd2cd4d9d5ec782a86f624fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009431"
---
# <a name="how-to-register-executable-control-panel-items"></a>Come registrare elementi Pannello di controllo eseguibili

Per Pannello di controllo elementi implementati come file .exe, non sono necessarie esportazioni speciali o gestione dei messaggi. Qualsiasi .exe file può essere registrato come oggetto comando per essere visualizzato con un punto di ingresso nella Pannello di controllo cartella.

Un esempio viene usato qui per illustrare i requisiti di registrazione. L'esempio mostra come registrare un Pannello di controllo denominato **My Impostazioni** come oggetto comando in modo che venga visualizzato nella finestra Pannello di controllo comando. Quando **si esegue il comando,** viene visualizzata anche la finestra My Impostazioni my Impostazioni `MyApp.exe /settings` .

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Generare un GUID per l'Pannello di controllo specificato. Il GUID identifica in modo univoco l Pannello di controllo specificato. In questo esempio è `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` il GUID dell'elemento Pannello di controllo specificato.

### <a name="step-2"></a>Passaggio 2:

Usando il GUID come nome, aggiungere una sottochiave al Registro di sistema come indicato di seguito.

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

I dati per la voce Default sono semplicemente il nome \_ REG SZ dell'Pannello di controllo elemento. La voce Default può essere utile per identificare la voce GUID, ma è facoltativa.

### <a name="step-3"></a>Passaggio 3:

Usando il GUID come nome, aggiungere una sottochiave e le relative voci al Registro di sistema come indicato di seguito.

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

-   **Default**. REG \_ SZ. Nome visualizzato per l'Pannello di controllo corrente.
-   **LocalizedString**. facoltativo. REG \_ SZ o REG \_ EXPAND \_ SZ. Nome del modulo e ID di tabella della stringa del nome localizzato dell'Pannello di controllo elemento. Il formato è un segno "at" (@) seguito dal nome del .exe o .dll che contiene la tabella di stringhe interfaccia utente multilingue (MUI). Le variabili di ambiente possono essere usate come sostituzione di una parte del percorso. Il percorso e il nome del file sono seguiti da una virgola (,) e da un trattino (-), seguito dall'ID nella tabella di stringhe.

    Se il modulo non ha una tabella di stringhe, questa voce può essere semplicemente la stringa del nome visualizzato. Se si usa solo la stringa del nome visualizzato anziché una tabella di stringhe, il nome non viene adattato alla lingua di visualizzazione corrente.

-   **InfoTip**. REG \_ SZ o REG \_ EXPAND \_ SZ. Descrizione dell'Pannello di controllo corrente. Queste informazioni vengono visualizzate in una finestra delle informazioni visualizzata quando il puntatore del mouse viene posizionato sull'icona dell'elemento. La sintassi è la stessa usata per LocalizedString, inclusa l'opzione di fornire semplicemente una stringa anziché un riferimento a una tabella di stringhe.
-   **System.ApplicationName**. REG \_ SZ. Nome canonico dell'elemento. Il comando del modulo `control.exe /name System.ApplicationName` apre l'elemento, ad esempio `control.exe /name MyCorporation.MySettings` . Per [altre informazioni sull'uso Pannello di controllo,](executing-control-panel-items.md) vedere Executing Pannello di controllo Items (Esecuzione di Control.exe).
-   **System.ControlPanel.Category**. REG \_ SZ. Valore che dichiara le categorie Pannello di controllo in cui viene visualizzato l'elemento. Più categorie sono separate da virgole. Nel caso dell'esempio precedente, la voce specifica che l'elemento My **Impostazioni** deve essere visualizzato nelle categorie Aspetto e **Personalizzazione** **e** Programmi. Vedere [Assegnazione di Pannello di controllo categorie per](assigning-control-panel-categories.md) i possibili valori di categoria.
-   **System.Software.TasksFileUrl**. REG \_ SZ o REG \_ EXPAND \_ SZ. Percorso del file XML che definisce i collegamenti [attività](creating-searchable-task-links.md). Può trattarsi di un percorso di file diretto, come illustrato nell'esempio, o di una risorsa incorporata specificata come nome di modulo e ID risorsa, ad esempio "%ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe,-31".

### <a name="step-4"></a>Passaggio 4:

Nella stessa sottochiave GUID aggiungere la sottochiave seguente al Registro di sistema per specificare il percorso del file che contiene l'icona e l'ID risorsa dell'immagine all'interno del file.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Si noti che anche se la sintassi è altrimenti simile alle voci LocalizedString e InfoTip descritte in precedenza, non viene usato alcun carattere '@' come prefisso nella voce REG SZ o REG EXPAND SZ che specifica il \_ \_ \_ percorso.

### <a name="step-5"></a>Passaggio 5:

Aggiungere le informazioni seguenti al Registro di sistema per fornire il comando chiamato dal sistema quando l'utente apre il Pannello di controllo.

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

[Registrazione di Pannello di controllo elementi](registering-control-panel-items.md)
</dt> <dt>

[Come registrare gli elementi Pannello di controllo DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



