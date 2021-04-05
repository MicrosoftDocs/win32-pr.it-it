---
title: API di HTTP Server
description: L'API server HTTP consente alle applicazioni di comunicare tramite HTTP senza utilizzare Microsoft Internet Information Server (IIS).
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- API di HTTP Server
- API server HTTP, pagina iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104117734"
---
# <a name="http-server-api"></a>API di HTTP Server

## <a name="purpose"></a>Scopo

L'API server HTTP consente alle applicazioni di comunicare tramite HTTP senza utilizzare Microsoft Internet Information Server (IIS). Le applicazioni possono eseguire la registrazione per ricevere richieste HTTP per URL specifici, ricevere richieste HTTP e inviare risposte HTTP. L'API server HTTP include il supporto SSL, in modo che le applicazioni possano scambiare dati tramite connessioni HTTP sicure senza IIS. È anche progettato per funzionare con le porte di completamento I/O.

## <a name="developer-audience"></a>Sviluppatori

Questa API è progettata per l'uso da programmatori C/C++.

## <a name="run-time-requirements"></a>Requisiti di runtime

L'API server HTTP è supportata nei sistemi operativi Windows Server 2003 e in Windows XP con Service Pack 2 (SP2). Tenere presente che Microsoft IIS 5 in esecuzione su Windows XP con SP2 non è in grado di condividere la porta 80 con altre applicazioni HTTP eseguite simultaneamente.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                           | Descrizione                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [Informazioni sull'API server HTTP](about-http-server-api.md)<br/>                   | Informazioni generali sul protocollo HTTP.<br/>                                                              |
| [Uso dell'API server HTTP](using-http-server-api.md)<br/>                   | Guida procedurale per l'utilizzo di HTTP.<br/>                                                             |
| [Riferimento all'API del server HTTP](http-server-api-reference.md)<br/>           | Documentazione di funzioni, strutture e tipi di enumerazione specifici disponibili in HTTP.<br/>    |
| [Applicazione di esempio server HTTP](http-server-sample-application.md)<br/> | Applicazione di esempio in cui viene illustrato come utilizzare l'API del server HTTP per eseguire attività lato server.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi HTTP di Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

