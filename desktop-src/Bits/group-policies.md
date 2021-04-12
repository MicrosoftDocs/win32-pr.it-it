---
title: Criteri di gruppo
description: Servizio trasferimento intelligente in background (BITS) USA i criteri di gruppo seguenti per configurare le impostazioni e i trasferimenti BITS. Per ulteriori informazioni sulla versione di bit utilizzata dalle diverse versioni di Windows, vedere l'argomento novità.
ms.assetid: 32c7e2b1-bac2-4708-a30c-f6b2a816c1a4
ms.topic: article
ms.date: 10/04/2018
ms.openlocfilehash: f3ff0070c489759055bdaae1d2e68d8718a7bae5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104220978"
---
# <a name="group-policies"></a>Criteri di gruppo

> [!NOTE]
> Per informazioni dettagliate su come usare la gestione di dispositivi mobili (MDM) per impostare i criteri per Servizio trasferimento intelligente in background (BITS), vedere [criteri CSP](/windows/client-management/mdm/policy-configuration-service-provider).

Servizio trasferimento intelligente in background (BITS) USA i criteri di gruppo seguenti per configurare le impostazioni e i trasferimenti BITS. Per ulteriori informazioni sulla versione di bit utilizzata dalle diverse versioni di Windows, vedere [l'argomento Novità](what-s-new.md) .

> [!NOTE]  
> Se il valore dei criteri non è impostato, BITS utilizzerà il valore predefinito del criterio.

**Per abilitare un criterio BITS**

1.  Per aprire Criteri di gruppo, immettere **gpedit. msc/gpcomputer: "***nomecomputer***"** nella finestra **Esegui** o al prompt dei comandi in una finestra di comando.
2.  I criteri BITS si trovano in **Configurazione computer**, **Modelli amministrativi**, **rete** **servizio trasferimento intelligente in background**.
3.  Fare clic con il pulsante destro del mouse sul criterio e scegliere **modifica**.
4.  Seguire le istruzioni per l'abilitazione e l'impostazione del criterio.

I criteri di gruppo per BITS si trovano nel registro di sistema in **HKEY \_ Local \_ Machine** \\ **software** \\ **Policies** \\ **Microsoft** \\ **Windows** \\ **bits**. Si noti che nel registro di sistema sono elencati solo i criteri configurati.

|Criteri|Descrizione|
|-|-|
|JobInactivityTimeout<br/>BITS 1,0|Per impostazione predefinita, BITS mantiene le informazioni su un processo per 90 giorni. Se non è presente alcuna attività per il processo per questo periodo di tempo, BITS Annulla il processo. Lo stato del trasferimento o le modifiche delle proprietà reimpostano il timer.<br/> Potrebbe essere necessario modificare questo criterio se l'utente non esegue l'accesso o non gestisce una connessione di rete per lunghi periodi di tempo.|
|MaxInternetBandwidth<br/>BITS 2,0|Limita la larghezza di banda di rete utilizzata dai bit per i trasferimenti in background (questo criterio non influisce sui trasferimenti in primo piano).<br/>Specificare un limite da usare durante un intervallo di tempo specifico e un limite da usare in tutti gli altri momenti. Limitare, ad esempio, l'uso della larghezza di banda di rete a 10 kilobit al secondo (Kbps) dalle 8:00 A.M. alle 5:00 e usano tutta la larghezza di banda non usata disponibile nel resto del tempo.<br/>**Nota**: la modifica del clock di sistema non influisce sull'intervallo di tempo di limitazione della larghezza di banda. Ad esempio, se l'ora corrente è 2:00. e l'intervallo di limitazione della larghezza di banda inizia alle 3:00, mentre lo stato di avanzamento del clock di sistema non significa che BITS imporrà la limitazione della larghezza di banda un'ora prima che il limite di larghezza di banda venga comunque eseguito in un'ora. Per riflettere la modifica del clock di sistema in bit, è necessario riavviare il computer o il servizio BITS.<br/>Specificare il limite in kilobit al secondo. Basare il limite sulle dimensioni del collegamento di rete, non sulle dimensioni della scheda di interfaccia di rete (NIC) del computer. BITS utilizza circa due kilobit se si specifica un valore minore di due kilobit. Per evitare che si verifichino trasferimenti BITS, specificare un limite di zero. Se si specifica un limite di zero, BITS inserisce tutti i processi in background in uno stato di errore temporaneo. Il codice di errore è impostato su BG_E_BLOCKED_BY_POLICY. BITS inserisce i processi nello stato in coda dopo la scadenza dell'intervallo di tempo.<br/> Se si disattiva o non si configura questo criterio, BITS utilizzerà tutta la larghezza di banda inutilizzata disponibile.<br/> Questo criterio viene in genere usato per impedire che i trasferimenti BITS si conpetano per la larghezza di banda di rete quando il client dispone di una scheda di rete veloce (10 Mbps) ma è connessa alla rete tramite un collegamento lento (56 Kbps).<br/> Per informazioni su come BITS usa la larghezza di banda di rete, vedere [larghezza di banda di rete](network-bandwidth.md).|
|MaxDownloadTime<br/>BITS 3,0|Determina il periodo di tempo durante il quale i bit possono trascorrere attivamente il trasferimento dei file nel processo. Il valore predefinito è 90 giorni.<br/> Per eseguire l'override di questo criterio per un processo specifico, chiamare il metodo [**IBackgroundCopyJob4:: SetMaximumDownloadTime**](/windows/desktop/api/bits3_0/nf-bits3_0-ibackgroundcopyjob4-setmaximumdownloadtime) .|
|MaxJobsPerMachine<br/>BITS 3,0|Limita il numero di processi che gli utenti possono creare nel computer. Il valore predefinito è 300 processi. Questo criterio non è applicabile a un utente con privilegi di amministratore o account del servizio.|
|MaxJobsPerUser<br/>BITS 3,0|Limita il numero di processi che un utente può creare nel computer. Il valore predefinito è 60 processi per utente. Questo criterio non è applicabile a un utente con privilegi di amministratore o account del servizio.|
|MaxFilesPerJob<br/>BITS 3,0|Limita il numero di file che un utente può aggiungere a un processo. Il valore predefinito è 200 file per processo. Questo criterio non è applicabile a un utente con privilegi di amministratore o account del servizio.|
|MaxRangesPerFile<br/>BITS 3,0|Limita il numero di intervalli che un utente può specificare per un file. Il valore predefinito è 500 intervalli. Questo criterio non è applicabile a un utente con privilegi di amministratore o account del servizio.|

BITS usa i criteri di gruppo seguenti per abilitare e configurare il modo in cui BITS interagisce con BranchCache.

|Criteri|Descrizione|
|-|-|
|DisableBranchCache<br/>BITS 4,0|Per impostazione predefinita, la funzionalità Windows BranchCache è abilitata. Impostare questo criterio per impedire ai client BITS di trasferire il contenuto mediante Windows BranchCache.<br/>**Nota**: questa impostazione non influisce sull'uso di Windows BranchCache da applicazioni diverse da BITS. Questo criterio non si applica ai trasferimenti BITS su Server Message Block (SMB). Questa impostazione non ha effetto se le impostazioni amministrative del computer per la cache di Branch di Windows disabilitano completamente il relativo utilizzo.|

BITS usa i criteri di gruppo seguenti per configurare la limitazione della larghezza di banda.

|Criteri|Descrizione|
|-|-|
|EnableMaintenanceLimits<br/>BITS 4,0|Limita la larghezza di banda di rete utilizzata da BITS per i trasferimenti in background durante i giorni e le ore di manutenzione. Le pianificazioni di manutenzione limitano ulteriormente la larghezza di banda di rete utilizzata per i trasferimenti in background.<br/> Specificare un limite da usare per i processi in background durante una pianificazione di manutenzione. Se, ad esempio, i processi con priorità normale sono attualmente limitati a 256 kbps in una pianificazione del lavoro, è possibile limitare ulteriormente la larghezza di banda di rete dei processi con priorità normale a 0 Kbps dalle 8:00. alle 10:00 in una pianificazione di manutenzione.<br/>**Nota**: i limiti della larghezza di banda impostati per il periodo di manutenzione sostituiscono tutti i limiti definiti per il lavoro e altre pianificazioni.|
|EnableBandwidthLimits<br/>BITS 4,0|Limita la larghezza di banda di rete utilizzata da BITS per i trasferimenti in background durante il lavoro e i giorni e le ore non lavorativi. La pianificazione del lavoro viene definita utilizzando un calendario settimanale costituito da giorni della settimana e ore del giorno. Tutte le ore e i giorni che non sono definiti in una pianificazione di lavoro sono considerati ore non lavorative.<br/> Specificare un limite da usare per i processi in background durante una pianificazione del lavoro. Ad esempio, è possibile limitare la larghezza di banda di rete dei processi con priorità bassa a 128 kbps da 8:00 AM alle 5:00 dal lunedì al venerdì, quindi impostare il limite a 512 kbps per le ore non lavorative.|


## <a name="related-topics"></a>Argomenti correlati
* [Provider di servizi di configurazione Policy](/windows/client-management/mdm/policy-configuration-service-provider)
