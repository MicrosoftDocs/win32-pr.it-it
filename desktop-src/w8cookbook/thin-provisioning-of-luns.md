---
title: Thin provisioning di unità logiche
description: Thin provisioning di unità logiche
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- LBA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4abb6fa3cec112737b23e3cd658a48984cb0fcd1
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104047499"
---
# <a name="thin-provisioning-of-logical-units"></a>Thin provisioning di unità logiche

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Il thin provisioning di Windows è un'interfaccia per la soluzione di provisioning dell'archiviazione end-to-end. Per offrire un servizio di provisioning di archiviazione estremamente disponibile, scalabile e intuitivo, richiede implementazioni affidabili dall'host server al dispositivo di destinazione di archiviazione. La funzionalità Windows Thin provisioning fornisce una visualizzazione sincrona dei dispositivi di archiviazione con thin provisioning all'amministratore di sistema, al responsabile IT e all'amministratore dell'archiviazione tramite l'identificazione dell'unità logica (LUN) con thin provisioning, la notifica delle soglie, la gestione dell'esaurimento delle risorse, il recupero dello spazio e il recupero dello stato del blocco logico (LBA). La funzionalità Windows Thin provisioning presenta un modello di servizio di provisioning dell'archiviazione affidabile che può essere applicato ai sistemi di archiviazione client-server, all'archiviazione di virtualizzazione e ai servizi di archiviazione cloud. Microsoft assicurerà la qualità elevata della funzionalità di thin provisioning imponendo i requisiti del kit di certificazione hardware di Windows Thin provisioning per i prodotti array di archiviazione.

Soluzione di archiviazione thin provisioning di Windows:

-   Consente agli amministratori di archiviazione di creare un LUN più grande con meno risorse disco fisico
-   Aggiunge o rimuove una risorsa disco fisico senza interrompere il servizio di provisioning dell'archiviazione
-   Avvisa gli utenti dell'utilizzo del volume di archiviazione tramite l'impostazione della soglia
-   Supporta il provisioning dell'archiviazione tramite la configurazione del pool di archiviazione condiviso
-   Aumenta o diminuisce le dimensioni del pool di archiviazione in base alla domanda e all'utilizzo dello spazio di archiviazione

Riepilogo delle funzionalità di Windows Thin provisioning:

-   Identificazione del LUN con thin provisioning
-   Handle per la notifica delle soglie, l'esaurimento delle risorse temporanee e l'esaurimento delle risorse permanente
-   Recupero dello spazio di archiviazione
-   Query sullo stato del mapping di blocchi logici

## <a name="manifestation"></a>Manifestazione

Senza la conoscenza corretta degli handle di Windows per il thin provisioning LUN, l'app potrebbe non riuscire con un comportamento imprevisto o per una ragione sconosciuta.

## <a name="using-thin-provisioning-luns"></a>Uso di LUN con thin provisioning

Per usare i LUN con thin provisioning in Windows 8 o Windows Server 2012, gli amministratori di sistema e di archiviazione devono essere a conoscenza di questi aspetti:

-   Identificazione del LUN con thin provisioning; gli amministratori di sistema o gli utenti finali possono usare Defrag e l'utilità di ottimizzazione archiviazione per identificare il tipo di supporto del dispositivo di archiviazione
-   Quando viene raggiunta una soglia o un evento di esaurimento delle risorse permanente, Windows registrerà un evento di sistema per avvisare l'amministratore di sistema
-   Il recupero dello spazio di archiviazione può essere eseguito manualmente o automaticamente tramite la notifica di eliminazione file o l'utilità di pianificazione di storage Optimizer
-   L'amministratore di archiviazione deve implementare la notifica delle soglie per avvisare l'amministratore del sistema o l'utente finale ed evitare interruzioni impreviste del servizio di archiviazione

## <a name="tests"></a>Test

-   Array di archiviazione deve ricevere il certificato di thin provisioning di Windows 8 per supportare le funzionalità di thin provisioning di Windows
-   Il kit di certificazione hardware di Windows Thin provisioning per array di archiviazione sarà uno strumento di test utile per verificare la funzionalità dell'array di archiviazione per il supporto delle funzionalità thin provisioning di Windows
-   Windows prevede che il LUN di thin provisioning e il LUN di provisioning completo funzionino nello stesso sistema senza problemi

## <a name="resources"></a>Risorse

-   [Specifica del comando di blocco SCSI T10 (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Servizi dashboard hardware](/windows-hardware/drivers/dashboard/)

 

 