---
description: Fornisce una panoramica delle modifiche apportate ai controlli padre di Windows introdotti in Windows 8.
ms.assetid: 7EB33215-8F8B-4EA4-87E6-A98F0D014548
title: Novità della sicurezza delle famiglie di Windows 8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2123ec7f0d9c3af66528c6c203a3e8ea64bd0384
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881417"
---
# <a name="whats-new-in-windows-8-family-safety"></a>Novità di Windows 8 Family Safety

## <a name="overview-of-parental-controls-changes-for-windows-8"></a>Panoramica delle modifiche ai controlli padre per Windows 8

Lo scopo di questo documento è fornire una panoramica delle modifiche apportate ai controlli padre di Windows in Windows 8 e abilitare i provider di soluzioni per il controllo parentale di terze parti per sfruttare i vantaggi di queste modifiche. In questo documento si presuppone la familiarità dei lettori con i controlli padre per Windows 7 e Windows Vista e verranno riportate solo le modifiche apportate a questa funzionalità in Windows 8 rilevanti per lo sviluppo di soluzioni per il controllo parentale di terze parti.

## <a name="key-design-decisions-for-windows-8-parental-controlfamily-safety-changes"></a>Decisioni di progettazione principali per il controllo parentale di Windows 8/modifiche alla sicurezza della famiglia

Le modifiche apportate ai controlli padre introdotti in Windows 8 continuano l'obiettivo principale dell'introduzione di miglioramenti delle funzionalità e allo stesso tempo la coesistenza di soluzioni di controllo padre di terze parti con la funzionalità predefinita. È necessario apportare le modifiche seguenti:

-   Utilizzo di Microsoft Family Safety per fornire la gestione remota e il monitoraggio delle attività remote.
-   Integrazione del filtraggio Web come parte delle restrizioni Microsoft e della possibilità di visualizzare i report delle attività in un computer Windows 8.
-   La funzionalità dei controlli padre nel pannello di controllo è stata rinominata in Family Safety e verrà indicata in questo documento.
-   Le restrizioni relative al tempo interno sono state migliorate grazie alla possibilità di controllare la quantità totale di tempo al giorno in cui è possibile usare il computer (tempo), oltre alla possibilità di controllare i tempi in cui è possibile usare il computer (coprifuoco). Il coprifuoco era disponibile nelle versioni precedenti di Windows.
-   La funzionalità di sicurezza della famiglia di Windows 8 può essere attivata durante il flusso di creazione di account standard.
-   Le funzionalità di estensibilità dei controlli padre di Windows Vista e Windows 7 sono continuate a essere supportate dalla sicurezza della famiglia di prodotti Windows 8, inclusa la possibilità di soluzioni di terze parti di sostituire il filtro contenuto Web o di sostituire l'interfaccia utente di configurazione in box continuando a basarsi sull'implementazione di tempo, applicazione, restrizioni del gioco e filtro del contenuto Web.
-   L'attivazione del provider di terze parti disattiva la gestione remota e la creazione di report dei controlli di sicurezza della famiglia di Windows 8 tramite il sito Web Safety
-   L'estendibilità di terze parti per la sicurezza della famiglia è supportata solo per le applicazioni desktop Windows 8.

## <a name="family-safety-and-standard-account-creation-in-windows-8"></a>Sicurezza della famiglia e creazione di account standard in Windows 8

Nell'ambito della creazione di account standard in Windows 8, un amministratore ha la possibilità di attivare il monitoraggio dell'account per sicurezza della famiglia. Di seguito è riportato un elenco delle funzionalità e della capacità del provider di terze parti di controllarlo:

-   Nell'ultima schermata del flusso di creazione di account standard di Windows 8, un amministratore viene visualizzato con una casella di controllo per attivare la sicurezza della famiglia per l'account appena creato.
-   Se questa casella di controllo è selezionata, Family Safety viene attivato per l'account con le impostazioni seguenti:
    -   Segnalazione attività
    -   Tutte le restrizioni sono disattivate
-   Se l'amministratore ha utilizzato un account Microsoft per accedere a Windows, il computer Windows 8 verrà configurato per la gestione remota delle impostazioni di sicurezza della famiglia e i report delle attività di posta elettronica. Il sito Web per la sicurezza della famiglia può essere usato per gestire tale computer in modalità remota.
-   Se il provider di terze parti desidera che la casella di controllo sia presente nel flusso di creazione di un account standard, è necessario che il valore seguente sia presente tra i valori di registrazione del provider. Per ulteriori informazioni sui dettagli di registrazione del provider, vedere la sezione relativa alla [registrazione](what-s-new-in-windows-7-parental-controls.md) del provider nell'argomento What ' s New in Windows 7 Parental Controls.

    

    | Termine                                                                                                                         | Descrizione                                                                                                                                                                                                                                                                                  |
    |------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span id="AddUserVisible"></span><span id="adduservisible"></span><span id="ADDUSERVISIBLE"></span>AddUserVisible<br/> | Valore **DWORD** facoltativo diverso da zero che specifica che l'opzione CheckBox per attivare il monitoraggio della sicurezza della famiglia per un account appena creato deve essere visibile durante la creazione dell'account standard in Windows 8 dopo che il provider è stato selezionato come provider di sicurezza della famiglia corrente.<br/> |

    

     

-   Poiché i provider di terze parti sono progettati per sostituire l'interfaccia utente di configurazione predefinita per i controlli di sicurezza della famiglia, per impostazione predefinita, l'installazione e l'attivazione di un provider di terze parti genereranno l'opzione CheckBox per attivare la sicurezza della famiglia durante la creazione dell'account standard, in modo che non venga visualizzata.

