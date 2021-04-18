---
description: Per l'utente, il sistema sembra essere on o off.
ms.assetid: 3d897a88-125e-457f-9ea7-ac2056b0767a
title: Stati di alimentazione del sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f18cf6323ae852a871869066a2e9baa2860e6978
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312014"
---
# <a name="system-power-states"></a>Stati di alimentazione del sistema

Per l'utente, il sistema sembra essere on o off. Nessun altro stato rilevabile. Tuttavia, il sistema supporta più Stati di alimentazione che corrispondono agli Stati di alimentazione definiti nella specifica ACPI (Advanced Configuration and Power Interface). Esistono anche varianti di questi Stati, ad esempio sospensione ibrida e avvio rapido. In questo argomento vengono introdotti questi Stati e viene descritto il modo in cui sono correlati tra loro.

> [!NOTE]
> Gli integratori di sistemi e gli sviluppatori che creano driver o applicazioni con un servizio di sistema devono prestare particolare attenzione ai problemi di qualità dei driver, ad esempio le perdite di memoria. Anche se la qualità dei driver è sempre stata importante, il tempo di attività tra i riavvii del kernel potrebbe essere significativamente più lungo rispetto alle versioni precedenti del sistema operativo, perché per le operazioni di sospensione e chiusura avviate dall'utente, il kernel, i driver e i servizi verranno conservati e ripristinati, non riavviati.

 

La tabella seguente elenca gli Stati di alimentazione ACPI dal consumo di energia più alto a quello più basso.



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
<td>Il sistema è completamente utilizzabile. I componenti hardware che non sono in uso possono risparmiare energia immettendo uno stato di alimentazione più basso.<br/></td>
</tr>
<tr class="even">
<td>Sospendi<br/> (Standby moderna)<br/></td>
<td>Inattività a basso consumo S0<br/></td>
<td>Alcuni sistemi SoC supportano uno stato di inattività a basso consumo noto come <a href="/windows-hardware/design/device-experiences/modern-standby">Modern standby</a>. In questo stato, il sistema è in grado di passare da uno stato di basso consumo a uno stato di potenza elevata, in modo che possa rispondere rapidamente agli eventi hardware e di rete. I sistemi che supportano la modalità standby moderna non usano S1-S3.<br/></td>
</tr>
<tr class="odd">
<td>Sospendi<br/></td>
<td>S1<br/> S2<br/> S3<br/></td>
<td>Il sistema sembra essere disattivato. La potenza utilizzata in questi stati (S1-S3) è minore di S0 e più di S4; S3 consuma meno energia rispetto a S2 e S2 consuma meno energia rispetto a S1. I sistemi in genere supportano uno di questi tre stati, non tutti e tre.<br/> In questi stati (S1-S3), la memoria volatile viene mantenuta aggiornata per mantenere lo stato del sistema. Alcuni componenti rimangono accesi, quindi il computer può essere riattivato dall'input dalla tastiera, dalla LAN o da un dispositivo USB.<br/> La <em>sospensione ibrida</em>, usata sui desktop, è la posizione in cui un sistema usa un file di ibernazione con S1-S3. Il file di ibernazione salva lo stato del sistema in caso di perdita dell'alimentazione del sistema in fase di sospensione.<br/>
<blockquote>
[!Note]<br />
I sistemi SoC che supportano la modalità standby moderna (stato di inattività a basso consumo) non usano S1-S3.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td>Ibernazione<br/></td>
<td>S4<br/></td>
<td>Il sistema sembra essere disattivato. Il consumo di energia viene ridotto al livello più basso. Il sistema salva il contenuto della memoria volatile in un file di ibernazione per mantenere lo stato del sistema. Alcuni componenti rimangono accesi, quindi il computer può essere riattivato dall'input dalla tastiera, dalla LAN o da un dispositivo USB. Il contesto di lavoro può essere ripristinato se archiviato in un supporto non volatile. <br/> L' <em>avvio rapido</em> è la posizione in cui l'utente viene disconnesso prima della creazione del file di ibernazione. Questo consente un file di ibernazione più piccolo, più appropriato per i sistemi con meno funzionalità di archiviazione.<br/></td>
</tr>
<tr class="odd">
<td>Soft off<br/></td>
<td>S5<br/></td>
<td>Il sistema sembra essere disattivato. Questo stato è costituito da un arresto e un ciclo di avvio completi.<br/></td>
</tr>
<tr class="even">
<td>Meccanico disattivato<br/></td>
<td>G3<br/></td>
<td>Il sistema è completamente disattivato e non usa alcun potere. Il sistema torna allo stato di lavoro solo dopo un riavvio completo.<br/></td>
</tr>
</tbody>
</table>



 

