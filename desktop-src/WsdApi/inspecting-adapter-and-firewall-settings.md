---
description: Un firewall non configurato correttamente può causare errori nelle applicazioni WSD.
ms.assetid: eba61235-29b4-463a-b7c5-d34d3b39b095
title: Controllo delle impostazioni di adapter e firewall
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490909c9f3acdc3025e72350118f303bfdae73d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344876"
---
# <a name="inspecting-adapter-and-firewall-settings"></a>Controllo delle impostazioni di adapter e firewall

Un firewall non configurato correttamente può causare errori nelle applicazioni WSD. In questo argomento vengono fornite alcune procedure per la risoluzione dei problemi da utilizzare quando i client e gli host WSD non possono vedersi reciprocamente nella rete. Le impostazioni del firewall devono essere ispezionate prima di utilizzare qualsiasi altra procedura di risoluzione dei problemi dell'applicazione.

**Per esaminare le impostazioni dell'adapter e del firewall**

1.  Verificare che l'eccezione **individuazione di rete** sia abilitata.
2.  Verificare che non siano presenti regole firewall specifiche per l'applicazione che bloccano l'applicazione.
3.  Abilitare in modo esplicito le porte utilizzate per l'individuazione e lo scambio di metadati.
4.  Disabilitare il firewall e rieseguire il test dell'applicazione.
    > [!Note]  
    > Dopo aver completato questo passaggio, è necessario abilitare nuovamente il firewall.

     

## <a name="verifying-that-the-network-discovery-exception-is-enabled"></a>Verifica per verificare se l'eccezione di individuazione della rete è abilitata

Se è in esecuzione un'applicazione WS-Discovery, è necessario consentire l'eccezione del firewall di **individuazione della rete** .

**Per abilitare l'eccezione del firewall di individuazione della rete**

1.  Fare clic sul pulsante **Start**, scegliere **Esegui**, quindi digitare **firewall.cpl**. Verrà visualizzata l'applet del **Pannello di controllo Windows Firewall** .
2.  Scegliere **Consenti programma tramite Windows Firewall**.
3.  Nella scheda **eccezioni** selezionare la casella di controllo **individuazione di rete** .
4.  Fare clic su **OK** per chiudere l'applet del firewall.

Eseguire nuovamente il test del programma dopo aver modificato il firewall. Se il programma funziona correttamente, è stata identificata la causa del problema e non è necessario eseguire ulteriori passaggi per la risoluzione dei problemi. In caso contrario, passare al passaggio successivo.

## <a name="checking-for-application-specific-firewall-rules"></a>Verifica delle regole del firewall specifiche dell'applicazione

La configurazione avanzata del Windows Firewall può essere eseguita in uno snap-in di Microsoft Management Control (MMC) denominato **Windows Firewall con sicurezza avanzata**. Questo snap-in può essere utilizzato per risolvere i problemi sospetti del firewall.

Gli sviluppatori possono usare le API di [sicurezza avanzata di Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-with-advanced-security-reference) per creare regole del firewall che si applicano alle applicazioni WSD. In particolare, è possibile usare il metodo [**Add**](/previous-versions/windows/desktop/api/netfw/nf-netfw-inetfwrules-add) dell'interfaccia [**INetFwRules**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwrules) per aggiungere una nuova regola del firewall. Se le regole del firewall non sono state create correttamente, i client e gli host potrebbero non essere in grado di vedere reciprocamente la rete.

**Per verificare le regole del firewall specifiche dell'applicazione**

1.  Fare clic sul pulsante **Start**, scegliere **Esegui**, quindi digitare **WF. msc**.
2.  Cercare regole specifiche dell'applicazione che potrebbero bloccare il traffico. Per ulteriori informazioni, vedere [Windows Firewall con sicurezza avanzata-diagnostica e strumenti per la risoluzione dei problemi](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc722062(v=ws.10)?ocid=fwlink).
3.  Rimuovere le regole specifiche dell'applicazione.

Se non sono state trovate regole specifiche dell'applicazione, procedere al passaggio successivo. Se è stata rilevata e rimossa una regola specifica dell'applicazione, testare nuovamente il programma dopo aver modificato il firewall. Se il programma funziona correttamente, è stata identificata la causa del problema e non è necessario eseguire ulteriori passaggi per la risoluzione dei problemi. In caso contrario, passare al passaggio successivo.

## <a name="enabling-the-ports-used-for-discovery-and-metadata-exchange"></a>Abilitazione delle porte utilizzate per l'individuazione e lo scambio di metadati

WS-Discovery utilizza la porta UDP 3702 per lo scambio di messaggi. Inoltre, le porte TCP 5357 e 5358 vengono talvolta utilizzate per lo scambio di metadati. Queste porte possono essere aperte in modo esplicito sul firewall usando le procedure descritte in [aprire una porta in Windows Firewall](https://windowshelp.microsoft.com/Windows/Help/4da18300-9044-47b6-9038-595c78db81ab1033.mspx).

Eseguire nuovamente il test del programma dopo aver modificato il firewall. Se il programma funziona correttamente, è stata identificata la causa del problema e non è necessario eseguire ulteriori passaggi per la risoluzione dei problemi. In caso contrario, passare al passaggio successivo.

## <a name="disabling-the-firewall"></a>Disabilitazione del firewall

Il Windows Firewall può essere disabilitato per risolvere i problemi sospetti. Altri firewall applicabili, ad esempio il firewall in un router, possono essere disabilitati anche per la risoluzione dei problemi. Per informazioni sull'abilitazione e la disabilitazione dell'Windows Firewall, vedere [attivare o disattivare l'Windows Firewall](https://windowshelp.microsoft.com/Windows/Help/bfe523a9-7eec-4d3f-add1-2f68b9cfa1c01033.mspx).

Eseguire nuovamente il test dell'applicazione dopo aver disattivato eventuali firewall applicabili. Se il programma ora funziona correttamente, il firewall blocca il traffico. Esistono alcune possibili cause di traffico bloccato.

-   Le eccezioni specifiche dell'applicazione hanno bloccato il traffico. Verificare la presenza di regole firewall specifiche per l'applicazione, come descritto in precedenza.
-   Il dispositivo ha impiegato troppo tempo per rispondere alle richieste UDP. Il Windows Firewall può bloccare le risposte UDP che restituiscono più di 4 secondi dopo l'invio della richiesta iniziale. Continuare la risoluzione dei problemi attenendosi alle procedure descritte in [utilizzo di un host e di un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md) per verificare se il problema si riproduce con un host che risponde in meno di 4 secondi.

Se l'applicazione non riesce ancora dopo la disabilitazione del firewall, il firewall non causa l'errore dell'applicazione. Riabilitare i firewall e continuare la risoluzione dei problemi attenendosi alle procedure fornite in [utilizzo di un host e un client generici per UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).

Al termine della risoluzione dei problemi, i firewall devono essere sempre riabilitati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Procedure di diagnostica WSDAPI](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[Introduzione con la risoluzione dei problemi di WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 
