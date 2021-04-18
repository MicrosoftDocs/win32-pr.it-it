---
description: I provider gestiscono i volumi in esecuzione e creano copie shadow di questi ultimi su richiesta.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb336dbb51fcbd715ea236ecdc0c62d81daf29d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310681"
---
# <a name="providers"></a>Provider

I [*provider*](vssgloss-p.md) gestiscono i volumi in esecuzione e creano copie shadow di questi ultimi su richiesta.

In risposta a una richiesta di un richiedente, un provider genera eventi COM per segnalare le applicazioni di una copia shadow in arrivo, quindi crea e gestisce tale copia fino a quando non è più necessaria.

Mentre è in esecuzione una copia shadow, il provider crea un ambiente in cui sono effettivamente presenti due copie indipendenti di qualsiasi volume di cui è stata eseguita la copia shadow: uno del disco in uso e aggiornato normalmente, l'altra copia che è fissa e stabile per il backup.

Mentre un provider predefinito viene fornito come parte di Windows, altri fornitori sono liberi di fornire le proprie implementazioni ottimizzate per le proprie offerte hardware e software di archiviazione.

Dal punto di vista di un utente finale o di uno sviluppatore di applicazioni di backup/ripristino, tutti i provider avranno la stessa interfaccia (vedere [selezione dei provider](selecting-providers.md)).

Tutti i provider devono essere in grado di eseguire le operazioni seguenti:

-   Intercettare le richieste di I/O tra il file system e il sistema di archiviazione di massa sottostante.
-   Acquisire e recuperare lo stato di un volume al momento della copia shadow, mantenendo una visualizzazione "temporizzata" dei file sul disco senza operazioni di I/O parziali riflesse nello stato.
-   Usare questa visualizzazione "temporizzata" per esporre (al minimo per le applicazioni abilitate per VSS) un volume virtuale contenente i dati copiati dall'ombreggiatura.

A seconda di come viene eseguita questa operazione, un provider può essere uno dei tre tipi seguenti:

-   [Provider di sistema](#system-provider)
-   [Provider di software](#software-providers)
-   [Provider hardware](#hardware-providers)

## <a name="system-provider"></a>Provider di sistema

Un provider di copia shadow, il [*provider di sistema*](vssgloss-s.md), viene fornito come parte predefinita di un'installazione del sistema operativo Windows. Attualmente, il provider di sistema è una particolare istanza di un provider di software. Tuttavia, questo potrebbe cambiare in futuro.

Per mantenere una visualizzazione temporizzata di un volume contenuto nella copia shadow, il provider di sistema utilizza una tecnica copy-on-Write. Le copie dei settori sul disco che sono state modificate, denominate "diffs", dall'inizio della creazione della copia shadow vengono archiviate in un'area di archiviazione della copia shadow.

Pertanto, il provider di sistema può esporre il volume Live, che può essere scritto e letto normalmente, e applicare le "diff" ai dati del volume attivo per esporre efficacemente i dati bloccati della copia shadow.

Per il provider di sistema, l'area di archiviazione della copia shadow deve trovarsi in un volume NTFS. Non è necessario che il volume per cui eseguire la copia shadow sia un volume NTFS, ma almeno un volume montato nel sistema deve essere un volume NTFS.

## <a name="software-providers"></a>Provider di software

I provider di copie shadow software intercettano ed elaborano le richieste di I/O in un livello software tra il file system e il software di gestione dei volumi. Questi provider vengono implementati come un componente DLL in modalità utente e almeno un driver di dispositivo in modalità kernel, in genere, ma non necessariamente, un driver del filtro di archiviazione. Il lavoro di creazione di queste copie shadow viene eseguito nel software.

Un provider di copia shadow software deve mantenere una visualizzazione temporizzata di un volume con accesso a un set di file che possono essere usati per ricreare accuratamente lo stato del volume prima della copia shadow. Un esempio è la tecnica copy-on-Write del provider di sistema.

Tuttavia, il servizio Copia Shadow del volume non impone alcuna restrizione sulla tecnica utilizzata dai provider di software per creare e gestire copie shadow e i fornitori di terze parti possono implementare i propri provider di software nel modo appropriato.

VSS fornisce inoltre supporto per la maggior parte delle funzionalità dei provider di copie shadow software, ad esempio la definizione del punto nel tempo, la sincronizzazione e lo scaricamento dei dati, fornendo un'interfaccia comune per le applicazioni di backup e la gestione della copia shadow.

Un provider di software, per definizione, sarà applicabile a una gamma più ampia di piattaforme di archiviazione rispetto a un provider hardware e dovrebbe essere in grado di lavorare anche con i dischi di base o i volumi logici. Questa generalità sacrifica le prestazioni che possono essere disponibili implementando copie shadow in hardware e non utilizza le funzionalità di acquisizione di volumi o di mirroring dei file specifiche del fornitore.

## <a name="hardware-providers"></a>Provider hardware

I provider di copie shadow hardware intercettano le richieste di I/O dal file system a livello hardware lavorando insieme a un adattatore o a un controller di archiviazione hardware. Il lavoro di creazione della copia shadow viene eseguito da un adattatore host, un dispositivo di archiviazione o un controller RAID esterno al sistema operativo.

Questi provider sono implementati come componente DLL in modalità utente che comunica con l'hardware che esporrà i dati della copia shadow: pertanto, è possibile che i provider di copie shadow hardware debbano chiamare o creare altri componenti in modalità kernel.

I provider hardware vengono esposti a copie shadow VSS di interi dischi o unità logiche (lun). I richiedenti continuano a gestire copie shadow dei volumi; tutto il mapping da volume a disco viene gestito internamente dal servizio Copia Shadow del volume. Le copie shadow create da provider hardware di volumi che risiedono su dischi dinamici hanno un requisito specifico, ovvero non possono essere importate nello stesso sistema. Devono essere creati trasportabili e importati in un secondo sistema.

Mentre un provider di copia shadow hardware utilizza la funzionalità VSS che definisce il punto nel tempo, consente la sincronizzazione dei dati, gestisce la copia shadow e fornisce un'interfaccia comune con le applicazioni di backup, VSS non specifica il meccanismo sottostante in base al quale il provider hardware produce e gestisce le copie shadow.

 

 



