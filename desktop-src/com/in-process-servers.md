---
title: In-Process server
description: In-Process server
ms.assetid: cc0c4350-fa75-4321-834f-711158776cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eccc4c65db19e4ed567a2fe6105fa4d81e9c52cc9165556d9f388d8af181eee3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854531"
---
# <a name="in-process-servers"></a>In-Process server

Se si implementa un'applicazione server OLE come server in-process, ovvero una DLL in esecuzione nello spazio di elaborazione dell'applicazione contenitore, anziché come server locale, un file EXE in esecuzione nel proprio spazio di elaborazione, la comunicazione tra contenitore e server è semplificata perché la comunicazione tra i due può assumere la forma di normali chiamate di funzione. Le chiamate di procedura remota non sono necessarie perché le due applicazioni vengono eseguite nello stesso spazio di processo. Come previsto, anche gli oggetti che gestiscono il marshalling dei parametri non sono necessari, anche se possono essere aggregati all'interno della DLL senza interferire con la comunicazione tra contenitore e server.

Quando un'applicazione server OLE viene implementata come server in-process, non è necessario un gestore di oggetti separato perché il server stesso si trova nello spazio di elaborazione del client. La differenza principale tra un server in-process e un gestore di oggetti è che il server è in grado di gestire l'oggetto in uno stato di esecuzione, mentre il gestore non lo è. Una conseguenza di questa differenza è che un server deve fornire un'interfaccia utente per la modifica dell'oggetto in esecuzione, mentre un gestore delega questo requisito al server dell'oggetto. Durante la creazione di un server in-process, è possibile eseguire l'aggregazione nel gestore predefinito OLE, consentendo di gestire attività di base, ad esempio visualizzazione, archiviazione e notifiche, mentre si implementano solo i servizi che il gestore non fornisce o non implementa nel modo richiesto.

Per altre informazioni, vedere i seguenti argomenti:

-   [Vantaggi](advantages.md)
-   [Svantaggi](disadvantages.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Documenti composti](compound-documents.md)
</dt> </dl>

 

 




