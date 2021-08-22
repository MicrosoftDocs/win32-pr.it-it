---
title: Abilitazione della sicurezza COM tramite DCOMCNFG
description: Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d6161cf7418e7eab705203df51710e789ad2ef7d6843051dd35399fb8388f27
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678691"
---
# <a name="enabling-com-security-using-dcomcnfg"></a>Abilitazione della sicurezza COM tramite DCOMCNFG

Dcomcnfg.exe fornisce un'interfaccia utente per la modifica di determinate impostazioni del Registro di sistema. Usando Dcomcnfg.exe, è possibile abilitare la sicurezza a livello di computer o a livello di processo. È possibile abilitare la sicurezza per un computer specifico in modo che quando un processo non fornisce le proprie impostazioni di sicurezza, a livello di codice o tramite i valori del Registro di sistema, verranno usati i valori impostati da Dcomcnfg.exe. Oppure è possibile usare Dcomcnfg.exe per abilitare la sicurezza solo per una determinata applicazione.

Quando si abilita la sicurezza, è necessario eseguire due attività principali:

-   Impostare un livello di autenticazione diverso da Nessuno.
-   Impostare le autorizzazioni, incluse le autorizzazioni di avvio e di accesso.

I passaggi da eseguire per eseguire queste attività variano a seconda che si abilitazione della sicurezza per l'intero computer o solo per una determinata applicazione. È anche possibile impostare altri valori per il computer o l'applicazione.

> [!Note]  
> È necessario essere un amministratore per eseguire Dcomcnfg.exe.

 

Negli argomenti seguenti vengono fornite procedure dettagliate su come impostare la sicurezza con Dcomcnfg.exe:

-   [Impostazione System-Wide sicurezza tramite DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md)
-   [Impostazione della sicurezza a livello di processo tramite DCOMCNFG](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sicurezza in COM](security-in-com.md)
</dt> <dt>

[Disattivazione della sicurezza](turning-off-security.md)
</dt> </dl>

 

 




