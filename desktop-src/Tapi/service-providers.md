---
description: I provider di servizi implementano controlli di dispositivo di telefonia dettagliati. Un provider di servizi di telefonia (TSP) fornisce controlli di chiamata e un provider di servizi multimediali, se esistente, fornisce il controllo sul flusso multimediale.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424c11d5b99af7440835e8822a5631e1b36f48cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968745"
---
# <a name="service-providers"></a>Provider di servizi

I provider di servizi implementano controlli di dispositivo di telefonia dettagliati. Un provider di servizi di telefonia (TSP) fornisce controlli di chiamata e un provider di servizi multimediali, se esistente, fornisce il controllo sul flusso multimediale.

Tutti i provider di servizi di telefonia vengono eseguiti nel processo TAPISRV. I provider di servizi possono creare thread nel contesto TAPISRV in base alle esigenze per svolgere il proprio lavoro e assicurarsi che nessuna delle risorse create venga distrutta dall'uscita di una singola applicazione. Il server TAPI converte i comandi dell'applicazione in base alle esigenze in un set coerente di comandi noto come TSPI (Telephony Service Provider Interface).

I provider di servizi multimediali vengono eseguiti nello spazio di processo dell'applicazione, consentendo la risposta rapida a volte necessaria nei controlli multimediali. La DLL TAPI garantisce una conformità coerente all'interfaccia del provider di servizi multimediali (MSPI).

Per una copertura più dettagliata dei provider di servizi, vedere [Panoramica del provider di servizi TAPI](./tapi-service-provider-overview.md).

Al di sotto della DLL del provider di servizi di telefonia, il provider di servizi può utilizzare qualsiasi funzione di sistema o altri componenti necessari. Queste funzioni includono [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol), che funzionano con componenti e servizi della modalità kernel progettati per il fornitore di hardware indipendenti, nonché dispositivi standard come le porte seriali e parallele per controllare i dispositivi esterni collegati localmente. Possono anche accedere ai servizi di rete (ad esempio RPC, Windows Sockets e named pipe) per la telefonia client/server.

La DLL dell'interfaccia utente del provider di servizi di telefonia viene caricata da TAPI nel processo di un'applicazione che richiama una delle funzioni del provider di servizi che possono visualizzare una finestra di dialogo, ad esempio [**TSPI \_ lineConfigDialog**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog). Il provider di servizi può anche causare il caricamento e l'esecuzione della DLL dell'interfaccia utente associata nel processo di un'applicazione se il provider di servizi deve visualizzare l'interfaccia utente in momenti imprevisti, ad esempio, per visualizzare la finestra di dialogo di **conversazione/blocco** visualizzata dal driver del modem universale (UniModel) quando viene usato un modem dati per comporre una chiamata vocale interattiva usando [**TSPI \_ lineMakeCall**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (non generalmente considerata una funzione di generazione dell'interfaccia utente).

Il gestore di richieste proxy è un'applicazione di telefonia completa che in genere viene eseguita in un server di telefonia (lo stesso server in cui è in esecuzione il provider del servizio di telefonia per i dispositivi linea associati). Questa architettura, anziché l'architettura del provider di servizi WOSA, viene usata quando un particolare servizio viene implementato in modo più appropriato in un'applicazione rispetto a un driver sul server. Le funzioni di gestione dell'agente di ACD, ad esempio, vengono implementate in un gestore di richieste proxy anziché in un provider di servizi.

Il provider di servizi di driver Unimodem per il controllo modem è disponibile nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 e Windows NT. La telefonia Windows include anche un mapper TSPI (Generic Service Provider Interface) in modalità kernel, KMDDSP, che consente di implementare i provider di servizi come driver di dispositivo in modalità kernel.

 

 
