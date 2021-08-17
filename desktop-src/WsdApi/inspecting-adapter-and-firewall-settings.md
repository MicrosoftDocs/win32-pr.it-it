---
description: Un firewall non configurato correttamente può causare errori nelle applicazioni WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Controllo degli adapter e dei firewall Impostazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ea14051ac65dbd0b749fa00566afc9ed82e5571f6027dafa003e12013888b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130783"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Controllo degli adapter e dei firewall Impostazioni

Un firewall non configurato correttamente può causare errori nelle applicazioni WSD. In questo argomento vengono descritte alcune procedure di risoluzione dei problemi da utilizzare quando i client e gli host WSD non possono vedersi reciprocmente in rete. Le impostazioni del firewall devono essere controllate prima di usare qualsiasi altra procedura di risoluzione dei problemi delle applicazioni.

**Per esaminare le impostazioni della scheda e del firewall**

1.  Verificare che **l'eccezione individuazione di** rete sia abilitata.
2.  Verificare che non siano presenti regole del firewall specifiche dell'applicazione che bloccano l'applicazione.
3.  Abilitare in modo esplicito le porte usate per l'individuazione e lo scambio di metadati.
4.  Disabilitare il firewall ed eseguire nuovamente il test dell'applicazione.
    > [!Note]  
    > Dopo aver completato questo passaggio, il firewall deve essere ri abilitato.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Verifica che l'eccezione di individuazione di rete sia abilitata

Se sono WS-Discovery applicazioni in esecuzione, è necessario consentire **l'eccezione** del firewall di individuazione di rete.

**Per abilitare l'eccezione del firewall di individuazione di rete**

1.  Fare **clic sul pulsante Start**, **scegliere** Esegui e quindi digitare **firewall.cpl**. Verrà aperta **l'Windows firewall Pannello di controllo** applet.
2.  Scegliere **Consenti un programma tramite Windows firewall.**
3.  Nella scheda **Eccezioni** selezionare la casella **di controllo Individuazione** di rete .
4.  Fare **clic su OK** per chiudere l'applet del firewall.

Ripetere il programma dopo aver apportato questa modifica al firewall. Se il programma ora funziona correttamente, la causa del problema è stata identificata e non sono necessari altri passaggi per la risoluzione dei problemi. In caso contrario, andare al passaggio successivo.

## <a name="checking-for-application-specific-firewall-rules"></a>Controllo delle regole del firewall specifiche dell'applicazione

La configurazione avanzata del firewall Windows può essere attivata in uno snap-in mmc (Microsoft Management Control) denominato **Windows Firewall con sicurezza avanzata**. Questo snap-in può essere utilizzato per risolvere i problemi del firewall sospetti.

Gli sviluppatori possono usare [Windows firewall](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) con API di sicurezza avanzata per creare regole del firewall che si applicano alle applicazioni WSD. In particolare, [**è possibile**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) usare il metodo Add [**dell'interfaccia INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) per aggiungere una nuova regola del firewall. Se le regole del firewall vengono create in modo non corretto, i client e gli host potrebbero non essere in grado di vedersi reciprocmente nella rete.

**Per verificare la presenza di regole del firewall specifiche dell'applicazione**

1.  Fare **clic sul pulsante Start**, **scegliere** Esegui e quindi **digitare wf.msc**.
2.  Cercare regole specifiche dell'applicazione che potrebbero bloccare il traffico. Per altre informazioni, vedere Firewall [Windows sicurezza avanzata - Strumenti di diagnostica e risoluzione dei problemi.](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink)
3.  Rimuovere le regole specifiche dell'applicazione.

Se non è stata trovata alcuna regola specifica dell'applicazione, andare al passaggio successivo. Se è stata trovata e rimossa una regola specifica dell'applicazione, ripetere il programma dopo aver apportato la modifica del firewall. Se il programma ora funziona correttamente, la causa del problema è stata identificata e non sono necessari altri passaggi per la risoluzione dei problemi. In caso contrario, andare al passaggio successivo.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Abilitazione delle porte usate per l'individuazione e lo scambio di metadati

WS-Discovery usa la porta UDP 3702 per lo scambio di messaggi. Inoltre, le porte TCP 5357 e 5358 vengono talvolta usate per lo scambio di metadati. Queste porte possono essere aperte in modo esplicito nel firewall usando le procedure descritte in [Aprire una porta nel firewall Windows.](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx)

Ripetere il programma dopo aver apportato questa modifica al firewall. Se il programma ora funziona correttamente, la causa del problema è stata identificata e non sono necessari altri passaggi per la risoluzione dei problemi. In caso contrario, andare al passaggio successivo.

## <a name="disabling-the-firewall"></a>Disabilitazione del firewall

Il Windows può essere disabilitato per facilitare la risoluzione di problemi sospetti. È anche possibile disattivare altri firewall applicabili, ad esempio il firewall in un router, per la risoluzione dei problemi. Per informazioni sull'abilitazione e la disabilitazione del firewall Windows, vedere Attivare o disattivare Windows [firewall.](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx)

Eseguire nuovamente il test dell'applicazione dopo aver disabilitato tutti i firewall applicabili. Se il programma ora funziona correttamente, il firewall blocca il traffico. Esistono alcune possibili cause del traffico bloccato.

-   Le eccezioni specifiche dell'applicazione bloccano il traffico. Verificare la presenza di regole del firewall specifiche dell'applicazione come descritto in precedenza.
-   Il dispositivo ha impiegato troppo tempo per rispondere alle richieste UDP. Il Windows firewall può bloccare le risposte UDP che restituiscono più di 4 secondi dopo l'invio della richiesta iniziale. Continuare la risoluzione dei problemi seguendo le procedure descritte in Uso di un host generico e di un client per [WS-Discovery UDP](using-a-generic-host-and-client-for-udp-ws-discovery.md) per verificare se il problema si riproduce con un host che risponde in meno di 4 secondi.

Se l'applicazione ha ancora esito negativo dopo la disabilitazione del firewall, il firewall non causa l'errore dell'applicazione. Abilitare nuovamente i firewall e continuare la risoluzione dei problemi seguendo le procedure descritte in Uso di un host generico e di un [client per UDP WS-Discovery.](using-a-generic-host-and-client-for-udp-ws-discovery.md)

I firewall devono essere sempre ri abilitati al termine della risoluzione dei problemi.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Attività iniziali risoluzione dei problemi relativi a WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
