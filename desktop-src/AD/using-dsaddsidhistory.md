---
title: Uso di DsAddSidHistory
description: In questo argomento viene descritto come utilizzare la funzione DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Uso di DsAddSidHistory Active Directory
- Active Directory Active Directory, usando, usando DsAddSidHistory
- DsAddSidHistory Active Directory, utilizzo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d45792dbd8c7a2bfa2dd047111a3ed165a2011e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707510"
---
# <a name="using-dsaddsidhistory"></a>Uso di DsAddSidHistory

La funzione [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) Ottiene l'ID di sicurezza (SID) dell'account primario di un'entità di sicurezza da un dominio (il dominio di origine) e lo aggiunge all'attributo **sIDHistory** di un'entità di sicurezza in un altro dominio (di destinazione) in un'altra foresta. Quando il dominio di origine è in modalità nativa di Windows 2000, questa funzione recupera anche i valori **sIDHistory** dell'entità di origine e li aggiunge al **sIDHistory** dell'entità di destinazione.

L'aggiunta di SID a una **sIDHistory** dell'entità di sicurezza è un'operazione sensibile alla sicurezza che concede all'entità di destinazione l'accesso a tutte le risorse accessibili all'entità di origine, purché esistano dei trust dai domini delle risorse applicabili al dominio di destinazione.

In un dominio Windows 2000 in modalità nativa un accesso utente crea un token di accesso che contiene il SID dell'account primario utente e i SID di gruppo, nonché l'utente **sIDHistory** e il **sIDHistory** dei gruppi di cui l'utente è membro. Con questi primi SID (valori **sIDHistory** ) nel token dell'utente viene concesso all'utente l'accesso alle risorse protette da elenchi di controllo di accesso (ACL) contenenti i SID precedenti.

Questa operazione facilita alcuni scenari di distribuzione di Windows 2000. In particolare, supporta uno scenario in cui gli account in una nuova foresta di Windows 2000 vengono creati per gli utenti e i gruppi già presenti in un ambiente di produzione Windows NT 4,0. Inserendo il SID dell'account Windows NT 4,0 nell'account Windows 2000 **sIDHistory**, l'accesso alle risorse di rete viene mantenuto per l'accesso dell'utente al nuovo account Windows 2000.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) supporta inoltre la migrazione di server di risorse i BDC (backup domain controller) windows NT 4,0 (o controller di dominio e server membro in un dominio Windows 2000 in modalità nativa) a un dominio Windows 2000 come server membro. Questa migrazione richiede la creazione, nel dominio Windows 2000 di destinazione, dei gruppi locali di dominio che contengono, nella rispettiva **sIDHistory**, i SID primari dei gruppi locali definiti in BDC (o gruppi locali di dominio a cui si fa riferimento negli ACL nei server Windows 2000) nel dominio di origine. Creando un gruppo locale di destinazione contenente **sIDHistory** e tutti i membri del gruppo locale di origine, l'accesso alle risorse del server migrate, protetto da ACL che fanno riferimento al gruppo locale di origine, viene mantenuto per tutti i membri.

> [!Note]  
> L'uso di [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede una comprensione delle implicazioni amministrative e di sicurezza più ampie in questi e in altri scenari. Per ulteriori informazioni, vedere il white paper "pianificazione della migrazione da Windows NT a Microsoft Windows 2000", fornito come Dommig.doc negli strumenti di supporto di Windows 2000. Questa documentazione è disponibile anche nel CD del prodotto in \\ strumenti di supporto \\ .

 

## <a name="authorization-requirements"></a>Requisiti di autorizzazione

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede privilegi di amministratore nei domini di origine e di destinazione. In particolare, il chiamante di questa API deve essere membro del gruppo Domain Admins nel dominio di destinazione. Viene eseguito un controllo hardcoded per l'appartenenza. Inoltre, il chiamante o l'account fornito nel parametro *SrcDomainCreds* , se non **null**, deve essere un membro del gruppo Administrators o Domain Administrators nel dominio di origine.

