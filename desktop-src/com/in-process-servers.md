---
title: Server In-Process
description: Server In-Process
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4886932b9669aa2d3cdd49979324f9ccc6e03d44
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221390"
---
# <a name="in-process-servers"></a>Server In-Process

Se si implementa un'applicazione server OLE come server in-process, ovvero una DLL in esecuzione nello spazio di processo dell'applicazione contenitore, anziché come server locale, un file EXE in esecuzione nello stesso spazio di processo, la comunicazione tra il contenitore e il server è semplificata perché la comunicazione tra i due può assumere la forma di normali chiamate di funzione. Non sono necessarie chiamate a procedure remote perché le due applicazioni vengono eseguite nello stesso spazio di processo. Come ci si aspetterebbe, anche gli oggetti che gestiscono il marshalling dei parametri non sono necessari, anche se possono essere aggregati all'interno della DLL senza interferire con la comunicazione tra il contenitore e il server.

Quando un'applicazione server OLE viene implementata come server in-process, non è necessario un gestore di oggetti separato perché il server si trova nello spazio di elaborazione del client. La differenza principale tra un server in-process e un gestore di oggetti è che il server è in grado di gestire l'oggetto in uno stato di esecuzione mentre il gestore non può. Una conseguenza di questa differenza è che un server deve fornire un'interfaccia utente per la modifica dell'oggetto in esecuzione, mentre un gestore delega questo requisito al server dell'oggetto. Durante la creazione di un server in-process, è possibile aggregare il gestore predefinito OLE, consentendo di gestire le faccende di base, ad esempio la visualizzazione, l'archiviazione e le notifiche, mentre si implementano solo i servizi che il gestore non fornisce o non implementa nel modo necessario.

Per altre informazioni, vedere i seguenti argomenti:

-   [Vantaggi](advantages.md)
-   [Svantaggi](disadvantages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




