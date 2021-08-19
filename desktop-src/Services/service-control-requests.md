---
description: Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la funzione ControlService.
ms.assetid: d6cdc876-8b74-460e-ad43-6455ddf428dd
title: Richieste di controllo del servizio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4320aad28f8a176fbf4aaa6b51539256a376a01b8edea034341cae7831ca4c40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117967570"
---
# <a name="service-control-requests"></a>Richieste di controllo del servizio

Per inviare richieste di controllo a un servizio in esecuzione, un programma di controllo del servizio usa la [**funzione ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Questa funzione specifica un valore di controllo che viene passato alla [**funzione HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex) del servizio specificato. Questo valore di controllo può essere un codice definito dall'utente oppure può essere uno dei codici standard che consentono al programma chiamante di eseguire le azioni seguenti:

-   Arrestare un servizio (SERVICE \_ CONTROL \_ STOP).
-   Sospendere un servizio (SERVICE \_ CONTROL \_ PAUSE).
-   Riprendere l'esecuzione di un servizio in pausa (SERVICE \_ CONTROL \_ CONTINUE).
-   Recuperare informazioni aggiornate sullo stato da un servizio (CONTROLLO \_ DEL \_ SERVIZIO INTERROGAE).

Ogni servizio specifica i valori di controllo che accetterà ed ela processerà. Per determinare quali dei valori di controllo standard vengono accettati da un servizio, usare la [**funzione QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) o specificare il valore del controllo SERVICE CONTROL INTERROGAE in una chiamata alla \_ funzione \_ [**ControlService.**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice) Il **membro dwControlsAccepted** della struttura [**SERVICE \_ STATUS**](/windows/desktop/api/Winsvc/ns-winsvc-service_status) restituita da queste funzioni indica se il servizio può essere arrestato, sospeso o ripreso. Tutti i servizi accettano il valore \_ del controllo SERVICE CONTROL \_ INTERROGAE.

La [**funzione QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex) segnala lo stato più recente per un servizio specificato, ma non ottiene uno stato aggiornato dal servizio stesso. L'uso del valore del controllo SERVICE CONTROL INTERROGAE in una chiamata a ControlService garantisce che le \_ \_ informazioni sullo stato restituite siano aggiornate. [](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controllo di un servizio tramite SC](controlling-a-service-using-sc.md)
</dt> </dl>

 

 