## <a name="domain-and-trust-requirements"></a>Requisiti di dominio e trust

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede che il dominio di destinazione sia in modalità nativa di Windows 2000 o versione successiva, perché solo questo tipo di dominio supporta l'attributo **sIDHistory** . Il dominio di origine può essere Windows NT 4,0 o Windows 2000, modalità mista o nativa. I domini di origine e di destinazione non devono trovarsi nella stessa foresta. I domini di Windows NT 4,0 sono per definizione non in una foresta. Questo vincolo tra foreste garantisce che i SID duplicati, che appaiono come SID primari o **sIDHistory** , non vengano creati nella stessa foresta.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede un trust esterno dal dominio di origine al dominio di destinazione nei casi elencati nella tabella seguente.



| Caso                                                                             | Descrizione                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il dominio di origine è Windows 2000.<br/>                                    | L'attributo di origine **sIDHistory** , disponibile solo nei domini di origine di Windows 2000, può essere letto solo usando LDAP, che richiede questo trust per la protezione dell'integrità.<br/>                                                                                             |
| Il dominio di origine è Windows NT 4,0 e *SrcDomainCreds* è **null**.<br/> | La rappresentazione, necessaria per supportare le operazioni del dominio di origine usando le credenziali del chiamante, dipende da questa relazione di trust. Per impostazione predefinita, la rappresentazione richiede anche che il controller di dominio di destinazione disponga di "trusted per la delega" abilitato per impostazione predefinita nei controller di dominio.<br/> |



 

Tuttavia, non è richiesta alcuna relazione di trust tra i domini di origine e di destinazione se il dominio di origine è Windows NT 4,0 e *SrcDomainCreds* non è **null**.

## <a name="source-domain-controller-requirements"></a>Requisiti del controller di dominio di origine

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede che il controller di dominio, selezionato come destinazione per le operazioni nel dominio di origine, sia il PDC nei domini di windows NT 4,0 o l'emulatore PDC nei domini di Windows 2000. Il controllo del dominio di origine viene generato tramite operazioni di scrittura, pertanto il PDC è necessario nei domini di origine di Windows NT 4,0 e la restrizione solo PDC garantisce che i controlli **DsAddSidHistory** vengano generati in un singolo computer. In questo modo si riduce la necessità di esaminare i log di controllo di tutti i controller di dominio per monitorare l'utilizzo di questa operazione.

> [!Note]  
> Nei domini di origine di Windows NT 4,0, il PDC, ovvero la destinazione delle operazioni nel dominio di origine, deve eseguire Service Pack 4 (SP4) e versioni successive per garantire un corretto supporto del controllo.

 

Il valore del registro di sistema seguente deve essere creato come \_ valore reg DWORD e impostato su 1 sul controller di dominio di origine per i controller di dominio di origine Windows NT 4,0 e windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

L'impostazione di questo valore Abilita le chiamate RPC sul trasporto TCP. Questa operazione è necessaria perché, per impostazione predefinita, le interfacce SAMRPC sono utilizzabili in remoto solo su named pipe. L'utilizzo di named pipe genera un sistema di gestione delle credenziali appropriato per gli utenti connessi in modo interattivo che effettuano chiamate di rete, ma non è flessibile per un processo di sistema che effettua chiamate di rete con credenziali fornite dall'utente. RPC su TCP è più adatto a tale scopo. L'impostazione di questo valore non diminuisce la sicurezza del sistema. Se questo valore viene creato o modificato, il controller di dominio di origine deve essere riavviato per rendere effettiva questa impostazione.

Un nuovo gruppo locale, " <SrcDomainName> $ $ $", deve essere creato nel dominio di origine a scopo di controllo.

## <a name="auditing"></a>Controllo

