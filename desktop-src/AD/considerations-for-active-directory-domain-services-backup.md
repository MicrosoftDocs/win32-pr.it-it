---
title: Considerazioni per il backup Active Directory Domain Services
description: È possibile replicare i dati del servizio directory. Prima di eseguire il ripristino, è necessario creare un piano di ripristino.
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, pianificazione del ripristino
- Active Directory Domain Services Active Directory, backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "104046546"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Considerazioni per il backup Active Directory Domain Services

È possibile replicare i dati del servizio directory. Prima di eseguire il ripristino, è necessario creare un piano di ripristino. Un'opzione consiste nel ripristinare una replica di una directory e quindi propagare le modifiche apportate dopo il backup da altre repliche nel dominio.

In alcuni casi è possibile che la replica ripristinata abbia la precedenza sulle altre repliche nel dominio. Se, ad esempio, un oggetto viene eliminato accidentalmente e l'eliminazione viene replicata in tutti i controller di dominio, è possibile ripristinare l'oggetto ripristinando una replica da un backup creato prima dell'eliminazione dell'oggetto. Si utilizzerà quindi l'utilità NTDSUtil per contrassegnare l'oggetto ripristinato come ripristinato in modo autorevole. L'oggetto ripristinato verrà quindi replicato negli altri controller di dominio e la replica ripristinata riceverà gli aggiornamenti per tutti gli altri oggetti verificatisi dopo l'esecuzione del backup. Il risultato finale per tutte le repliche è identico a quello prima del ripristino, ad eccezione del fatto che l'oggetto ripristinato in modo autorevole non viene più eliminato.

Tutte le modifiche che si verificano durante il backup vengono archiviate in un log temporaneo e aggiunte alla fine del set di backup al termine del backup.

Qualsiasi piano di ripristino deve garantire che l'età del backup non superi il Active Directory la durata di rimozione definitiva. Per ulteriori informazioni sulla durata dell'oggetto contrassegnato per la rimozione definitiva, vedere l'argomento [di TechNet Introduzione all'amministrazione di Active Directory backup e ripristino](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)). Il ripristino di un backup precedente alla durata di rimozione definitiva può causare la replica da parte del controller di dominio ripristinato degli oggetti che non verranno replicati in altri controller di dominio. Questo errore si verifica se un oggetto viene eliminato dopo il backup e il ripristino viene eseguito dopo che la rimozione definitiva per l'oggetto eliminato è stata rimossa in modo permanente. Il controller di dominio ripristinato avrebbe l'oggetto esistente prima dell'eliminazione e gli altri controller di dominio non avrebbero mai registrato l'oggetto. In tal caso, un amministratore dovrà eliminare manualmente ogni oggetto non replicato nel controller di dominio ripristinato.

I backup incrementali dei Active Directory Domain Services non sono supportati. sono necessari backup completi.

 

 