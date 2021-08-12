---
description: I provider gestiscono i volumi in esecuzione e creano le copie shadow dei volumi su richiesta.
ms.assetid: 4e6b46b0-df9e-4458-b0ac-e237d7656337
title: Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58c9e098981c6246392fef75f717b1d7676df1aa134e4faef3e436ee8b3eb537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118591328"
---
# <a name="providers"></a>Provider

[*I*](vssgloss-p.md) provider gestiscono i volumi in esecuzione e creano le copie shadow dei volumi su richiesta.

In risposta a una richiesta da parte di un richiedente, un provider genera eventi COM per segnalare alle applicazioni una copia shadow in arrivo, quindi crea e mantiene tale copia fino a quando non è più necessaria.

Mentre è presente una copia shadow, il provider crea un ambiente in cui sono effettivamente presenti due copie indipendenti di qualsiasi volume che è stato copiato shadow: una il disco in esecuzione usato e aggiornato come di consueto, l'altro una copia fissa e stabile per il backup.

Mentre un provider predefinito viene fornito come parte di Windows, altri fornitori sono liberi di fornire le proprie implementazioni ottimizzate per le proprie offerte hardware e software di archiviazione.

Dal punto di vista di un utente finale o di uno sviluppatore di applicazioni di backup/ripristino, tutti i provider avranno la stessa interfaccia (vedere [Selezione dei provider](selecting-providers.md)).

Tutti i provider devono essere in grado di eseguire le operazioni seguenti:

-   Intercettare le richieste di I/O tra il file system e il sistema di archiviazione di massa sottostante.
-   Acquisire e recuperare lo stato di un volume al momento della copia shadow, mantenendo una visualizzazione "tempormente" dei file sul disco senza operazioni di I/O parziali riflesse nello stato.
-   Usare questa visualizzazione "tempor" per esporre (in modo minimo alle applicazioni abilitate per VSS) un volume virtuale contenente i dati copiati shadow.

A seconda di come viene eseguita questa operazione, un provider può essere uno dei tre tipi seguenti:

-   [Provider di sistema](#system-provider)
-   [Provider di software](#software-providers)
-   [Provider di hardware](#hardware-providers)

## <a name="system-provider"></a>Provider di sistema

Un provider di copie shadow, il [*provider*](vssgloss-s.md)di sistema , viene fornito come parte predefinita di un'Windows del sistema operativo. Attualmente, il provider di sistema è una particolare istanza di un provider di software. Tuttavia, questo potrebbe cambiare in futuro.

Per mantenere una visualizzazione "tempor" di un volume contenuto nella copia shadow, il provider di sistema usa una tecnica di copia in scrittura. Le copie dei settori su disco modificate (denominate "diff") dall'inizio della creazione della copia shadow vengono archiviate in un'area di archiviazione delle copie shadow.

Pertanto, il provider di sistema può esporre il volume live, che può essere scritto e letto normalmente, e applicare le "diff" ai dati del volume live per esporre in modo efficace i dati bloccati della copia shadow.

Per il provider di sistema, l'area di archiviazione della copia shadow deve trovarsi in un volume NTFS. Non è necessario che il volume per cui eseguire la copia shadow sia un volume NTFS, ma almeno un volume montato nel sistema deve essere un volume NTFS.

## <a name="software-providers"></a>Provider di software

I provider di copie shadow software intercettano ed elaborano le richieste di I/O in un livello software tra il file system e il software di gestione dei volumi. Questi provider vengono implementati come componente DLL in modalità utente e almeno un driver di dispositivo in modalità kernel, in genere (ma non necessariamente) un driver di filtro di archiviazione. Il lavoro di creazione di queste copie shadow viene eseguito nel software.

Un provider di copie shadow software deve mantenere una visualizzazione "tempormente" di un volume avendo accesso a un set di file che può essere usato per ri-creare in modo accurato lo stato del volume prima della copia shadow. Un esempio è la tecnica di copia in scrittura del provider di sistema.

Tuttavia, VSS non pone alcuna restrizione sulla tecnica che i provider di software usano per creare e gestire copie shadow e i fornitori di terze parti sono liberi di implementare i propri provider software come meglio si adattano.

VsS offre inoltre il supporto per gran parte delle funzionalità dei provider di copie shadow software, ad esempio la definizione tempor volta, la sincronizzazione e lo scaricamento dei dati, fornendo un'interfaccia comune per le applicazioni di backup e la gestione della copia shadow.

Un provider software sarà, per definizione, applicabile a una gamma più ampia di piattaforme di archiviazione rispetto a un provider di hardware e dovrebbe essere in grado di usare allo stesso modo dischi di base o volumi logici. Questa generalità sacrifica le prestazioni che possono essere disponibili implementando copie shadow nell'hardware e non usa alcuna funzionalità di acquisizione del volume o mirroring dei file specifica del fornitore.

## <a name="hardware-providers"></a>Provider di hardware

I provider di copie shadow dell'hardware intercettano le richieste di I/O dal file system a livello hardware lavorando in combinazione con una scheda di archiviazione hardware o un controller. Il lavoro di creazione della copia shadow viene eseguito da una scheda host, un'appliance di archiviazione o un controller RAID all'esterno del sistema operativo.

Questi provider vengono implementati come componente DLL in modalità utente che comunica con l'hardware che esporrà i dati della copia shadow: pertanto, i provider di copie shadow hardware potrebbero dover chiamare o creare altri componenti in modalità kernel.

I provider hardware espongono alle copie shadow vss di interi dischi o unità logiche (LUN). I richiedenti continuano a gestire le copie shadow dei volumi. tutto il mapping da volume a disco viene gestito internamente da VSS. Le copie shadow create dai provider hardware di volumi che risiedono su dischi dinamici hanno un requisito specifico: non possono essere importate nello stesso sistema. Devono essere creati trasportabili e importati in un secondo sistema.

Mentre un provider di copie shadow dell'hardware usa la funzionalità vss che definisce il punto nel tempo, consente la sincronizzazione dei dati, gestisce la copia shadow e fornisce un'interfaccia comune con le applicazioni di backup, VSS non specifica il meccanismo sottostante con cui il provider hardware produce e gestisce le copie shadow.

 

 



