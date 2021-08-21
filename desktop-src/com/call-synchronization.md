---
title: Sincronizzazione delle chiamate
description: Sincronizzazione delle chiamate
ms.assetid: e74407ef-f500-4d13-aef4-ca6bb37d5858
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9969c968294a3dfdbfbc4cb78d40e64ad65c17392bf3b9fd09fc7a5f99b9049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048739"
---
# <a name="call-synchronization"></a>Sincronizzazione delle chiamate

Le applicazioni COM devono essere in grado di gestire correttamente l'input dell'utente durante l'elaborazione di una o più chiamate da COM o dal sistema operativo. COM fornisce la sincronizzazione delle chiamate solo per apartment a thread singolo. Gli apartment a thread multipli (contenenti thread a thread libero) non ricevono chiamate durante l'esecuzione di chiamate (sullo stesso thread). Gli apartment multithreading non possono effettuare chiamate sincronizzate di input. Le chiamate asincrone vengono convertite in chiamate sincrone in apartment multithreading. Il filtro messaggi non viene chiamato per alcun thread in un apartment multithreading. Per altre informazioni sui problemi di threading, vedere [Processi, thread e apartment.](processes--threads--and-apartments.md)

Le chiamate COM tra processi rientrano in tre categorie, come indicato di seguito:

<dl> <dt>

<span id="Synchronous_calls"></span><span id="synchronous_calls"></span><span id="SYNCHRONOUS_CALLS"></span>*Chiamate sincrone*
</dt> <dd>

La maggior parte delle comunicazioni che avviene all'interno di COM è sincrona. Quando si eseguono chiamate sincrone, il chiamante attende la risposta prima di continuare e può ricevere messaggi in arrivo durante l'attesa. COM entra in un ciclo modale per attendere la risposta, ricevendo e inviando altri messaggi in modo controllato.

</dd> <dt>

<span id="Asynchronous_notifications"></span><span id="asynchronous_notifications"></span><span id="ASYNCHRONOUS_NOTIFICATIONS"></span>*Notifiche asincrone*
</dt> <dd>

Quando si inviano notifiche asincrone, il chiamante non attende la risposta. COM usa [**PostMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) o eventi di alto livello per inviare notifiche asincrone, a seconda della piattaforma. COM definisce cinque metodi asincroni [**di IAdviseSink:**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink)

-   [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange)
-   [**OnViewChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onviewchange)
-   [**OnRename**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onrename)
-   [**OnSave**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onsave)
-   [**OnClose**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-onclose)

> [!Note]  
> Durante l'elaborazione di una chiamata asincrona da parte di COM, non è possibile effettuare chiamate sincrone. Ad esempio, l'implementazione di [**OnDataChange**](/windows/desktop/api/ObjIdl/nf-objidl-iadvisesink-ondatachange) di un'applicazione contenitore non può contenere una chiamata a [**IPersistStorage::Save.**](/windows/desktop/api/ObjIdl/nf-objidl-ipersiststorage-save) Queste chiamate sono le uniche chiamate asincrone supportate da COM. Al momento non è possibile creare un'interfaccia personalizzata asincrona.

 

</dd> <dt>

<span id="Input-synchronized_calls"></span><span id="input-synchronized_calls"></span><span id="INPUT-SYNCHRONIZED_CALLS"></span>*Chiamate sincronizzate con input*
</dt> <dd>

Quando si effettuano chiamate sincronizzate con input, l'oggetto chiamato deve completare la chiamata prima di cedere il controllo. In questo modo si garantisce che la gestione dello stato attivo funzioni correttamente e che i dati immessi dall'utente vengano elaborati in modo appropriato. Queste chiamate vengono effettuate da COM tramite la [**funzione SendMessage,**](/windows/win32/api/winuser/nf-winuser-sendmessage) senza immettere un ciclo modale. Durante l'elaborazione di una chiamata sincronizzata con input, l'oggetto chiamato non deve chiamare alcuna funzione o metodo (inclusi i metodi sincroni) che potrebbe cedere il controllo. I metodi seguenti sono sincronizzati con input

-   [**IOleWindow::GetWindow**](/windows/desktop/api/OleIdl/nf-oleidl-iolewindow-getwindow)
-   [**IOleInPlaceActiveObject::OnFrameWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-onframewindowactivate)
-   [**IOleInPlaceActiveObject::OnDocWindowActivate**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-ondocwindowactivate)
-   [**IOleInPlaceActiveObject::ResizeBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceactiveobject-resizeborder)
-   [**IOleInPlaceUIWindow::GetBorder**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-getborder)
-   [**IOleInPlaceUIWindow::RequestBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-requestborderspace)
-   [**IOleInPlaceUIWindow::SetBorderSpace**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceuiwindow-setborderspace)
-   [**IOleInPlaceFrame::SetMenu**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setmenu)
-   [**IOleInPlaceFrame::SetStatusText**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceframe-setstatustext)
-   [**IOleInPlaceObject::SetObjectRects**](/windows/desktop/api/OleIdl/nf-oleidl-ioleinplaceobject-setobjectrects)

</dd> </dl>

Per ridurre al minimo i problemi che possono verificarsi durante l'elaborazione asincrona dei messaggi, la maggior parte delle chiamate al metodo COM è sincrona. Con la comunicazione sincrona, non è necessario codice speciale per inviare e gestire i messaggi in arrivo. Quando un'applicazione effettua una chiamata sincrona al metodo, COM entra in un ciclo di attesa modale che gestisce le risposte necessarie e invia i messaggi in arrivo alle applicazioni in grado di elaborarli.

COM gestisce le chiamate ai metodi assegnando un identificatore denominato ID *di thread logico*. Ne viene assegnato uno nuovo quando un utente seleziona un comando di menu o quando l'applicazione avvia una nuova operazione COM. Alle chiamate successive correlate alla chiamata COM iniziale viene assegnato lo stesso ID thread logico della chiamata iniziale.

 

 