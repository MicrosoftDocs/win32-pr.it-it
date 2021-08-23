---
description: La scrittura di un provider sicuro richiede la considerazione della modalità di hosting del provider, della modalità di gestione della rappresentazione e della verifica dei diritti di accesso ai dati da parte degli utenti.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Protezione del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dec112c7e207a23d36700d8fb5de3b3964590b514f9cf5a6aa5fbc03243cf40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119732841"
---
# <a name="securing-your-provider"></a>Protezione del provider

La scrittura di un provider sicuro richiede la considerazione della modalità di hosting del provider, della modalità di gestione della rappresentazione e della verifica dei diritti di accesso ai dati da parte degli utenti. È possibile proteggere i dati nello spazio dei nomi del provider richiedendo che i dati siano crittografati prima di inviarli in rete. Per altre informazioni, vedere [Richiesta di una connessione crittografata a uno spazio dei nomi.](requiring-an-encrypted-connection-to-a-namespace.md)

Se un utente ha accesso **FULL \_ WRITE** in qualsiasi spazio dei nomi, può creare sottoscrizioni tra spazi dei nomi per i dati in uno spazio dei nomi in cui l'utente è limitato. Poiché un provider può essere caricato in qualsiasi spazio dei nomi ed eseguito in qualsiasi contesto di sicurezza, il provider deve eseguire i propri controlli di accesso per garantire che solo gli utenti autorizzati siano autorizzati ad accedere ai dati o a eseguire metodi. Per altre informazioni, vedere Esecuzione [dei controlli di accesso.](performing-access-checks.md)

Negli argomenti seguenti viene illustrata la sicurezza del provider:

-   [Hosting e sicurezza dei provider](provider-hosting-and-security.md)
-   [Esecuzione di controlli di accesso](performing-access-checks.md)
-   [Chiavi del Registro di sistema per il controllo della sicurezza del provider](registry-keys-for-controlling-provider-security-.md)
-   [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
-   [Rappresentazione di un client](impersonating-a-client.md)

Gli argomenti seguenti illustrano l'interazione tra client e script con la sicurezza del provider:

-   [Impostazione dell'autenticazione in WMI](setting-authentication-in-wmi.md)
-   [Connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Uso di WMI](using-wmi.md)
</dt> </dl>

 

 
