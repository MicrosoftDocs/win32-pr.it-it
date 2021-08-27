---
title: Uso di DsAddSidHistory
description: Questo argomento descrive come usare la funzione DsAddSidHistory.
ms.assetid: cbf4983c-551d-4771-870e-a192ed898eb7
ms.tgt_platform: multiple
keywords:
- Uso di Active Directory DsAddSidHistory
- Active Directory Active Directory , tramite, uso di DsAddSidHistory
- DsAddSidHistory Active Directory , con
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e987a55f7fe39a8e4705f6aca9e44189e0f7a2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881839"
---
# <a name="using-dsaddsidhistory"></a>Uso di DsAddSidHistory

La [**funzione DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ottiene l'ID di sicurezza dell'account primario (SID) di un'entità di sicurezza da un dominio (il dominio di origine) e lo aggiunge all'attributo **sIDHistory** di un'entità di sicurezza in un altro dominio (di destinazione) in una foresta diversa. Quando il dominio di origine è in modalità nativa Windows 2000, questa funzione recupera anche i valori **sIDHistory** dell'entità di origine e li aggiunge all'oggetto **sIDHistory** dell'entità di destinazione.

L'aggiunta di SID a **sIDHistory** di un'entità di sicurezza è un'operazione sensibile alla sicurezza che concede in modo efficace all'entità di destinazione l'accesso a tutte le risorse accessibili all'entità di origine, a condizione che esistano relazioni di trust dai domini di risorse applicabili al dominio di destinazione.

In un dominio di Windows 2000 un utente accede a crea un token di accesso che contiene il SID e i SID del gruppo dell'account primario dell'utente, nonché l'utente **sIDHistory** e **sIDHistory** dei gruppi di cui l'utente è membro. La presenza di questi PRECEDENTI SID **(valori sIDHistory)** nel token dell'utente concede all'utente l'accesso alle risorse protette da elenchi di controllo di accesso (ACL) contenenti i SID precedenti.

Questa operazione facilita alcuni scenari di Windows 2000. In particolare, supporta uno scenario in cui vengono creati account in una nuova foresta di Windows 2000 per utenti e gruppi già esistenti in un ambiente di produzione Windows NT 4.0. Inserendo il SID dell'account Windows NT 4.0 nell'account Windows 2000 **sIDHistory**, l'accesso alle risorse di rete viene mantenuto per l'utente che accede al nuovo account Windows 2000.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) supporta anche la migrazione dei server di risorse dei controller di dominio di backup (ODC) di Windows NT 4.0 e dei controller di dominio e dei server membri in un dominio Windows 2000 in modalità nativa a un dominio di Windows 2000 come server membri. Questa migrazione richiede la creazione, nel dominio Windows 2000 di destinazione, di gruppi locali di dominio che contengono, in **sIDHistory**, i SID primari dei gruppi locali definiti nel BDC (o i gruppi locali di dominio a cui si fa riferimento negli ACL nei server Windows 2000) nel dominio di origine. Creando un gruppo locale di destinazione contenente **sIDHistory** e tutti i membri del gruppo locale di origine, l'accesso alle risorse del server di cui è stata eseguita la migrazione, protette da ACL che fanno riferimento al gruppo locale di origine, viene mantenuto per tutti i membri.

