---
description: I log WinHTTP possono essere usati per risolvere i problemi delle applicazioni WSDAPI. Ciò è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS ha esito negativo.
ms.assetid: 75ba330d-afcd-4d8f-93c7-a1b9f80dd050
title: Acquisizione di log WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 648ebb95182096fc4a853c2685f896fa2902a828c8ed0ab143ce89c04831c7ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991781"
---
# <a name="capturing-winhttp-logs"></a>Acquisizione di log WinHTTP

[I log WinHTTP](/windows/desktop/WinHttp/winhttp-start-page) possono essere usati per risolvere i problemi delle applicazioni WSDAPI. Ciò è utile quando lo scambio di metadati ha esito negativo o quando la negoziazione SSL/TLS ha esito negativo.

Questa procedura illustra come acquisire i log WinHTTP nel PC client. L'applicazione client basata su WSDAPI non deve essere in esecuzione quando la registrazione è abilitata. Se l'applicazione client è in esecuzione quando la registrazione è abilitata, il client e/o il PC devono essere riavviati prima di WS-Discovery e il traffico di scambio dei metadati verrà visualizzato nei log WinHTTP.

**Per acquisire i log WinHTTP**

1.  Aprire una finestra del prompt dei comandi con privilegi elevati nel PC client.
2.  Eseguire il comando seguente: **netsh winhttp set tracing trace-file-prefix="C: \\ Temp \\ dpws" level=verbose format=ansi state=enabled max-trace-file-size=1073741824**

    Questo comando abilita la registrazione WinHTTP. Tutti i file di log verranno archiviati nella directory C: Temp e i nomi dei file inizieranno con il prefisso \\ dpws. Verranno archiviati al massimo 1 GB di file di log.

3.  Se il processo che usa WinHTTP nel client è già in esecuzione, riavviare il computer. Ad esempio, se [vengono](/previous-versions/windows/desktop/fundisc/fd-portal) usate le API di individuazione delle funzioni, il computer deve essere riavviato. Le API di individuazione delle funzioni chiamano WinHTTP dall'interno di un host del servizio, che potrebbe essere già stato avviato quando è stata abilitata la traccia.
4.  Avviare l'applicazione client basata su WSDAPI. È possibile usare l'applicazione in fase di debug o il client di debug WSD.
5.  Riprodurre l'errore dell'applicazione.
6.  Terminare l'applicazione client basata su WSDAPI.
7.  Se il processo che usa WinHTTP non viene terminato con l'applicazione client, riavviare il computer. Ad esempio, se [vengono](/previous-versions/windows/desktop/fundisc/fd-portal) usate le API di individuazione delle funzioni, il computer deve essere riavviato.
8.  Eseguire il comando seguente: **netsh winhttp set tracing state=disabled**

    Questo comando disabilita la registrazione WinHTTP.

9.  Esaminare i log DPWS in C: Temp e verificare che siano state inviate le \\ richieste e i messaggi necessari.
10. Se viene usata la comunicazione del canale sicuro (HTTPS), verificare la presenza di errori SSL/TLS.

Dopo aver acquisito i log WinHTTP, è possibile esaminare i log per cercare la causa di un errore dell'applicazione WSDAPI. Si noti che l'editor di testo usato per visualizzare questi log deve essere eseguito come amministratore. Per altre informazioni, vedere [Uso della registrazione WinHTTP per verificare il traffico.](using-winhttp-logging-to-verify-get-traffic.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[WinHTTP](/windows/desktop/WinHttp/winhttp-start-page)
</dt> <dt>

[Uso della registrazione WinHTTP per verificare il traffico](using-winhttp-logging-to-verify-get-traffic.md)
</dt>
</dl>
