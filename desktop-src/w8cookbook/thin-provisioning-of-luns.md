---
title: Thin provisioning di unità logiche
description: Thin provisioning di unità logiche
ms.assetid: D64ECA7B-62AC-4C14-BE4B-84DA2E20C16B
keywords:
- LUN
- Lba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64ed5385322601e633f79755fb192f1dce578f2bec0f944fa2f4f412c32d69a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935051"
---
# <a name="thin-provisioning-of-logical-units"></a>Thin provisioning di unità logiche

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Windows Il thin provisioning è un'interfaccia per la soluzione di provisioning dell'archiviazione end-to-end. Per offrire un servizio di provisioning di archiviazione a disponibilità elevata, scalabile e semplice da usare, sono necessarie implementazioni affidabili dall'host del server al dispositivo di destinazione di archiviazione. La funzionalità di thin provisioning di Windows offre una visualizzazione sincrona dei dispositivi di archiviazione di thin provisioning all'amministratore di sistema, al responsabile IT e all'amministratore di archiviazione tramite l'identificazione delle unità logiche (LUN) con thin provisioning, la notifica delle soglie, la gestione dell'esaurimento delle risorse, il recupero dello spazio e il recupero dello stato di indirizzamento a blocchi logici (LBA). La Windows thin provisioning offre un modello di servizio di provisioning di archiviazione affidabile che può essere applicato ai sistemi di archiviazione client-server, all'archiviazione di virtualizzazione e ai servizi di archiviazione cloud. Microsoft garantirà l'elevata qualità della funzionalità di thin provisioning, Windows i requisiti del kit di certificazione hardware per il thin provisioning per i prodotti array di archiviazione.

La Windows di archiviazione di thin provisioning:

-   Consente agli amministratori di archiviazione di creare un LUN più grande con meno risorse disco fisico
-   Aggiunge o rimuove la risorsa disco fisico senza interrompere il servizio di provisioning di archiviazione
-   Avvisa gli utenti dell'utilizzo del volume di archiviazione tramite l'impostazione di soglia
-   Supporta il provisioning dell'archiviazione tramite la configurazione del pool di archiviazione condiviso
-   Aumenta o riduce le dimensioni del pool di archiviazione in base alla richiesta e all'utilizzo dello spazio di archiviazione

Riepilogo delle funzionalità Windows thin provisioning:

-   Identificazione LUN di thin provisioning
-   Handle per la notifica di soglia, l'esaurimento temporaneo delle risorse e l'esaurimento permanente delle risorse
-   Archiviazione recupero dello spazio
-   Mapping delle query sullo stato dei blocchi logici

## <a name="manifestation"></a>Manifestazione

Senza la corretta comprensione degli handle Windows thin provisioning LUN, l'app potrebbe non riuscire con un comportamento imprevisto o per una causa sconosciuta.

## <a name="using-thin-provisioning-luns"></a>Uso di LUN di thin provisioning

Per usare LUN con thin provisioning in Windows 8 o Windows Server 2012, gli amministratori di sistema e di archiviazione devono essere a conoscenza di questi aspetti:

-   Identificazione LUN di thin provisioning; Gli amministratori di sistema o gli utenti finali possono usare Defrag e l'utilità Archiviazione Optimizer per identificare il tipo di supporto del dispositivo di archiviazione
-   Quando viene raggiunta una soglia o un evento di esaurimento delle risorse permanente, Windows registra un evento di sistema per avvisare l'amministratore di sistema
-   Archiviazione recupero dello spazio può essere eseguito manualmente o automaticamente tramite la notifica di eliminazione dei file o l'utilità di pianificazione di Ottimizzazione archiviazione
-   Archiviazione amministratore deve implementare la notifica di soglia per avvisare l'amministratore di sistema o l'utente finale ed evitare interruzioni impreviste del servizio di archiviazione

## <a name="tests"></a>Test

-   Archiviazione array deve ricevere un Windows 8 thin provisioning per supportare Windows funzionalità di thin provisioning
-   Windows Thin Provisioning Hardware Certification Kit per l'array di archiviazione sarà uno strumento di test utile per verificare la funzionalità dell'array di archiviazione per Windows funzionalità di thin provisioning
-   Windows prevede che il LUN di thin provisioning e il LUN di provisioning completo funzionino nello stesso sistema senza problemi

## <a name="resources"></a>Risorse

-   [T10 SCSI Block Command Spec (SBC3r27)](https://www.t10.org/cgi-bin/ac.pl?t=f&f=sbc3r27.pdf)
-   [Servizi dashboard hardware](/windows-hardware/drivers/dashboard/)

 

 