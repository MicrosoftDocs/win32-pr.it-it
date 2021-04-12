---
title: Impostazione della sicurezza System-Wide tramite DCOMCNFG
description: Quando si desidera che tutte le applicazioni in un computer che non forniscono la propria sicurezza per condividere le stesse impostazioni di sicurezza predefinite, è necessario impostare la sicurezza a livello di sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7feaaf356263a48c2c93eb9b3b3764b7352cd39
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396411"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Impostazione della sicurezza System-Wide tramite DCOMCNFG

La modifica delle impostazioni di sicurezza a livello di sistema influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo. Questo potrebbe impedire il corretto funzionamento di tali applicazioni. Se si modificano le impostazioni di sicurezza a livello di sistema in modo da influire sulle impostazioni di sicurezza per una particolare applicazione COM, è necessario modificare le impostazioni di sicurezza a livello di processo per quella particolare applicazione COM. Per ulteriori informazioni sull'impostazione della sicurezza a livello di processo, vedere [impostazione della sicurezza a livello di processo](setting-processwide-security.md).

Quando si desidera che tutte le applicazioni in un computer che non forniscono la propria sicurezza per condividere le stesse impostazioni di sicurezza predefinite, è necessario impostare la sicurezza a livello di sistema. L'uso di Dcomcnfg.exe consente di impostare in modo semplice i valori predefiniti nel registro di sistema che si applicano a tutte le applicazioni in un computer.

È importante comprendere che se il client o il server chiama in modo esplicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza a livello di processo, le impostazioni predefinite nel registro di sistema verranno ignorate e verranno usati i parametri per **CoInitializeSecurity** per le impostazioni di sicurezza per il processo. Inoltre, se si utilizza Dcomcnfg.exe per specificare le impostazioni di sicurezza per un processo specifico, le impostazioni del computer predefinite verranno sostituite dalle impostazioni del processo.

Quando si Abilita la sicurezza a livello di sistema, è necessario impostare il livello di autenticazione su un valore diverso da None ed è necessario impostare le autorizzazioni di avvio e accesso. È possibile impostare il livello di rappresentazione predefinito ed è anche possibile abilitare il rilevamento dei riferimenti. Negli argomenti seguenti vengono fornite procedure dettagliate:

