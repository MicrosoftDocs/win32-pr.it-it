---
title: Linee guida per la programmazione Servizi Desktop remoto
description: Argomenti che forniscono linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.
ms.assetid: e0cd52c5-40d7-4a48-9d10-fdbcea46a5a0
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, linee guida per la programmazione
- linee guida per la programmazione Servizi Desktop remoto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e767740a2f279c90ce4f0eb37c49919749465ad1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299959"
---
# <a name="remote-desktop-services-programming-guidelines"></a>Linee guida per la programmazione Servizi Desktop remoto

La maggior parte delle applicazioni basate su Windows a 32 bit o a 64 bit vengono eseguite "così come sono" in un ambiente Servizi Desktop remoto (noto in precedenza come servizi Terminal). Tuttavia, alcune applicazioni funzionano correttamente ed eseguono buone attività in un ambiente di Servizi Desktop remoto, mentre altre no. Negli argomenti seguenti vengono fornite le linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.

## <a name="in-this-section"></a>Contenuto della sezione

<dl> <dt>

[Linee guida per più utenti](multiple-user-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni per più utenti in un ambiente Servizi Desktop remoto.

</dd> <dt>

[Linee guida sulle prestazioni](performance-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni che offrono prestazioni ottimali in un ambiente Servizi Desktop remoto.

</dd> <dt>

[Linee guida generali per la programmazione](general-programming-guidelines.md)
</dt> <dd>

Linee guida per lo sviluppo di applicazioni in un ambiente Servizi Desktop remoto.

</dd> </dl>

Molte di queste linee guida sono buone procedure di programmazione che trarranno vantaggio dalle applicazioni in esecuzione in qualsiasi ambiente Windows. Tuttavia, alcune ottimizzazioni consigliate, ad esempio la limitazione degli effetti grafici, sono ottimizzazioni che si desiderano solo quando l'applicazione è in esecuzione in Servizi Desktop remoto. Per un esempio di codice che illustra come rilevare un ambiente di Servizi Desktop remoto, vedere [rilevamento dell'ambiente Servizi Desktop remoto](detecting-the-terminal-services-environment.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>


</dt> <dt>

[Servizi terminal è ora Servizi Desktop remoto](terminal-services-is-now-remote-desktop-services.md)
</dt> <dt>

[Formato file modello amministrativo](/previous-versions/windows/desktop/Policy/administrative-template-file-format)
</dt> <dt>

[Diritti di accesso e sicurezza della chiave del registro di sistema](/windows/desktop/SysInfo/registry-key-security-and-access-rights)
</dt> <dt>

[Hive del registro di sistema](/windows/desktop/SysInfo/registry-hives)
</dt> <dt>

[Descrittori di sicurezza](/windows/desktop/SecAuthZ/security-descriptors)
</dt> <dt>

[Diritti di accesso standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> <dt>

[Modello di controllo di accesso](/windows/desktop/SecAuthZ/access-control-model)
</dt> </dl>

 

 