---
description: Impostazione dei diritti amministrativi per una partizione
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: Impostazione dei diritti amministrativi per una partizione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748279"
---
# <a name="setting-administrative-rights-for-a-partition"></a>Impostazione dei diritti amministrativi per una partizione

Agli utenti assegnati al ruolo di amministratore dell'applicazione di sistema COM+ è consentito creare, modificare ed eliminare partizioni COM+. All'interno dello strumento di amministrazione Servizi componenti, i ruoli amministrativi possono essere assegnati agli utenti espandendo la cartella **ruoli** dell'applicazione di sistema com+.

A partire da Windows Server 2003, la funzionalità di autenticazione per l'applicazione di sistema COM+ include il valore EOAC \_ Disable \_ AAA. Questo valore, che disabilita le attivazioni di Activate-As-Activator (AAA), viene usato nella chiamata [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) quando viene avviata l'applicazione di sistema. Impostando la funzionalità di autenticazione su EOAC \_ Disable AAA è possibile consentire a \_ un'applicazione in esecuzione con un account con privilegi, ad esempio LocalSystem, di impedire l'utilizzo dell'identità per l'avvio di componenti non attendibili.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Raccolta delle metriche della partizione](collecting-partition-metrics.md)
</dt> <dt>

[Configurazione della cache della partizione](configuring-the-partition-cache.md)
</dt> <dt>

[Raggruppamento di applicazioni in partizioni](grouping-applications-into-partitions.md)
</dt> <dt>

[Gestione delle partizioni locali](managing-local-partitions.md)
</dt> <dt>

[Gestione di partizioni all'interno Active Directory](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