## <a name="family-safety-top-level-user-interface-changes-in-windows-8"></a>Modifiche all'interfaccia utente di livello superiore per la sicurezza della famiglia in Windows 8

Windows 8 apporta le seguenti modifiche all'interfaccia utente di livello superiore del pannello di controllo dei controlli padre:

-   Quando i controlli di sicurezza della famiglia sono attivati per almeno un account standard in un computer Windows 8, viene visualizzato il collegamento Gestisci impostazioni nel sito Web per la sicurezza della famiglia, che consente a un amministratore di stabilire la gestione remota delle impostazioni di protezione per la famiglia di computer Windows 8 tramite il sito Web di sicurezza della famiglia.
-   Quando un computer Windows 8 è configurato per la gestione remota tramite il sito Web Family Safety, il controllo delle informazioni consente a un amministratore di disabilitare la gestione remota di un computer Windows 8 tramite il sito Web per la sicurezza della famiglia.
-   La sezione controlli è visibile solo quando almeno un provider di terze parti è registrato con la sicurezza della famiglia. L'interfaccia utente e la funzionalità di questa sezione sono identiche alla sezione controlli aggiuntivi nei controlli padre di Windows 7. Per ulteriori informazioni, vedere la sezione relativa alle modifiche dell'interfaccia utente di primo livello del controllo parentale nell'argomento [controlli padre di Windows 7](what-s-new-in-windows-7-parental-controls.md) .
-   Quando un provider di terze parti viene installato e selezionato come provider corrente, la gestione remota delle impostazioni di protezione della famiglia di computer Windows 8 tramite il sito Web per la sicurezza della famiglia è disabilitata.

## <a name="family-safety-in-box-restrictions-changes-in-windows-8"></a>Sicurezza della famiglia In-Box modifiche alle restrizioni in Windows 8

Windows 8 apporta le modifiche seguenti alle restrizioni incassate per la sicurezza della famiglia:

Restrizioni Web

-   L'implementazione è cambiata da un filtro del provider di servizi a più livelli (LSP) a un driver della piattaforma filtro Windows (WFP) che comunica con il processo di monitoraggio della sicurezza della famiglia eseguito nelle sessioni degli utenti.

Limiti di tempo

-   Le restrizioni relative all'ora in box sono state migliorate grazie alla possibilità di controllare la quantità totale di tempo al giorno in cui è possibile usare il computer (tempo), oltre alla possibilità di controllare i momenti in cui è possibile usare il computer (coprifuoco), disponibile nelle versioni precedenti di Windows.
-   Interfaccia utente per il coprifuoco consente il controllo indipendente per ogni giorno della settimana con granularità di mezz'ora.
-   L'interfaccia utente per il periodo di tempo consente ai controlli per i giorni feriali o i fine settimana o il controllo indipendente per ogni giorno della settimana con una granularità di 15 minuti.
-   Il meccanismo di cambio rapido utente (FUS) non viene più usato per bloccare forzatamente o bloccare l'accesso dell'utente controllato in un periodo di tempo bloccato. A tale scopo, viene usato un passaggio a un desktop separato.
-   Gli eventi di avviso di disconnessione non sono più disponibili per le applicazioni da sottoscrivere.

## <a name="family-safety-api-changes-in-windows-8"></a>Modifiche alle API per la sicurezza della famiglia in Windows 8

Le API usate per la sicurezza della famiglia espongono i criteri e le impostazioni delle restrizioni predefinite e la funzionalità di registrazione.

Registrazione

-   Gli eventi personalizzati non sono più supportati nel Visualizzatore report attività di sicurezza della famiglia.

Lettura/scrittura delle impostazioni dell'API WMI

-   WpcUserSettings: in precedenza, le restrizioni del timer supportavano una granularità di 1 ora. In Windows 8 la proprietà esistente rappresenta la prima mezz'ora per ogni ora. È stata aggiunta una nuova proprietà di mezz'ora per rappresentare la seconda metà di ogni ora. È stata introdotta una nuova proprietà aggiuntiva che rappresenta il limite di tempo giornaliero.

Filtro contenuto Web consente/blocca esportazione/importazione di un formato

-   La funzionalità di esportazione dell'elenco Consenti/blocca filtro contenuti Web non è più supportata.

Schema del provider WMI per le impostazioni della famiglia

-   Per riflettere i miglioramenti apportati alle restrizioni temporali, sono state apportate le aggiunte seguenti alla classe WpcUserSettings:
    -   `[write: ToInstance ToSubClass, Description("Logon Half-Hours (30 minute offset) mask for this user"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 LogonHalfHours[7];`
    -   `[write: ToInstance ToSubClass, Description("Daily minute allowance"): ToInstance ToSubClass, read: ToInstance ToSubClass] uint32 AllowanceMinutes[7];`

> [!Note]  
> Windows 8 usa una nuova chiave del registro di sistema per indicare che l'API Family Safety è abilitata per un determinato utente.
>
> **HKLM** \\ **Microsoft** \\ **Software** \\ di **Windows** \\ **CurrentVersion** \\ **Controlli padre** \\ **Utenti** \\ di **{UserSID}** \\ **Web** \\ **Filtra su**

 

La seguente chiave del registro di sistema è supportata solo per Windows 7.

**HKLM** \\ **Microsoft** \\ **Software** \\ di **Windows** \\ **CurrentVersion** \\ **Controlli padre** \\ **Utenti** \\ di **{UserSID}** \\ **Controlli padre su**

Per entrambe le chiavi, il valore "0x00" (**DWORD**) indica che la funzionalità è disabilitata per l'utente corrente e il valore "0x01" (**DWORD**) indica che la funzionalità è abilitata per l'utente corrente. Quando si tenta di leggere i valori di queste chiavi, sostituire il token "{UserSid}" con l'ID di sistema dell'utente.

 

 




