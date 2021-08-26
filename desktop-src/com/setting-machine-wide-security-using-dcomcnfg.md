---
title: Impostazione System-Wide sicurezza tramite DCOMCNFG
description: Quando si vuole che tutte le applicazioni in un computer che non forniscono la propria sicurezza con cui condividere le stesse impostazioni di sicurezza predefinite, si imposta la sicurezza a livello di sistema.
ms.assetid: 23d1e222-c00b-497c-adc8-4ae14c5bdd98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7914fd3b1561900426e2928a5277cb845918e3b8d1b1ad1569ea8db0d112e218
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119954371"
---
# <a name="setting-system-wide-security-using-dcomcnfg"></a>Impostazione System-Wide sicurezza tramite DCOMCNFG

La modifica delle impostazioni di sicurezza a livello di sistema influirà su tutte le applicazioni server COM che non impostano la propria sicurezza a livello di processo. Ciò potrebbe impedire il corretto funzionamento di tali applicazioni. Se si modificano le impostazioni di sicurezza a livello di sistema per influire sulle impostazioni di sicurezza per una determinata applicazione COM, è invece necessario modificare le impostazioni di sicurezza a livello di processo per tale particolare applicazione COM. Per altre informazioni sull'impostazione della sicurezza a livello di processo, vedere [Impostazione della sicurezza a livello di processo](setting-processwide-security.md).

Quando si vuole che tutte le applicazioni in un computer che non forniscono la propria sicurezza con cui condividere le stesse impostazioni di sicurezza predefinite, si imposta la sicurezza a livello di sistema. LDcomcnfg.exe consente di impostare facilmente i valori predefiniti nel Registro di sistema applicabili a tutte le applicazioni in un computer.

È importante comprendere che se il client o il server chiama in modo esplicito [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) per impostare la sicurezza a livello di processo, le impostazioni predefinite nel Registro di sistema verranno ignorate e i parametri a **CoInitializeSecurity** verranno usati invece per le impostazioni di sicurezza per il processo. Inoltre, se si usa Dcomcnfg.exe impostazioni di sicurezza per un processo specifico, le impostazioni predefinite del computer vengono sostituite dalle impostazioni per il processo.

Quando si abilita la sicurezza a livello di sistema, è necessario impostare il livello di autenticazione su un valore diverso da Nessuno ed è necessario impostare le autorizzazioni di avvio e accesso. È possibile impostare il livello di rappresentazione predefinito ed è anche possibile abilitare il rilevamento dei riferimenti. Negli argomenti seguenti vengono fornite procedure dettagliate:

