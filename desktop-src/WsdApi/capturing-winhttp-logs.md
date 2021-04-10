---
description: I log WinHTTP possono essere usati per risolvere i problemi delle applicazioni WSDAPI. Questa operazione è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS non riesce.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Acquisizione dei log WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378801e97b2eef8c1ea0c40a5973844d75a94e02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131143"
---
# <a name="capturing-winhttp-logs"></a>Acquisizione dei log WinHTTP

I log [WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) possono essere usati per risolvere i problemi delle applicazioni wsdapi. Questa operazione è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS non riesce.

Questa procedura illustra come acquisire i log WinHTTP nel computer client. Quando è abilitata la registrazione, l'applicazione client basata su WSDAPI non deve essere in esecuzione. Se l'applicazione client è in esecuzione quando la registrazione è abilitata, il client e/o il PC devono essere riavviati prima che WS-Discovery e il traffico di scambio dei metadati venga visualizzato nei log WinHTTP.

**Per acquisire i log WinHTTP**

1.  Aprire una finestra del prompt dei comandi con privilegi elevati nel computer client.
2.  Eseguire il comando seguente: **netsh winhttp set tracing trace-file-prefix = "C: \\ temp \\ DPWS" level = verbose Format = ANSI state = enabled max-trace-file-size = 1073741824**

    Questo comando Abilita la registrazione WinHTTP. Tutti i file di log verranno archiviati nella directory C: \\ Temp e i nomi file inizieranno con il prefisso DPWS. Verranno archiviati al massimo 1 GB di file di log.

3.  Se il processo che usa WinHTTP sul client è già in esecuzione, riavviare il computer. Se, ad esempio, vengono utilizzate le API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) , è necessario riavviare il computer. Le API di individuazione della funzione chiamano WinHTTP dall'interno di un host del servizio, che potrebbe essere già stato avviato quando è stata abilitata la traccia.
4.  Avviare l'applicazione client basata su WSDAPI. L'applicazione di cui è in corso il debug o il client di debug WSD può essere utilizzato.
5.  Riprodurre l'errore dell'applicazione.
6.  Terminare l'applicazione client basata su WSDAPI.
7.  Se il processo che usa WinHTTP non viene terminato con l'applicazione client, riavviare il computer. Se, ad esempio, vengono utilizzate le API di [individuazione delle funzioni](/previous-versions/windows/desktop/fundisc/fd-portal) , è necessario riavviare il computer.
8.  Eseguire il comando seguente: **netsh winhttp set tracing state = disabled**

    Questo comando Disabilita la registrazione WinHTTP.

9.  Esaminare i registri di DPWS in C: \\ Temp e verificare che le richieste e i messaggi richiesti siano stati inviati.
10. Se è in uso la comunicazione del canale sicuro (HTTPS), verificare la presenza di errori SSL/TLS.

Dopo l'acquisizione dei log WinHTTP, è possibile esaminare i log per cercare la cause di un errore dell'applicazione WSDAPI. Si noti che l'editor di testo utilizzato per visualizzare questi log deve essere eseguito come amministratore. Per altre informazioni, vedere [uso della registrazione WinHTTP per verificare il traffico](using-winhttp-logging-to-verify-get-traffic.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Uso della registrazione WinHTTP per verificare il traffico Get](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
