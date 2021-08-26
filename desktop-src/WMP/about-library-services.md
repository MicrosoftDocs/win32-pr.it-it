---
title: Informazioni sui servizi di libreria
description: Informazioni sui servizi di libreria
ms.assetid: 2334aa4a-7988-481d-9b21-9f7b432fbd05
keywords:
- Windows Media Player,library
- Windows Media Player a oggetti, libreria
- modello a oggetti, libreria
- Windows Media Player ActiveX, libreria per il modello a oggetti
- ActiveX, libreria per il modello a oggetti
- Windows Media Player Controllo ActiveX per dispositivi mobili, libreria per il modello a oggetti
- Windows Media Player Mobile, libreria per il modello a oggetti
- Windows Media Player libreria, informazioni su
- Windows Media Player, servizi
- libreria,servizi
- library,about
- versioni di Windows Media Player,servizi di libreria
- enumerazioni, servizi di libreria
- eventi, servizi di libreria
- esempi, servizi di libreria
- interfacce, servizi di libreria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dc6f073fa4c361f114589e080145a3cb3bb0a8c78736ba2dd1464332a7f7adc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004513"
---
# <a name="about-library-services"></a>Informazioni sui servizi di libreria

Nelle versioni precedenti di Windows Media Player il software usava un database di libreria singolo per ogni utente. Questo database è stato archiviato nel computer dell'utente ed è concettualmente associato all'utente e a una particolare istanza del lettore.

Windows Media Player 11 introduce i concetti di librerie multiple e remote. Ora, oltre alla libreria predefinita o locale, Windows Media Player può visualizzare il contenuto recuperato dalle librerie in altri computer connessi a una rete, che potrebbe includere altri utenti connessi allo stesso computer. Il lettore può anche visualizzare le visualizzazioni della libreria da altre origini, ad esempio dispositivi abilitati per MTP o CD di dati. Dal punto di vista dell'utente finale, ciò significa che il contenuto multimediale digitale che si trova in molte posizioni diverse può essere gestito da più posizioni usando la stessa interfaccia Windows Media Player utente. Dal punto di vista dello sviluppatore, ciò significa che è possibile usare le interfacce COM di Windows Media Player SDK per enumerare le librerie disponibili e quindi usarle come se si usava la libreria locale nelle versioni precedenti.

Per enumerare le librerie disponibili, usare **l'interfaccia IWMPLibraryServices.** Questa interfaccia espone il [metodo IWMPLibraryServices::getCountByType,](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getcountbytype) che recupera il conteggio delle librerie di un determinato tipo. I tipi di libreria sono definiti [dall'enumerazione WMPLibraryType.](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype) Questa enumerazione include un valore per la libreria locale, wmpltLocal. Questo perché la funzionalità dei servizi di libreria consente sempre di usare la libreria locale usando **IWMPLibraryServices** e le interfacce correlate.

> [!Note]  
> **L'enumerazione WMPLibraryType** include il valore wmpltRemote, che rappresenta le librerie multimediali condivise dalla rete. Per accedere a tali librerie condivise, il controllo Player deve essere in esecuzione in modalità remota. Per informazioni sull'esecuzione del controllo Player in modalità remota, vedere [Remoting the Windows Media Player Control](remoting-the-windows-media-player-control.md).

 

