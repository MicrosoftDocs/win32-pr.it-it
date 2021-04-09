---
title: Abilitazione della traccia EAPHost
description: Può aiutare gli utenti a individuare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP. Le informazioni di debug possono includere chiamate API eseguite, chiamate di funzione interne eseguite e transizioni di stato eseguite.
ms.assetid: 5f401101-59aa-4ee8-825a-0b998489eed9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fdee8a5516b218e51f0151e1964885789560d82
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/18/2020
ms.locfileid: "104047636"
---
# <a name="enabling-eaphost-tracing"></a>Abilitazione della traccia EAPHost

I log di traccia contenenti informazioni di debug possono aiutare gli utenti a individuare le cause principali dei problemi che si verificano durante il processo di autenticazione EAP. Le informazioni di debug possono includere chiamate API eseguite, chiamate di funzione interne eseguite e transizioni di stato eseguite.

La traccia può essere abilitata sia sul lato client sia sul lato Authenticator. La traccia può essere abilitata anche per le chiamate alle API del [servizio Routing e accesso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page) . Per ulteriori informazioni, vedere [la pagina relativa alla traccia nel servizio Routing e accesso remoto](#tracing-on-the-routing-and-remote-access-service).

> [!Note]  
> I log di traccia sono disponibili solo in lingua inglese.

 

Quando è abilitata la traccia EAPHost, le informazioni di registrazione vengono archiviate in un file con estensione ETL in un percorso specificato dall'utente. Se si verificano errori durante l'autenticazione EAP, la traccia genera un file con estensione ETL che può essere inviato a Microsoft supporto tecnico Developer per l'analisi della causa radice. I partner che hanno accesso ai file di Microsoft Windows Build shares, symbols e TraceFormat possono convertire i file con estensione ETL in un file di testo normale usando lo strumento **tracerpt** .

Gli errori del server dei criteri di rete non vengono acquisiti nei log EAPHost. Se si sta tentando di risolvere un errore di NPS, visualizzare il IASSAM. LOG e [IASNAP. ](https://go.microsoft.com/fwlink/p/?linkid=84108) File di log.

## <a name="tracing-on-the-client"></a>Traccia nel client

Per abilitare la traccia sul lato client:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **logman** **Start Trace** **EapHostPeer** **-o** **. \\ EapHostPeer. etl** **-p** **{5F31090B-D990-4e91-B16D-46121D0255AA} 0x4000ffff 0** **-ETS**
3.  Riprodurre lo scenario che si desidera tracciare.
4.  Eseguire il comando seguente: **logman** **Stop** **EapHostPeer** **-ETS**
5.  Convertire il file ETL in testo usando il comando seguente: **tracerpt EapHostPeer. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostPeer.txt**
    > [!Note]  
    > Se non si dispone dell'accesso allo strumento tracerpt, evitare l'ultimo passaggio e inviare il file con estensione ETL a Microsoft supporto tecnico Developer.

     

## <a name="tracing-on-the-authenticator"></a>Traccia nell'autenticatore

Per abilitare la traccia sul lato Authenticator:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **logman** **Start Trace** **EapHostAuthr** **-o** **. \\ EapHostAuthr. etl** **-p** **{F6578502-DF4E-4a67-9661-E3A2F05D1D9B} 0x4000ffff 0** **-ETS**
3.  Riprodurre lo scenario che si desidera tracciare.
4.  Eseguire il comando seguente: **logman** **Stop** **EapHostAuthr** **-ETS**
5.  Convertire il file ETL in testo usando il comando seguente: **tracerpt EapHostAuthr. etl** **– PDB** **&lt; PDBPATH &gt;** **-TP** **&lt; tracemessagefilesdirectorypath &gt;** **-o** **EapHostAuthr.txt**
    > [!Note]  
    > Se non si dispone dell'accesso allo strumento tracerpt, evitare l'ultimo passaggio e inviare invece il file con estensione ETL a Microsoft supporto tecnico Developer.

     

## <a name="event-tracing"></a>Traccia eventi

In Windows 7 e nelle versioni successive di Windows, EapHost fornisce la traccia basata su eventi per l'autenticatore e il peer. Il vantaggio della traccia basata su eventi è che non sono necessari file di simboli per visualizzare i messaggi di traccia. Per abilitare la traccia eventi:

1.  Aprire **eventviewer**.
2.  Messaggi EapHost critici registrati in: "visualizzazioni personalizzate \\ eventi amministrativi"
3.  Messaggi non critici registrati in: "applicazioni e servizi \\ Microsoft \\ Windows \\ EAPHost
4.  I messaggi di evento di tipo "analitico" e "debug" possono essere visualizzati nello stesso percorso selezionando **Mostra log analitici e di debug** dal menu **Visualizza** della barra del titolo.

## <a name="tracing-on-the-routing-and-remote-access-service"></a>Traccia nel servizio Routing e accesso remoto

Per abilitare la traccia RRAS:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **netsh** **RAS** **set** **TR** **\* *_ _* en**
3.  Aprire **% systemroot% \\ Tracing** per visualizzare le tracce RAS

Per disabilitare la traccia RRAS:

1.  Aprire una finestra del prompt dei comandi con privilegi elevati.
2.  Eseguire il comando seguente: **netsh** **RAS** **set** **TR** **\* *_ _* dis**

Per ulteriori informazioni, vedere [comandi netsh](/previous-versions/windows/it-pro/windows-server-2003/cc779693(v=ws.10)).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Uso di EAPHost](using-eap-host.md)
</dt> <dt>

[Servizio Routing e Accesso remoto (RRAS)](/windows/desktop/RRAS/routing-start-page)
</dt> </dl>

 

 