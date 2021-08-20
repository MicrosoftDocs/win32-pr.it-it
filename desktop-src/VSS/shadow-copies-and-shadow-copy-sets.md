---
description: Una copia shadow è uno snapshot di un volume che duplica tutti i dati presenti in tale volume in un istante ben definito. VSS identifica ogni copia shadow da un GUID permanente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Copie shadow e set di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 764478c371cf4a622612865ef7a529955780d82847125874253533d331c195f3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998156"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Copie shadow e set di copie shadow

Una [*copia shadow*](vssgloss-s.md) è uno snapshot di un volume che duplica tutti i dati presenti in tale volume in un istante ben definito. VSS identifica ogni copia shadow da un GUID permanente.

Un [*set di copie*](vssgloss-s.md) shadow è una raccolta di copie shadow di vari volumi tutti presi contemporaneamente. VSS identifica ogni set di copie shadow da un GUID permanente.

Il modo in cui un determinato fornitore di hardware o software sceglie di implementare le copie shadow è completamente a sua discrezione. Dopo aver creato una copia shadow, sono effettivamente disponibili al sistema due immagini del volume copiato tramite shadow: il volume originale, accessibile in modo convenzionale. e i dati copiati, a cui è possibile accedere tramite l'API vss.

Ciò consente l'esecuzione di due set di attività contemporaneamente:

-   Le applicazioni ordinarie nel sistema possono continuare o riprendere rapidamente usando il volume originale, aggiornando i dati sul disco.
-   Le applicazioni che usano l'API del richiedente VSS per accedere al volume copiato tramite shadow possono eseguire backup o operazioni simili.

Le copie shadow non devono essere implementate nello stesso modo per ogni file, directory o volume. Implementazioni diverse del meccanismo di copia shadow ([*provider*](vssgloss-p.md)) possono usare approcci diversi per la creazione di una copia shadow. Tuttavia, per tutte le applicazioni che usano l'API VSS, tutte le copie shadow dovrebbero essere uguali.

Per informazioni sull'implementazione Windows provider di servizi predefiniti, vedere [Provider di sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Stato predefinito della copia shadow

Anche se file system scarica tutti i buffer di I/O prima di creare una copia shadow, questo non garantisce che l'I/O incompleto venga gestito correttamente.

Pertanto, supponendo che il sistema non abbia applicazioni abilitate per VSS, i dati in una copia shadow sono in uno stato coerente [*con l'arresto anomalo del sistema.*](vssgloss-c.md) Una copia shadow in uno stato coerente con l'arresto anomalo del sistema contiene un'immagine del disco uguale a quella esistente in seguito a un arresto irreversico del sistema. Tutti i file aperti saranno ancora presenti nel volume, ma non è garantito che siano esenti da operazioni di I/O incomplete o da danneggiamenti dei dati.

Sebbene lo stato coerente con l'arresto anomalo del sistema non si occupi completamente di tutti i problemi associati alla definizione di un set di backup stabile (vedere [Problemi](common-volume-backup-issues.md)comuni di backup del volume), presenta diversi vantaggi rispetto al set di backup che le operazioni di backup convenzionali devono usare:

-   Un volume contenuto in una copia shadow, anche in uno stato coerente con l'arresto anomalo del sistema, contiene comunque tutti i file. Un set di backup creato senza una copia shadow non conterrà tutti i file aperti al momento del backup. I file mantenuti aperti al momento dell'operazione di backup vengono esclusi dal backup.
-   La copia shadow del volume viene creata in un istante e non attraversando un file system attivo, che in genere richiede molto più tempo.

Le applicazioni in un sistema che non supportano VSS, ovvero elaboratori di testi, editor e così via, probabilmente avranno i file lasciati in uno stato coerente con l'arresto anomalo del sistema. Tuttavia, le applicazioni compatibili con VSS (writer) possono coordinare le azioni in modo che lo stato dei file nella copia shadow sia ben definito e coerente.

## <a name="shadow-copy-freeze-and-thaw"></a>Blocco e disgelo della copia shadow

La creazione di ogni operazione di copia shadow vss è racchiusa tra parentesi dagli eventi [*Freeze*](vssgloss-f.md) e [*Thaw,*](vssgloss-t.md) che i writer usano per impostare i file in uno stato stabile prima della copia shadow.

La presenza di eventi Freeze e Thaw come parte del modello VSS implica:

-   La gestione dell'evento Freeze indica che gli utenti che sviluppano writer devono avere un punto chiaramente delineato nel ciclo di backup in cui assicurano che tutte le operazioni di scrittura sul disco siano arrestate e che i file siano in uno stato ben definito per il backup.
-   La gestione dell'evento Thaw fornisce il meccanismo che consente ai writer di riprendere le operazioni di scrittura sul disco ed eliminare eventuali file temporanei o altre informazioni sullo stato temporanee create in associazione alla copia shadow.
-   La finestra predefinita tra gli eventi Freeze e Thaw è breve (in genere 60 secondi). Pertanto, l'interruzione effettiva di qualsiasi servizio fornito da un writer può essere ridotta al minimo.
-   La gestione di altri eventi (ad esempio PrepareForSnapshot) che precedono e segue rispettivamente gli eventi Freeze e Thaw offrono la flessibilità necessaria per consentire ai writer di completare operazioni complesse per supportare le copie shadow.

 

 