Le operazioni [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) vengono controllate per assicurarsi che gli amministratori di dominio di origine e di destinazione siano in grado di rilevare il momento in cui questa funzione è stata eseguita. Il controllo è obbligatorio nei domini di origine e di destinazione. **DsAddSidHistory** verifica che la modalità di controllo sia attiva in ogni dominio e che il controllo della gestione degli account degli eventi di esito positivo o negativo sia attiva. Nel dominio di destinazione viene generato un evento di controllo "Aggiungi cronologia SID" univoco per ogni operazione **DsAddSidHistory** riuscita o non riuscita.

Gli eventi di controllo "Aggiungi cronologia SID" non sono disponibili nei sistemi Windows NT 4,0. Per generare eventi di controllo che riflettono in modo non ambiguo l'utilizzo di [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) nel dominio di origine, vengono eseguite operazioni su un gruppo speciale il cui nome è l'identificatore univoco nel log di controllo. Un gruppo locale, " <SrcDomainName> $ $ $", il cui nome è composto dal nome NetBIOS del dominio di origine aggiunto con tre simboli del dollaro ($) (codice ASCII = 0x24 e Unicode = U + 0024), deve essere creato nel controller di dominio di origine prima di chiamare **DsAddSidHistory**. Ogni utente di origine e gruppo globale che è la destinazione di questa operazione viene aggiunto e quindi rimosso dall'appartenenza di questo gruppo. In questo modo vengono generati gli eventi di controllo Aggiungi membro ed Elimina membro nel dominio di origine, che può essere monitorato cercando gli eventi che fanno riferimento al nome del gruppo.

> [!Note]  
> Non è possibile controllare le operazioni [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) sui gruppi locali in un dominio di origine in modalità mista windows NT 4,0 o Windows 2000 perché i gruppi locali non possono essere membri di un altro gruppo locale e pertanto non possono essere aggiunti allo speciale <SrcDomainName> gruppo locale "$ $ $". Questa mancanza di controllo non presenta un problema di sicurezza per il dominio di origine, perché l'accesso alle risorse del dominio di origine non è influenzato da questa operazione. L'aggiunta del SID di un gruppo locale di origine a un gruppo locale di destinazione non concede l'accesso alle risorse di origine, protette da tale gruppo locale, a tutti gli utenti aggiuntivi. L'aggiunta di membri al gruppo locale di destinazione non concede l'accesso alle risorse di origine. Ai membri aggiunti viene concesso l'accesso solo ai server nel dominio di destinazione migrati dal dominio di origine, che può avere risorse protette dal SID del gruppo locale di origine.

 

## <a name="data-transmission-security"></a>Sicurezza della trasmissione dei dati

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) impone le misure di sicurezza seguenti:

-   Chiamato da una workstation Windows 2000, le credenziali del chiamante vengono usate per l'autenticazione e la protezione della privacy per la chiamata RPC al controller di dominio di destinazione. Se *SrcDomainCreds* non è **null**, sia la workstation che il controller di dominio di destinazione devono supportare la crittografia a 128 bit per la protezione della privacy. Se la crittografia a 128 bit non è disponibile e vengono specificati *SrcDomainCreds* , è necessario effettuare la chiamata nel controller di dominio di destinazione.
-   Il controller di dominio di destinazione comunica con il controller di dominio di origine utilizzando *SrcDomainCreds* o le credenziali del chiamante per autenticare reciprocamente e proteggere l'integrità la lettura del SID dell'account di origine (usando una ricerca Sam) e **sIDHistory** (usando una lettura LDAP).

## <a name="threat-models"></a>Modelli di rischio

