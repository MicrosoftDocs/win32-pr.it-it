---
title: Registrazione (piattaforma filtro Windows)
description: Windows Filtering Platform (WFP) consente di registrare le gocce di pacchetti e gli errori IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300813"
---
# <a name="logging-windows-filtering-platform"></a>Registrazione (piattaforma filtro Windows)

Windows Filtering Platform (WFP) consente di registrare le gocce di pacchetti e gli errori IKE/AuthIP.

Gli eventi registrati vengono definiti nel tipo enumerato di [**\_ \_ \_ tipo evento NET FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e sono i seguenti.

-   Errori in modalità principale IKE/AuthIP.
-   Errori in modalità rapida IKE/AuthIP.
-   Errori della modalità estesa AuthIP.
-   Pacchetti eliminati durante la classificazione.
-   Pacchetti eliminati da IPsec.

Per impostazione predefinita, la registrazione per WFP è abilitata per i pacchetti in ingresso unicast e per tutti i pacchetti in uscita (unicast, multicast e broadcast). La registrazione può essere abilitata per il resto dei pacchetti o disabilitata per tutti i pacchetti tramite la funzione di gestione [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) . Le impostazioni degli eventi vengono mantenute tra i riavvii.

Gli eventi registrati vengono archiviati in un log circolare, ovvero i nuovi eventi eseguono l'override di quelli obsoleti quando il log raggiunge le dimensioni massime e possono essere analizzati utilizzando le funzioni di [gestione degli eventi](fwp-mgmt-functions.md) fornite da WFP. Il registro eventi ha una dimensione massima di 128 KB e può avere circa 100 a 150 eventi.

Le funzioni di enumerazione in generale e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particolare creano uno snapshot del log al momento della creazione dell'handle di enumerazione. Le chiamate successive che usano lo stesso handle di enumerazione restituiscono il set successivo di elementi che seguono quelli nell'ultimo buffer di output.

Quando un'applicazione Disabilita la registrazione di WFP (chiamando [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), tutte le applicazioni sono interessate. Il registro eventi non viene pulito fino a quando un'applicazione non Abilita nuovamente la registrazione di WFP, ma non è possibile eseguire query sul registro eventi prima.

Il registro eventi di WFP viene svuotato dopo un riavvio.

 

 




