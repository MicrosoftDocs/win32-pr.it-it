---
description: Personalizzazione dell'aspetto e del comportamento di una singola cartella con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Come personalizzare le cartelle con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104553380"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Come personalizzare le cartelle con Desktop.ini

Le cartelle del file System vengono in genere visualizzate con un'icona standard e un set di proprietà, che specificano, ad esempio, se la cartella è condivisa. È possibile personalizzare l'aspetto e il comportamento di una singola cartella creando un file di Desktop.ini per la cartella.

## <a name="instructions"></a>Istruzioni

### <a name="using-desktopini-files"></a>Uso di file di Desktop.ini

Le cartelle vengono normalmente visualizzate con l'icona della cartella standard. Un uso comune del file Desktop.ini consiste nell'assegnare un'icona personalizzata o un'immagine di anteprima a una cartella. È inoltre possibile utilizzare Desktop.ini per creare un *infotip* che visualizza informazioni sulla cartella e controlla alcuni aspetti del comportamento della cartella, ad esempio specificando nomi localizzati per la cartella o gli elementi nella cartella.

**Utilizzare la procedura seguente per personalizzare lo stile di una cartella con Desktop.ini:**

1.  Usare [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) per rendere la cartella una cartella di sistema. In questo modo viene impostato il bit di sola lettura nella cartella per indicare che è necessario abilitare il comportamento speciale riservato per Desktop.ini. È anche possibile creare una cartella di sistema dalla riga di comando usando **attrib + s** *FolderName*.
2.  Creare un file di Desktop.ini per la cartella. È necessario contrassegnarlo come *nascosto* e *sistema* per assicurarsi che sia nascosto agli utenti normali.
3.  Verificare che il file Desktop.ini creato sia in formato Unicode. Questa operazione è necessaria per archiviare le stringhe localizzate che possono essere visualizzate dagli utenti.

### <a name="creating-a-desktopini-file"></a>Creazione di un file di Desktop.ini

Il file di Desktop.ini è un file di testo che consente di specificare la modalità di visualizzazione di una cartella file system. Oggetto \[ . \] La sezione ShellClassInfo consente di personalizzare la visualizzazione della cartella assegnando valori a diverse voci:

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Voce**         | **Valore**                                                                                                                                                                                                                                                                                                                                                                      |
| **ConfirmFileOp** | Impostare questa voce su 0 per evitare che venga visualizzato l'avviso "si sta eliminando una cartella di sistema" quando si elimina o si trasferisce la cartella.                                                                                                                                                                                                                                                                  |
| **Nosharing**     | Non supportato in Windows Vista o versioni successive. Impostare questa voce su 1 per impedire la condivisione della cartella.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Se si desidera specificare un'icona personalizzata per la cartella, impostare questa voce sul nome file dell'icona. L'estensione del nome di file ico è preferibile, ma è anche possibile specificare file con estensione bmp o exe e DLL contenenti icone. Se si usa un percorso relativo, l'icona è disponibile per gli utenti che visualizzano la cartella sulla rete. È anche necessario impostare la voce **IconIndex** . |
| **IconIndex**     | Impostare questa voce per specificare l'indice per un'icona personalizzata. Se il file assegnato a **IconFile** contiene solo una singola icona, impostare **IconIndex** su 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Impostare questa voce su una stringa di testo informativo. Viene visualizzato come infotip quando il cursore passa il puntatore del mouse sulla cartella. Se l'utente fa clic sulla cartella, il testo delle informazioni viene visualizzato nel blocco di informazioni della cartella, sotto le informazioni standard.                                                                                                                      |



 

Le illustrazioni seguenti sono della cartella Music con un file di Desktop.ini personalizzato. La cartella ora:

-   Dispone di un'icona personalizzata.
-   Non Visualizza l'avviso "si sta eliminando una cartella di sistema" se la cartella viene spostata o eliminata.
-   Non può essere condivisa.
-   Visualizza il testo informativo quando il cursore passa sulla cartella.

Le opzioni della cartella nelle illustrazioni seguenti sono impostate per visualizzare i file nascosti, in modo che Desktop.ini sia visibile. La cartella ha un aspetto simile al seguente:

![screenshot della cartella con icona personalizzata](images/webview4.jpg)

Quando il cursore viene posizionato sulla cartella, viene visualizzato infotip.

![screenshot della cartella con un infotip](images/webview6.jpg)

L'icona personalizzata sostituisce l'icona della cartella in qualsiasi posizione in cui viene visualizzato il nome della cartella.

![screenshot dell'icona personalizzata che sostituisce la cartella](images/webview5.jpg)

Il file di desktop.ini seguente è stato usato per personalizzare la cartella Music, come illustrato nelle illustrazioni precedenti.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



