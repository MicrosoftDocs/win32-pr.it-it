---
title: Registrazione (Windows Filtering Platform)
description: Windows Filtering Platform (WFP) consente di registrare le eliminazioni di pacchetti e gli errori IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1500be04837126e6907b663e4496c58c05380d313a1465b9c8db05b5ea39d832
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068911"
---
# <a name="logging-windows-filtering-platform"></a>Registrazione (Windows Filtering Platform)

La Windows filtering platform (WFP) fornisce la registrazione delle eliminazioni di pacchetti e degli errori IKE/AuthIP.

Gli eventi registrati sono definiti nel tipo [**enumerato FWPM \_ NET EVENT \_ \_ TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e sono i seguenti.

-   Errori della modalità principale IKE/AuthIP.
-   Errori in modalità rapida IKE/AuthIP.
-   Errori in modalità estesa AuthIP.
-   Pacchetti eliminati durante la classificazione.
-   Pacchetti eliminati da IPsec.

Per impostazione predefinita, la registrazione per WFP è abilitata per i pacchetti in ingresso unicast e per tutti i pacchetti in uscita (unicast, multicast e broadcast). La registrazione può essere abilitata per il resto dei pacchetti o disabilitata per tutti i pacchetti tramite la funzione di gestione [**FwpmEngineSetOptions0.**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) Le impostazioni degli eventi vengono mantenute tra un riavvio e l'altro.

Gli eventi registrati vengono archiviati in un log circolare, che è un nuovo evento che [](fwp-mgmt-functions.md) sostituisce quelli precedenti quando il log raggiunge le dimensioni massime e può essere analizzato usando le funzioni di gestione degli eventi fornite da WFP. Il registro eventi ha una dimensione massima di 128 KB e può contenere circa 100-150 eventi.

Le funzioni di enumerazione in generale e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particolare, estrarranno uno snapshot del log al momento della creazione dell'handle di enumerazione. Le chiamate successive che usano lo stesso handle di enumerazione restituiscono il set successivo di elementi che segue quelli nell'ultimo buffer di output.

Quando un'applicazione disabilita la registrazione WFP (chiamando [**FwpmEngineSetOptions0),**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)tutte le applicazioni sono interessate. Il registro eventi non viene pulito fino a quando un'applicazione non abilita nuovamente la registrazione DI WINDOWS, ma non è possibile eseguire query sul registro eventi prima di quel momento.

Il registro eventi WFP viene svuotato dopo un riavvio.

 

 




