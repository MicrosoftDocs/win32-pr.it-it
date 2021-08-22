---
description: Come escludere un'applicazione dalla finestra di dialogo Apri con per il tipo di file non associato.
title: Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d90ae5ab49128df1eedd9b760286ce54f6b6498cbe00d4a945145a80f956cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350913"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>Come escludere un'applicazione dalla finestra di dialogo Apri con per i tipi di file non associati

Quando un utente tenta di aprire un file che non è membro di alcun tipo di file registrato (ovvero un tipo di file sconosciuto) o quando un utente seleziona **Apri con** o **Apri con -> Scegli** programma predefinito dal menu di scelta rapida di un file, shell presenta un sottomenu o una finestra di dialogo che consente all'utente di specificare il programma usato per aprire il file.

Per impostazione predefinita, qualsiasi applicazione registrata come sottochiave di **HKEY \_ CLASSES \_ ROOT** Applications viene visualizzata nella finestra Apri con \\  dialogo.  Queste applicazioni vengono presentate **in** Apri con indipendentemente dal fatto che l'applicazione sia registrata per gestire il tipo di file.

Per impedire la visualizzazione di un'applicazione nella finestra di dialogo **Apri con** quando l'applicazione non deve o non può essere usata per aprire determinati tipi di file, usare una delle due tecniche descritte in questo argomento.

## <a name="instructions"></a>Istruzioni

### <a name="step-1"></a>Passaggio 1:

Aggiungere una voce NoOpenWith alla sottochiave dell'applicazione. Quando un'applicazione usa un tipo di file, Windows le informazioni per compilare **l'elenco Programmi** consigliati. Questo elenco viene visualizzato nel **sottomenu Apri con,** come illustrato nello screenshot seguente.

![Screenshot del menu di scelta rapida con il sottomenu aperto con visualizzato](images/file-assoc/openwithsubmenu.png)

Queste applicazioni consigliate sono visualizzate anche nella parte **Programmi** consigliati della finestra **di dialogo** Apri con, come illustrato nello screenshot seguente.

![Screenshot della finestra di dialogo Apri con con i programmi consigliati](images/file-assoc/openwithdialog.png)

> [!Note]  
> Se un'applicazione si è registrata in [OpenWithList](fa-file-types.md) o OpenWithProgIDs per il tipo di file, verrà visualizzata nell'elenco **Programmi** consigliati anche se la voce NoOpenWith è impostata. Tenere inoltre presente che, indipendentemente dal fatto che un'applicazione sia disponibile in un elenco di programmi consigliati, un utente può passare manualmente a qualsiasi file eseguibile.

 

Le applicazioni possono disabilitare questo rilevamento specificando un valore NoOpenWith nella sottochiave dell'applicazione.

La voce NoOpenWith è un **valore REG \_ SZ** vuoto, come illustrato nell'esempio seguente.

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

L'impostazione della voce NoOpenWith ha anche gli effetti seguenti:

-   Impedisce l'aggiunta di un file al Jump List dell'applicazione tramite trascinamento della selezione, a meno che l'applicazione non sia registrata in modo specifico per gestire tale tipo di file.
-   Impedisce alla finestra di dialogo file comune e a qualsiasi chiamata alla funzione [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) di aggiungere qualsiasi file al Jump List dell'applicazione, a meno che l'applicazione non sia registrata in modo specifico per gestire tale tipo di file.

### <a name="step-2"></a>Passaggio 2:

Il secondo modo per impedire la visualizzazione di un'applicazione nella finestra di dialogo **Apri con** è usare la sottochiave **SupportedTypes** per elencare in modo esplicito le estensioni dei tipi di file che l'applicazione può aprire. In questo modo l'applicazione non viene visualizzata **Apri con** finestra di dialogo per i tipi di file che non può aprire. Fa anche in modo che l'applicazione venga visualizzata **nell'elenco Programmi consigliati,** come descritto in precedenza.

Questo metodo è particolarmente utile se un'applicazione può salvare un file come un determinato tipo di file, ma non può aprirlo. Un'applicazione deve anche impostare il flag DONTADDTORECENT di FOS \_ tramite [**IFileDialog::SetOptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions) quando si chiama la **finestra di** dialogo Salva. In questo modo l'elemento non  viene aggiunto alle **parti Recenti** o Frequenti di un Jump List. Impedisce inoltre di tenere traccia dell'applicazione in [OpenWithList.](fa-file-types.md)

Ogni estensione supportata viene aggiunta come voce nella sottochiave **SupportedTypes,** come illustrato nell'esempio seguente. Le voci sono di tipo **REG \_ SZ** o **REG \_ NULL,** senza valori associati.

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

Se viene specificata una sottochiave **SupportedTypes,** solo i file con queste estensioni sono idonei per l'aggiunta  al Jump List dell'applicazione o per essere monitorati nell'elenco destinazioni recenti o **frequenti** di un'applicazione.

La voce NoOpenWith esegue l'override della sottochiave **SupportedTypes** e nasconde l'applicazione **nella** Apri con finestra di dialogo.

 

 
