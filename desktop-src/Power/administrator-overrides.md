---
description: Sostituzioni amministratore
ms.assetid: 25b6ce86-52c8-4f7f-97af-86b2eaf3e9af
title: Sostituzioni amministratore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af73f6d6fe3fe7d4edb8272c4d39c385a84973e4a3263c448505f5235adec855
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033021"
---
# <a name="administrator-overrides"></a>Sostituzioni amministratore

Windows un singolo elenco di controllo di accesso predefinito in tutti gli oggetti criteri di risparmio energia. L'ACL concede autorizzazioni di lettura, scrittura e modifica ai membri del gruppo Authenticated Users. A tutti gli altri utenti viene concessa l'autorizzazione di sola lettura. Le applicazioni che chiamano le funzioni dei criteri di risparmio energia possono determinare se un utente dispone delle autorizzazioni per un'impostazione di risparmio energia specificata usando la [**funzione PowerSettingAccessCheck.**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck)

Le impostazioni di risparmio energia possono essere sostituite tramite Criteri di gruppo. Le sostituzioni possono essere impostate tramite criteri di gruppo di dominio o criteri di gruppo locali. [**PowerSettingAccessCheck segnala**](/windows/desktop/api/PowrProf/nf-powrprof-powersettingaccesscheck) se un'impostazione di risparmio energia specificata ha un override di Criteri di gruppo.

Lo strumento da riga di **comando** PowerCfg.exeun messaggio di errore quando non è possibile completare un comando perché l'utente non dispone delle autorizzazioni per modificare l'impostazione di risparmio energia o perché l'impostazione di risparmio energia ha un override di Criteri di gruppo.

L Opzioni risparmio energia appalto Pannello di controllo non fornisce il supporto per la configurazione delle autorizzazioni di accesso ai criteri di risparmio energia. La modifica delle autorizzazioni deve essere eseguita **tramitePowerCfg.exe**.

 

 



