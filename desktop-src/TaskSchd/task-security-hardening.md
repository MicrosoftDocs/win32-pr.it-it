---
title: Protezione avanzata delle attività
description: L'uso della funzionalità di protezione avanzata delle attività consentirà ai proprietari delle attività di eseguire le attività con i privilegi minimi necessari.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221449"
---
# <a name="task-security-hardening"></a>Protezione avanzata delle attività

L'uso della funzionalità di protezione avanzata delle attività consentirà ai proprietari delle attività di eseguire le attività con i privilegi minimi necessari. Si noti che questa funzionalità è abilitata per impostazione predefinita e i proprietari delle attività possono apportare ulteriori modifiche utilizzando il tipo di identificatore di sicurezza del token del processo attività e la matrice dei privilegi necessari per l'attività.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Tipo di SID del token del processo attività e matrice di privilegi necessari per l'attività

Se si specifica **ProcessTokenSidType** a livello di definizione di attività, i proprietari delle attività possono richiedere l'esecuzione di un processo di attività con il tipo di SID "None" o con il tipo di SID "senza restrizioni". Se il campo è presente nella definizione di attività, la convalida garantisce che l'ID utente dell'attività contenga il nome o la stringa SID corrispondente per uno di questi account di servizio predefiniti del sistema operativo: "servizio di rete" o "servizio locale".

Il tipo di SID "None" indica che l'attività viene eseguita in un processo che non contiene un SID del token di processo. non verrà apportata alcuna modifica all'elenco dei gruppi di token di processo. Il SID dell'account dell'entità attività (LocalService/NetworkService) in questo caso ha accesso completo al token di processo.

Il tipo di SID "senza restrizioni" indica che un SID attività sarà derivato dal percorso completo dell'attività e verrà aggiunto all'elenco dei gruppi di token di processo. Ad esempio, \\ Microsoft \\ Windows \\ RAC \\ RacTask, che viene eseguito nell'account del servizio locale, il SID dell'attività deriva dal nome Microsoft-Windows-RAC-RacTask dove "-" sostituisce " \\ " perché " \\ " è un carattere di nome utente non valido. Il nome del gruppo noto per il SID attività sarà "NT TASK \\ <modified full task path> " (DomainName \\ username Format). Verrà modificato anche l'elenco di controllo di accesso discrezionale (DACL) predefinito del token di processo per consentire il controllo completo solo per il SID dell'attività e il SID di sistema locale e il controllo di lettura al SID dell'account dell'entità attività. "schtasks.exe/showsid/TN <full task path> " indicherà il SID dell'attività corrispondente all'attività.

Quando viene avviata un'azione dell'attività non COM, il motore di pianificazione registra l'account dell'entità attività, ottiene il token di processo ed esegue una query sull'elenco di privilegi di cui dispone il token, quindi lo confronta con l'elenco dei privilegi specificato in RequiredPrivileges. Se nel secondo caso non è specificato alcun privilegio, questo viene contrassegnato come privilegio SE \_ \_ rimosso. L'azione eseguibile verrà quindi avviata con l'handle del token risultante tramite l'API CreateProcessAsUser ha.

Quando viene avviata, un'azione dell'attività COM deve essere attivata dal processo taskhost.exe. Il motore di pianificazione esegue una query sul blocco di contesto di ogni taskhost.exe in esecuzione con lo stesso account dell'attività iniziale. Se viene rilevato che un processo host è stato avviato con un superset dei privilegi necessari per l'attività di avvio, l'attività viene ospitata in tale processo. Se questo processo non viene trovato, combina le informazioni di protezione avanzata di tutte le attività in esecuzione in TaskHost sotto l'account dell'entità attività con la maschera RequiredPrivileges specificata e quindi avvia una nuova istanza di taskhost.exe.

Se RequiredPrivileges non è presente nella definizione di attività, per il processo attività verranno utilizzati i privilegi predefiniti dell'account dell'entità attività senza SeImpersonatePrivilege. Se **ProcessTokenSidType** non è presente nella definizione di attività, viene usato "Unrestricted" come valore predefinito.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di registrazione delle attività](task-registration-information.md)
</dt> <dt>

[Informazioni sul Utilità di pianificazione](about-the-task-scheduler.md)
</dt> <dt>

[Contesti di sicurezza per le attività](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