L' [**enumerazione \_ \_ dello stato di alimentazione del sistema**](/windows/desktop/api/WinNT/ne-winnt-system_power_state) definisce i valori utilizzati per specificare gli Stati di alimentazione del sistema.

## <a name="working-state-s0"></a>Stato di lavoro (S0)

Durante lo stato di lavoro, il sistema è attivo e in esecuzione. In termini semplici, il dispositivo è "acceso". Se la schermata è attiva o disattivata, il dispositivo è in uno stato di esecuzione completa. Per conservare l'energia, soprattutto nei dispositivi a batteria, è consigliabile spegnere i componenti hardware quando non vengono usati.

> [!IMPORTANT]
> Spegnere i componenti hardware ogni volta che non vengono usati, indipendentemente dallo stato. Il consumo di energia basso è una considerazione importante per i consumer di dispositivi mobili.

 

## <a name="sleep-state-modern-standby"></a>Stato sospensione (standby moderno)

Nella modalità di inattività a basso consumo S0 dello stato di lavoro, noto anche come [Modern standby](/windows-hardware/design/device-experiences/modern-standby), il sistema rimane parzialmente in esecuzione. Durante la fase di standby moderna, il sistema può rimanere aggiornato ogni volta che è disponibile una rete appropriata e riattivare anche quando è richiesta un'azione in tempo reale, ad esempio la manutenzione del sistema operativo. Modern standby viene riattivato significativamente più velocemente rispetto a S1-S3. Per altre informazioni, vedere [Modern standby](/windows-hardware/design/device-experiences/modern-standby).

> [!Note]  
> La modalità standby moderna è disponibile solo in alcuni sistemi SoC. Quando è supportato, il sistema non supporta S1-S3.

 

## <a name="sleep-state-s1-s3"></a>Stato sospensione (S1-S3)

Il sistema entra in modalità sospensione in base a diversi criteri, incluse le attività dell'utente o dell'applicazione e le preferenze impostate dall'utente nella pagina di **sospensione di Power &** dell'app **Impostazioni** . Per impostazione predefinita, il sistema usa lo stato di sospensione a bassa alimentazione supportato da tutti i dispositivi di riattivazione abilitati. Per ulteriori informazioni sul modo in cui il sistema determina quando immettere la sospensione, vedere [criteri di sospensione del sistema](system-sleep-criteria.md).

Prima che il sistema entri in stato di sospensione, determina lo stato di sospensione appropriato, notifica le applicazioni e i driver della transizione in sospeso, quindi passa il sistema allo stato di sospensione. Nel caso di una transizione critica, ad esempio quando viene raggiunta la soglia di batteria critica, il sistema non notifica le applicazioni e i driver. È necessario preparare le applicazioni e intraprendere l'azione appropriata quando il sistema torna allo stato di lavoro.

In questi stati (S1-S3), la memoria volatile viene mantenuta aggiornata per mantenere lo stato del sistema. Alcuni componenti rimangono accesi, quindi il computer può essere riattivato dall'input dalla tastiera, dalla LAN o da un dispositivo USB.

