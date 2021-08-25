---
description: I provider di servizi implementano controlli dettagliati dei dispositivi di telefonia. Un provider di servizi di telefonia (TSP) fornisce controlli di chiamata e un provider di servizi multimediali, se esistente, fornisce il controllo sul flusso multimediale.
ms.assetid: eb63d55e-4a2b-4bc0-8001-99772f418d72
title: Provider di servizi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba0bc427b79daadc8dc89e49a29e18ebbd9797bed74da7f890dc851d6ee97b13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773121"
---
# <a name="service-providers"></a>Provider di servizi

I provider di servizi implementano controlli dettagliati dei dispositivi di telefonia. Un provider di servizi di telefonia (TSP) fornisce controlli di chiamata e un provider di servizi multimediali, se esistente, fornisce il controllo sul flusso multimediale.

Tutti i provider di servizi di telefonia vengono eseguiti nel processo TAPISRV. I provider di servizi possono creare thread nel contesto TAPISRV in base alle esigenze per eseguire il proprio lavoro e avere la certezza che nessuna delle risorse create verrà distrutta dall'uscita di una singola applicazione. Il server TAPI converte i comandi dell'applicazione in base alle esigenze in un set coerente di comandi noto come TSPI (Telefonia Service Provider Interface).

I provider di servizi multimediali vengono eseguiti nello spazio di elaborazione dell'applicazione, consentendo la risposta rapida talvolta necessaria nei controlli multimediali. La DLL TAPI garantisce un'aderenza coerente all'interfaccia MSPI (Media Service Provider Interface).

Per una descrizione più dettagliata dei provider di servizi, vedere [Panoramica del provider di servizi TAPI.](./tapi-service-provider-overview.md)

Sotto la DLL del provider di servizi di telefonia, il provider di servizi può usare qualsiasi funzione di sistema o altri componenti necessari. Queste funzioni includono [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) e [**DeviceIoControl,**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol)che funzionano con componenti e servizi indipendenti in modalità kernel progettati dal fornitore dell'hardware, nonché dispositivi standard come le porte seriali e parallele per controllare i dispositivi esterni collegati localmente. Possono anche accedere ai servizi di rete ,ad esempio RPC, Windows Socket e Named Pipes, per la telefonia client/server.

La DLL dell'interfaccia utente del provider di servizi di telefonia viene caricata da TAPI nel processo di un'applicazione che richiama una qualsiasi delle funzioni del provider di servizi in grado di visualizzare una finestra di dialogo, ad esempio [**\_ lineConfigDialog TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog) Il provider di servizi può anche fare in modo che la DLL dell'interfaccia utente associata venga caricata ed eseguita nel processo di un'applicazione se il provider di servizi deve visualizzare l'interfaccia utente in momenti imprevisti, ad esempio per visualizzare la finestra di dialogo **Talk/Hang-up** visualizzata da Universal Modem Driver (UNIMODEM) quando un modem dati viene usato per effettuare una chiamata vocale interattiva usando [**\_ lineMakeCall TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall) (non in genere considerata una funzione che genera l'interfaccia utente).

Il gestore richieste proxy è un'applicazione di telefonia completa che in genere viene eseguita in un server di telefonia (lo stesso server in cui il provider di servizi di telefonia è in esecuzione per i dispositivi line associati). Questa architettura, anziché l'architettura del provider di servizi WOSA, viene usata quando un particolare servizio viene implementato in modo più appropriato in un'applicazione rispetto a un driver nel server. Ad esempio, le funzioni di gestione dell'agente ACD vengono implementate in un gestore di richieste proxy anziché in un provider di servizi.

Il provider di servizi driver UNIMODEM per il controllo modem è disponibile nei sistemi operativi Windows Server 2003, Windows XP, Windows 2000 e Windows NT. Windows La telefonia include anche un mapper TSPI (Telephony Service Provider Interface) in modalità kernel generico, KMDDSP, che consente l'implementazione dei provider di servizi come driver di dispositivo in modalità kernel.

 

 
