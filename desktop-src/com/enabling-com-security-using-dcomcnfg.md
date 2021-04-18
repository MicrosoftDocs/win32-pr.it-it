---
title: Abilitazione della sicurezza COM tramite DCOMCNFG
description: Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298017"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Abilitazione della sicurezza COM tramite DCOMCNFG

Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema. Con Dcomcnfg.exe è possibile abilitare la sicurezza a livello di computer o a livello di processo. È possibile abilitare la sicurezza per un determinato computer in modo che quando un processo non fornisce le proprie impostazioni di sicurezza, a livello di codice o tramite i valori del registro di sistema, verranno utilizzati i valori impostati da Dcomcnfg.exe. In alternativa, è possibile usare Dcomcnfg.exe per abilitare la sicurezza solo per una particolare applicazione.

Quando si Abilita la sicurezza, è necessario eseguire due attività principali:

-   Impostare un livello di autenticazione diverso da None.
-   Impostare le autorizzazioni, incluse le autorizzazioni di avvio e di accesso.

I passaggi necessari per eseguire queste attività variano a seconda che si stia abilitando la protezione per l'intero computer o solo per una particolare applicazione. Inoltre, potrebbe essere necessario impostare altri valori per il computer o l'applicazione.

> [!Note]  
> Per eseguire Dcomcnfg.exe, è necessario essere un amministratore.

 

Negli argomenti seguenti vengono fornite procedure dettagliate su come impostare la sicurezza con Dcomcnfg.exe:

-   [Impostazione della sicurezza System-Wide tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Impostazione della sicurezza di Processwide tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> <dt>

[Disattivazione della sicurezza](turning-off-security.md)
</dt> </dl>

 

 




