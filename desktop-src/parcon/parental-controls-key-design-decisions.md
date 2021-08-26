---
description: Controllo genitori Decisioni di progettazione chiave
ms.assetid: 0b41cf81-0770-4408-97a8-a178fae78d23
title: Controllo genitori Decisioni di progettazione chiave
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fef8f1e1d1b629c9fbb4354fb266376453938a35bde80e7b60f57be8f77da70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939291"
---
# <a name="parental-controls-key-design-decisions"></a>Controllo genitori Decisioni di progettazione chiave

Le principali decisioni di progettazione nello sviluppo di Windows Controllo genitori di Vista sono:

## <a name="essential-dependency-on-windows-vista-user-account-control-uac-feature"></a>Dipendenza essenziale dalla funzionalità Windows controllo dell'account utente di Vista

Una decisione chiave per il controllo genitori di Windows Vista è affidarsi alla nuova funzionalità Controllo dell'account utente per implementare le identità degli account con diritti ridotti, particolarmente necessarie per le restrizioni offline per gli utenti controllati. Per altre informazioni sul controllo dell'account utente, vedere The [Windows Vista and Windows Server 2008 Developer Story: Windows Vista Application Development Requirements for User Account Control (UAC)](/previous-versions/aa905330(v=msdn.10))(Storia per gli sviluppatori di Windows Vista per il controllo dell'account utente). In breve, ogni account con diritti di amministratore ha in effetti i privilegi per eseguire il ruolo padre o di guardiano della visualizzazione dei dati di log e dell'impostazione dei criteri. Il controllo genitori può essere impostato solo per gli utenti con diritti standard (in precedenza denominati account utente con privilegi minimi o LUA), perché solo questi non possono modificare i log e le impostazioni con elenchi di controllo di accesso (ACL) configurati solo per gli amministratori per la scrittura. In altre parole:

-   Un'identità padre o di tutela equivale in modo implicito a un account con diritti di amministratore.
-   Gli utenti controllati dai genitori devono essere utenti standard.

## <a name="nearly-all-settings-are-available-by-apis"></a>Quasi tutti Impostazioni sono disponibili dalle API

Ad eccezione di elementi come le definizioni di sistema ratings, le impostazioni disponibili per la manipolazione da parte del controllo genitori Interfaccia utente possono essere modificate anche dalle API esposte. È necessario che i programmi implementino l'elevazione dei diritti amministrativi per modificare le impostazioni, come indicato in precedenza per controllo dell'account utente.

## <a name="windows-vista-parental-controls-is-a-consumer-only-technology"></a>Windows Vista Parent Controls è una tecnologia solo consumer

Windows Vista Parent Controls non deve essere usato con gli account di dominio. Come tecnologia consumer, controllo genitori non viene distribuito negli SKU aziendali di Windows Vista. Se un computer fa parte di un dominio, i Family Safety dell'interfaccia utente verranno eliminati.

Verrà fornito un meccanismo per esporre la funzionalità per il caso aggiunto a un dominio, ma solo gli account utente non di dominio possono essere configurati con Controllo genitori.

 

 
