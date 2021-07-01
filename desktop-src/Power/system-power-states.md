---
description: Per l'utente, il sistema sembra essere spento o spento.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Stati di alimentazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efde8a130d6dbe2b44c34e8ab45b973a64f3b255
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120816"
---
# <a name="system-power-states"></a>Stati di alimentazione del sistema

Per l'utente, il sistema sembra essere spento o spento. Non sono presenti altri stati rilevabili. Tuttavia, il sistema supporta più stati di alimentazione che corrispondono agli stati di alimentazione definiti nella specifica Advanced Configuration and Power Interface (ACPI). Esistono anche varianti di questi stati, ad esempio sospensione ibrida e avvio rapido. In questo argomento vengono presentati questi stati e viene descritto il modo in cui sono correlati tra loro.

> [!NOTE]
> Gli integratori di sistemi e gli sviluppatori che creano driver o applicazioni con un servizio di sistema devono prestare particolare attenzione ai problemi di qualità dei driver, ad esempio le perdite di memoria. Anche se la qualità del driver è sempre stata importante, il tempo di attività tra i riavvii del kernel potrebbe essere notevolmente più lungo rispetto alle versioni precedenti del sistema operativo perché in caso di sospensione e arresto avviati dall'utente, il kernel, i driver e i servizi verranno mantenuti e ripristinati, non riavviati.

 

Nella tabella seguente sono elencati gli stati di alimentazione ACPI dal consumo di energia massimo al più basso.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Stato di alimentazione</th>
<th>Stato ACPI</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>OK<br/></td>
<td>S0<br/></td>
<td>Il sistema è completamente utilizzabile. I componenti hardware non in uso possono risparmiare energia immettendo uno stato di alimentazione inferiore.<br/></td>
</tr>
<tr class="even">
<td>Sospendi<br/> (Standby moderno)<br/></td>
<td>S0 low-power idle<br/></td>
<td>Alcuni sistemi SoC supportano uno stato di inattività a basso consumo noto come <a href="/windows-hardware/design/device-experiences/modern-standby">Standby moderno.</a> In questo stato, il sistema può passare molto rapidamente da uno stato a basso consumo a uno a potenza elevata, in modo che possa rispondere rapidamente agli eventi hardware e di rete. I sistemi che supportano modern standby non usano S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>Sospendi<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>Il sistema sembra essere disattivato. L'alimentazione utilizzata in questi stati (S1-S3) è minore di S0 e maggiore di S4; S3 consuma meno potenza di S2 e S2 ne consuma meno di S1. I sistemi supportano in genere uno di questi tre stati, non tutti e tre.<br/> In questi stati (S1-S3), la memoria volatile viene mantenuta aggiornata per mantenere lo stato del sistema. Alcuni componenti rimangono acceso in modo che il computer possa riattivarsi dall'input dalla tastiera, dalla LAN o da un dispositivo USB.<br/> <em>La sospensione ibrida,</em>usata nei desktop, è la posizione in cui un sistema usa un file di ibernazione con S1-S3. Il file di ibernazione salva lo stato del sistema nel caso in cui il sistema perda l'alimentazione durante la sospensione.<br/>
<blockquote>
[!Note]<br />
I sistemi SoC che supportano lo standby moderno (lo stato di inattività a basso consumo) non usano S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Ibernazione<br/></td>
<td>S4<br/></td>
<td>Il sistema sembra essere disattivato. Il consumo di energia è ridotto al livello più basso. Il sistema salva il contenuto della memoria volatile in un file di ibernazione per mantenere lo stato del sistema. Alcuni componenti rimangono acceso in modo che il computer possa riattivarsi dall'input dalla tastiera, dalla LAN o da un dispositivo USB. Il contesto di lavoro può essere ripristinato se è archiviato in supporti non volatile. <br/> <em>L'avvio</em> rapido è il punto in cui l'utente viene disconnesso prima della creazione del file di ibernazione. Ciò consente un file di ibernazione più piccolo, più appropriato per i sistemi con meno funzionalità di archiviazione.<br/></td>
</tr>
<tr class="odd">
<td>Soft Off<br/></td>
<td>S5<br/></td>
<td>Il sistema sembra essere disattivato. Questo stato è costituito da un ciclo di arresto e avvio completo.<br/></td>
</tr>
<tr class="even">
<td>Meccanico spento<br/></td>
<td>G3<br/></td>
<td>Il sistema è completamente spento e non consuma energia. Il sistema torna allo stato di lavoro solo dopo un riavvio completo.<br/></td>
</tr>
</tbody>
</table>



 

