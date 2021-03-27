---
description: La radice di un'estensione dello spazio dei nomi viene in genere visualizzata da Esplora risorse come cartella nelle visualizzazioni albero e cartella.
title: Impostazione della posizione di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882805"
---
# <a name="specifying-a-namespace-extensions-location"></a>Impostazione della posizione di un'estensione dello spazio dei nomi

La radice di un'estensione dello spazio dei nomi viene in genere visualizzata da Esplora risorse come cartella nelle visualizzazioni albero e cartella. Per visualizzare le sottocartelle e i file dell'estensione in Esplora risorse, è necessario specificare la posizione della cartella radice nella gerarchia dello spazio dei nomi della shell. Questo percorso viene definito *punto di giunzione*.

-   [Uso delle cartelle virtuali come punti di giunzione](#using-virtual-folders-as-junction-points)
-   [Uso delle cartelle del file System come punti di giunzione](#using-file-system-folders-as-junction-points)
-   [Apertura di una visualizzazione di un'estensione dello spazio dei nomi](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Uso delle cartelle virtuali come punti di giunzione

Il modo più semplice per definire il punto di giunzione di un'estensione consiste nel rendere la cartella radice una sottocartella di una cartella virtuale di sistema. Questo tipo di punto di giunzione viene definito punto di *giunzione virtuale*. Le cartelle **Desktop** e **computer locale** sono le località tipiche per i punti di giunzione virtuali, ma è anche possibile definire un punto di giunzione virtuale in un computer remoto oppure nelle cartelle **risorse di rete**, **Internet Explorer** e **Pannello di controllo** .

Per definire un punto di giunzione virtuale, creare una sottochiave della chiave che rappresenti la cartella virtuale appropriata e denominarla con il formato stringa dell'identificatore di classe dell'estensione (CLSID). Il CLSID registrato verrà visualizzato come segue.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

Il *nome della cartella virtuale* è una delle sottochiavi riportate nella tabella seguente.



| Location          | Nome cartella virtuale                        |
|-------------------|--------------------------------------------|
| Control panel     | **ControlPanel**                           |
| Desktop           | **Desktop**                                |
| Rete intera    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Risorse del computer       | **MyComputer**                             |
| Risorse di rete | **NetworkNeighborhood**                    |
| Computer remoto   | **ComputerRemoto**                         |
| File utente       | **UsersFiles**                             |



 

Le estensioni remote devono essere inizializzate con [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Uso delle cartelle del file System come punti di giunzione

Esistono due modi per definire file system cartelle come punti di giunzione. L'approccio più semplice consiste nel creare una cartella nel percorso appropriato e aggiungere un punto al nome della cartella, seguito dal formato stringa del CLSID dell'estensione. Solo il nome della cartella sarà visibile in Esplora risorse. Nell'esempio seguente viene creato un punto di giunzione con un nome visualizzato di cartella.


```
MyFolder.{Extension CLSID}
```



In alternativa, è possibile definire una cartella denominata convenzionalmente come punto di giunzione per:

-   Rendere la cartella di sola lettura.
-   Creazione della cartella di una cartella di sistema chiamando [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Inserimento di un file di Desktop.ini nascosto nella cartella che include il CLSID dell'estensione.

Desktop.ini è un file di testo standard che può essere aggiunto a qualsiasi cartella per personalizzare alcuni aspetti del comportamento della cartella. Per informazioni generali su come usare questo file, vedere [How to Customize Folders with Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Per definire una cartella come punto di giunzione, il \[ . \] La sezione ShellClassInfo di Desktop.ini deve contenere il CLSID dell'estensione, come indicato di seguito:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Apertura di una visualizzazione di un'estensione dello spazio dei nomi

Quando un utente accede a un punto di giunzione, Esplora risorse crea automaticamente una visualizzazione della cartella radice. È anche possibile creare una vista avviando esplicitamente Explorer.exe con il CLSID dell'estensione come argomento. È possibile, ad esempio, usare questo approccio per avviare una visualizzazione di un'estensione da un menu di scelta rapida o da un collegamento. Ad esempio, per avviare una visualizzazione di estensione che include una visualizzazione albero, è possibile usare la stringa di comando seguente.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Una stringa di comando alternativa può essere usata per avviare una visualizzazione di un oggetto all'interno dell'estensione. Questa funzionalità può essere utile, ad esempio, per un'estensione che utilizza una visualizzazione cartelle per consentire agli utenti di visualizzare il contenuto di uno dei diversi file compressi.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



Il parametro *ObjectName* è il nome dell'oggetto che deve essere visualizzato. Esplora risorse converte il nome nel PIDL corrispondente e passa il PIDL al metodo [**IPersistFolder:: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) dell'oggetto nuova cartella.

> [!Note]  
> La stringa CLSID deve essere preceduta da una coppia di due punti (::) in alternativa, il comando avrà esito negativo. Il flag Slash-e (/e) usato nelle due righe di comando di esempio illustrate in precedenza indica a Esplora risorse di visualizzare una visualizzazione albero. Il flag deve essere separato dai due puntini di una virgola. Se non si desidera una visualizzazione albero, omettere il flag/e e la virgola.

 

 

 



