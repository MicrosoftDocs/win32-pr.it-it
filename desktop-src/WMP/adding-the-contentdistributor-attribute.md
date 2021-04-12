---
title: Aggiunta dell'attributo ContentDistributor
description: Aggiunta dell'attributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player Online Stores, aggiunta dell'attributo ContentDistributor
- archivi online, aggiunta dell'attributo ContentDistributor
- digitare 1 Store online, aggiunta dell'attributo ContentDistributor
- digitare 2 archivi online, aggiunta dell'attributo ContentDistributor
- Windows Media Player Online Stores, attributo ContentDistributor
- archivi online, attributo ContentDistributor
- digitare 1 Store online, attributo ContentDistributor
- digitare 2 archivi online, attributo ContentDistributor
- Aggiunta dell'attributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104330100"
---
# <a name="adding-the-contentdistributor-attribute"></a>Aggiunta dell'attributo ContentDistributor

Quando l'utente tenta di riprodurre il contenuto di uno Store online o di copiare il contenuto in un CD o un dispositivo, Windows Media Player chiama determinati metodi nell'oggetto COM. A tale scopo, il lettore necessita di un modo per distinguere il contenuto da quello degli altri provider del negozio online. Aggiungendo il nome della chiave del negozio online come valore per **contentdistributor** (un alias per l'attributo Windows Media Format SDK denominato **WM/contentdistributor**) al contenuto basato su Windows Media, si garantisce che il lettore possa identificare il contenuto associato al servizio.

L'aggiunta di un valore per **contentdistributor** garantisce inoltre che Windows Media Player creerà un nodo nella libreria per il contenuto fornito. Vedere [integrazione della libreria](library-integration.md).

Questo valore può essere specificato in due modi:

-   Usare il modello a oggetti di Windows Media Player. Quando si esegue questa operazione, Windows Media Player aggiunge il valore specificato al database di libreria. Infine, il lettore scriverà anche il valore dell'attributo nel file multimediale digitale.
-   Usare Windows Media Format SDK per aggiungere l'attributo **WM/contentdistributor** a livello di codice. Quando si esegue questa operazione, Windows Media Player legge il valore dell'attributo e lo aggiunge al database quando il file multimediale digitale viene aggiunto alla libreria.

Quando si crea l'oggetto COM di archivio online, il valore dell'attributo file impostato per **contentdistributor** e il valore assegnato alla costante KszContentDistributorID in progettoutente. h devono corrispondere esattamente. Ricordare che è stato specificato questo valore costante per l'oggetto COM quando è stato creato il progetto tramite la creazione guidata progetto. Questo valore può essere modificato manualmente. Assicurarsi di usare una stringa che identifichi in modo univoco il servizio.

## <a name="using-the-windows-media-player-object-model"></a>Uso del modello a oggetti di Windows Media Player

Per specificare un valore per **contentdistributor** usando il modello a oggetti di Windows Media Player, usare il metodo [Media. setItemInfo](media-setiteminfo.md) . Il codice di esempio seguente specifica il valore "Proseware" per **contentdistributor** per l'elemento multimediale attualmente in riproduzione:


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a>Uso di Windows Media Format SDK

Windows Media Player SDK include un file C++ di esempio, denominato SetContentDistributor. cpp, che illustra come usare Windows Media Format 9 Series SDK per aggiungere l'attributo **WM/contentdistributor** . È possibile individuare questo file di esempio nella cartella denominata Metadata in cui è stato installato l'SDK. Per usare questo codice è necessario attenersi alla procedura seguente:

1.  Installare Windows Media Format 9 Series SDK e configurare il runtime come descritto nella documentazione.
2.  Creare un nuovo progetto C++ vuoto in Visual Studio e aggiungere al progetto il file di esempio denominato SetContentDistributor. cpp.
3.  Aggiungere il percorso delle cartelle lib di Windows Media Format 9 Series SDK all'elenco dei percorsi di file. Scegliere **Opzioni** dal menu **Strumenti**.
4.  Nella finestra di dialogo **Opzioni** fare clic su **progetti**, quindi fare clic su **directory di VC + +**.
5.  Nella casella di riepilogo **Visualizza directory per** fare clic su file di **libreria**.
6.  Utilizzare i pulsanti per aggiungere i percorsi alle caselle di riepilogo.
7.  Aprire la finestra di dialogo Pagine delle proprietà per il progetto. Scegliere **proprietà di configurazione**, quindi **linker**, quindi **input**. Digitare "Wmvcore. lib" nella casella di testo **dipendenze aggiuntive** .

Il codice di esempio crea un programma da riga di comando. Gli argomenti forniti durante l'esecuzione del programma specificano il percorso del file multimediale digitale da modificare e una stringa per il valore dell'attributo **contentdistributor** . Il codice usa **IWMHeaderInfo:: SetAttribute** per aggiungere l'attributo al file specificato. È possibile utilizzare questo esempio così com'è o utilizzarlo come punto di partenza per il programma.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni comuni ai negozi online di tipo 1 e di tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