[**\_ L'enumerazione SYSTEM POWER \_ STATE**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) definisce i valori utilizzati per specificare gli stati di alimentazione del sistema.

## <a name="working-state-s0"></a>Stato di lavoro (S0)

Durante lo stato di lavoro, il sistema è attivo e in esecuzione. In parole semplici, il dispositivo è "on". Indipendentemente dal fatto che lo schermo sia attivo o spento, il dispositivo è in stato di esecuzione completa. Per risparmiare energia, in particolare nei dispositivi a batteria, è consigliabile spenti i componenti hardware quando non vengono usati.

> [!IMPORTANT]
> Power-down hardware components whenever they're not being used, regard of the state. Un basso consumo di energia è una considerazione importante per i consumer di dispositivi mobili.

 

## <a name="sleep-state-modern-standby"></a>Stato sospensione (standby moderno)

Nella modalità di inattività A basso consumo S0 dello stato di lavoro, detta anche [Standby](/windows-hardware/design/device-experiences/modern-standby)moderno, il sistema rimane parzialmente in esecuzione. Durante lo standby moderno, il sistema può rimanere aggiornato ogni volta che è disponibile una rete appropriata e anche riattivarsi quando è necessaria un'azione in tempo reale, ad esempio la manutenzione del sistema operativo. Lo standby moderno si riattiva molto più velocemente rispetto a S1-S3. Per altre informazioni, vedere [Modern Standby.](/windows-hardware/design/device-experiences/modern-standby)

> [!Note]  
> Modern Standby è disponibile solo in alcuni sistemi SoC. Quando è supportato, il sistema non supporta S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Stato sospensione (S1-S3)

Il sistema entra in sospensione in base a diversi criteri, tra cui l'attività dell'utente o dell'applicazione e le preferenze impostate dall'utente nella pagina Sospensione **di Power &** dell'app Impostazioni.  Per impostazione predefinita, il sistema usa lo stato di sospensione più basso supportato da tutti i dispositivi di riattivazione abilitati. Per altre informazioni su come il sistema determina quando entrare in sospensione, vedere [Criteri di sospensione del sistema.](system-sleep-criteria.md)

Prima che il sistema entri in sospensione, determina lo stato di sospensione appropriato, notifica ad applicazioni e driver la transizione in sospeso e quindi passa allo stato di sospensione. In caso di transizione critica, ad esempio quando viene raggiunta la soglia della batteria critica, il sistema non invia notifiche ad applicazioni e driver. Le applicazioni devono essere preparate a questo scopo e intraprendere l'azione appropriata quando il sistema torna allo stato di lavoro.

In questi stati (S1-S3), la memoria volatile viene mantenuta aggiornata per mantenere lo stato del sistema. Alcuni componenti rimangono acceso in modo che il computer possa riattivarsi dall'input dalla tastiera, dalla LAN o da un dispositivo USB.

Il sistema si riattiva anche dalla sospensione in risposta all'attività dell'utente o a un evento di riattivazione definito da un'applicazione. Per altre informazioni, vedere [Eventi di riattivazione del sistema.](system-wake-up-events.md) Il tempo necessario per la riattivazione del sistema dipende dallo stato di sospensione da cui viene riattivato. Il sistema impiega più tempo per la riattivazione da uno stato a potenza inferiore (S3) rispetto a uno stato con potenza superiore (S1) a causa delle operazioni aggiuntive che l'hardware potrebbe eseguire (stabilizzare l'alimentatore, reinizializzare il processore e così via).

> [!Caution]  
> Quando si chiama [**SetThreadExecutionState,**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate)il valore **ES \_ AWAYMODE \_ REQUIRED** deve essere usato solo quando è assolutamente necessario per le applicazioni multimediali che richiedono al sistema di eseguire attività in background, ad esempio la registrazione di contenuto multimediale o lo streaming di contenuti multimediali ad altri dispositivi mentre il sistema sembra essere in sospensione. Le applicazioni che non richiedono l'elaborazione in background critica o che vengono eseguite in computer portatili non devono abilitare la modalità di rimozione perché impedisce al sistema di risparmiare energia attivando una vera sospensione.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Sospensione ibrida (S1-S3 + file di ibernazione)

*La sospensione* ibrida è uno stato speciale che è una combinazione degli stati di sospensione e ibernazione, quando un sistema usa un file di ibernazione con S1-S3. È disponibile solo in alcuni sistemi. Se abilitata, il sistema scrive un file di ibernazione, ma entra in uno stato di sospensione con potenza superiore. Se l'alimentazione viene persa durante la sospensione del sistema, il sistema si riattiva dalla modalità di ibernazione, che richiede più tempo ma ripristina lo stato del sistema dell'utente.

## <a name="hibernate-state-s4"></a>Stato di ibernazione (S4)

Windows usa l'ibernazione per offrire un'esperienza di avvio rapido. Quando disponibile, viene usato anche nei dispositivi mobili per estendere la durata della batteria utilizzabile di un sistema fornendo un meccanismo per salvare tutto lo stato dell'utente prima di arrestare il sistema. In una transizione di ibernazione, tutto il contenuto della memoria viene scritto in un file nell'unità di sistema primaria, il *file di ibernazione*. In questo modo viene preservato lo stato del sistema operativo, delle applicazioni e dei dispositivi. Nel caso in cui il footprint di memoria combinato consuma tutta la memoria fisica, il file di ibernazione deve essere sufficientemente grande da garantire che vi sia spazio sufficiente per salvare tutto il contenuto della memoria fisica. Poiché i dati vengono scritti in un archivio non volatile, la DRAM non deve mantenere l'aggiornamento automatico e può essere spenta, il che significa che il consumo di energia di ibernazione è molto basso, quasi uguale all'accensione.

Durante un arresto e un avvio completi (S5), l'intera sessione utente viene disattesa e riavviata all'avvio successivo. Al contrario, durante l'ibernazione (S4), la sessione utente viene chiusa e lo stato dell'utente viene salvato.

### <a name="fast-startup-reduced-hibernation-file"></a>Avvio rapido (file di ibernazione ridotto)

*Avvio rapido è* un tipo di arresto che usa un file di ibernazione per velocizzare l'avvio successivo. Durante questo tipo di arresto, l'utente viene disconnesso prima della creazione del file di ibernazione. L'avvio rapido consente un file di ibernazione più piccolo, più appropriato per i sistemi con meno funzionalità di archiviazione. Per altre informazioni, vedere [Tipi di file di ibernazione.](#hibernation-file-types)

Quando si usa l'avvio rapido, il sistema sembra che l'utente si sia verificato un arresto completo (S5), anche se il sistema ha effettivamente passato S4. Ciò include il modo in cui il sistema risponde agli allarmi di riattivazione del dispositivo.

L'avvio rapido disconnette le sessioni utente, ma il contenuto del kernel (sessione 0) viene scritto sul disco rigido. Ciò consente un avvio più veloce.

Per avviare a livello di codice un arresto rapido in stile avvio, chiamare la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con il flag **SHUTDOWN \_ HYBRID** o la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con il flag **EWX \_ HYBRID \_ SHUTDOWN.**

> [!Note]  
> A partire da Windows 8, l'avvio rapido è la transizione predefinita quando viene richiesto un arresto del sistema. Un arresto completo (S5) si verifica quando viene richiesto un riavvio del sistema (o un'applicazione chiama un'API di arresto).

 

### <a name="entering-hibernation"></a>Immissione della modalità di ibernazione

Quando viene effettuata una richiesta di ibernazione, quando il sistema entra in ibernazione, si verificano i passaggi seguenti:

1.  Le app e i servizi vengono informati
2.  I driver vengono informati
3.  Lo stato dell'utente e del sistema viene salvato su disco in formato compresso
4.  Il firmware viene notificato

> [!Note]  
> A partire Windows 8, tutti i core nel sistema vengono usati per comprimere i dati in memoria e scriverlo su disco.

 

Per avviare una transizione di ibernazione a livello di codice, chiamare la [**funzione SetSuspendState.**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate)

### <a name="resuming-from-hibernation"></a>Ripresa dall'ibernazione

Quando un sistema riprende dall'ibernazione.

Quando un sistema è acceso, i passaggi seguenti vengono eseguiti quando il sistema riprende dall'ibernazione.

1.  POST di sistema
2.  La memoria di sistema viene decompressa e ripristinata dal file di ibernazione
3.  Inizializzazione del dispositivo
4.  I driver vengono ripristinati allo stato precedente all'ibernazione
5.  I servizi vengono ripristinati allo stato precedente all'ibernazione
6.  Il sistema diventa disponibile per l'accesso

Un ripristino dall'ibernazione inizia con un POST di sistema simile a un arresto S5. Il boot manager del sistema operativo determina che è necessario un ripristino dalla modalità di ibernazione rilevando un file di ibernazione valido. Quindi indirizza il sistema alla ripresa, ripristinando il contenuto della memoria e tutti i registri dell'architettura. In caso di ripresa dall'ibernazione, il contenuto della memoria di sistema viene letto di nuovo dal disco, decompresso e ripristinato, inserendo il sistema nello stato esatto in cui era in stato di ibernazione. Dopo il ripristino della memoria, i dispositivi vengono rieseguiti e il computer torna allo stato in esecuzione, pronto per l'accesso.

> [!Note]  
> Durante la ripresa dall'ibernazione, i driver e i servizi vengono informati, ma non riavviati. Vengono ripristinati solo nello stato in cui si trovavano prima dell'ibernazione.

 

### <a name="hibernation-file-types"></a>Tipi di file di ibernazione

I file di ibernazione vengono usati per la sospensione ibrida, l'avvio rapido e l'ibernazione standard (descritti in precedenza). Esistono due tipi, differenziati in base alle dimensioni, un file di ibernazione con dimensioni complete e ridotte. Solo l'avvio rapido può usare un file di ibernazione ridotto.



| Tipo di file di ibernazione | Dimensioni predefinite           | Supporta...                           |
|-----------------------|------------------------|---------------------------------------|
| Full                  | 40% della memoria fisica | ibernazione, sospensione ibrida, avvio rapido |
| Ridotto               | 20% della memoria fisica | avvio rapido                          |



 

Per verificare o modificare il tipo di file di ibernazione usato, eseguire **l'powercfg.exe** predefinita. Gli esempi seguenti illustrano come. Per altre informazioni, eseguire `powercfg /? hibernate`.



| Esempio                                                                        | Descrizione                                                                                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `powercfg /a`<br/>                                                | **Verificare il tipo di file di ibernazione.** Quando viene usato un file di ibernazione completo, i risultati specificano che l'ibernazione è un'opzione disponibile. Quando si usa un file di ibernazione ridotto, i risultati diranno che l'ibernazione non è supportata. Se il sistema non ha alcun file di ibernazione, i risultati diranno che l'ibernazione non è stata abilitata.<br/> |
| `powercfg /h /type full`<br/>                                     | **Modificare il tipo di file di ibernazione in full.** Questa operazione non è consigliata nei sistemi con meno di 32 GB di spazio di archiviazione.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Modificare il tipo di file di ibernazione in ridotto.** Se il comando restituisce "il parametro non è corretto", vedere l'esempio seguente.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Riprovare a modificare il tipo di file di ibernazione in ridotto.** Se il file di ibernazione è impostato su una dimensione personalizzata maggiore del 40%, è necessario innanzitutto impostare le dimensioni del file su zero. Ripetere quindi la configurazione ridotta.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Stato soft off (S5)

Lo stato soft off è quando il sistema si arresta completamente senza un file di ibernazione. Il soft off è noto anche come "arresto completo". Durante un arresto e un avvio completi, l'intera sessione utente viene disattesa e riavviata all'avvio successivo. Di conseguenza, un avvio/avvio da questo stato richiede molto più tempo rispetto a S1-S4. Un arresto completo (S5) si verifica quando viene richiesto un riavvio del sistema (o un'applicazione chiama un'API di arresto).

## <a name="mechanical-off-state-g3"></a>Stato di guasto meccanico (G3)

In questo stato, il sistema è completamente spento e non consuma energia. Il sistema torna allo stato di lavoro solo dopo un riavvio completo.

## <a name="wake-on-lan-behavior"></a>Comportamento di riattivazione LAN

La funzionalità di riattivazione LAN riattiva il computer da uno stato di alimentazione insufficiente quando una scheda di rete rileva un evento WOL (in genere, un pacchetto Ethernet appositamente costruito).

LA MODALITÀ DI SOSPENSIONE è supportata dalla sospensione (S3) o dall'ibernazione (S4). Non è supportata dagli stati di arresto di avvio rapido o soft off (S5). Le schede di interfaccia di rete non sono riattivate in questi stati perché gli utenti non si aspettano che i propri sistemi si riattivino da soli.

> [!Note]  
> L'opzione SOFT OFF (S5) non è ufficialmente supportata. Tuttavia, il BIOS in alcuni sistemi può supportare l'arming di schede di interfaccia di rete per la riattivazione, anche se Windows non è coinvolto nel processo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>
