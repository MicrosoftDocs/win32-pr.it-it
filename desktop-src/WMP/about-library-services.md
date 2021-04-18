---
title: Informazioni sui servizi di libreria
description: Informazioni sui servizi di libreria
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player, libreria
- Modello a oggetti di Windows Media Player, libreria
- modello a oggetti, libreria
- Controllo ActiveX di Windows Media Player, libreria per il modello a oggetti
- Controllo ActiveX, libreria per il modello a oggetti
- Controllo ActiveX Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player Library, informazioni
- Windows Media Player Library, servizi
- libreria, servizi
- libreria, informazioni
- versioni di Windows Media Player, servizi di libreria
- enumerazioni, servizi di libreria
- eventi, servizi di libreria
- esempi, servizi di libreria
- interfacce, servizi di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 743efc8ae5cb464aa38655314c52112bc9541de6
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "106299501"
---
# <a name="about-library-services"></a>Informazioni sui servizi di libreria

Nelle versioni precedenti di Windows Media Player, il software usava un singolo database di libreria per ogni utente. Questo database è stato archiviato nel computer dell'utente ed è stato concettualmente associato all'utente e a una particolare istanza del lettore.

Windows Media Player 11 introduce i concetti di librerie multiple e remote. Ora, oltre alla libreria predefinita o *locale*, Windows Media Player può visualizzare il contenuto recuperato dalle librerie in altri computer connessi a una rete, che potrebbero includere altri utenti connessi allo stesso computer. Il lettore può anche visualizzare le visualizzazioni delle librerie da altre origini, ad esempio i dispositivi abilitati per MTP o i CD di dati. Dal punto di vista dell'utente finale, ciò significa che il contenuto multimediale digitale presente in molte posizioni diverse può essere gestito da più posizioni usando la stessa interfaccia utente di Windows Media Player familiare. Dal punto di vista dello sviluppatore, ciò significa che è possibile utilizzare le interfacce COM di Windows Media Player SDK per enumerare le librerie disponibili e quindi utilizzarle come la libreria locale nelle versioni precedenti.

Per enumerare le librerie disponibili, usare l'interfaccia **IWMPLibraryServices** . Questa interfaccia espone il metodo [IWMPLibraryServices:: getCountByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) , che recupera il numero di librerie di un determinato tipo. I tipi di libreria sono definiti dall'enumerazione [WMPLibraryType](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) . Questa enumerazione include un valore per la libreria locale, wmpltLocal. Ciò è dovuto al fatto che la funzionalità Servizi di libreria consente sempre di utilizzare la libreria locale utilizzando **IWMPLibraryServices** e le interfacce correlate.

> [!Note]  
> L'enumerazione **WMPLibraryType** include il valore wmpltRemote, che rappresenta le librerie multimediali condivise dalla rete. Per accedere a queste librerie condivise, il controllo Player deve essere eseguito in modalità remota. Per informazioni sull'esecuzione del controllo Player in modalità remota, vedere [la pagina relativa alla comunicazione remota del controllo Windows Media Player](remoting-the-windows-media-player-control.md).

 

Dopo aver recuperato il numero di librerie, è possibile eseguire l'iterazione della raccolta di librerie disponibili chiamando ripetutamente [IWMPLibraryServices:: getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) in un ciclo, passando un nuovo valore di indice a ogni iterazione. Questo metodo recupera un puntatore a un'interfaccia [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) , che rappresenta la singola libreria.

Dopo aver recuperato un puntatore a **IWMPLibrary**, è possibile chiamare [IWMPLibrary:: Get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) per recuperare un puntatore a un'interfaccia **IWMPMediaCollection** . Con questo puntatore di interfaccia è possibile usare una singola libreria in modo analogo alla libreria locale. È anche possibile recuperare una stringa contenente il nome della libreria chiamando [IWMPLibrary:: Get \_ Name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), che è utile se è necessario visualizzare il nome della libreria per l'utente. È possibile chiamare [IWMPLibrary:: Get \_ Type](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) per ottenere il **WMPLibraryType** di una determinata libreria.

