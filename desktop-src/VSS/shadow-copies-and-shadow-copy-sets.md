---
description: Una copia shadow è uno snapshot di un volume che duplica tutti i dati contenuti in tale volume in un momento preciso e preciso. VSS identifica ogni copia shadow da un GUID permanente.
ms.assetid: 8ef2478a-c8bc-4517-9a14-e1d9226ec4cd
title: Copie shadow e set di copie shadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18709842b1fb0fbf6d6cce2557b51042dfb024ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310665"
---
# <a name="shadow-copies-and-shadow-copy-sets"></a>Copie shadow e set di copie shadow

Una [*Copia Shadow*](vssgloss-s.md) è uno snapshot di un volume che duplica tutti i dati contenuti in tale volume in un momento preciso e preciso. VSS identifica ogni copia shadow da un GUID permanente.

Un [*set*](vssgloss-s.md) di copie shadow è una raccolta di copie shadow di diversi volumi eseguite contemporaneamente. VSS identifica ogni copia shadow impostata da un GUID permanente.

Il modo in cui un particolare fornitore di hardware o software sceglie di implementare copie shadow è completamente a sua discrezione. Una volta creata una copia shadow, sono disponibili nel sistema due immagini del volume di cui è stata eseguita la copia shadow: il volume originale, a cui è possibile accedere convenzionalmente; e i dati copiati, a cui è possibile accedere tramite l'API VSS.

In questo modo è possibile eseguire due set di attività allo stesso tempo:

-   Le applicazioni ordinarie del sistema possono continuare o riprendere rapidamente usando il volume originale, aggiornando i dati sul disco.
-   Le applicazioni che utilizzano l'API del richiedente VSS per accedere al volume copiato shadow possono eseguire backup o operazioni simili.

Le copie shadow non devono essere implementate nello stesso modo per ogni file, directory o volume. Implementazioni diverse del meccanismo di copia shadow ([*provider*](vssgloss-p.md)) possono utilizzare approcci diversi per la creazione di una copia shadow. Tuttavia, per tutte le applicazioni che utilizzano l'API VSS, tutte le copie shadow dovrebbero apparire uguali.

Per informazioni sull'implementazione predefinita del provider Windows, vedere [provider di sistema](providers.md).

## <a name="default-shadow-copy-state"></a>Stato copia shadow predefinita

Anche se il file system Scarica tutti i buffer di I/O prima di creare una copia shadow, questo non garantisce che l'I/O incompleto venga gestito correttamente.

Pertanto, supponendo che il sistema non disponga di applicazioni abilitate per VSS, i dati in una copia shadow si affermeranno in uno [*stato coerente con l'arresto anomalo*](vssgloss-c.md). Una copia shadow in uno stato coerente con l'arresto anomalo del sistema contiene un'immagine del disco identica a quella esistente dopo un arresto irreversibile del sistema. Tutti i file aperti continueranno a esistere nel volume, ma non è garantito che siano privi di operazioni di I/O incomplete o di danneggiamento dei dati.

Sebbene lo stato coerente con l'arresto anomalo del sistema non occupi completamente tutti i problemi associati alla definizione di un set di backup stabile (vedere [problemi comuni di backup del volume](common-volume-backup-issues.md)), presenta diversi vantaggi rispetto al set di backup che avrebbe dovuto utilizzare le operazioni di backup convenzionali:

-   Un volume contenuto in una copia shadow, anche in uno stato coerente con l'arresto anomalo del sistema, contiene comunque tutti i file. Un set di backup creato senza una copia shadow non conterrà tutti i file aperti al momento del backup. I file mantenuti aperti al momento dell'operazione di backup vengono esclusi dal backup.
-   La copia shadow del volume viene creata in un istante e non attraversando un file system attivo, che in genere richiede molto più tempo.

Le applicazioni in un sistema che non sono compatibili con VSS (elaboratori di testo, editor e così via) avranno probabilmente i file lasciati in uno stato coerente con l'arresto anomalo del sistema. Tuttavia, le applicazioni compatibili con VSS (writer) possono coordinare le azioni in modo che lo stato dei file nella copia shadow sia ben definito e coerente.

## <a name="shadow-copy-freeze-and-thaw"></a>Blocca e sblocca copia shadow

La creazione di ogni operazione di copia shadow VSS è racchiusa tra eventi di [*blocco*](vssgloss-f.md) e [*sblocco*](vssgloss-t.md) , che i writer utilizzano per inserire i file in uno stato stabile prima della copia shadow.

La presenza di eventi di blocco e sblocco come parte del modello VSS significa:

-   La gestione dell'evento Freeze significa che gli utenti che sviluppano Writer devono avere un punto ben definito nel ciclo di backup, in cui assicurano che tutte le operazioni di scrittura sul disco siano interrotte e che i file siano in uno stato ben definito per il backup.
-   La gestione dell'evento di sblocco fornisce il meccanismo per i writer per riprendere le Scritture sul disco ed eliminare eventuali file temporanei o altre informazioni sullo stato temporaneo create in associazione alla copia shadow.
-   La finestra predefinita tra gli eventi Freeze e scongela è breve (in genere 60 secondi); Pertanto, è possibile ridurre al minimo l'interruzione effettiva di tutti i servizi forniti da un writer.
-   La gestione di altri eventi, ad esempio PrepareForSnapshot, prima e dopo gli eventi di blocco e sblocco, fornisce rispettivamente la flessibilità necessaria per consentire ai writer di completare operazioni complesse per supportare le copie shadow.

 

 



