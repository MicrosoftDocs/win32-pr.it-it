---
title: Uso di Netsh per gestire le tracce
description: In Windows 7, netsh.exe può essere utilizzato da un prompt dei comandi per abilitare e configurare le tracce di rete. In questa sezione vengono descritti alcuni dei comandi netsh.exe che consentono di risolvere i problemi di traccia, inclusa la nuova funzionalità di traccia Netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1978345da984ac90699b5355b36af18b9b285d5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396122"
---
# <a name="using-netsh-to-manage-traces"></a>Uso di Netsh per gestire le tracce

In Windows 7, netsh.exe può essere utilizzato da un prompt dei comandi per abilitare e configurare le tracce di rete. In questa sezione vengono descritti alcuni dei comandi netsh.exe che consentono di risolvere i problemi di traccia, inclusa la nuova funzionalità di **traccia Netsh** . Si noti che i comandi netsh devono essere eseguiti da un prompt dei comandi con privilegi elevati.

## <a name="collecting-traces"></a>Raccolta di tracce

Gli scenari sono set predefiniti di provider di traccia che possono essere abilitati per la risoluzione dei problemi. Per visualizzare l'elenco degli scenari correlati alla rete disponibili, digitare **netsh trace show Scenarios** (**netsh trace show providers** elenca tutti i provider disponibili, inclusi quelli che non sono rilevanti per la rete).

Quando è stato identificato uno scenario rilevante per i problemi, è possibile visualizzare un elenco di tutti i provider inclusi in tale scenario. Ad esempio, per visualizzare tutti i provider abilitati nello scenario InternetClient, digitare **netsh trace show scenario InternetClient**.

È possibile avviare una traccia per tutti i provider in uno scenario o in un set di scenari specifico. Ad esempio, per avviare una traccia per tutti i provider abilitati nello scenario InternetClient, digitare **netsh trace start scenario = InternetClient**. Per acquisire i provider per più di uno scenario, è possibile specificare tutti gli scenari appropriati, ad esempio lo **scenario di avvio della traccia Netsh = scenario filesharing = DirectAccess**. Si noti che è possibile abilitare una sola sessione di traccia alla volta. non è possibile acquisire contemporaneamente le informazioni di traccia da diversi set di provider in file distinti.

È inoltre possibile avviare una traccia per i provider aggiuntivi non inclusi in tale scenario specifico. Ad esempio, potrebbe essere necessario avviare le tracce per tutti i provider abilitati nello scenario WLAN e anche il provider DHCP. A tale scopo, digitare **netsh trace start scenario = WLAN provider = Microsoft-Windows-DHCP-client**.

È anche possibile visualizzare altri dettagli su un provider specifico digitando **netsh trace show provider** seguito dal nome del provider.

Per visualizzare tutte le opzioni e i filtri disponibili, è possibile digitare **netsh trace start/?**.

Per arrestare la traccia, digitare **netsh trace stop**.

## <a name="using-the-output-files"></a>Uso dei file di output

Quando la traccia viene arrestata, per impostazione predefinita vengono generati due file: un file di log di traccia eventi (ETL) e un file con estensione cab.

Gli eventi di traccia vengono raccolti nel file ETL, che possono essere visualizzati tramite strumenti come Network Monitor. Per impostazione predefinita, il file ETL verrà denominato NetTrace. etl oppure è possibile specificare un nome diverso includendo **TRACEFILE = filename. etl** all'avvio della traccia.

Il file con estensione cab contiene informazioni dettagliate sul software e sull'hardware del sistema, ad esempio le informazioni sull'adapter, la compilazione, il sistema operativo e le impostazioni wireless. Il file con estensione cab verrà denominato nettrace.cab per impostazione predefinita, a meno che non sia stato specificato un altro nome come indicato in precedenza.

Il file con estensione cab conterrà due file, che avranno sempre lo stesso nome. Report. etl è un'altra copia delle stesse informazioni incluse in NetTrace. etl. Il file report.html include informazioni aggiuntive sugli eventi di traccia e le altre informazioni raccolte. Per ricevere la maggior parte dei dettagli disponibili, includere il comando **report = yes** all'avvio di una traccia.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Utilizzo dei filtri per ridurre la quantità di dati nel file di traccia ETL

Quando le acquisizioni si verificano in un lungo periodo di tempo, il file di traccia ETL può diventare molto grande. Negli scenari in cui sono abilitati più provider, con conseguente traffico elevato, i vincoli del buffer ETW possono causare l'eliminazione di alcune tracce. A parte questa considerazione, la riduzione della quantità di dati nel file di traccia ETL può semplificare la risoluzione dei problemi riducendo la quantità di dati da rivedere.

I filtri di traccia Netsh possono essere utilizzati per ridurre le dimensioni del file di traccia ETL. Questi filtri di traccia sono livelli ETW e parole chiave che possono essere applicati a singoli provider.

Per visualizzare un elenco di filtri che è possibile applicare, digitare **netsh trace start/?**

Un esempio di filtro è **netsh trace start internetClient provider = Microsoft-Windows-TCPIP Level = 5 Keywords = UT: ReceivePath, UT: SendPath**.

In questo esempio, il livello è impostato su 5, il che significa che verrà visualizzato il numero massimo di eventi. Nella tabella seguente sono illustrate le impostazioni disponibili:



|       |               |                                                                            |
|-------|---------------|----------------------------------------------------------------------------|
| Level | Impostazione       | Descrizione                                                                |
| 1     | Critico      | Verranno visualizzati solo gli eventi critici.                                        |
| 2     | Errors        | Verranno visualizzati gli errori e gli eventi critici.                                  |
| 3     | Avvisi      | Verranno visualizzati gli eventi, gli errori e gli avvisi critici.                       |
| 4     | Informativo | Verranno visualizzati gli eventi critici, gli errori, gli avvisi e gli eventi informativi. |
| 5     | Dettagliato       | Verranno visualizzati tutti gli eventi.                                                  |



 

Le parole chiave **UT: ReceivePath** e **UT: SentPath** filtrano gli eventi in modo da visualizzare solo gli eventi tracciati nel percorso di ricezione o di trasmissione. È possibile trovare un elenco completo di parole chiave per un provider specifico digitando **netsh trace show provider** seguito dal nome del provider. Se, ad esempio, si digita **netsh trace show provider Microsoft-Windows-TCPIP** , vengono visualizzate informazioni sul provider Microsoft-Windows-Tcpip, incluso un elenco di parole chiave.

Netsh supporta inoltre la funzionalità di filtro dei pacchetti (simile a Network Monitor) quando l'acquisizione di pacchetti è attivata (impostando **capture = yes**). Il filtro dei pacchetti può essere utilizzato per acquisire un numero limitato di pacchetti in un file di traccia. Ad esempio, **netsh trace Start Capture = Yes IPv4. Address = = x.x.** x. x, dove x. x. x. x è l'indirizzo IP, acquisisce solo i pacchetti con traffico IPv4 con tale indirizzo di origine o di destinazione specifico.

Per ulteriori informazioni sull'utilizzo del filtro pacchetti, è possibile digitare **netsh trace show capturefilterHelp**.

 

 




