---
title: Metodi IPaperSink
description: Il Copaper espone l'interfaccia IConnectionPointContainer, in modo che i client possano connettersi a un documento per ricevere le notifiche degli eventi specificati che si verificano in un documento.
ms.assetid: 2466c721-b275-4dbc-a604-2d5e6a29d6a1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8dee615b278c5214ad1efa3c10d22759620103
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223981"
---
# <a name="ipapersink-methods"></a>Metodi IPaperSink

Il Copaper espone l'interfaccia [**IConnectionPointContainer**](/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer) , in modo che i client possano connettersi a un documento per ricevere le notifiche degli eventi specificati che si verificano in un documento. Esponendo questa interfaccia, il Copaper diventa un oggetto collegabile. Un client può chiamare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per questa interfaccia e usarlo per ottenere i punti di connessione dell'oggetto. La partecipazione client in questo schema è illustrata nell'esempio **StoClien** associato.

In sostanza, il client implementa il cosiddetto sink sotto forma di oggetto sink con un'interfaccia sink. L'interfaccia di sink riceve le chiamate di notifica degli eventi in uscita da un foglio di lavoro dopo che il sink è stato connesso correttamente dal client a un'istanza di Copaper. Il client esegue la connessione utilizzando un oggetto punto di connessione gestito da un documento. In un singolo oggetto COM collegabile possono essere presenti numerosi punti di connessione. Nell'esempio **StoServe** , il Copaper dispone di un solo punto di connessione che gestisce gli eventi della carta di disegno.

Un numero qualsiasi di client può connettersi a un solo punto di connessione. Il \_ punto di connessione PAPERSINK di CONNPOINT in un documento gestisce un gruppo di connessioni che possono aumentare dinamicamente in fase di esecuzione. I dettagli completi sul supporto degli oggetti collegabili della cocarta sono codificati in file CONNECT. H e CONNECT. CPP e non verrà analizzato qui. La costruzione è molto simile a quella che è stata studiata nell'esempio di codice di conservazione.

Il client **StoClien** implementa gli oggetti sink appropriati per i punti di connessione che si prevede di trovare in un documento. Dal contesto del documento, l'oggetto sink importante implementato da **StoClien** espone l'interfaccia **IPaperSink** . Si tratta dell'interfaccia in uscita usata da Copaper per notificare **StoClien** di vari eventi in un documento.

Di seguito è riportato un riepilogo dei metodi di **IPaperSink** da IPAPER. H nella \\ directory di pari livello Inc.



| Metodo   | Descrizione                                                   |
|----------|---------------------------------------------------------------|
| Bloccato   | Un client ha assunto il controllo e bloccato il documento.           |
| Sbloccato | Un client ha ceduto il controllo del documento.               |
| Loaded   | Un client ha caricato il contenuto della carta dal relativo file composto. |
| Salvato    | Un client ha salvato il contenuto cartaceo nel proprio file composto.    |
| InkStart | Un client ha avviato una sequenza di disegno inchiostro a colori sul foglio.   |
| InkDraw  | Un client sta inserendo punti dati Ink sulla superficie della carta.     |
| InkStop  | Un client ha interrotto la sequenza di disegno input penna sulla carta.   |
| Cancellati   | Un client ha cancellato tutti i dati dell'input penna dal documento.              |
| Ridimensionata  | Un client ha ridimensionato il documento.                               |



 

Questi metodi sono ampiamente esplicativi. Sebbene il sink debba implementare tutti questi metodi in un certo modo, molti sono implementati come stub e non vengono usati negli esempi di / **StoClien** StoServe.

Un metodo importante utilizzato in questi esempi è il metodo Loaded. Quando viene indicato al client di caricare un nuovo disegno da un file, è necessario un modo per notificare al client quando vengono caricati i nuovi dati. A tale scopo, il Copaper chiama **IPaperSink:: Loaded** sul sink client. Il client può quindi chiamare [**iPaper:: redisegnato**](ipaper--redraw.md) per richiedere che il Copaper riproduca i nuovi dati nel client. Il ridisegno fa sì che il disegno caricato nella visualizzazione del client venga ridisegnato. Al termine del caricamento, il disegno appena caricato viene visualizzato automaticamente nella finestra fornita dal client.

Vedere [**iPaper:: redisegnato**](ipaper--redraw.md) per informazioni complete sulla connettività di questo metodo iPaper a **IPaperSink**.

I  metodi IPaperSink **InkStart**, **InkDraw** e **InkStop** vengono usati per inviare i singoli pacchetti di dati Ink al client. Al momento della ricezione, il client dipinge tali elementi nella visualizzazione nello stesso modo in cui sono stati originariamente inviati al documento. La logica precedente è sufficientemente generale da consentire a più client che sono tutti in ascolto sullo stesso \_ punto di connessione PAPERSINK CONNPOINT. Se un'istanza di un documento comune è stata condivisa da questi client, è possibile che tutti visualizzino lo stesso disegno connettendosi a questo punto di connessione.

 

 