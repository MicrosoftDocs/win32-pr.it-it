---
title: Creazione di un progetto di esempio
description: Creazione di un progetto di esempio
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player Online Stores, creazione di progetti di esempio
- negozi online, creazione di progetti di esempio
- digitare 2 archivi online, creazione di progetti di esempio
- Windows Media Player Online Stores, progetti di esempio
- negozi online, progetti di esempio
- digitare 2 archivi online, progetti di esempio
- Windows Media Player Online Stores, creazione guidata progetto
- negozi online, creazione guidata progetto
- digitare 2 archivi online, creazione guidata progetto
- plug-in, creazione guidata progetto
- Plug-in di Windows Media Player, creazione guidata progetto
- creazione di progetti di esempio
- esempi, digitare 2 archivi online
- Creazione guidata progetto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/21/2020
ms.locfileid: "104117435"
---
# <a name="creating-a-sample-project"></a>Creazione di un progetto di esempio

Per creare un nuovo progetto utilizzando la creazione guidata progetto, attenersi alla seguente procedura:

1.  Aprire Microsoft Visual Studio.
2.  Scegliere **Nuovo** dal menu **File**, quindi fare clic su **Progetto**.
3.  Nella casella di riepilogo **Tipi progetto** scegliere **Visual C++ progetti**.
4.  Nella casella di riepilogo **modelli** scegliere **Windows Media Player procedura guidata degli archivi online**.
5.  Digitare un nome e un percorso per il progetto.
6.  Fare clic su **OK** per avviare la creazione guidata progetto.
7.  Selezionare il **tipo 2 (integrazione di base)** e fare clic su **Avanti**.
8.  Digitare il nome descrittivo e l'ID del server di distribuzione del contenuto per il servizio. Digitare l'URL della pagina Web che rimuove il servizio dal computer dell'utente.
    > [!Note]  
    > Il valore fornito per l'ID del server di distribuzione del contenuto non deve contenere spazi. La procedura guidata consente di rimuovere gli spazi dalla stringa fornita.

     

9.  Fare clic su **Finish** (Fine) per creare il progetto.

La procedura guidata genera automaticamente un nuovo progetto C++ per la creazione di un plug-in di archiviazione di tipo 2 in cui vengono implementate le interfacce **IWMPSubscriptionService** e **IWMPSubscriptionService2** . Ogni volta che si esegue la procedura guidata, viene creato lo stesso progetto, ma il componente creato quando si compila il progetto ha un ID classe univoco. Il nome del progetto, il nome descrittivo e l'ID del server di distribuzione del contenuto possono anche variare a seconda dei valori specificati al momento dell'esecuzione della procedura guidata. Il progetto di esempio registra il componente usando un nome di chiave che corrisponde al valore specificato per il nome descrittivo.

Nell'esempio viene utilizzato il codice Active Template Library (ATL) per fornire implementazioni COM.

La procedura guidata crea automaticamente i seguenti file:

-   *NomeProgetto* dll. cpp. Implementa le esportazioni DLL (Dynamic Link Library), ad esempio la funzione principale del punto di ingresso della DLL. Contiene anche la dichiarazione del modulo e della mappa dell'oggetto ATL.
-   *NomeProgetto*. cpp. Contiene le implementazioni predefinite per i metodi delle interfacce IWMPSubscriptionService e IWMPSubscriptionService2. Contiene inoltre il codice per definire le finestre di dialogo che vengono aperte dall'esempio quando i metodi vengono chiamati da Windows Media Player.
-   *NomeProgetto*. def. Dichiara le esportazioni DLL.
-   StdAfx. cpp. Include intestazioni standard.
-   WMP. h. Il file di intestazione Media Player di Windows.
-   wmpplug. h. Il file di intestazione del plug-in di Windows Media Player.
-   SubscriptionServices. h. Il file di intestazione di Windows Media Player Online Stores.
-   Resource. h. Contiene le definizioni di risorse.
-   **NomeProgetto**. h. Contiene le definizioni di classe per l'oggetto di archivio online e le finestre di dialogo. Definisce l'ID classe dell'oggetto e la costante ID del server di distribuzione del contenuto.
-   StdAfx. h. Contiene le inclusioni di sistema standard.
-   *NomeProgetto*. RC. File di script di risorsa. Contiene le definizioni per le risorse e i controlli della finestra di dialogo. Questa è anche la posizione in cui viene archiviata la tabella delle stringhe. La tabella delle stringhe contiene il nome del progetto e le costanti di stringa del nome descrittivo. In genere si utilizza questo file nell'editor risorse di Visual Studio, non come testo normale.
-   *NomeProgetto*. RGS. File di script del registro di sistema. Questo file contiene le informazioni utilizzate per aggiungere la classe Component al registro di sistema in modo che Windows Media Player possa individuarlo. È possibile modificare il nome della chiave per il servizio in questo file.

> [!Note]  
> È necessario impostare l'indirizzo di base per la DLL su 0x0F100000 per evitare conflitti con Windows Media Player.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione del plug-in per un negozio online di tipo 2**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**Interfaccia IWMPSubscriptionService2**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




