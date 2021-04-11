---
title: Sincronizzazione delle chiamate
description: Sincronizzazione delle chiamate
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec9254aceaaa8a6fa26d56d4a86987cc955b90dc
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047427"
---
# <a name="call-synchronization"></a>Sincronizzazione delle chiamate

Le applicazioni COM devono essere in grado di gestire correttamente l'input dell'utente durante l'elaborazione di una o più chiamate da COM o dal sistema operativo. COM fornisce la sincronizzazione delle chiamate solo per gli Apartment a thread singolo. Gli apartment multithread (contenenti thread a thread libero) non ricevono chiamate durante l'esecuzione di chiamate (sullo stesso thread). Gli apartment multithreading non possono effettuare chiamate sincronizzate di input. Le chiamate asincrone vengono convertite in chiamate sincrone in Apartment con multithreading. Il filtro messaggi non viene chiamato per alcun thread in un Apartment a thread multipli. Per ulteriori informazioni sui problemi di threading, vedere [processi, thread e Apartment](processes--threads--and-apartments.md).

Le chiamate COM tra processi rientrano in tre categorie, come indicato di seguito:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Chiamate sincrone*
</dt> <dd>

La maggior parte della comunicazione che si verifica all'interno di COM è sincrona. Quando si effettuano chiamate sincrone, il chiamante attende la risposta prima di continuare e può ricevere i messaggi in ingresso in attesa. COM immette un ciclo modale per attendere la risposta, ricevendo e inviando altri messaggi in modo controllato.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notifiche asincrone*
</dt> <dd>

Quando si inviano le notifiche asincrone, il chiamante non attende la risposta. COM utilizza gli eventi [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) o di alto livello per inviare notifiche asincrone, a seconda della piattaforma. COM definisce cinque metodi asincroni di [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink):

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Mentre COM sta elaborando una chiamata asincrona, non è possibile effettuare chiamate sincrone. Ad esempio, l'implementazione di un'applicazione contenitore di [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) non può contenere una chiamata a [**IPersistStorage:: Save**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save). Queste chiamate sono le uniche chiamate asincrone supportate da COM. In questo momento non è possibile creare un'interfaccia personalizzata asincrona.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Chiamate sincronizzate di input*
</dt> <dd>

Quando si effettuano chiamate sincronizzate in input, l'oggetto chiamato deve completare la chiamata prima di cedere il controllo. Ciò garantisce che la gestione dello stato attivo funzioni correttamente e che i dati immessi dall'utente vengano elaborati in modo appropriato. Queste chiamate vengono effettuate da COM tramite la funzione [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage) , senza immettere un ciclo modale. Durante l'elaborazione di una chiamata sincronizzata in input, l'oggetto chiamato non deve chiamare alcun metodo o funzione (inclusi i metodi sincroni) che potrebbero restituire il controllo. I metodi seguenti sono sincronizzati con l'input

-   [**IOleWindow:: GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject:: OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject:: OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject:: ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**Oleinplaceuiwindow:: GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**Oleinplaceuiwindow:: RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**Oleinplaceuiwindow:: SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame:: semenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame:: SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject:: SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Per ridurre al minimo i problemi che possono derivare dall'elaborazione asincrona dei messaggi, la maggior parte delle chiamate al metodo COM è sincrona. Con la comunicazione sincrona, non è necessario un codice speciale per la distribuzione e la gestione dei messaggi in arrivo. Quando un'applicazione esegue una chiamata a un metodo sincrono, COM immette un ciclo di attesa modale che gestisce le risposte necessarie e invia i messaggi in ingresso alle applicazioni in grado di elaborarle.

COM gestisce le chiamate al metodo assegnando un identificatore denominato *ID thread logico*. Ne viene assegnato uno nuovo quando un utente seleziona un comando di menu o quando l'applicazione avvia una nuova operazione COM. Alle chiamate successive correlate alla chiamata COM iniziale viene assegnato lo stesso ID di thread logico della chiamata iniziale.

 

 