È possibile gestire l'evento [IWMPEvents3:: LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) per stabilire quando una raccolta diventa disponibile e l'evento [IWMPEvents3:: LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) per stabilire quando una libreria si disconnette. Ognuno di questi eventi fornisce un puntatore **IWMPLibrary** che rappresenta la libreria connessa o disconnessa. È possibile chiamare [IWMPLibrary:: è identico](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) per determinare se la libreria connessa o disconnessa è una libreria attualmente in uso.

Esistono alcune differenze importanti quando si lavora con una libreria recuperata tramite l'interfaccia **IWMPLibraryServices** rispetto all'uso di una libreria recuperata tramite [IWMPCore:: Get \_ mediacollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). Si applicano le differenze seguenti:

-   È in genere possibile recuperare i risultati delle query molto più velocemente dalle librerie recuperate tramite **IWMPLibraryServices**. Si presuppone che altri fattori, ad esempio i tempi di accesso alla rete e al disco rigido, siano uguali.
-   L'elenco degli attributi dei metadati degli elementi multimediali disponibili dalle librerie recuperate tramite **IWMPLibraryServices** è in genere un subset di quelli disponibili dalla libreria locale recuperata tramite [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore).
-   Se si recupera la libreria locale tramite **IWMPLibraryServices**, tutti gli stessi attributi sono disponibili per l'uso come quelli disponibili quando si recupera la libreria locale tramite **IWMPCore**. Tuttavia, sarà possibile recuperare i risultati della query molto più velocemente per gli attributi più usati.
-   È consigliabile usare le raccolte di stringhe per creare elementi dell'interfaccia utente quando si lavora con le librerie recuperate tramite **IWMPLibraryServices**. Ad esempio, [IWMPMediaCollection2:: getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) consente di usare una query personalizzata, rappresentata dall'interfaccia **IWMPQuery** , per recuperare una raccolta di stringhe.
-   Le librerie Remote recuperate tramite l'interfaccia **IWMPLibraryServices** potrebbero non essere sempre connesse all'istanza corrente del lettore. Ciò significa che è importante gestire gli eventi **LibraryConnect** e **LibraryDisconnect** per capire quando viene modificata la disponibilità della libreria e per gestire l'evento [IWMPEvents3:: StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) per stabilire quando le stringhe vengono aggiunte o rimosse dalle raccolte di stringhe usate per visualizzare gli elementi dell'interfaccia utente. È inoltre necessario gestire gli eventi **StringCollectionChange** per la libreria locale per motivi analoghi.

È importante comprendere che le raccolte di stringhe per una determinata libreria possono cambiare in qualsiasi momento. Una raccolta di stringhe può essere vuota quando la si recupera per la prima volta, come nel caso di una libreria che è stata recentemente connessa, ma il lettore non ne ha ancora enumerato il contenuto. Viceversa, una raccolta di stringhe potrebbe già contenere tutte le informazioni necessarie. In questo caso, è possibile che non si riceva mai un evento **StringCollectionChange** perché il contenuto della libreria è stato completamente enumerato prima della creazione della query e non sono state apportate altre modifiche.

Pertanto, per tenere aggiornata l'interfaccia utente, è necessario enumerare il contenuto della raccolta di stringhe quando si recupera l'interfaccia **IWMPStringCollection** e gestire l'evento **StringCollectionChange** per conoscere gli aggiornamenti quando si verificano.

## <a name="sample"></a>Esempio

Nell'esempio denominato WMPML viene illustrato come utilizzare i servizi di libreria. Per ulteriori informazioni sugli esempi di Windows Media Player SDK, vedere [esempi](samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla libreria**](about-the-library.md)
</dt> <dt>

[**Informazioni sull'oggetto query**](about-the-query-object.md)
</dt> <dt>

[**Interfaccia IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**Interfaccia IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
</dt> <dt>

[**Interfaccia IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
</dt> <dt>

[**Interfaccia IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPMediaCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)
</dt> <dt>

[**Interfaccia IWMPMediaCollection (VB e C#)**](iwmpmediacollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPStringCollection**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)
</dt> <dt>

[**Interfaccia IWMPStringCollection (VB e C#)**](iwmpstringcollection--vb-and-c.md)
</dt> <dt>

[**Interfaccia IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
</dt> <dt>

[**Interfaccia IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
</dt> <dt>

[**Utilizzo della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