La tabella seguente elenca le minacce potenziali associate alla chiamata [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) e risolve le misure di sicurezza attinenti alla minaccia specifica.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Potenziale minaccia</th>
<th>Misura di sicurezza</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Attacco man-in-the-Middle<br/> Un utente non autorizzato intercetta il <em>SID di ricerca della chiamata return dell'oggetto di origine</em> , sostituendo il SID dell'oggetto di origine con un SID arbitrario per l'inserimento in un oggetto di destinazione sIDHistory.<br/></td>
<td>Il <em>SID di ricerca dell'oggetto di origine</em> è una RPC autenticata, usando le credenziali di amministratore del chiamante, con la protezione dei messaggi di integrità dei pacchetti. Ciò garantisce che la chiamata return non possa essere modificata senza rilevamento. Il controller di dominio di destinazione crea un &quot; evento di controllo di aggiunta della cronologia SID univoco &quot; che riflette il SID aggiunto all'account di destinazione <strong>sIDHistory</strong>.<br/></td>
</tr>
<tr class="even">
<td>Dominio di origine Trojan<br/> Un utente non autorizzato crea un &quot; dominio di origine Trojan Horse &quot; in una rete privata con lo stesso SID di dominio e alcuni degli stessi SID di account del dominio di origine legittimo. L'utente non autorizzato tenta quindi di eseguire <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> in un dominio di destinazione per ottenere il SID di un account di origine. Questa operazione viene eseguita senza la necessità di credenziali di amministratore di dominio di origine reale e senza uscire da un audit trail nel dominio di origine reale. Il metodo dell'utente non autorizzato per la creazione del dominio di origine Trojan Horse può essere uno dei seguenti:
<ul>
<li>Ottenere una copia (backup BDC) del dominio di origine SAM.</li>
<li>Creare un nuovo dominio, modificare il SID di dominio su disco in modo che corrisponda al SID del dominio di origine legittimo, quindi creare un numero sufficiente di utenti per creare un'istanza di un account con il SID desiderato.</li>
<li>Creare una replica di integrazione applicativa dei dati. Sono necessarie le credenziali di amministratore del dominio di origine. Quindi, l'utente non autorizzato porta la replica in una rete privata per implementare l'attacco.</li>
</ul>
<br/></td>
<td>Sebbene esistano molti modi per consentire a un utente non autorizzato di recuperare o creare un SID dell'oggetto di origine desiderato, l'utente non autorizzato non può utilizzarlo per aggiornare <strong>sIDHistory</strong> di un account senza essere membro del gruppo di amministratori del dominio di destinazione. Poiché il controllo del controller di dominio di destinazione per l'appartenenza dell'amministratore di dominio è hardcoded, nel controller di dominio di destinazione non è disponibile alcun metodo per modificare i dati di controllo di accesso che proteggono questa funzione. Il tentativo di clonare un account di origine Trojan Horse viene controllato nel dominio di destinazione. Questo attacco viene mitigato riservando l'appartenenza al gruppo Domain Administrators solo per individui altamente attendibili.<br/></td>
</tr>
<tr class="odd">
<td>Modifica su disco della cronologia SID<br/> Un utente non autorizzato sofisticato, con credenziali di amministratore di dominio e con accesso fisico a un controller di dominio nel dominio di destinazione, potrebbe modificare un valore di account <strong>sIDHistory</strong> su disco.<br/></td>
<td>Questo tentativo non è abilitato dall'uso di <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Questo attacco è mitigato impedendo l'accesso fisico ai controller di dominio a tutti gli amministratori tranne quelli altamente attendibili.<br/></td>
</tr>
<tr class="even">
<td>Codice non autorizzato usato per rimuovere le protezioni<br/> Un utente non autorizzato o un amministratore non autorizzato con accesso fisico al codice del servizio directory potrebbe creare codice non autorizzato che:
<ol>
<li>Rimuove il controllo per l'appartenenza al gruppo Domain Administrators nel codice.</li>
<li>Modifica le chiamate sul controller di dominio di origine che punta il SID a una LookupSidFromName non controllata.</li>
<li>Rimuove le chiamate al log di controllo.</li>
</ol>
<br/></td>
<td>Un utente con accesso fisico al codice DS e sufficientemente esperto per creare codice non autorizzato ha la possibilità di modificare in modo arbitrario l'attributo <strong>sIDHistory</strong> di un account. L'API <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> non aumenta questo rischio per la sicurezza.<br/></td>
</tr>
<tr class="odd">
<td>Risorse vulnerabili ai SID rubati<br/> Se un utente non autorizzato ha avuto esito positivo utilizzando uno dei metodi descritti qui per modificare un account <strong>sIDHistory</strong>e se i domini delle risorse di interesse considerano attendibile il dominio dell'account utente non autorizzato, l'utente non autorizzato può ottenere l'accesso non autorizzato alle risorse del SID rubato, potenzialmente senza uscire da un audit trail nel dominio dell'account da cui il SID è stato rubato.<br/></td>
<td>Gli amministratori del dominio delle risorse proteggono le proprie risorse impostando solo le relazioni di trust che hanno senso dal punto di vista della sicurezza. L'utilizzo di <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> è limitato, nel dominio di destinazione attendibile, ai membri del gruppo Domain Administrators che dispongono già di autorizzazioni ampie nell'ambito delle rispettive responsabilità.<br/></td>
</tr>
<tr class="even">
<td>Dominio di destinazione non autorizzato<br/> Un utente non autorizzato crea un dominio di Windows 2000 con un account il cui <strong>sIDHistory</strong> contiene un SID che è stato rubato da un dominio di origine. L'utente non autorizzato utilizza questo account per l'accesso non autorizzato alle risorse.<br/></td>
<td>Per poter utilizzare <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>, l'utente non autorizzato richiede le credenziali di amministratore per il dominio di origine e lascia un audit trail sul controller di dominio di origine. Il dominio di destinazione non autorizzato ottiene accesso non autorizzato solo in altri domini che considerano attendibile il dominio non autorizzato, che richiede privilegi di amministratore in tali domini di risorse.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="operational-constraints"></a>Vincoli operativi

