---
description: Sono disponibili diverse implementazioni di restrizioni.
ms.assetid: a00d9a3a-d052-492c-b9e7-3ecb1455a392
title: Controlli padre In-Box restrizioni & interfacce utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e5f155f8323fd6b006e510d75865ea25e278c70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318395"
---
# <a name="parental-controls-in-box-restrictions--user-interfaces"></a>Controlli padre In-Box restrizioni & interfacce utente

Sono disponibili diverse implementazioni di restrizioni.

-   [Restrizioni Web](#web-restrictions)
-   [Limiti di tempo](#time-limits)
-   [Giochi](#games)
-   [Consenti e blocca programmi specifici](#allow-and-block-specific-programs)

## <a name="web-restrictions"></a>Restrizioni Web

-   Filtro del contenuto Web incassato con un servizio di classificazione dinamica gratuito. Configurabile singolarmente per ogni utente controllato.
-   Filtra tutto il traffico HTTP quando è abilitato, restituisce una pagina formattata personalizzata se bloccata. Consente la funzionalità accettabile con tutti i browser principali. Monitorando tutte le richieste HTTP GET e post per una pagina, consente di bloccare le singole parti di pagine Web.
-   Altamente configurabile tramite l'interfaccia utente che consente o blocca elenchi di URL, set di impostazioni della categoria di classificazione semplificati o controllo ActiveX di più di 12 categorie, oltre a un criterio per bloccare i download di file.

> [!Note]  
> Il blocco di download di file effettivo richiede che le applicazioni implementino la restrizione, rispettando l'impostazione fornita.

 

-   Implementato come driver Windows Filtering Platform (WFP) che comunica con il processo di monitoraggio della sicurezza della famiglia eseguito nelle sessioni degli utenti. L'implementazione è cambiata da un filtro del provider di servizi a più livelli (LSP) a un driver della piattaforma filtro Windows (WFP) che comunica con il processo di monitoraggio della sicurezza della famiglia eseguito nelle sessioni degli utenti.

    **Windows 7 e Windows Vista:** Implementato come filtro LSP (Layered Service Provider) che comunica con un servizio con diritti limitati per la gestione e il monitoraggio complessivi. Il filtro rimane nella catena LSP quando è disabilitato, ma passa tutto il traffico attraverso. Questa implementazione è supportata solo per i sistemi operativi elencati.

-   Le applicazioni possono fornire interfaccia utente per mostrare il blocco parziale della pagina e rispettare i criteri per bloccare il download dei file. Possono anche richiamare un'API per consentire all'utente di richiedere l'autorizzazione per visualizzare una pagina bloccata. Questo override amministrativo richiama una piccola applicazione che Mostra gli URL tentati e che richiede le credenziali per consentirli.
-   Viene fornita un'API per casi speciali in cui è necessario che un'applicazione si registri per ignorare il filtro o che gli URL specifici siano sempre consentiti.
-   Poiché dovrebbe essere in esecuzione un solo filtro contenuto Web alla volta, terze parti possono registrarsi come filtro attivo e disabilitare il filtro predefinito. Questa estendibilità, associata alla possibilità di visualizzare un filtro di terze parti nell'interfaccia utente, consente una sostituzione semplice. I filtri devono rimuovere la registrazione quando vengono disinstallati.

## <a name="time-limits"></a>Limiti di tempo

-   Le restrizioni relative all'ora in box sono state migliorate grazie alla possibilità di controllare la quantità totale di tempo al giorno in cui è possibile usare il computer (tempo), oltre alla possibilità di controllare i momenti in cui è possibile usare il computer (coprifuoco), disponibile nelle versioni precedenti di Windows.
-   Interfaccia utente per il coprifuoco consente il controllo indipendente per ogni giorno della settimana con granularità di mezz'ora
-   L'interfaccia utente per il tempo consentito consente ai controlli per i giorni della settimana e i fine settimana o il controllo indipendente per ogni giorno della settimana con una granularità di 15 minuti
-   Il meccanismo di cambio rapido utente (FUS) non viene più usato per bloccare forzatamente o bloccare l'accesso dell'utente controllato in un periodo di tempo bloccato. A tale scopo, viene usato un passaggio a un desktop separato. Si noti che FUS mantiene lo stato dell'utente quando è bloccato.

## <a name="games"></a>Giochi

-   Funziona insieme a Esplora giochi.
-   Consente agli amministratori di controllare quali giochi possono essere riprodotti tramite un'interfaccia utente avanzata per la selezione di un sistema e un livello di classificazione dei giochi (oltre a descrittori, se presenti) e/o mediante l'abilitazione o il blocco dei titoli in modo specifico.
-   I metadati nelle classificazioni di giochi vengono ottenuti in uno dei due modi seguenti:
    -   I titoli supportati distribuiscono i propri file di definizione del gioco (GDFs).
    -   Circa 2000 titoli legacy sono coperti da un database interno.
-   Per l'imposizione vengono usati tre meccanismi:
    -   Negare gli ACL per l'accesso in scrittura controllato all'utente alla cartella del gioco.
    -   Terminazione del processo per i titoli legacy mediante la tecnologia shim di compatibilità delle applicazioni.
    -   Usare l'API di controllo automatico per i titoli supportati per bloccare l'esecuzione.
-   È consigliabile conoscere gli eventi relativi ai limiti temporali descritti nella sezione precedente.
-   La documentazione per GDFs e Game Explorer verrà fornita principalmente tramite le versioni di DirectX SDK.

## <a name="allow-and-block-specific-programs"></a>Consenti e blocca programmi specifici

-   Noto anche come restrizione generale dell'applicazione (GAR).
-   Disattivazione per impostazione predefinita. Se attivata, consente solo a un utente controllato di eseguire le applicazioni approvate da un amministratore, con eccezioni ragionevoli.
-   Interfaccia utente fornisce un elenco di nomi di programma con percorsi corrispondenti, ognuno con una casella di controllo Consenti. Viene inoltre fornito un pulsante Sfoglia.
-   Implementato usando criteri di restrizione software (SRP), noto anche come più sicuro:
    -   Impedisce l'esecuzione da tutti i supporti (chiavi USB, dischi floppy e così via).
    -   Usa le regole di percorso per specificare i programmi che possono essere eseguiti.
    -   Le autorizzazioni di scrittura ACL NTFS vengono revocate da qualsiasi elemento consentito per l'esecuzione da parte dell'utente controllato.
    -   Se bloccato e successivamente sottoposto a override per consentire, l'applicazione deve essere riavviata manualmente.
-   Le eccezioni sono le seguenti:
    -   Tutti i file binari necessari per il funzionamento di un subset di base di Windows.
    -   Tutti i file eseguibili registrati tramite un'API devono essere consentiti per un determinato utente.
    -   Giochi specificati come consentiti in restrizioni per i giochi.
-   Si noti che il comando RunAs è bloccato da progettazione per un utente quando GAR è on.

 

 



