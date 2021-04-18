---
description: Per la scrittura di un provider sicuro è necessario considerare la modalità di hosting del provider, il modo in cui il provider gestisce la rappresentazione e verificare che gli utenti vengano controllati per i diritti di accesso ai dati.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sicurezza del provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309884"
---
# <a name="securing-your-provider"></a>Sicurezza del provider

Per la scrittura di un provider sicuro è necessario considerare la modalità di hosting del provider, il modo in cui il provider gestisce la rappresentazione e verificare che gli utenti vengano controllati per i diritti di accesso ai dati. È possibile proteggere i dati nello spazio dei nomi del provider richiedendo che i dati vengano crittografati prima di inviarli in una rete. Per ulteriori informazioni, vedere la pagina relativa [alla richiesta di una connessione crittografata a uno spazio dei nomi](requiring-an-encrypted-connection-to-a-namespace.md).

Se un utente dispone di accesso in **\_ scrittura completo** in qualsiasi spazio dei nomi, l'utente può creare sottoscrizioni tra gli spazi dei nomi per i dati in uno spazio dei nomi in cui l'utente è limitato. Poiché un provider può essere caricato in qualsiasi spazio dei nomi ed eseguito in qualsiasi contesto di sicurezza, il provider deve eseguire i propri controlli di accesso per garantire che solo gli utenti autorizzati possano accedere ai dati o eseguire metodi. Per ulteriori informazioni, vedere [esecuzione dei controlli di accesso](performing-access-checks.md).

Negli argomenti seguenti viene illustrata la sicurezza del provider:

-   [Hosting e sicurezza del provider](provider-hosting-and-security.md)
-   [Esecuzione di controlli di accesso](performing-access-checks.md)
-   [Chiavi del registro di sistema per il controllo della sicurezza del provider](registry-keys-for-controlling-provider-security-.md)
-   [Accesso agli spazi dei nomi WMI](access-to-wmi-namespaces.md)
-   [Rappresentazione di un client](impersonating-a-client.md)

Negli argomenti seguenti viene illustrato come i client e gli script interagiscono con la sicurezza del provider:

-   [Impostazione dell'autenticazione in WMI](setting-authentication-in-wmi.md)
-   [Connessione tra sistemi operativi diversi](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [Impostazione del livello di sicurezza del processo predefinito tramite VBScript](setting-the-default-process-security-level-using-vbscript.md)
-   [Impostazione della sicurezza del processo dell'applicazione client](setting-client-application-process-security.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione della sicurezza WMI](maintaining-wmi-security.md)
</dt> <dt>

[Utilizzo di WMI](using-wmi.md)
</dt> </dl>

 

 