> [!Note]  
> [**L'uso di DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede una conoscenza delle implicazioni amministrative e di sicurezza più ampie in questi e in altri scenari. Per altre informazioni, vedere l'white paper "Planning Migration from Windows NT to Microsoft Windows 2000" (Pianificazione della migrazione da Windows NT a Microsoft Windows 2000), fornito come Dommig.doc negli strumenti di supporto di Windows 2000. Questa documentazione è disponibile anche nel CD del prodotto in Strumenti \\ di \\ supporto.

 

## <a name="authorization-requirements"></a>Requisiti di autorizzazione

[**DsAddSidHistory richiede**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) privilegi di amministratore nei domini di origine e di destinazione. In particolare, il chiamante di questa API deve essere un membro del gruppo Domain Administrators nel dominio di destinazione. Viene eseguito un controllo hard coded per questa appartenenza. Inoltre, il chiamante o l'account specificato nel *parametro SrcDomainCreds,* se diverso da **NULL,** deve essere membro del gruppo Administrators o Domain Administrators nel dominio di origine.

## <a name="domain-and-trust-requirements"></a>Requisiti di dominio e trust

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede che il dominio di destinazione sia in modalità nativa Windows 2000 o versione successiva, perché solo questo tipo di dominio supporta **l'attributo sIDHistory.** Il dominio di origine può essere Windows NT 4.0 o Windows 2000, in modalità mista o nativa. I domini di origine e di destinazione non devono essere nella stessa foresta. Windows NT 4.0 i domini sono per definizione non presenti in una foresta. Questo vincolo tra foreste garantisce che i SID duplicati, visualizzati come SID primari o **valori sIDHistory,** non siano creati nella stessa foresta.

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede un trust esterno dal dominio di origine al dominio di destinazione nei casi elencati nella tabella seguente.



| Caso                                                                             | Descrizione                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Il dominio di origine Windows 2000.<br/>                                    | **L'attributo sIDHistory** di origine, disponibile solo Windows 2000 domini di origine, può essere di sola lettura tramite LDAP, che richiede questo trust per la protezione dell'integrità.<br/>                                                                                             |
| Il dominio di origine Windows NT 4.0 e *SrcDomainCreds* è **NULL.**<br/> | La rappresentazione, necessaria per supportare le operazioni del dominio di origine utilizzando le credenziali del chiamante, dipende da questo trust. La rappresentazione richiede anche che il controller di dominio di destinazione abbia "Trusted for Delegation" abilitato per impostazione predefinita nei controller di dominio.<br/> |



 

Tuttavia, non è necessaria alcuna relazione di trust tra i domini di origine e di destinazione se il dominio di origine è Windows NT 4.0 e *SrcDomainCreds* non è **NULL.**

## <a name="source-domain-controller-requirements"></a>Requisiti del controller di dominio di origine

[**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) richiede che il controller di dominio, selezionato come destinazione per le operazioni nel dominio di origine, sia il PDC nei domini di Windows NT 4.0 o il Emulator PDC in domini Windows 2000. Il controllo del dominio di origine viene generato tramite operazioni di scrittura, pertanto il PDC è necessario nei domini di origine di Windows NT 4.0 e la restrizione solo PDC garantisce che i controlli **DsAddSidHistory** siano generati in un singolo computer. In questo modo si riduce la necessità di esaminare i log di controllo di tutti i controller di dominio per monitorare l'uso di questa operazione.

> [!Note]  
> In Windows NT di origine 4.0, il PDC (destinazione delle operazioni nel dominio di origine) deve eseguire Service Pack 4 (SP4) e versioni successive per garantire il supporto di controllo appropriato.

 

Il valore del Registro di sistema seguente deve essere creato come valore DWORD REG e impostato su 1 nel controller di dominio di origine per i controller di dominio di origine \_ Windows NT 4.0 e Windows 2000.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Control
            Lsa
               TcpipClientSupport
```

L'impostazione di questo valore abilita le chiamate RPC sul trasporto TCP. Questa operazione è necessaria perché, per impostazione predefinita, le interfacce SAMRPC sono utilizzabili in remoto solo su named pipe. L'uso di named pipe comporta un sistema di gestione delle credenziali adatto per gli utenti connessi in modo interattivo che effettuano chiamate in rete, ma non è flessibile per un processo di sistema che effettua chiamate di rete con le credenziali fornite dall'utente. RPC su TCP è più adatto a tale scopo. L'impostazione di questo valore non riduce la sicurezza del sistema. Se questo valore viene creato o modificato, è necessario riavviare il controller di dominio di origine per l'applicazione di questa impostazione.

A scopo di controllo, è necessario creare un nuovo gruppo &lt; locale, "SrcDomainName &gt; $$$", nel dominio di origine.

## <a name="auditing"></a>Controllo

[**Le operazioni DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) vengono verificate per garantire che gli amministratori di dominio di origine e di destinazione siano in grado di rilevare quando questa funzione è stata eseguita. Il controllo è obbligatorio sia nel dominio di origine che in quello di destinazione. **DsAddSidHistory** verifica che la modalità di controllo sia attivata in ogni dominio e che il controllo di Gestione account degli eventi di esito positivo/negativo sia attivata. Nel dominio di destinazione viene generato un evento di controllo "Aggiungi cronologia Sid" univoco per ogni operazione **DsAddSidHistory** riuscita o non riuscita.

Gli eventi di controllo "Aggiungi cronologia Sid" univoci non sono disponibili Windows NT sistemi 4.0. Per generare eventi di controllo che riflettono senza ambiguità l'uso di [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) nel dominio di origine, esegue operazioni su un gruppo speciale il cui nome è l'identificatore univoco nel log di controllo. È necessario creare un gruppo locale, "SrcDomainName $$$", il cui nome è composto dal nome NetBIOS del dominio di origine accodato da tre simboli di dollaro &lt; ($) (codice ASCII = 0x24 e Unicode = U+0024), nel controller di dominio di origine prima di chiamare &gt; **DsAddSidHistory**. Ogni utente di origine e gruppo globale che rappresenta la destinazione di questa operazione viene aggiunto e quindi rimosso dall'appartenenza di questo gruppo. In questo modo vengono generati gli eventi di controllo Add Member e Delete Member nel dominio di origine, che possono essere monitorati cercando gli eventi che fanno riferimento al nome del gruppo.

> [!Note]  
> Non è possibile controllare le operazioni [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) sui gruppi locali in un dominio di origine Windows NT 4.0 o Windows 2000 in modalità mista perché i gruppi locali non possono essere resi membri di un altro gruppo locale e pertanto non possono essere aggiunti al gruppo locale speciale " &lt; SrcDomainName &gt; $$". Questa mancanza di controllo non presenta un problema di sicurezza per il dominio di origine, perché l'accesso alle risorse del dominio di origine non è interessato da questa operazione. L'aggiunta del SID di un gruppo locale di origine a un gruppo locale di destinazione non concede l'accesso alle risorse di origine, protette da tale gruppo locale, ad altri utenti. L'aggiunta di membri al gruppo locale di destinazione non concede loro l'accesso alle risorse di origine. Ai membri aggiunti viene concesso l'accesso solo ai server nel dominio di destinazione migrati dal dominio di origine, che può avere risorse protette dal SID del gruppo locale di origine.

 

## <a name="data-transmission-security"></a>Sicurezza della trasmissione dei dati

[**DsAddSidHistory applica**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) le misure di sicurezza seguenti:

-   Chiamato da una workstation Windows 2000, le credenziali del chiamante vengono usate per autenticare e proteggere la privacy della chiamata RPC al controller di dominio di destinazione. Se *SrcDomainCreds* non è **NULL,** sia la workstation che il controller di dominio di destinazione devono supportare la crittografia a 128 bit per proteggere la privacy delle credenziali. Se la crittografia a 128 bit non è disponibile e si specifica *SrcDomainCreds,* la chiamata deve essere effettuata nel controller di dominio di destinazione.
-   Il controller di dominio di destinazione comunica con il controller di dominio di origine usando *SrcDomainCreds* o le credenziali del chiamante per l'autenticazione reciproca e la protezione dell'integrità della lettura del SID dell'account di origine (tramite una ricerca SAM) e **sIDHistory** (tramite una lettura LDAP).

## <a name="threat-models"></a>Modelli di minaccia

La tabella seguente elenca le potenziali minacce associate alla chiamata [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) e risolve le misure di sicurezza pertinenti alla minaccia specifica.




| Potenziale minaccia | Misura di sicurezza | 
|------------------|------------------|
| Attacco man-in-the-middle<br /> Un utente non autorizzato intercetta il <em>SID</em> di ricerca della chiamata di restituzione dell'oggetto di origine, sostituendo il SID dell'oggetto di origine con un SID arbitrario per l'inserimento in un SIDhistory dell'oggetto di destinazione.<br /> | Il <em>SID di ricerca dell'oggetto</em> di origine è una RPC autenticata, che usa le credenziali di amministratore del chiamante, con protezione dei messaggi di integrità dei pacchetti. In questo modo si garantisce che la chiamata di ritorno non possa essere modificata senza rilevamento. Il controller di dominio di destinazione crea un evento di controllo "Aggiungi cronologia SID" univoco che riflette il SID aggiunto all'account <strong>di destinazione sIDHistory.</strong><br /> | 
| Dominio di origine Trojan<br /> Un utente non autorizzato crea un dominio di origine "Trojan Horse" in una rete privata con lo stesso SID di dominio e alcuni degli stessi SID account del dominio di origine legittimo. L'utente non autorizzato tenta quindi di <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>eseguire DsAddSidHistory</strong></a> in un dominio di destinazione per ottenere il SID di un account di origine. Questa operazione viene eseguita senza la necessità di credenziali di amministratore di dominio di origine reale e senza lasciare un audit trail nel dominio di origine reale. Il metodo dell'utente non autorizzato per la creazione del dominio di origine Trojan Horse può essere uno dei seguenti:<ul><li>Ottenere una copia (backup BDC) del dominio di origine SAM.</li><li>Creare un nuovo dominio, modificando il SID del dominio su disco in modo che corrisponda al SID del dominio di origine legittimo, quindi creare un numero sufficiente di utenti per creare un'istanza di un account con il SID desiderato.</li><li>Creare una replica BDC. Sono necessarie le credenziali di amministratore del dominio di origine. L'utente non autorizzato porta quindi la replica a una rete privata per implementare l'attacco.</li></ul><br /> | Anche se esistono molti modi per un utente non autorizzato di recuperare o creare un SID dell'oggetto di origine desiderato, l'utente non autorizzato non può usarlo per aggiornare il valore <strong>sIDHistory</strong> di un account senza essere membro del gruppo Domain Administrators di destinazione. Poiché il controllo, nel controller di dominio di destinazione, per l'appartenenza all'amministratore di dominio è hard coded, nel controller di dominio di destinazione, non esiste alcun metodo per eseguire una modifica del disco per modificare i dati di controllo di accesso che proteggono questa funzione. Viene eseguito un tentativo di clonazione di un account di origine Trojan Horse nel dominio di destinazione. Questo attacco viene mitigato riservando l'appartenenza al gruppo Domain Administrators solo per utenti altamente attendibili.<br /> | 
| Modifica su disco della cronologia SID<br /> Un utente sofisticato non autorizzato, con credenziali di amministratore di dominio e con accesso fisico a un controller di dominio nel dominio di destinazione, potrebbe modificare un valore <strong>sIDHistory</strong> dell'account su disco.<br /> | Questo tentativo non è abilitato tramite <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>. Questo attacco viene mitigato impedendo l'accesso fisico ai controller di dominio a tutti gli amministratori ad eccezione di quelli altamente attendibili.<br /> | 
| Codice non autorizzato usato per rimuovere le protezioni<br /> Un utente non autorizzato o un amministratore non autorizzato con accesso fisico al codice del servizio directory potrebbe creare codice non autorizzato che:<ol><li>Rimuove il controllo dell'appartenenza al gruppo Domain Administrators nel codice.</li><li>Modifica le chiamate nel controller di dominio di origine che punta al SID a un lookupSidFromName che non è stato audito.</li><li>Rimuove le chiamate al log di controllo.</li></ol><br /> | Un utente con accesso fisico al codice DS e sufficientemente esperto per creare codice non autorizzato può modificare arbitrariamente l'attributo <strong>sIDHistory</strong> di un account. <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>L'API DsAddSidHistory</strong></a> non aumenta questo rischio per la sicurezza.<br /> | 
| Risorse vulnerabili ai SID rubati<br /> Se un utente non autorizzato è riuscito a usare uno dei metodi descritti qui per modificare un account <strong>sIDHistory</strong>e se i domini di risorse di interesse considera attendibile il dominio dell'account utente non autorizzato, l'utente non autorizzato può ottenere l'accesso non autorizzato alle risorse del SID rubato, potenzialmente senza lasciare un audit trail nel dominio dell'account da cui è stato rubato il SID.<br /> | Gli amministratori di dominio delle risorse proteggono le risorse configurando solo le relazioni di trust che hanno senso dal punto di vista della sicurezza. L'uso di <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a> è limitato, nel dominio di destinazione trusted, ai membri del gruppo Domain Administrators che hanno già ampie autorizzazioni nell'ambito delle rispettive responsabilità.<br /> | 
| Dominio di destinazione non autorizzato<br /> Un utente non autorizzato crea un Windows 2000 con un account il cui <strong>sIDHistory</strong> contiene un SID rubato da un dominio di origine. L'utente non autorizzato usa questo account per l'accesso non autorizzato alle risorse.<br /> | L'utente non autorizzato richiede le credenziali di amministratore per il dominio di origine per usare <a href="/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya"><strong>DsAddSidHistory</strong></a>e lascia un audit trail nel controller di dominio di origine. Il dominio di destinazione non autorizzato ottiene l'accesso non autorizzato solo in altri domini che considera attendibile il dominio non autorizzato, che richiede privilegi di amministratore in tali domini di risorse.<br /> | 




 

## <a name="operational-constraints"></a>Vincoli operativi

Questa sezione descrive i vincoli operativi dell'uso [**della funzione DsAddSidHistory.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)

Il SID *di SrcPrincipal* non deve esistere già nella foresta di destinazione, come SID dell'account primario o nella **sIDHistory** di un account. L'eccezione è che [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) non genera un errore durante il tentativo di aggiungere un SID a **un oggetto sIDHistory** che contiene un SID identico. Questo comportamento consente **l'esecuzione di DsAddSidHistory** più volte con input identico, con esito positivo e uno stato finale coerente, per semplificare l'uso da parte degli sviluppatori di strumenti.

> [!Note]  
> La latenza di replica del catalogo globale può fornire una finestra durante la quale è possibile creare SID duplicati. Tuttavia, i SID duplicati possono essere facilmente eliminati da un amministratore.

 

*SrcPrincipal* e *DstPrincipal* devono essere di uno dei tipi seguenti:

-   Utente
-   Gruppo abilitato per la sicurezza, tra cui:

    <dl> Gruppo locale  
    Gruppo globale  
    Gruppo locale di dominio (Windows solo in modalità nativa 2000)  
    Gruppo universale (Windows solo in modalità nativa 2000)  
    </dl>

I tipi di oggetto *SrcPrincipal* e *DstPrincipal* devono corrispondere.

-   Se *SrcPrincipal* è un utente, *DstPrincipal* deve essere un utente.
-   Se *SrcPrincipal è* un gruppo locale o locale di dominio, *DstPrincipal* deve essere un gruppo locale di dominio.
-   Se *SrcPrincipal è* un gruppo globale o universale, *DstPrincipal* deve essere un gruppo globale o universale.

*SrcPrincipal* e *DstPrincipal* non possono essere di uno dei tipi seguenti: ([**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ha esito negativo con un errore in questi casi)

-   Computer (workstation o controller di dominio)
-   Trust tra domini
-   Account duplicato temporaneo (funzionalità virtualmente inutilizzata, legacy di LANman)
-   Account con SID noti. I SID noti sono identici in ogni dominio. in modo da aggiungerli a **un oggetto sIDHistory** violerebbe il requisito di univocità SID di una foresta Windows 2000. Gli account con SID noti includono i gruppi locali seguenti:

    <dl> Operatori di account  
    Administrators  
    Operatori di backup  
    Guests  
    Operatori di stampa  
    Replicator  
    Operatori server  
    Utenti  
    </dl>

Se *SrcPrincipal* ha un identificatore relativo noto (RID) e un prefisso specifico di dominio, ovvero amministratori di dominio, utenti di dominio e computer di dominio, *DstPrincipal* deve disporre dello stesso RID noto per consentire l'esito positivo di [**DsAddSidHistory.**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) Gli account con RID noti includono gli utenti e i gruppi globali seguenti:

-   Amministratore
-   Guest
-   Amministratori di dominio
-   Guest di dominio
-   Utenti del dominio

## <a name="setting-the-registry-value"></a>Impostazione del valore del Registro di sistema

La procedura seguente illustra come impostare il valore del Registro di sistema TcpipClientSupport.

**Per impostare il valore del Registro di sistema TcpipClientSupport**

1.  Creare il valore del Registro di sistema seguente come valore DWORD REG nel controller di dominio di origine \_ e impostarne il valore su 1.

    **HKEY \_ LOCAL \_ MACHINE \\ SYSTEM \\ CurrentControlSet \\ Control \\ Lsa \\ TcpipClientSupport**

2.  Riavviare quindi il controller di dominio di origine. Questo valore del Registro di sistema fa sì che il SAM sia in ascolto su TCP/IP. [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) avrà esito negativo se questo valore non è impostato nel controller di dominio di origine.

## <a name="enabling-auditing-of-usergroup-management-events"></a>Abilitazione del controllo degli eventi di gestione utenti/gruppi

La procedura seguente illustra come abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine o di destinazione Windows 2000 o Windows Server 2003.

**Per abilitare il controllo degli eventi di gestione utente/gruppo in un dominio di origine o di destinazione Windows 2000 o Windows Server 2003**

1.  Nello Utenti e computer di Active Directory snap-in MMC selezionare il contenitore Controller di dominio di dominio di destinazione.
2.  Fare clic con il **pulsante destro del mouse** su Controller di dominio e scegliere **Proprietà**.
3.  Fare clic **sulla Criteri di gruppo** di controllo.
4.  Selezionare i **criteri controller di dominio predefiniti e** fare clic su **Modifica**.
5.  In **Configurazione computer Windows Impostazioni sicurezza Impostazioni criteri locali Criteri di \\ \\ \\ \\ controllo** fare doppio clic su **Controlla gestione account**.
6.  Nella finestra **Audit Account Management (Controlla** gestione account) selezionare **Success (Operazione riuscita)** **e Failure** auditing (Controllo degli errori). Gli aggiornamenti dei criteri hanno effetto dopo un riavvio o dopo un aggiornamento.
7.  Verificare che il controllo sia abilitato visualizzando i criteri di controllo effettivi nello Criteri di gruppo snap-in MMC.

La procedura seguente illustra come abilitare il controllo degli eventi di gestione utenti/gruppi in un dominio Windows NT 4.0.

**Per abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio Windows NT 4.0**

1.  In **Gestione utenti per domini** fare clic sul menu **Criteri** e selezionare **Controlla**.
2.  Selezionare **Controlla questi eventi**.
3.  Per **Gestione utenti e gruppi,** selezionare Esito positivo e Non **riuscito.**

La procedura seguente illustra come abilitare il controllo degli eventi di gestione utenti/gruppi in un dominio di origine Windows NT 4.0, Windows 2000 o Windows Server 2003.

**Per abilitare il controllo degli eventi di gestione di utenti/gruppi in un dominio di origine Windows NT 4.0, Windows 2000 o Windows Server 2003**

1.  In **Gestione utenti per domini** fare clic sul menu **Utente** e selezionare Nuovo **gruppo locale.**
2.  Immettere un nome di gruppo composto dal nome NetBIOS del dominio di origine aggiunto con tre segni di dollaro ($), ad esempio FABRIKAM$$$. Il campo della descrizione deve indicare che questo gruppo viene usato per controllare l'uso [**di DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) o delle operazioni di clonazione. Assicurarsi che non siano presenti membri nel gruppo. Fare clic su **OK**.

[**L'operazione DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya) ha esito negativo se il controllo di origine e destinazione non è abilitato come descritto di seguito.

## <a name="set-up-trust-if-required"></a>Configurare l'attendibilità se necessario

Se si verifica una delle condizioni seguenti, è necessario stabilire una relazione di trust dal dominio di origine al dominio di destinazione ( questa operazione deve verificarsi in una foresta diversa):

-   Il dominio di origine Windows Server 2003.
-   Il dominio di origine Windows NT 4.0 e *SrcDomainCreds* è **NULL.**

 

 





