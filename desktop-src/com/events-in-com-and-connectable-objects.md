---
title: Eventi in COM e oggetti collegabili
description: Quando un programma rileva un evento che si è verificato, può inviare una notifica ai client.
ms.assetid: f6ffbd1d-4bc1-4dc2-b3ed-ee12359e3d75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa5115cfd08d57658eec879d44b4361e88965b3c
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "104046228"
---
# <a name="events-in-com-and-connectable-objects"></a>Eventi in COM e oggetti collegabili

Quando un programma rileva un evento che si è verificato, può inviare una notifica ai client. Se, ad esempio, un programma di titolo azionario rileva una modifica nel prezzo di una borsa, può notificare a tutti i client la modifica. Questo processo di notifica viene definito *generazione di un evento*.

Con COM, gli oggetti server possono usare gli eventi COM per generare eventi senza informazioni sugli oggetti a cui verrà inviata una notifica. Gli oggetti possono inoltre utilizzare *oggetti collegabili* per mantenere informazioni dettagliate sui client che hanno richiesto le notifiche.

Gli oggetti COM collegabili forniscono interfacce in uscita ai client oltre alle interfacce in ingresso. Di conseguenza, gli oggetti e i relativi client possono interagire con la comunicazione bidirezionale. Le interfacce in ingresso vengono implementate in un oggetto e ricevono chiamate da client esterni di un oggetto, mentre le interfacce in uscita vengono implementate nel sink del client e ricevono chiamate dall'oggetto. L'oggetto definisce un'interfaccia che si desidera utilizzare e il client la implementa.

Un oggetto definisce le interfacce in ingresso e fornisce le implementazioni di tali interfacce. Le interfacce in entrata sono disponibili per i client tramite il metodo [**IUnknown:: QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q)) dell'oggetto. I client chiamano i metodi di un'interfaccia in ingresso nell'oggetto e l'oggetto esegue le azioni desiderate per conto del client.

Le interfacce in uscita sono definite anche da un oggetto, ma il client fornisce le implementazioni delle interfacce in uscita su un oggetto sink creato dal client. L'oggetto chiama quindi i metodi dell'interfaccia in uscita sull'oggetto sink per notificare al client le modifiche apportate all'oggetto, per attivare eventi nel client, per richiedere qualcosa dal client o, di fatto, per qualsiasi scopo con cui il creatore dell'oggetto viene visualizzato.

Un esempio di interfaccia in uscita è un'interfaccia IButtonSink definita da un controllo pulsante di push per notificare ai client i relativi eventi. Ad esempio, l'oggetto Button chiama IButtonSink:: OnClick sull'oggetto sink del client quando l'utente fa clic sul pulsante sullo schermo. Il controllo Button definisce l'interfaccia in uscita. Affinché un client del pulsante gestisca l'evento, il client deve implementare tale interfaccia in uscita su un oggetto sink, quindi connettere il sink al controllo Button. Quindi, quando si verificano eventi nel pulsante, il pulsante chiamerà il sink, a quel punto il client può eseguire qualsiasi azione da assegnare a tale pulsante.

Gli oggetti collegabili forniscono un meccanismo generale per la comunicazione da oggetto a client. Tutti gli oggetti che desiderano esporre eventi o notifiche di qualsiasi tipo possono utilizzare questa tecnologia. Oltre alla tecnologia di oggetti collegabile generale, COM offre numerose interfacce di sink e siti per scopi specifici usati dagli oggetti per notificare ai client di eventi specifici di interesse per il client. Ad esempio, [**IAdviseSink**](/windows/desktop/api/ObjIdl/nn-objidl-iadvisesink) può essere utilizzato dagli oggetti per notificare ai client i dati e visualizzare le modifiche nell'oggetto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Architettura degli oggetti collegabili](architecture-of-connectable-objects.md)
-   [Interfacce di oggetti collegabili](connectable-object-interfaces.md)

 

 




