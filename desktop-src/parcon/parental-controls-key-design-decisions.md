---
description: Decisioni di progettazione principali dei controlli padre
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Decisioni di progettazione principali dei controlli padre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39cb4be775a3380cb9fe7aa677362df31a2dc453
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058248"
---
# <a name="parental-controls-key-design-decisions"></a>Decisioni di progettazione principali dei controlli padre

Le principali decisioni di progettazione per lo sviluppo di controlli padre di Windows Vista sono:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dipendenza essenziale dalla funzionalità controllo dell'account utente di Windows Vista

Una decisione chiave per i controlli padre di Windows Vista consiste nel basarsi sulla nuova funzionalità di controllo dell'account utente per implementare le identità degli account con diritti ridotti, specialmente necessaria per le restrizioni offline sugli utenti controllati. Per ulteriori informazioni su UAC, vedere [la storia per sviluppatori di Windows Vista e Windows Server 2008: requisiti per lo sviluppo di applicazioni Windows Vista per il controllo dell'account utente (UAC)](/previous-versions/aa905330(v=msdn.10)). In breve, ogni account con diritti di amministratore dispone di privilegi sufficienti per eseguire il ruolo padre o tutore della visualizzazione dei dati di log e dell'impostazione dei criteri. I controlli padre possono essere impostati solo su utenti con diritti standard (in precedenza denominati account utente con privilegi minimi o LUAs), perché solo non possono modificare i registri e le impostazioni con elenchi di controllo di accesso (ACL) configurati solo per la scrittura da parte degli amministratori. In altre parole:

-   Un'identità padre o tutore è implicitamente uguale a un account con diritti di amministratore.
-   Gli utenti controllati dal padre devono essere utenti standard.

## <a name="nearly-all-settings-are-available-by-apis"></a>Quasi tutte le impostazioni sono disponibili dalle API

Ad eccezione di elementi come le definizioni di sistema di classificazione, le impostazioni disponibili per la manipolazione dall'interfaccia utente dei controlli padre possono essere modificate anche dalle API esposte. È necessario che i programmi implementino l'elevazione dei diritti amministrativi per modificare le impostazioni, come indicato in precedenza per UAC.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Vista Parental Controls è una tecnologia di solo consumo

I controlli padre di Windows Vista non sono destinati all'utilizzo con account di dominio. Come tecnologia consumer, i controlli padre non vengono distribuiti negli SKU aziendali di Windows Vista. Se un computer è aggiunto a un dominio, i collegamenti dell'interfaccia utente per la sicurezza della famiglia verranno eliminati.

Verrà fornito un meccanismo per esporre la funzionalità per il case aggiunto al dominio, ma solo gli account utente non di dominio possono essere configurati con i controlli padre.

 

 