-   [Impostazione del System-Wide di autenticazione predefinito](#setting-system-wide-default-authentication-level)
-   [Impostazione delle System-Wide di avvio](#setting-system-wide-launch-permissions)
-   [Impostazione delle System-Wide di accesso](#setting-system-wide-access-permissions)
-   [Impostazione del System-Wide di rappresentazione](#setting-system-wide-impersonation-level)
-   [Impostazione del System-Wide di riferimento](#setting-system-wide-reference-tracking)
-   [Abilitazione e disabilitazione di DCOM](#enabling-and-disabling-dcom)
-   [Argomenti correlati](#related-topics)

## <a name="setting-system-wide-default-authentication-level"></a>Impostazione del System-Wide di autenticazione predefinito

Il livello di autenticazione viene usato per indicare a COM a quale livello si vuole autenticare il client. Questi livelli offrono vari livelli di protezione, da nessuna protezione alla crittografia completa. Per abilitare la sicurezza per un computer, è necessario scegliere un livello di autenticazione diverso da Nessuno. È possibile scegliere tale impostazione, usando Dcomcnfg.exe, completando i passaggi seguenti.

**Per impostare il livello di autenticazione a livello di sistema**

1.  Eseguire Dcomcnfg.exe.

2.  Scegliere la **scheda Proprietà** predefinite.

3.  Nella casella **di riepilogo DefaultÂ AuthenticationÂ Level** (Livello di autenticazione predefinito) scegliere un valore diverso da **(Nessuno)**.

4.  Se si impostano altre proprietà per il computer, fare clic sul **pulsante Applica** per applicare il nuovo livello di autenticazione. In caso contrario, **fare clic su OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="setting-system-wide-launch-permissions"></a>Impostazione delle System-Wide di avvio

Le autorizzazioni di avvio impostate con Dcomcnfg.exe un elenco di utenti, a ognuno dei quali viene concessa o negata in modo esplicito l'autorizzazione per avviare qualsiasi server che non fornisce le proprie impostazioni di autorizzazione di avvio. Quando si impostano le autorizzazioni di avvio, è possibile aggiungere o rimuovere uno o più utenti o gruppi da questo elenco. Per ogni utente aggiunto, è necessario specificare se all'utente viene concessa o negata l'autorizzazione di avvio.

**Per impostare le autorizzazioni di avvio per un computer**

1.  Nella pagina **delle proprietà Sicurezza** predefinita in Dcomcnfg.exe scegliere il **pulsante** Modifica impostazione predefinita nell'area Autorizzazioni **di avvio** predefinite.

2.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo da rimuovere e scegliere il **pulsante** Rimuovi. L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK.**

3.  Se si vuole aggiungere un utente o un gruppo, scegliere il **pulsante** Aggiungi.

4.  Se si conosce il nome utente completo da aggiungere, digitarlo nella **casella di testo Aggiungi** nomi. Se non si conosce il nome utente, vedere Impostazione della sicurezza a livello di processo **tramite DCOMCNFG** per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo dalla casella **di** riepilogo Nomi e scegliere il **pulsante** Aggiungi.

5.  Nella casella **di riepilogo Tipo di** accesso selezionare il tipo di accesso **(Consenti avvio** o Nega **avvio**). Per aggiungere altri utenti che avranno anche il tipo di accesso selezionato, ripetere il passaggio 4. Al termine dell'aggiunta di utenti per il tipo di accesso selezionato, scegliere **il pulsante OK.**

6.  Per aggiungere utenti con un tipo di accesso diverso, ripetere i passaggi 4 e 5. In caso contrario, **scegliere OK** per applicare le modifiche.

## <a name="setting-system-wide-access-permissions"></a>Impostazione delle System-Wide di accesso

Dcomcnfg.exe consente di impostare le autorizzazioni di accesso per controllare l'elenco di utenti a cui viene concesso o negato l'accesso ai metodi di tali server che non forniscono autorizzazioni di accesso personalizzate. È possibile aggiungere utenti o gruppi all'elenco, specificando se l'autorizzazione di accesso viene concessa o negata. È anche possibile rimuovere gli utenti dall'elenco.

Quando si impostano le autorizzazioni di accesso, è necessario assicurarsi che SYSTEM sia incluso nell'elenco degli utenti a cui viene concesso l'accesso. Se sono state concesse autorizzazioni di accesso a Everyone, SYSTEM viene incluso in modo implicito.

Il processo di impostazione delle autorizzazioni di accesso per un computer è simile all'impostazione delle autorizzazioni di avvio. È necessario eseguire i passaggi seguenti.

**Per impostare le autorizzazioni di accesso per un computer**

1.  Nella pagina **delle proprietà Sicurezza** predefinita Dcomcnfg.exe scegliere il pulsante Modifica predefinito nell'area Autorizzazioni di **accesso** predefinite. 

2.  Per rimuovere utenti o gruppi, selezionare l'utente o il gruppo da rimuovere e scegliere il **pulsante** Rimuovi. L'utente o il gruppo selezionato non verrà più visualizzato nella casella di riepilogo. Al termine della rimozione di utenti e gruppi, scegliere **OK.**

3.  Se si vuole aggiungere un utente o un gruppo, scegliere il **pulsante** Aggiungi.

4.  Se si conosce il nome utente completo da aggiungere, digitarlo nella **casella di testo Aggiungi** nomi. Se non si conosce il nome utente, vedere Impostazione della sicurezza a livello di processo [tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md) per trovarlo. Dopo aver individuato il nome utente, selezionare l'utente o il gruppo dalla casella **di** riepilogo Nomi e scegliere il **pulsante** Aggiungi.

5.  Nella casella **di riepilogo Tipo di** accesso selezionare il tipo di accesso **(Consenti accesso** o Nega **accesso**). Per aggiungere altri utenti che avranno il tipo di accesso selezionato, ripetere il passaggio 4. Al termine dell'aggiunta di utenti per il tipo di accesso selezionato, scegliere **il pulsante OK.**

6.  Per aggiungere utenti con un tipo di accesso diverso, ripetere i passaggi 4 e 5. In caso contrario, **scegliere OK** per applicare le modifiche.

## <a name="setting-system-wide-impersonation-level"></a>Impostazione del System-Wide di rappresentazione

Il livello di rappresentazione, impostato dal client, determina la quantità di autorità data al server per agire per conto del client. Ad esempio, quando il client ha impostato il livello di rappresentazione per delegare, il server può accedere alle risorse locali e remote come client e il server può mascherarsi oltre più limiti di computer se la funzionalità di mascheramento è impostata. Per determinare il livello di rappresentazione da scegliere, vedere [Livelli di](impersonation-levels.md) rappresentazione e [Cloaking.](cloaking.md)

L'impostazione del livello di rappresentazione predefinito per l'intero computer indica a COM quale livello di rappresentazione usare quando un client specifico del computer non specifica un livello di rappresentazione a livello di codice tramite [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) o [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

**Per impostare il livello di rappresentazione per un computer**

1.  Con Dcomcnfg.exe in esecuzione, scegliere la **scheda Proprietà** predefinite.

2.  Nella casella **di riepilogo Livello di rappresentazione** predefinito scegliere il livello di rappresentazione desiderato.

3.  Se si impostano altre proprietà per il computer, scegliere il **pulsante Applica** per applicare il nuovo livello di rappresentazione. In caso contrario, **scegliere OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="setting-system-wide-reference-tracking"></a>Impostazione del System-Wide di riferimento

Quando si abilita il rilevamento dei riferimenti, si chiede a COM di eseguire controlli di sicurezza aggiuntivi e di tenere traccia delle informazioni che consentono di evitare che gli oggetti vengano rilasciati troppo presto. Tenere presente che questi controlli aggiuntivi sono costosi. Per altre informazioni sul rilevamento dei riferimenti, vedere [Rilevamento dei riferimenti](reference-tracking.md). Usare la procedura seguente per abilitare o disabilitare il rilevamento dei riferimenti.

**Per impostare il rilevamento dei riferimenti per un computer**

1.  Con Dcomcnfg.exe in esecuzione, scegliere la **scheda Proprietà** predefinite.

2.  Per abilitare (o disabilitare) il rilevamento dei riferimenti, selezionare (o deselezionare) la casella di controllo **Fornisci** sicurezza aggiuntiva per il rilevamento dei riferimenti nella parte inferiore della pagina.

3.  Se si impostano altre proprietà per il computer, scegliere **il pulsante** Applica per applicare la nuova impostazione. In caso contrario, **scegliere OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="enabling-and-disabling-dcom"></a>Abilitazione e disabilitazione di DCOM

Quando un computer fa parte di una rete, il protocollo di collegamento DCOM consente agli oggetti COM di tale computer di comunicare con gli oggetti COM in altri computer. È possibile disabilitare DCOM per un computer specifico, ma in questo modo verranno disabilitate tutte le comunicazioni tra gli oggetti in tale computer e gli oggetti in altri computer.

La disabilitazione di DCOM in un computer non ha alcun effetto sugli oggetti COM locali. COM cerca comunque le autorizzazioni di avvio specificate. Se non è stata specificata alcuna autorizzazione di avvio, vengono usate le autorizzazioni di avvio predefinite. Anche se si disabilita DCOM, se un utente ha accesso fisico al computer, potrebbe avviare un server nel computer a meno che non si impostano le autorizzazioni di avvio per non consentirlo.

> [!Note]  
> Se si disabilita DCOM in un computer remoto, non sarà possibile accedere in remoto al computer in un secondo momento per riattivare DCOM. Per ri-abilitare DCOM, è necessario l'accesso fisico al computer.

 

**Per abilitare (o disabilitare) manualmente DCOM per un computer**

1.  Eseguire Dcomcnfg.exe.

2.  Scegliere la **scheda Proprietà predefinite.**

3.  Selezionare (o deselezionare) la casella di controllo **Enable Distributed COMÂ on this Computer** (Abilita COMÂ distribuito nel computer).

4.  Se si impostano altre proprietà per il computer, fare clic sul **pulsante** Applica per abilitare (o disabilitare) DCOM. In caso contrario, **fare clic su OK** per applicare le modifiche e uscire Dcomcnfg.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Impostazione della sicurezza a livello di processo](setting-processwide-security.md)
</dt> </dl>

 

 




