---
description: Sostituzioni amministratore
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Sostituzioni amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c43e16c9aa3eb3ab9fd5ee7c8d17b9bb4536315
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312071"
---
# <a name="administrator-overrides"></a>Sostituzioni amministratore

Windows dispone di un singolo elenco di controllo di accesso (ACL) predefinito per tutti gli oggetti Criteri di risparmio energia. L'ACL concede le autorizzazioni di lettura, scrittura e modifica ai membri del gruppo Authenticated Users. A tutti gli altri utenti viene concessa l'autorizzazione di sola lettura. Le applicazioni che chiamano funzioni dei criteri di risparmio energia possono determinare se un utente dispone delle autorizzazioni per un'impostazione di risparmio energia specificata tramite la funzione [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) .

È possibile eseguire l'override delle impostazioni di risparmio energia tramite Criteri di gruppo. Le sostituzioni possono essere impostate tramite criteri di gruppo di dominio o criteri di gruppo locali. [**PowerSettingAccessCheck**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) segnala se per un'impostazione di risparmio energia specificata è presente un override di criteri di gruppo.

Lo strumento da riga di comando **PowerCfg.exe** Visualizza un messaggio di errore quando non è possibile completare un comando perché l'utente non dispone delle autorizzazioni per modificare l'impostazione di risparmio energia o perché per l'impostazione di risparmio energia è stato eseguito un override di criteri di gruppo.

L'applicazione Opzioni risparmio energia nel pannello di controllo non offre il supporto per la configurazione delle autorizzazioni di accesso ai criteri di risparmio energia. La modifica delle autorizzazioni deve essere eseguita tramite **PowerCfg.exe**.

 

 



