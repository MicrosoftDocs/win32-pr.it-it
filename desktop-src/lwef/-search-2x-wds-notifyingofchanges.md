---
title: Notifica dell'indice delle modifiche (funzionalità legacy dell'ambiente Windows)
description: Con Microsoft Windows Desktop Search (WDS) 2,6, i gestori di protocollo per un determinato archivio dati possono indicare all'indicizzatore WDS quando i dati nel relativo archivio cambiano.
ms.assetid: 700b1707-dd11-4a30-8f00-5c4aae1173ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6021cfe5cd7061a3d3255e56d08e665a6caedf03
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104225194"
---
# <a name="notifying-the-index-of-changes-legacy-windows-environment-features"></a>Notifica dell'indice delle modifiche (funzionalità legacy dell'ambiente Windows)

> [!NOTE]
> Windows Desktop Search 2. x è una tecnologia obsoleta originariamente disponibile come componente aggiuntivo per Windows XP e Windows Server 2003. Nelle versioni successive usare invece [Windows Search](../search/-search-3x-wds-overview.md) .

Con Microsoft Windows Desktop Search (WDS) 2,6, i gestori di protocollo per un determinato archivio dati possono indicare all'indicizzatore WDS quando i dati nel relativo archivio cambiano. Ciò consente di migliorare le prestazioni assicurando che l'indicizzatore non esegue la ricerca per indici incrementali nell'intero archivio. Usando le API di notifica, i gestori di protocollo possono notificare all'indicizzatore che un elemento è stato spostato o eliminato e possono aggiungere degli ambiti alla coda di ricerca per indicizzazione dell'indicizzatore WDS degli URL che richiedono l'indicizzazione. La notifica è utile per le applicazioni, ad esempio la posta elettronica, in cui il gestore di protocollo monitora l'archivio e notifica all'indicizzatore che gli elementi sono stati modificati e richiedono l'indicizzazione.

## <a name="isearchitemschangedsink"></a>ISearchItemsChangedSink

I gestori di protocollo inviano notifiche all'indicizzatore delle modifiche tramite l'interfaccia [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) . Le informazioni sulle modifiche ai dati devono essere raccolte \_ negli \_ struct di modifica degli elementi di ricerca e nel \_ tipo \_ di ricerca dei \_ tipi di enumerazione delle modifiche e quindi comunicate all'indicizzatore tramite il metodo **OnItemsChanged** dell'interfaccia **ISearchItemsChangedSink** .

Per accedere a questa interfaccia, un gestore di protocollo personalizzato deve prima creare un'istanza di un oggetto [**ISearchManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchmanager) per ottenere l'accesso all'oggetto [**ISearchCatalogManager**](/windows/desktop/api/searchapi/nn-searchapi-isearchcatalogmanager) . Da qui, è possibile creare un'istanza di un oggetto [**ISearchItemsChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchitemschangedsink) e inviare una notifica all'indicizzatore delle modifiche dei dati.

Il metodo OnItemsChanged consente di raccogliere e comunicare le modifiche ai dati nell'archivio dati del cliente per avviare l'indicizzazione.



| Direzione | Variabile              | Descrizione                                                              |
|-----------|-----------------------|--------------------------------------------------------------------------|
| In        | dwNumberofChanges     | Numero totale di modifiche nella notifica.                             |
| In        | DataChangeEntries\[\] | Tutte le notifiche di modifica in una matrice di strutture di modifica degli elementi di ricerca \_ \_ . |
| In uscita       | dwBatchId             | ID batch che verrà restituito con errori.                       |
| In uscita       | hrCompletionCodes\[\] | Indica se ogni URL è stato accettato per l'indicizzazione.                    |



 

La \_ \_ struttura di modifica degli elementi di ricerca identifica il tipo di modifica che si è verificata, nonché l'URL corrente dell'elemento e l'URL precedente, se applicabile. La struttura viene definita nel modo seguente:



| Nome della proprietà | Tipo di proprietà                  | Descrizione                                                                |
|---------------|--------------------------------|----------------------------------------------------------------------------|
| Modifica        | \_tipo \_ di \_ modifica di ricerca       | Tipo di modifica a cui viene inviata una notifica.                                 |
| URL           | LPWSTR                         | URL per l'oggetto che è stato modificato.                                   |
| OldURL        | LPWSTR                         | Se la notifica è uno spostamento, viene fornito l'URL precedente e deve essere univoco. |
| Priorità      | \_priorità di notifica di ricerca \_ | Priorità della modifica.                                                |



 

Il \_ tipo \_ di ricerca dell'enumerazione delle \_ modifiche viene definito nel modo seguente:



| Valore enum                           | Valore   | Descrizione                                                                                     |
|--------------------------------------|---------|-------------------------------------------------------------------------------------------------|
| modifica di ricerca \_ \_ Aggiungi                  | 0       | La notifica riguarda un URL aggiuntivo.                                                      |
| \_Elimina modifiche di ricerca \_               | 1       | La notifica è relativa all'eliminazione di un URL.                                                  |
| modifica ricerca \_ modifiche \_               | 2       | La notifica è che un URL è stato modificato.                                               |
| \_modifica \_ \_ ridenominazione spostamento modifiche         | 3       | La notifica riguarda lo spostamento e la ridenominazione di un oggetto in un nuovo URL.                          |
| Cerca \_ \_ nella directory della semantica di modifica \_ | 0x10000 | La notifica riguarda un URL del contenitore.                                                        |
| \_semantica di modifica della ricerca \_ \_ superficiale   | 0x20000 | La notifica riguarda un URL del contenitore che deve avere solo le proprietà del contenitore indicizzate. |
| \_sicurezza della \_ semantica delle modifiche di ricerca \_  | 0x40000 | La notifica riguarda un URL o un URL del contenitore in cui sono state modificate le proprietà di sicurezza.    |



 

L' \_ \_ enumerazione di priorità della notifica di ricerca viene definita nel modo seguente:



| Valore enum               | Valore | Descrizione                                                                                                                                                                    |
|--------------------------|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cerca \_ \_ priorità normale | 0     | Quando si indicizza l'URL, è necessario utilizzare solo una priorità normale. Queste notifiche vengono elaborate prima della normale indicizzazione incrementale in background dei file e degli archivi di un utente. |



 

 

 
