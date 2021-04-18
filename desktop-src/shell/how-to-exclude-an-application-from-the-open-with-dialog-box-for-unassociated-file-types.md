---
description: Come escludere un'applicazione dalla finestra di dialogo Apri con per il tipo di file non associato.
title: Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9443416e95fca112623d487bf58f4fce1d51d13d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563322"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati

Quando un utente tenta di aprire un file che non è un membro di un tipo di file registrato, ovvero un tipo di file sconosciuto, oppure quando un utente seleziona **Apri con** o **apri con-> scegliere programma predefinito** dal menu di scelta rapida di un file, la shell Visualizza un sottomenu o una finestra di dialogo che consente all'utente di specificare il programma utilizzato per aprire il file.

Per impostazione predefinita, qualsiasi applicazione registrata come sottochiave delle applicazioni **\_ \_ radice delle classi HKEY** \\  viene visualizzata nella finestra di dialogo **Apri con** . Queste applicazioni vengono presentate in modo **aperto** , indipendentemente dal fatto che l'applicazione sia registrata per gestire il tipo di file.

Per impedire che un'applicazione venga visualizzata nella finestra di dialogo **Apri con** quando l'applicazione non deve o non può essere utilizzata per aprire determinati tipi di file, utilizzare una delle due tecniche descritte in questo argomento.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una voce NoOpenWith alla sottochiave dell'applicazione. Quando un'applicazione utilizza un tipo di file, Windows registra tali informazioni per compilare l'elenco dei **Programmi consigliati** . Questo elenco viene visualizzato nel sottomenu **Apri con** , come illustrato nella schermata seguente.

![screenshot del menu di scelta rapida con il sottomenu Apri con visualizzato](images/file-assoc/openwithsubmenu.png)

Queste applicazioni consigliate sono inoltre visualizzate nella parte **Programmi consigliati** della finestra di dialogo **Apri con** , come illustrato nella schermata seguente.

![screenshot della finestra di dialogo Apri con con i programmi consigliati](images/file-assoc/openwithdialog.png)

> [!Note]  
> Se un'applicazione è stata registrata in [OpenWithList](fa-file-types.md) o OpenWithProgIDs per il tipo di file, verrà visualizzata nell'elenco **Programmi consigliati** anche se è impostata la voce NoOpenWith. Tenere inoltre presente che, indipendentemente dal fatto che un'applicazione venga offerta in un elenco di programmi consigliati, un utente può passare manualmente a qualsiasi file eseguibile.

 

Le applicazioni possono disabilitare questo rilevamento specificando un valore NoOpenWith nella sottochiave dell'applicazione.

La voce NoOpenWith è un valore **reg \_ SZ** vuoto, come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

L'impostazione della voce NoOpenWith presenta anche questi effetti:

-   Impedisce l'aggiunta di un file alla Jump List dell'applicazione tramite il trascinamento della selezione, a meno che l'applicazione non sia stata registrata in modo specifico per gestire il tipo di file.
-   Impedisce alla finestra di dialogo file comune e a qualsiasi chiamata alla funzione [**funzione SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) di aggiungere qualsiasi file alla Jump List dell'applicazione, a meno che l'applicazione non sia stata registrata in modo specifico per gestire il tipo di file.

### <a name="step-2"></a>Passaggio 2:

Il secondo modo per impedire che un'applicazione venga visualizzata nella finestra di dialogo **Apri con** , consiste nell'usare la sottochiave **SupportedTypes** per elencare in modo esplicito le estensioni dei tipi di file che l'applicazione può aprire. In questo modo si impedisce che l'applicazione venga visualizzata nella finestra di dialogo **Apri con** per i tipi di file che non è in grado di aprire. Fa anche in modo che l'applicazione venga visualizzata nell'elenco **Programmi consigliati** , come illustrato in precedenza.

Questo metodo è particolarmente utile se un'applicazione può salvare un file come un determinato tipo di file ma non è in grado di aprire il tipo di file. Un'applicazione deve inoltre impostare il \_ flag Fos DONTADDTORECENT tramite [**IFileDialog:: SetOption**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) quando si chiama la finestra di dialogo **Salva** . In questo modo si impedisce l'aggiunta dell'elemento alle parti **recenti** o **frequenti** di una Jump List. Impedisce inoltre di tenere traccia dell'applicazione in [OpenWithList](fa-file-types.md).

Ogni estensione supportata viene aggiunta come voce sotto la sottochiave **SupportedTypes** , come illustrato nell'esempio seguente. Le voci sono di tipo **reg \_ SZ** o **reg \_ null**, senza valori associati.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Se viene fornita una sottochiave **SupportedTypes** , solo i file con tali estensioni sono idonei per l'aggiunta alla Jump List dell'applicazione o per essere rilevati nell'elenco di destinazioni **recenti** o **frequenti** di un'applicazione.

La voce NoOpenWith esegue l'override della sottochiave **SupportedTypes** e nasconde l'applicazione nella finestra di dialogo **Apri con** .

 

 
