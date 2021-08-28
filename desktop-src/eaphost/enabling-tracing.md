---
title: Abilitazione della traccia EAPHost
description: Può aiutare gli utenti a trovare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP. Le informazioni di debug possono includere le chiamate API eseguite, le chiamate di funzione interne eseguite e le transizioni di stato eseguite.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c638fa7f546028cd9cf66227cfe3c302d6599492d1cbbfcfdac6c2b428273db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086293"
---
# <a name="enabling-eaphost-tracing"></a>Abilitazione della traccia EAPHost

I log di traccia contenenti informazioni di debug possono aiutare gli utenti a individuare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP. Le informazioni di debug possono includere le chiamate API eseguite, le chiamate di funzione interne eseguite e le transizioni di stato eseguite.

La traccia può essere abilitata sia sul lato client che sul lato autenticatore. La traccia può essere abilitata anche per le chiamate alle API del servizio Routing e Accesso remoto [(RRAS).](/windows/desktop/RRAS/routing-start-page) Per altre informazioni, vedere [Tracing on the Routing and Remote Access Service](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> I log di traccia sono disponibili solo in inglese.

 

Quando la traccia EAPHost è abilitata, le informazioni di registrazione vengono archiviate in un file con estensione etl in un percorso specificato dall'utente. Se si verificano errori durante l'autenticazione EAP, la traccia genera un file con estensione etl che può essere inviato al Sviluppatore Microsoft per l'analisi della causa radice. I partner che hanno accesso a condivisioni di compilazione, simboli e file traceformat di Microsoft Windows possono convertire i file con estensione etl in un file di testo normale usando lo **strumento tracerpt.**

Gli errori del server dei criteri di rete non vengono acquisiti nei log EAPHost. Se si sta tentando di risolvere un errore di Server dei criteri di rete, visualizzare IASSAM. LOG e [IASNAP. File DI LOG.](https://go.microsoft.com/fwlink/p/?linkid=84108)

## <a name="tracing-on-the-client"></a>Traccia nel client

Per abilitare la traccia sul lato client:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **logman** **start trace** **EapHostPeer** **-o** **. \\ EapHostPeer.etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ets**
3.  Riprodurre lo scenario da tracciare.
4.  Eseguire il comando seguente: **logman** **stop** **EapHostPeer** **-ets**
5.  Convertire il file etl in testo usando il comando seguente: **tracerpt EapHostPeer.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Se non si ha accesso a tracerpt, evitare l'ultimo passaggio e inviare il file con estensione etl a Sviluppatore Microsoft support.

     

## <a name="tracing-on-the-authenticator"></a>Traccia sul Authenticator

Per abilitare la traccia sul lato autenticatore:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **logman** **start trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr.etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ets**
3.  Riprodurre lo scenario da tracciare.
4.  Eseguire il comando seguente: **logman** **stop** **EapHostAuthr** **-ets**
5.  Convertire il file etl in testo usando il comando seguente: **tracerpt EapHostAuthr.etl** **–pdb** **&lt; pdbpath &gt;** **-tp** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Se non si ha accesso a tracerpt, evitare l'ultimo passaggio e inviare invece il file con estensione etl a Sviluppatore Microsoft support.

     

## <a name="event-tracing"></a>Traccia eventi

In Windows 7 e versioni successive di Windows, EapHost fornisce la traccia basata su eventi sull'autenticatore e sul peer. Il vantaggio della traccia basata su eventi è che non sono necessari file di simboli per visualizzare i messaggi di traccia. Per abilitare la traccia eventi:

1.  Aprire **EventViewer.**
2.  I messaggi critici EapHost vengono registrati in: "Custom Views Administrative Events" (Eventi amministrativi \\ visualizzazioni personalizzate)
3.  I messaggi non critici vengono registrati in: "Applicazioni e servizi \\ Microsoft \\ Windows \\ EapHost
4.  I messaggi di evento di tipo "Analisi" e "Debug" possono essere visualizzati nello stesso percorso selezionando **Mostra** registri analitici e di debug dal **menu** visualizza nella barra del titolo.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Traccia nel servizio Routing e Accesso remoto

Per abilitare la traccia RRAS:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **netsh** **ras** **set** **tr** _ **\* *_* en**
3.  Aprire **la traccia %systemroot% \\** per visualizzare le tracce RAS

Per disabilitare la traccia di RRAS:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **netsh** **ras** **set** **tr** _ **\* *_* dis**

Per altre informazioni, vedere [Comandi Netsh.](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10))

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[Servizio Routing e Accesso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 