In questa sezione vengono descritti i vincoli operativi dell'utilizzo della funzione [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) .

Il SID di *SrcPrincipal* non deve essere già presente nella foresta di destinazione, come SID dell'account primario o nel **sIDHistory** di un account. L'eccezione è che [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) non genera un errore quando si tenta di aggiungere un SID a un **sIDHistory** che contiene un SID identico. Questo comportamento consente a **DsAddSidHistory** di essere eseguito più volte con un input identico, ottenendo risultati positivi e uno stato finale coerente, per semplificare l'utilizzo dello strumento.

> [!Note]  
> La latenza di replica del catalogo globale può fornire una finestra durante la quale possono essere creati SID duplicati. Tuttavia, i SID duplicati possono essere eliminati facilmente da un amministratore.

 

*SrcPrincipal* e *DstPrincipal* devono essere di uno dei tipi seguenti:

-   User
-   Gruppo con sicurezza abilitata, tra cui:

    <dl> Gruppo locale  
    Gruppo globale  
    Gruppo locale di dominio (solo modalità nativa di Windows 2000)  
    Gruppo universale (solo modalità nativa di Windows 2000)  
    </dl>

I tipi di oggetto *SrcPrincipal* e *DstPrincipal* devono corrispondere.

-   Se *SrcPrincipal* è un utente, *DstPrincipal* deve essere un utente.
-   Se *SrcPrincipal* è un gruppo locale o di dominio locale, *DstPrincipal* deve essere un gruppo locale di dominio.
-   Se *SrcPrincipal* è un gruppo globale o universale, *DstPrincipal* deve essere un gruppo globale o universale.

*SrcPrincipal* e *DstPrincipal* non possono essere di uno dei tipi seguenti: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ha esito negativo con un errore in questi casi)

-   Computer (workstation o controller di dominio)
-   Trust tra domini
-   Account duplicato temporaneo (funzionalità praticamente inutilizzata, legacy di LANman)
-   Account con SID ben noti. I SID ben noti sono identici in ogni dominio; in questo modo, l'aggiunta a un **sIDHistory** viola il requisito di unicità dei SID di una foresta di Windows 2000. Gli account con SID ben noti includono i seguenti gruppi locali:

    <dl> Operatori account  
    Administrators  
    Operatori di backup  
    Guests  
    Operatori di stampa  
    Replicator  
    Operatori server  
    Utenti  
    </dl>

