---
description: La radice di un'estensione dello spazio dei nomi viene in genere visualizzata Windows Explorer come cartella nelle visualizzazioni albero e cartella.
title: Specifica del percorso di un'estensione dello spazio dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e20b9a1644b2272ee06ff8a792198f79ffebca8b8a971b690c1be1160830aae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719887"
---
# <a name="specifying-a-namespace-extensions-location"></a>Specifica del percorso di un'estensione dello spazio dei nomi

La radice di un'estensione dello spazio dei nomi viene in genere visualizzata Windows Explorer come cartella nelle visualizzazioni albero e cartella. Per Windows Explorer per visualizzare i file e le sottocartelle dell'estensione, è necessario specificare dove si trova la cartella radice nella gerarchia dello spazio dei nomi shell. Questa posizione viene definita punto di *giunzione*.

-   [Uso di cartelle virtuali come punti di giunzione](#using-virtual-folders-as-junction-points)
-   [Uso delle cartelle del file system come punti di giunzione](#using-file-system-folders-as-junction-points)
-   [Apertura di una visualizzazione di un'estensione dello spazio dei nomi](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Uso di cartelle virtuali come punti di giunzione

Il modo più semplice per definire il punto di giunzione di un'estensione è rendere la cartella radice una sottocartella di una cartella virtuale di sistema. Questo tipo di punto di giunzione viene definito punto *di giunzione virtuale.* Le **cartelle Desktop** e **Computer locale** sono le posizioni tipiche per i punti di giunzione virtuali, ma è anche possibile definire un punto di giunzione virtuale in un computer remoto o nelle cartelle Risorse di rete, **Internet Explorer** e **Pannello di controllo.** 

Per definire un punto di giunzione virtuale, creare una sottochiave della chiave che rappresenta la cartella virtuale appropriata e denomarla con il formato stringa dell'identificatore di classe (CLSID) dell'estensione. Il CLSID registrato verrà visualizzato come segue.

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

*Nome cartella virtuale* è una delle sottochiavi nella tabella seguente.



| Località          | Nome cartella virtuale                        |
|-------------------|--------------------------------------------|
| Control panel     | **ControlPanel**                           |
| Desktop           | **Desktop**                                |
| Intera rete    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Risorse del computer       | **MyComputer**                             |
| Risorse di rete | **NetworkNeighborhood**                    |
| Computer remoto   | **RemoteComputer**                         |
| File degli utenti       | **UsersFiles**                             |



 

Le estensioni remote devono essere inizializzate [**con IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Uso delle cartelle del file system come punti di giunzione

Esistono due modi per definire le file system come punti di giunzione. L'approccio più semplice consiste nel creare una cartella nel percorso appropriato e aggiungere un punto al nome della cartella, seguito dal formato stringa del CLSID dell'estensione. Solo il nome della cartella sarà visibile in Windows Explorer. Nell'esempio seguente viene creato un punto di giunzione con il nome visualizzato MyFolder.


```
MyFolder.{Extension CLSID}
```



In alternativa, è possibile definire una cartella con nome convenzionale come punto di giunzione tramite:

-   Rendere la cartella di sola lettura.
-   Rendere la cartella una cartella di sistema chiamando [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Inserimento di Desktop.ini file nascosto nella cartella che include il CLSID dell'estensione.

Desktop.ini è un file di testo standard che può essere aggiunto a qualsiasi cartella per personalizzare determinati aspetti del comportamento della cartella. Per una descrizione generale di come usare questo file, vedere [Come personalizzare le ](how-to-customize-folders-with-desktop-ini.md)cartelle con Desktop.ini. Per definire una cartella come punto di giunzione, \[ . La sezione ShellClassInfo Desktop.ini deve contenere il \] CLSID dell'estensione come indicato di seguito:


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Apertura di una visualizzazione di un'estensione dello spazio dei nomi

Quando un utente esplora un punto di giunzione, Windows Explorer crea automaticamente una visualizzazione della cartella radice. È anche possibile creare una vista avviando in modo Explorer.exe con il CLSID dell'estensione come argomento. È ad esempio possibile usare questo approccio per avviare una visualizzazione di un'estensione da un menu di scelta rapida o da un collegamento. Ad esempio, per avviare una visualizzazione di MyExtension che include una visualizzazione albero, è possibile usare la stringa di comando seguente.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



È possibile usare una stringa di comando alternativa per avviare una visualizzazione di un oggetto all'interno dell'estensione. Questa funzionalità è utile, ad esempio, per un'estensione che usa una visualizzazione cartelle per consentire agli utenti di visualizzare il contenuto di uno dei diversi file compressi.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



Il *parametro objectname* è il nome dell'oggetto da visualizzare. Windows Explorer converte il nome nel file PIDL corrispondente e passa il file PIDL al metodo [**IPersistFolder::Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) del nuovo oggetto cartella.

> [!Note]  
> La stringa CLSID deve essere preceduta da una coppia di due punti (::) oppure il comando avrà esito negativo. Il flag slash-e (/e) usato nelle due righe di comando di esempio mostrate in precedenza indica Windows Explorer per visualizzare una visualizzazione albero. Il flag deve essere separato dai due punti da una virgola. Se non si vuole una visualizzazione albero, omettere il flag /e e la virgola.

 

 

 



