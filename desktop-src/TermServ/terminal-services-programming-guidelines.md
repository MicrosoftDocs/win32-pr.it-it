---
title: Servizi Desktop remoto linee guida per la programmazione
description: Argomenti che forniscono linee guida per lo sviluppo di applicazioni in un Servizi Desktop remoto locale.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , linee guida per la programmazione
- linee guida per la programmazione Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f1f935ada4dfe486b418b5ec3b6f347eb6166e6b392a3adc1bd8c1e5987a773
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999871"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Servizi Desktop remoto linee guida per la programmazione

La maggior parte delle applicazioni esistenti basate su Windows a 32 o 64 bit viene eseguita "così come è" in un ambiente Servizi Desktop remoto (precedentemente noto come Servizi terminal). Tuttavia, alcune applicazioni funzionano correttamente e funzionano correttamente in un ambiente Servizi Desktop remoto, mentre altre no. Gli argomenti seguenti forniscono linee guida per lo sviluppo di applicazioni in un Servizi Desktop remoto locale.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Linee guida per più utenti](multiple-user-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni per più utenti in un Servizi Desktop remoto locale.

</dd> <dt>

[Linee guida per le prestazioni](performance-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni con prestazioni molto Servizi Desktop remoto ambiente.

</dd> <dt>

[Linee guida generali per la programmazione](general-programming-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni in un Servizi Desktop remoto locale.

</dd> </dl>

Molte di queste linee guida sono buone procedure di programmazione che trarranno vantaggio dalle applicazioni in esecuzione in qualsiasi Windows ambiente. Tuttavia, alcune ottimizzazioni consigliate, ad esempio la limitazione degli effetti grafici, sono ottimizzazioni che è consigliabile solo quando l'applicazione è in esecuzione in Servizi Desktop remoto. Per un esempio di codice che illustra come rilevare un ambiente Servizi Desktop remoto, vedere [Detecting the Servizi Desktop remoto Environment](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Servizi terminal è ora disponibile Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Formato file modello amministrativo](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Sicurezza e diritti di accesso delle chiavi del Registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Hive del Registro di sistema](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 