Se *SrcPrincipal* dispone di un identificatore relativo (RID) noto e di un prefisso specifico del dominio, ovvero gli amministratori di dominio, gli utenti di dominio e i computer del dominio, *DstPrincipal* deve avere lo stesso RID noto per consentire il corretto funzionamento di [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) . Gli account con RID noto includono gli utenti e i gruppi globali seguenti:

-   Amministratore
-   Guest
-   Amministratori di dominio
-   Guest di dominio
-   Utenti del dominio

## <a name="setting-the-registry-value"></a>Impostazione del valore del registro di sistema

Nella procedura seguente viene illustrato come impostare il valore del registro di sistema TcpipClientSupport.

**Per impostare il valore del registro di sistema TcpipClientSupport**

1.  Creare il valore del registro di sistema seguente come \_ valore reg DWORD sul controller di dominio di origine e impostarne il valore su 1.

    **HKEY \_ Local \_ computer \\ System \\ CurrentControlSet \\ Control \\ LSA \\ TcpipClientSupport**

2.  Riavviare quindi il controller di dominio di origine. Questo valore del registro di sistema causa l'ascolto da parte di SAM su TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) avrà esito negativo se il valore non è impostato sul controller di dominio di origine.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Abilitazione del controllo degli eventi di gestione di utenti/gruppi

Nella procedura seguente viene illustrato come abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine o di destinazione di Windows 2000 o Windows Server 2003.

**Per abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine o di destinazione di Windows 2000 o Windows Server 2003**

1.  Nello snap-in MMC utenti e computer Active Directory selezionare il contenitore controller di dominio di destinazione.
2.  Fare clic con il pulsante destro del mouse su **controller di dominio** e scegliere **Proprietà**.
3.  Fare clic sulla scheda **criteri di gruppo** .
4.  Selezionare il **criterio controller di dominio predefiniti** e fare clic su **modifica**.
5.  In **Configurazione computer \\ impostazioni di Windows impostazioni di \\ sicurezza \\ \\ criteri locali controlla**, fare doppio clic su **Controlla gestione account**.
6.  Nella finestra **Controlla gestione account** selezionare il controllo di **esito positivo** e **negativo** . Gli aggiornamenti dei criteri diventano effettivi dopo un riavvio o dopo un aggiornamento.
7.  Verificare che il controllo sia abilitato visualizzando i criteri di controllo effettivi nello snap-in MMC Criteri di gruppo.

Nella procedura seguente viene illustrato come abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio Windows NT 4,0.

**Per abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio Windows NT 4,0**

1.  In **User Manager for Domains** fare clic sul menu **Policies** e selezionare **Audit**.
2.  Selezionare **Controlla questi eventi**.
3.  Per la **gestione di utenti e gruppi**, verificare l' **esito positivo e negativo**.

Nella procedura seguente viene illustrato come abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine Windows NT 4,0, Windows 2000 o Windows Server 2003.

**Per abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine Windows NT 4,0, Windows 2000 o Windows Server 2003**

1.  In **Gestione utenti per domini** fare clic sul menu **utente** e selezionare **nuovo gruppo locale**.
2.  Immettere un nome di gruppo composto dal nome NetBIOS del dominio di origine aggiunto con tre simboli di dollaro ($), ad esempio FABRIKAM $ $ $. Il campo descrizione deve indicare che questo gruppo viene usato per controllare l'uso di [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) o di operazioni di clonazione. Verificare che non vi siano membri nel gruppo. Fare clic su **OK**.

L'operazione [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ha esito negativo se il controllo di origine e di destinazione non è abilitato come descritto qui.

## <a name="set-up-trust-if-required"></a>Imposta attendibilità se necessario

Se viene soddisfatta una delle condizioni seguenti, è necessario stabilire una relazione di trust dal dominio di origine al dominio di destinazione (questo deve verificarsi in una foresta diversa):

-   Il dominio di origine è Windows Server 2003.
-   Il dominio di origine è Windows NT 4,0 e *SrcDomainCreds* è **null**.

 

 





