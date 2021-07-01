---
title: Uso di Netsh per gestire le tracce
description: In Windows 7 è netsh.exe da un prompt dei comandi per abilitare e configurare le tracce di rete. In questa sezione vengono descritti alcuni dei comandi netsh.exe che consentono di risolvere i problemi di traccia, inclusa la nuova funzionalità di traccia netsh.
ms.assetid: f0f0fc7b-7cfa-43c7-89a3-3b80050875f8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c1cf869f60b69e227e78e19e8e05d3765ddb67d
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119026"
---
# <a name="using-netsh-to-manage-traces"></a>Uso di Netsh per gestire le tracce

In Windows 7 è netsh.exe da un prompt dei comandi per abilitare e configurare le tracce di rete. In questa sezione vengono descritti alcuni dei comandi netsh.exe che consentono di risolvere i problemi di traccia, inclusa la nuova **funzionalità di traccia netsh.** Si noti che i comandi netsh devono essere eseguiti da un prompt dei comandi con privilegi elevati.

## <a name="collecting-traces"></a>Raccolta di tracce

Gli scenari sono set predefiniti di provider di traccia che possono essere abilitati per la risoluzione dei problemi. Per visualizzare l'elenco degli scenari correlati alla rete disponibili, digitare **netsh trace show scenarios** (**netsh trace show providers** elenca tutti i provider disponibili, inclusi quelli non rilevanti per la rete).

Dopo aver identificato uno scenario rilevante per i problemi, è possibile visualizzare un elenco di tutti i provider inclusi in tale scenario. Ad esempio, per visualizzare tutti i provider abilitati nello scenario InternetClient, digitare **netsh trace show scenario internetclient**.

È possibile avviare una traccia per tutti i provider in un determinato scenario o set di scenari. Ad esempio, per avviare una traccia per tutti i provider abilitati nello scenario InternetClient, digitare **netsh trace start scenario=internetclient**. Per acquisire i provider per più di uno scenario, è possibile specificare tutti gli scenari appropriati, ad esempio **netsh trace start scenario=FileSharing scenario=DirectAccess.** Si noti che è possibile attivare una sola sessione di traccia alla volta. Non è possibile acquisire simultaneamente informazioni di traccia da set diversi di provider in file separati.

È anche possibile avviare una traccia per provider aggiuntivi non inclusi in tale scenario specifico. Ad esempio, potrebbe essere necessario avviare tracce per tutti i provider abilitati nello scenario WLAN e anche per il provider DHCP. A tale scopo, digitare **netsh trace start scenario=wlan provider=Microsoft-Windows-Dhcp-Client**.

È anche possibile visualizzare altri dettagli su un provider specifico digitando **netsh trace show provider** seguito dal nome del provider.

Per visualizzare tutte le opzioni e i filtri disponibili, è possibile digitare **netsh trace start /?**.

Per arrestare la traccia, digitare **netsh trace stop**.

## <a name="using-the-output-files"></a>Uso dei file di output

Quando la traccia viene arrestata, per impostazione predefinita vengono generati due file: un file di log di traccia eventi (ETL) e .cab file.

Gli eventi di traccia vengono raccolti nel file ETL, che può essere visualizzato usando strumenti come Network Monitor. Il file ETL verrà denominato nettrace.etl per impostazione predefinita oppure è possibile specificare un nome diverso includendo **tracefile=filename.etl** all'avvio della traccia.

Il file .cab contiene informazioni dettagliate sul software e sull'hardware nel sistema, ad esempio le informazioni sulla scheda, la build, il sistema operativo e le impostazioni wireless. Il .cab file verrà denominato nettrace.cab per impostazione predefinita, a meno che non sia stato specificato un altro nome come indicato in precedenza.

Questo .cab file conterrà due file, che avranno sempre lo stesso nome. Report.etl è un'altra copia delle stesse informazioni incluse in nettrace.etl. Il file report.html include informazioni aggiuntive sugli eventi di traccia e sulle altre informazioni raccolte. Per ricevere la maggior parte dei dettagli disponibili, includere il **comando report = yes all'avvio** di una traccia.

## <a name="using-filters-to-reduce-the-amount-of-data-in-the-etl-trace-file"></a>Uso di filtri per ridurre la quantità di dati nel file di traccia ETL

Quando le acquisizioni avvengono per un lungo periodo di tempo, il file di traccia ETL può diventare molto grande. Negli scenari in cui sono abilitati più provider, con conseguente traffico elevato, i vincoli del buffer ETW possono causare l'uscita di alcune tracce. A parte questa considerazione, la riduzione della quantità di dati nel file di traccia ETL può semplificare la risoluzione dei problemi riducendo la quantità di dati da esaminare.

I filtri di traccia Netsh possono essere usati per ridurre le dimensioni del file di traccia ETL. Questi filtri di traccia sono parole chiave e livelli ETW che possono essere applicati ai singoli provider.

Per visualizzare un elenco di filtri che è possibile applicare, digitare **netsh trace start /?**

Un esempio di filtro è **netsh trace start InternetClient provider=Microsoft-Windows-TCPIP level=5 keywords=ut:ReceivePath,ut:SendPath**.

In questo esempio il livello è impostato su 5, il che significa che verrà visualizzato il numero massimo di eventi. La tabella seguente illustra le impostazioni disponibili:



| Level      | Impostazione              | Descrizione                                                                           |
|-------|---------------|----------------------------------------------------------------------------|
| 1     | Critico      | Verranno visualizzati solo gli eventi critici.                                        |
| 2     | Errors        | Verranno visualizzati gli errori e gli eventi critici.                                  |
| 3     | Avvisi      | Verranno visualizzati eventi critici, errori e avvisi.                       |
| 4     | Informativa | Verranno visualizzati eventi critici, errori, avvisi ed eventi in informazioni. |
| 5     | Dettagliato       | Verranno visualizzati tutti gli eventi.                                                  |



 

Le parole **chiave ut:ReceivePath** e **ut:SentPath** filtrano gli eventi in modo da visualizzare solo gli eventi tracciati nel percorso di ricezione o invio. È possibile trovare un elenco completo di parole chiave per un provider specifico digitando **netsh trace show provider** seguito dal nome del provider. Ad esempio, **digitando netsh trace show provider Microsoft-Windows-TCPIP** verranno visualizzate informazioni sul provider Microsoft-Windows-TCPIP, incluso un elenco di parole chiave.

Netsh supporta anche la funzionalità di filtro dei pacchetti (simile a Network Monitor) quando l'acquisizione di pacchetti è attivata (impostando **capture = yes).** Il filtro dei pacchetti può essere usato per acquisire un numero limitato di pacchetti in un file di traccia. Ad esempio, **netsh trace start capture = yes ipv4.address == x.x.x.x** , dove x.x.x.x è l'indirizzo IP, acquisisce solo i pacchetti con traffico ipv4 con l'indirizzo di origine o di destinazione specifico.

Per altre informazioni su come usare il filtro dei pacchetti, è possibile digitare **netsh trace show capturefilterHelp**.

 

 




