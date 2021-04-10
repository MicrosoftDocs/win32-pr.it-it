---
title: Informazioni sulla pubblicazione del servizio
description: Un servizio è un'applicazione che rende disponibili i dati o le operazioni ai client di rete. Un servizio viene spesso implementato come un servizio formale basato su Microsoft Win32, ma ciò non è obbligatorio.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee34c1f0955f45f1bd4c689455ac03e79d987480
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955050"
---
# <a name="about-service-publication"></a>Informazioni sulla pubblicazione del servizio

Un servizio è un'applicazione che rende disponibili i dati o le operazioni ai client di rete. Un servizio viene spesso implementato come un servizio formale basato su Microsoft Win32, ma ciò non è obbligatorio.

La pubblicazione del servizio è la creazione e la gestione dei dati relativi a una o più istanze di un determinato servizio in modo che i client di rete possano trovare e usare il servizio. La pubblicazione di un servizio in Active Directory Domain Services consente ai client e agli amministratori di spostarsi da una visualizzazione incentrata sul computer del sistema distribuito a una visualizzazione incentrata sul servizio.

**Microsoft Windows NT 3,51 e sistemi operativi successivi:** Un sistema distribuito è un gruppo di computer che eseguono vari servizi. Per accedere a un servizio, un'applicazione richiede i dati sui computer che hanno offerto il servizio.

**Windows 2000 Server, windows 2000 Advanced Server e windows 2000 Datacenter Server:** I servizi pubblicano l'esistenza usando oggetti Active Directory Domain Services. Gli oggetti contengono informazioni di binding utilizzate dalle applicazioni client per la connessione alle istanze del servizio. Per accedere a un servizio, un client non deve essere a conoscenza di computer specifici: gli oggetti in un server di Active Directory includono queste informazioni. Un client esegue una query sul server Active Directory per un oggetto che rappresenta un servizio (chiamato oggetto punto di connessione) e utilizza i dati di associazione dall'oggetto per la connessione al servizio.

Nella tabella seguente vengono illustrati esempi di associazioni.



| Servizio      | Binding                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Servizio file | Nome UNC di una condivisione. Ad esempio \\ \\ , "MyServer \\ condivisione".                                                                                                                                                              |
| Servizio Web  | URL. Ad esempio " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Servizio RPC  | Binding RPC (Remote Procedure Call): informazioni speciali codificate utilizzate per la connessione al server RPC. Le associazioni RPC possono essere convertite in e da stringhe con le API RPC. Ad esempio: "ncacn \_ IP \_ TCP:Server. fabrikam. com". |



 

In un sistema distribuito, i computer sono motori e le entità interessanti sono i servizi disponibili. Dal punto di vista dell'utente, l'identità del computer che fornisce un particolare servizio non è importante. È importante accedere al servizio stesso.

Questo è anche il caso della gestione dei servizi. L'amministratore di una determinata zona DNS non è interessato ai computer che eseguono il servizio DNS; l'amministratore desidera amministrare DNS. Probabilmente saranno presenti più istanze del servizio DNS, una delle quali è autorevole. I computer che supportano il servizio DNS non sono importanti per l'amministratore DNS. Ciò che è importante è come gestire il servizio come una singola risorsa distribuita, non come singoli processi in esecuzione in computer diversi.

 

 




