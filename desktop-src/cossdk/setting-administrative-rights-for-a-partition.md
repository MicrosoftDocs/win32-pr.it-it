---
description: Impostazione dei diritti amministrativi per una partizione
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Impostazione dei diritti amministrativi per una partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33431c5beff76e015d28b6a7e886823620126f2ed9b84db68af9a8f3b8ac1d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117915824"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Impostazione dei diritti amministrativi per una partizione

Gli utenti a cui è stato assegnato il ruolo Amministratore dell'applicazione di sistema COM+ possono creare, modificare ed eliminare partizioni COM+. All'interno dello strumento amministrativo Servizi componenti è possibile assegnare ruoli amministrativi agli utenti espandendo la **cartella Ruoli** dell'applicazione di sistema COM+.

A Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ DISABLE \_ AAA. Questo valore, che disabilita le attivazioni activate-as-activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) all'avvio dell'applicazione di sistema. L'impostazione della funzionalità di autenticazione su EOAC DISABLE AAA consente a un'applicazione eseguita con un account con privilegi (ad esempio LocalSystem) di impedire che la propria identità venga usata per avviare componenti non \_ \_ attendibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche delle partizioni](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache delle partizioni](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione delle partizioni all'interno di Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