Dopo aver recuperato il conteggio delle librerie, è possibile scorrere la raccolta di librerie disponibili chiamando ripetutamente [IWMPLibraryServices::getLibraryByType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibraryservices-getlibrarybytype) in un ciclo, passando un nuovo valore di indice a ogni iterazione. Questo metodo recupera un puntatore a [un'interfaccia IWMPLibrary,](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary) che rappresenta la singola libreria.

Dopo aver recuperato un puntatore a **IWMPLibrary,** è possibile chiamare [IWMPLibrary::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_mediacollection) per recuperare un puntatore a **un'interfaccia IWMPMediaCollection.** Con questo puntatore a interfaccia è possibile usare una singola libreria in modo simile a quella locale. È anche possibile recuperare una stringa contenente il nome della libreria chiamando [IWMPLibrary::get \_ name](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_name), utile se è necessario visualizzare il nome della libreria all'utente. È possibile chiamare [il tipo \_ IWMPLibrary::get](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-get_type) per ottenere **WMPLibraryType** di una libreria specifica.

È possibile gestire [l'evento IWMPEvents3::LibraryConnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect) per sapere quando una libreria diventa disponibile e l'evento [IWMPEvents3::LibraryDisconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect) per sapere quando si disconnette una libreria. Ognuno di questi eventi fornisce un **puntatore IWMPLibrary** che rappresenta la libreria connessa o disconnessa. È possibile chiamare [IWMPLibrary::isIdentical](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmplibrary-isidentical) per determinare se la libreria connessa o disconnessa è una libreria attualmente in uso.

Esistono alcune differenze importanti quando si usa una libreria recuperata tramite **l'interfaccia IWMPLibraryServices** rispetto a una libreria recuperata tramite [IWMPCore::get \_ mediaCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection). Si applicano le differenze seguenti:

-   È in genere possibile recuperare i risultati delle query molto più velocemente dalle librerie recuperate **tramite IWMPLibraryServices**. Si presuppone che altri fattori, ad esempio i tempi di accesso alla rete e al disco rigido, siano uguali.
-   L'elenco degli attributi dei metadati degli elementi multimediali disponibili dalle librerie recuperate tramite **IWMPLibraryServices** è in genere un subset di quelli disponibili dalla libreria locale recuperata tramite [IWMPCore.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)
-   Se si recupera la libreria locale tramite **IWMPLibraryServices**, tutti gli stessi attributi sono disponibili per l'uso come quelli disponibili quando si recupera la libreria locale tramite **IWMPCore**. Tuttavia, sarà possibile recuperare i risultati delle query molto più velocemente per gli attributi usati più di frequente.
-   È consigliabile usare raccolte di stringhe per creare elementi dell'interfaccia utente quando si usano librerie recuperate tramite **IWMPLibraryServices**. Ad esempio, [IWMPMediaCollection2::getStringCollectionByQuery](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection2-getstringcollectionbyquery) consente di usare una query personalizzata (rappresentata **dall'interfaccia IWMPQuery)** per recuperare una raccolta di stringhe.
-   Le librerie remote recuperate **tramite l'interfaccia IWMPLibraryServices** potrebbero non essere sempre connesse all'istanza corrente di Player. Ciò significa che è importante gestire gli eventi **LibraryConnect** e **LibraryDisconnect** per sapere quando cambia la disponibilità della libreria e gestire l'evento [IWMPEvents3::StringCollectionChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange) per sapere quando le stringhe vengono aggiunte o rimosse dalle raccolte di stringhe usate per visualizzare gli elementi dell'interfaccia utente. È anche necessario gestire **gli eventi StringCollectionChange** per la libreria locale per motivi simili.

È importante comprendere che le raccolte di stringhe per una determinata libreria possono cambiare in qualsiasi momento. Una raccolta di stringhe potrebbe essere vuota quando la si recupera per la prima volta, come nel caso di una libreria connessa di recente ma che il lettore non ha ancora enumerato il contenuto. Al contrario, una raccolta di stringhe potrebbe già contenere tutte le informazioni necessarie. In questo caso, è possibile che non si riceva mai un evento **StringCollectionChange** perché il contenuto della libreria è stato completamente enumerato prima di creare la query e non cambia nulla.

Pertanto, per mantenere aggiornata l'interfaccia utente, è necessario enumerare il contenuto della raccolta di stringhe quando si recupera l'interfaccia **IWMPStringCollection** e si gestisce l'evento **StringCollectionChange** per conoscere gli aggiornamenti quando si verificano.

## <a name="sample"></a>Esempio

L'esempio denominato WMPML illustra come usare i servizi di libreria. Per altre informazioni sugli esempi Windows Media Player SDK, vedere [Esempi](samples.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Informazioni sulla libreria**](about-the-library.md)
</dt> <dt>

[**Informazioni sull'oggetto Query**](about-the-query-object.md)
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

[**Uso della libreria**](working-with-the-library.md)
</dt> </dl>

 

 




