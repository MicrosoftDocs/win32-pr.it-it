---
title: Informazioni sulla pubblicazione del servizio
description: Un servizio è un'applicazione che rende i dati o le operazioni disponibili per i client di rete. Spesso, un servizio viene implementato come servizio formale basato su Microsoft Win32, ma non è obbligatorio.
ms.assetid: 500f37ff-2551-44a0-91d8-56f0df5afa69
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3945107125df04bbdb862d476d0aba78711ba8f89622c732e0d6ae53d65d1eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117840906"
---
# <a name="about-service-publication"></a>Informazioni sulla pubblicazione del servizio

Un servizio è un'applicazione che rende i dati o le operazioni disponibili per i client di rete. Spesso, un servizio viene implementato come servizio formale basato su Microsoft Win32, ma non è obbligatorio.

La pubblicazione del servizio è l'azione di creazione e gestione dei dati relativi a una o più istanze di un determinato servizio in modo che i client di rete possano trovare e utilizzare il servizio. La pubblicazione di un servizio Active Directory Domain Services consente a client e amministratori di passare da una vista incentrata sul computer del sistema distribuito a una visualizzazione incentrata sui servizi.

**Microsoft Windows NT 3.51 e sistemi operativi successivi:** Un sistema distribuito era un gruppo di computer che eseguono vari servizi. Per accedere a un servizio, un'applicazione richiedeva dati sui computer che offrivano il servizio.

**Windows 2000 Server, Windows 2000 Advanced Server e Windows 2000 Datacenter Server:** I servizi pubblicano la loro esistenza Active Directory Domain Services oggetti . Gli oggetti contengono informazioni di associazione utilizzate dalle applicazioni client per connettersi alle istanze del servizio. Per accedere a un servizio, un client non deve conoscere computer specifici: gli oggetti in un server Active Directory includono queste informazioni. Un client esegue una query sul server Active Directory per trovare un oggetto che rappresenta un servizio (denominato oggetto punto di connessione) e usa i dati di associazione dall'oggetto per connettersi al servizio.

Nella tabella seguente vengono illustrati esempi di associazioni.



| Servizio      | Binding                                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Servizio file | Nome UNC per una condivisione. Ad esempio " \\ \\ MyServer \\ MyshareName".                                                                                                                                                              |
| Servizio Web  | Url. Ad esempio " https://www.fabrikam.com ".                                                                                                                                                                                 |
| Servizio RPC  | Associazione RPC (Remote Procedure Call): informazioni speciali codificate usate per connettersi al server RPC. Le associazioni RPC possono essere convertite in e da stringhe con le API RPC. Ad esempio: "ncacn \_ ip \_ tcp:server.fabrikam.com". |



 

In un sistema distribuito i computer sono motori e le entità interessanti sono i servizi disponibili. Dal punto di vista dell'utente, l'identità del computer che fornisce un particolare servizio non è importante. L'aspetto importante è l'accesso al servizio stesso.

Questo è anche il caso della gestione dei servizi. L'amministratore di una determinata zona DNS non è interessato ai computer che eseguono il servizio DNS. l'amministratore vuole amministrare DNS. È probabile che siano presenti più istanze del servizio DNS, una delle quali è autorevole. I computer che supportano il servizio DNS non sono importanti per l'amministratore DNS. L'aspetto importante è come gestire il servizio come singola risorsa distribuita, non come singoli processi in esecuzione in computer diversi.

 

 




