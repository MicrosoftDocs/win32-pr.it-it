---
description: Personalizzazione dell'aspetto e del comportamento di una singola cartella con Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Come personalizzare le cartelle con Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581749"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Come personalizzare le cartelle con Desktop.ini

Le cartelle del file system vengono in genere visualizzate con un'icona standard e un set di proprietà, che specificano, ad esempio, se la cartella è condivisa. È possibile personalizzare l'aspetto e il comportamento di una singola cartella creando un file Desktop.ini per tale cartella.

## <a name="instructions"></a>Istruzioni

### <a name="using-desktopini-files"></a>Uso Desktop.ini file

Le cartelle vengono in genere visualizzate con l'icona della cartella standard. Un uso comune del file Desktop.ini è assegnare un'icona personalizzata o un'immagine di anteprima a una cartella. È anche possibile usare Desktop.ini per creare un *suggerimento* che visualizza informazioni sulla cartella e controlla alcuni aspetti del comportamento della cartella, ad esempio la specifica dei nomi localizzati per la cartella o gli elementi nella cartella.

**Usare la procedura seguente per personalizzare lo stile di una cartella con Desktop.ini:**

1.  Usare [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) per rendere la cartella una cartella di sistema. In questo modo viene impostato il bit di sola lettura nella cartella per indicare che il comportamento speciale riservato per Desktop.ini deve essere abilitato. È anche possibile impostare una cartella come cartella di sistema dalla riga di comando usando **attrib +s** *FolderName*.
2.  Creare un Desktop.ini file per la cartella. È consigliabile contrassegnarlo come *nascosto* e *di* sistema per assicurarsi che sia nascosto agli utenti normali.
3.  Assicurarsi che Desktop.ini file creato sia in formato Unicode. Questa operazione è necessaria per archiviare le stringhe localizzate che possono essere visualizzate agli utenti.

### <a name="creating-a-desktopini-file"></a>Creazione di un Desktop.ini file

Il Desktop.ini file è un file di testo che consente di specificare la modalità file system una cartella. Oggetto \[ . La sezione ShellClassInfo consente di personalizzare la visualizzazione della \] cartella assegnando valori a diverse voci:

| Valore             | Descrizione                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | Impostare questa voce su 0 per evitare l'eliminazione di una cartella di sistema quando si elimina o si sposta la cartella.                                                                                                                                                                                                                                                                  |
| **NoSharing**     | Non supportato in Windows Vista o versioni successive. Impostare questa voce su 1 per impedire la condivisione della cartella.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Se si vuole specificare un'icona personalizzata per la cartella, impostare questa voce sul nome file dell'icona. L'estensione di file con estensione ico è preferibile, ma è anche possibile specificare .bmp file o .exe e .dll che contengono icone. Se si usa un percorso relativo, l'icona è disponibile per gli utenti che visualizzano la cartella in rete. È anche necessario impostare la **voce IconIndex.** |
| **IconIndex**     | Impostare questa voce per specificare l'indice per un'icona personalizzata. Se il file assegnato a **IconFile** contiene solo una singola icona, impostare **IconIndex** su 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Impostare questa voce su una stringa di testo informativo. Viene visualizzato come suggerimento quando il cursore passa sulla cartella. Se l'utente fa clic sulla cartella, il testo delle informazioni viene visualizzato nel blocco di informazioni della cartella, sotto le informazioni standard.                                                                                                                      |



 

Le illustrazioni seguenti illustrano la cartella Musica con un file Desktop.ini personalizzato. La cartella ora:

-   Ha un'icona personalizzata.
-   Se la cartella viene spostata o eliminata, non viene visualizzato l'avviso "Si sta eliminando una cartella di sistema".
-   Non può essere condivisa.
-   Visualizza testo informativo quando il cursore passa il mouse sulla cartella.

Le opzioni della cartella nelle illustrazioni seguenti sono impostate per visualizzare i file nascosti in modo che Desktop.ini visibile. La cartella è simile alla seguente:

![Screenshot della cartella con l'icona personalizzata](images/webview4.jpg)

Quando il cursore passa sulla cartella, viene visualizzata la descrizione comando.

![Screenshot della cartella con un suggerimento](images/webview6.jpg)

L'icona personalizzata sostituisce l'icona della cartella ovunque venga visualizzato il nome della cartella.

![Screenshot dell'icona personalizzata che sostituisce l'icona della cartella](images/webview5.jpg)

Il file desktop.ini seguente è stato usato per personalizzare la Musica, come illustrato nelle illustrazioni precedenti.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