-   [Impostazione System-Wide livello di autenticazione predefinito](#setting-system-wide-default-authentication-level)
-   [Impostazione delle autorizzazioni di avvio System-Wide](#setting-system-wide-launch-permissions)
-   [Impostazione delle autorizzazioni di accesso System-Wide](#setting-system-wide-access-permissions)
-   [Impostazione del livello di rappresentazione System-Wide](#setting-system-wide-impersonation-level)
-   [Impostazione System-Wide rilevamento dei riferimenti](#setting-system-wide-reference-tracking)
-   [Abilitazione e disabilitazione di DCOM](#enabling-and-disabling-dcom)
-   [Argomenti correlati](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Impostazione System-Wide livello di autenticazione predefinito

Il livello di autenticazione viene usato per indicare a COM il livello in cui si vuole che il client venga autenticato. Questi livelli offrono diversi livelli di protezione, da nessuna protezione alla crittografia completa. Per abilitare la sicurezza per un computer, è necessario scegliere un livello di autenticazione diverso da nessuno. È possibile scegliere tale impostazione, usando Dcomcnfg.exe, completando i passaggi seguenti.

**Per impostare il livello di autenticazione a livello di sistema**

1.  Eseguire Dcomcnfg.exe.

2.  Scegliere la scheda **proprietà predefinite** .

3.  Nella casella di riepilogo **DefaultÂ AuthenticationÂ Level** scegliere un valore diverso da **(nessuno)**.

4.  Se si intende impostare più proprietà per il computer, fare clic sul pulsante **applica** per applicare il nuovo livello di autenticazione. In caso contrario, fare clic su **OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Impostazione delle autorizzazioni di avvio System-Wide

Le autorizzazioni di avvio impostate con Dcomcnfg.exe determinano un elenco di utenti a cui viene concessa o negata in modo esplicito l'autorizzazione per avviare un server che non fornisce le proprie impostazioni di autorizzazione di avvio. Quando si impostano le autorizzazioni di avvio, è possibile aggiungere o rimuovere uno o più utenti o gruppi da questo elenco. Per ogni utente aggiunto, è necessario specificare se all'utente viene concessa o negata l'autorizzazione di avvio.

**Per impostare le autorizzazioni di avvio per un computer**

1.  Nella pagina delle proprietà **sicurezza predefinita** in Dcomcnfg.exe scegliere il pulsante **Modifica impostazioni predefinite** nell'area **autorizzazioni di avvio predefinite** .

2.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo che si desidera rimuovere e scegliere il pulsante **Rimuovi** . L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK**.

3.  Se si desidera aggiungere un utente o un gruppo, scegliere il pulsante **Aggiungi** .

4.  Se si conosce il nome utente completo che si desidera aggiungere, digitarlo nella casella di testo **Aggiungi nomi** . Se non si conosce il nome utente, vedere **impostazione della sicurezza Processwide tramite DCOMCNFG** per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo nella casella di riepilogo **nomi** e scegliere il pulsante **Aggiungi** .

5.  Nella casella **di riepilogo tipo di accesso** selezionare il tipo di accesso ( **Consenti** avvio o **Nega avvio**). Per aggiungere altri utenti che avranno anche il tipo di accesso selezionato, ripetere il passaggio 4. Al termine dell'aggiunta degli utenti per il tipo di accesso selezionato, scegliere il pulsante **OK** .

6.  Per aggiungere utenti che avranno un tipo di accesso diverso, ripetere i passaggi 4 e 5. In caso contrario, scegliere **OK** per applicare le modifiche.

## <a name="setting-system-wide-access-permissions"></a>Impostazione delle autorizzazioni di accesso System-Wide

Dcomcnfg.exe consente di impostare le autorizzazioni di accesso per controllare l'elenco di utenti a cui viene concesso o negato l'accesso ai metodi dei server che non forniscono le proprie autorizzazioni di accesso. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

Quando si impostano le autorizzazioni di accesso, è necessario assicurarsi che il sistema sia incluso nell'elenco di utenti a cui è stato concesso l'accesso. Se sono state concesse le autorizzazioni di accesso a tutti, il sistema viene incluso in modo implicito.

Il processo di impostazione delle autorizzazioni di accesso per un computer è simile all'impostazione delle autorizzazioni di avvio. È necessario eseguire i passaggi seguenti.

**Per impostare le autorizzazioni di accesso per un computer**

1.  Nella pagina delle proprietà **sicurezza predefinita** in Dcomcnfg.exe scegliere il pulsante **Modifica impostazioni predefinite** nell'area **autorizzazioni di accesso predefinite** .

2.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo che si desidera rimuovere e scegliere il pulsante **Rimuovi** . L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK**.

3.  Se si desidera aggiungere un utente o un gruppo, scegliere il pulsante **Aggiungi** .

4.  Se si conosce il nome utente completo che si desidera aggiungere, digitarlo nella casella di testo **Aggiungi nomi** . Se non si conosce il nome utente, vedere [impostazione della sicurezza a livello di processo tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo nella casella di riepilogo **nomi** e scegliere il pulsante **Aggiungi** .

5.  Nella casella **di riepilogo tipo di accesso** selezionare il tipo di accesso ( **Consenti accesso** o **Nega accesso**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 4. Al termine dell'aggiunta degli utenti per il tipo di accesso selezionato, scegliere il pulsante **OK** .

6.  Per aggiungere utenti che avranno un tipo di accesso diverso, ripetere i passaggi 4 e 5. In caso contrario, scegliere **OK** per applicare le modifiche.

## <a name="setting-system-wide-impersonation-level"></a>Impostazione del livello di rappresentazione System-Wide

Il livello di rappresentazione, impostato dal client, determina la quantità di autorità assegnata al server per agire per conto del client. Ad esempio, quando il client ha impostato il livello di rappresentazione su Delegate, il server può accedere alle risorse locali e remote come client e il server può mascherare più limiti del computer se è impostata la funzionalità di mascheramento. Per determinare il livello di rappresentazione da scegliere, vedere [livelli di rappresentazione](impersonation-levels.md) e [mascheramento](cloaking.md).

L'impostazione del livello di rappresentazione predefinito per l'intero computer indica a COM quale livello di rappresentazione usare quando un particolare client nel computer non specifica un livello di rappresentazione a livello di codice tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Per impostare il livello di rappresentazione per un computer**

1.  Con Dcomcnfg.exe in esecuzione, scegliere la scheda **proprietà predefinite** .

2.  Nella casella di riepilogo **livello di rappresentazione predefinito** scegliere il livello di rappresentazione desiderato.

3.  Se si intende impostare più proprietà per il computer, scegliere il pulsante **applica** per applicare il nuovo livello di rappresentazione. In caso contrario, scegliere **OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Impostazione System-Wide rilevamento dei riferimenti

Quando si Abilita il rilevamento dei riferimenti, si chiede a COM di eseguire ulteriori controlli di sicurezza e di tenere traccia delle informazioni che impediscono il rilascio degli oggetti troppo presto. Tenere presente che questi controlli aggiuntivi sono costosi. Per ulteriori informazioni sul rilevamento dei riferimenti, vedere [Tracking Reference](reference-tracking.md). Utilizzare la procedura seguente per abilitare o disabilitare il rilevamento dei riferimenti.

**Per impostare il rilevamento dei riferimenti per un computer**

1.  Con Dcomcnfg.exe in esecuzione, scegliere la scheda **proprietà predefinite** .

2.  Per abilitare (o disabilitare) la verifica dei riferimenti, selezionare (o deselezionare) la casella di controllo **fornire sicurezza aggiuntiva per il rilevamento dei riferimenti** nella parte inferiore della pagina.

3.  Se si intende impostare più proprietà per il computer, scegliere il pulsante **applica** per applicare la nuova impostazione. In caso contrario, scegliere **OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Abilitazione e disabilitazione di DCOM

Quando un computer fa parte di una rete, il protocollo wire DCOM consente agli oggetti COM in tale computer di comunicare con oggetti COM in altri computer. È possibile disabilitare DCOM per un computer specifico, ma in questo modo si disabilita tutta la comunicazione tra gli oggetti in tale computer e gli oggetti di altri computer.

La disabilitazione di DCOM in un computer non ha alcun effetto sugli oggetti COM locali. COM cerca ancora le autorizzazioni di avvio specificate. Se non è stata specificata alcuna autorizzazione di avvio, vengono usate le autorizzazioni di avvio predefinite. Anche se si disabilita DCOM, se un utente dispone di accesso fisico al computer, è possibile che avvii un server nel computer a meno che non si impostino le autorizzazioni di avvio in modo che non lo consentano.

> [!Note]  
> Se si disabilita DCOM in un computer remoto, non sarà possibile accedere in modalità remota al computer in un secondo momento per abilitare di nuovo DCOM. Per abilitare di nuovo DCOM, sarà necessario l'accesso fisico al computer.

 

**Per abilitare o disabilitare manualmente DCOM per un computer**

1.  Eseguire Dcomcnfg.exe.

2.  Scegliere la scheda **Proprietà DefaultÂ** .

3.  Selezionare (o deselezionare) la casella **di controllo Abilita ei distribuita nel computer** .

4.  Se si intende impostare più proprietà per il computer, fare clic sul pulsante **applica** per abilitare o disabilitare DCOM. In caso contrario, fare clic su **OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




