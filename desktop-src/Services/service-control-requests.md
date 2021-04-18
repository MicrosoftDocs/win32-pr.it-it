---
description: Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la funzione ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Richieste di controllo del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6cb5edf56137e2c98ea7db440a4db5e55df5e8f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306533"
---
# <a name="service-control-requests"></a>Richieste di controllo del servizio

Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Questa funzione specifica un valore di controllo che viene passato alla funzione [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servizio specificato. Questo valore di controllo può essere un codice definito dall'utente o uno dei codici standard che consentono al programma chiamante di eseguire le azioni seguenti:

-   Arrestare un servizio (arresto del controllo del servizio \_ \_ ).
-   Sospendere un servizio ( \_ sospensione del controllo del servizio \_ ).
-   Riprendere l'esecuzione di un servizio sospeso (il \_ controllo del servizio \_ continua).
-   Recuperare le informazioni aggiornate sullo stato da un servizio ( \_ interrogazione del controllo del servizio \_ ).

Ogni servizio specifica i valori di controllo che accetteranno ed elaborano. Per determinare quali valori di controllo standard vengono accettati da un servizio, utilizzare la funzione [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o specificare il valore del controllo interrogare il controllo del servizio \_ \_ in una chiamata alla funzione [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) . Il membro **dwControlsAccepted** della struttura [**di \_ stato del servizio**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) restituito da queste funzioni indica se il servizio può essere arrestato, sospeso o ripreso. Tutti i servizi accettano il \_ \_ valore del controllo interrogare il controllo del servizio.

La funzione [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) segnala lo stato più recente per un servizio specificato, ma non ottiene uno stato aggiornato dal servizio stesso. L'utilizzo del \_ valore del controllo interrogare il controllo del servizio \_ in una chiamata a [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) garantisce che le informazioni sullo stato restituite siano correnti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un servizio con SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