Il sistema si riattiva inoltre dalla sospensione in risposta all'attività dell'utente o a un evento di riattivazione definito da un'applicazione. Per ulteriori informazioni, vedere [eventi di riattivazione del sistema](system-wake-up-events.md). La quantità di tempo necessaria per riattivare il sistema dipende dallo stato di sospensione da cui viene riattivato. Il sistema impiega più tempo per riattivarsi da uno stato di basso consumo (S3) rispetto a uno stato più elevato (S1) a causa del lavoro aggiuntivo che l'hardware potrebbe dover eseguire (stabilizzare l'alimentatore, reinizializzare il processore e così via).

> [!Caution]  
> Quando si chiama [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate), il valore di **es \_ modalità utente assente \_ required** deve essere usato solo quando è strettamente necessario per le applicazioni multimediali che richiedono al sistema di eseguire attività in background, ad esempio la registrazione di contenuti televisivi o flussi multimediali in altri dispositivi mentre il sistema sembra rimanere in sospensione. Le applicazioni che non richiedono un'elaborazione in background critica o che vengono eseguite su computer portatili non devono abilitare la modalità di disattivazione, in quanto impedisce al sistema di risparmiare energia immettendo la sospensione vera.

 

### <a name="hybrid-sleep-s1-s3--hibernation-file"></a>Sospensione ibrida (S1-S3 + file di ibernazione)

La *sospensione ibrida* è uno stato speciale costituito da una combinazione degli Stati di sospensione e ibernazione, ovvero quando un sistema usa un file di ibernazione con S1-S3. È disponibile solo in alcuni sistemi. Quando è abilitata, il sistema scrive un file di ibernazione ma entra in uno stato di sospensione più elevato. Se il risparmio di energia si interrompe mentre il sistema è in sospensione, il sistema viene riattivato dalla modalità di ibernazione, operazione che richiede più tempo, ma ripristina lo stato del sistema dell'utente.

## <a name="hibernate-state-s4"></a>Stato di ibernazione (S4)

Windows utilizza la modalità di ibernazione per offrire un'esperienza di avvio rapido. Se disponibile, viene usato anche nei dispositivi mobili per estendere la durata della batteria utilizzabile di un sistema fornendo un meccanismo per salvare tutto lo stato dell'utente prima di arrestare il sistema. In una transizione di ibernazione, tutto il contenuto della memoria viene scritto in un file nell'unità di sistema primaria, il *file di ibernazione*. Viene mantenuto lo stato del sistema operativo, delle applicazioni e dei dispositivi. Nel caso in cui il footprint di memoria combinato usi tutta la memoria fisica, il file di ibernazione deve essere sufficientemente grande da garantire che ci sia spazio per salvare tutto il contenuto della memoria fisica. Poiché i dati vengono scritti in una risorsa di archiviazione non volatile, non è necessario che DRAM mantenga l'aggiornamento automatico e possa essere spento, il che significa che il consumo di energia di ibernazione è molto basso, quasi come lo spegnimento.

Durante un arresto e un avvio completi (S5), l'intera sessione utente viene eliminata e riavviata al successivo avvio. Al contrario, durante un ibernazione (S4), la sessione utente viene chiusa e lo stato utente viene salvato.

### <a name="fast-startup-reduced-hibernation-file"></a>Avvio rapido (file di ibernazione ridotto)

L' *avvio rapido* è un tipo di arresto che usa un file di ibernazione per velocizzare l'avvio successivo. Durante questo tipo di arresto, l'utente viene disconnesso prima della creazione del file di ibernazione. L'avvio rapido consente un file di ibernazione più piccolo, più appropriato per i sistemi con meno funzionalità di archiviazione. Per altre informazioni, vedere [tipi di file di ibernazione](#hibernation-file-types).

Quando si usa l'avvio rapido, il sistema viene visualizzato all'utente come se si fosse verificato un arresto completo (S5), anche se il sistema ha effettivamente attraversato S4. Questo include il modo in cui il sistema risponde alla sveglia del dispositivo.

L'avvio rapido disconnette le sessioni utente, ma il contenuto del kernel (Session 0) viene scritto nel disco rigido. Questo consente un avvio più veloce.

Per avviare a livello di codice un arresto rapido dello stile di avvio, chiamare la funzione [**InitiateShutdown**](/windows/desktop/api/winreg/nf-winreg-initiateshutdowna) con il flag di **arresto \_ ibrido** o la funzione [**ExitWindowsEx**](/windows/desktop/api/winuser/nf-winuser-exitwindowsex) con il flag di **\_ \_ arresto ibrido EWX** .

> [!Note]  
> A partire da Windows 8, l'avvio rapido è la transizione predefinita quando viene richiesto un arresto del sistema. Un arresto completo (S5) si verifica quando viene richiesto un riavvio del sistema (o un'applicazione chiama un'API di arresto).

 

### <a name="entering-hibernation"></a>Immissione dell'ibernazione

Quando viene effettuata una richiesta di ibernazione, i passaggi seguenti si verificano quando il sistema entra in stato di ibernazione:

1.  Notifiche per app e servizi
2.  Driver notificati
3.  L'utente e lo stato del sistema vengono salvati su disco in un formato compresso
4.  Notifica del firmware

> [!Note]  
> A partire da Windows 8, tutti i core del sistema vengono usati per comprimere i dati in memoria e scriverli su disco.

 

Per avviare una transizione di ibernazione a livello di codice, chiamare la funzione [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .

### <a name="resuming-from-hibernation"></a>Ripresa dalla modalità di ibernazione

Quando un sistema riprende dalla modalità di ibernazione.

Quando un sistema è acceso, i passaggi seguenti si verificano quando il sistema riprende dalla modalità di ibernazione.

1.  POST di sistema
2.  La memoria di sistema viene decompressa e ripristinata dal file di ibernazione
3.  Inizializzazione del dispositivo
4.  I driver vengono ripristinati allo stato in cui si trovavano prima della sospensione
5.  I servizi vengono ripristinati allo stato in cui si trovavano prima della sospensione
6.  Il sistema diventa disponibile per l'accesso

Un resume dalla modalità di ibernazione inizia con un POST di sistema simile a un arresto di S5. Il gestore di avvio del sistema operativo determina che è necessario un ripristino dalla modalità di ibernazione rilevando un file di ibernazione valido. Indica quindi al sistema di riprendere il contenuto della memoria e di tutti i registri architetturali. Nel caso di un riavvio dalla modalità di ibernazione, il contenuto della memoria di sistema viene letto dal disco, decompresso e ripristinato, inserendo il sistema nello stato esatto in cui si trovava al momento della sospensione. Una volta ripristinata la memoria, i dispositivi vengono riavviati, il computer torna allo stato di esecuzione, pronto per l'accesso.

> [!Note]  
> Durante un riavvio dalla modalità di ibernazione, i driver e i servizi vengono informati, ma non vengono riavviati. Vengono ripristinati solo nello stato in cui si trovavano prima della sospensione.

 

### <a name="hibernation-file-types"></a>Tipi di file di ibernazione

I file di ibernazione vengono usati per la sospensione ibrida, l'avvio rapido e l'ibernazione standard (descritta in precedenza). Esistono due tipi, differenziati per dimensione, un file di ibernazione con dimensioni complete e ridotte. Solo l'avvio veloce può usare un file di ibernazione ridotto.



| Tipo di file di ibernazione | Dimensioni predefinite           | Supporta...                           |
|-----------------------|------------------------|---------------------------------------|
| Full                  | 40% della memoria fisica | ibernazione, sospensione ibrida, avvio veloce |
| Ridotto               | 20% della memoria fisica | avvio rapido                          |



 

Per verificare o modificare il tipo di file di ibernazione utilizzato, eseguire l'utilità **powercfg.exe** . Gli esempi seguenti illustrano come. Per altre informazioni, eseguire `powercfg /? hibernate`.



|                                                                         |                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Esempio                                                                 | Descrizione                                                                                                                                                                                                                                                                                                                                        |
| `powercfg /a`<br/>                                                | **Verificare il tipo di file di ibernazione.** Quando viene usato un file di ibernazione completo, il risultato è che l'ibernazione è un'opzione disponibile. Quando si usa un file di ibernazione ridotto, i risultati diranno che l'ibernazione non è supportata. Se il sistema non ha alcun file di ibernazione, i risultati diranno che l'ibernazione non è stata abilitata.<br/> |
| `powercfg /h /type full`<br/>                                     | **Modificare il tipo di file di ibernazione in full.** Questa operazione non è consigliata per i sistemi con meno di 32 GB di spazio di archiviazione.<br/>                                                                                                                                                                                                                        |
| `powercfg /h /type reduced`<br/>                                  | **Modificare il tipo di file di ibernazione in ridotto.** Se il comando restituisce "il parametro non è corretto", vedere l'esempio seguente.<br/>                                                                                                                                                                                                        |
| `powercfg /h /size 0`<br/> `powercfg /h /type reduced`<br/> | **Riprovare a modificare il tipo di file di ibernazione in ridotto.** Se il file di ibernazione è impostato su una dimensione personalizzata superiore al 40%, è necessario innanzitutto impostare la dimensione del file su zero. Quindi riprovare a eseguire la configurazione ridotta.<br/>                                                                                                                       |



 

## <a name="soft-off-state-s5"></a>Stato soft off (S5)

Lo stato di soft off è quando il sistema si arresta completamente senza un file di ibernazione. Soft off è anche noto come "arresto completo". Durante un arresto e un avvio completi, l'intera sessione utente viene eliminata e riavviata al successivo avvio. Di conseguenza, un avvio/avvio da questo stato richiede molto più tempo di S1-S4. Un arresto completo (S5) si verifica quando viene richiesto un riavvio del sistema (o un'applicazione chiama un'API di arresto).

## <a name="mechanical-off-state-g3"></a>Stato meccanico disattivato (G3)

In questo stato, il sistema è completamente disattivato e non consuma alcuna potenza. Il sistema torna allo stato di lavoro solo dopo un riavvio completo.

## <a name="wake-on-lan-behavior"></a>Comportamento di riattivazione LAN

La funzionalità di riattivazione LAN (WOL) riattiva il computer da uno stato di alimentazione basso quando una scheda di rete rileva un evento WOL (in genere, un pacchetto Ethernet appositamente costruito).

WOL è supportato dalla sospensione (S3) o dallo stato di ibernazione (S4). Non è supportata dagli Stati di arresto dell'avvio rapido o soft off (S5). Le schede di rete non sono munite di riattivazione in questi stati perché gli utenti non si aspettano che i sistemi vengano riattivati autonomamente.

> [!Note]  
> WOL non è ufficialmente supportato da soft off (S5). Tuttavia, il BIOS in alcuni sistemi può supportare l'inserimento di schede di rete per la riattivazione, anche se Windows non è impegnato nel processo.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sul risparmio energia](about-power-management.md)
</dt> </dl>
