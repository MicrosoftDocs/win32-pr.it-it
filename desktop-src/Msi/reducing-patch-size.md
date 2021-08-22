---
description: A partire da Windows Installer versione 3.0, gli autori di patch possono usare la baseline del prodotto memorizzata nella cache dal programma di installazione per gestire più facilmente le applicazioni con patch differenziali più piccole.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Riduzione delle dimensioni delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9024307ecb0971b02c93036dd0de2aefbe797dcf5645f0f07045c4df8956a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534081"
---
# <a name="reducing-patch-size"></a>Riduzione delle dimensioni delle patch

A partire da Windows Installer versione 3.0, gli autori di patch possono usare la baseline del prodotto memorizzata nella cache dal programma di installazione per gestire più facilmente le applicazioni con patch differenziali più piccole. In molti casi, una [*patch differenziale*](d-gly.md) che fornisce informazioni di manutenzione a un'applicazione può essere notevolmente più piccola rispetto a una patch con file completi o a un pacchetto di installazione che recapita le stesse informazioni.

**Windows Installer 2.0:** Non supportato. A partire da Windows Installer 3.0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornati.

Windows Il programma di installazione offre tre metodi per l'aggiornamento e la manutenzione delle [applicazioni:](small-updates.md)aggiornamenti di piccole dimensioni, aggiornamenti [secondari](minor-upgrades.md)e [aggiornamenti principali.](major-upgrades.md) Un aggiornamento di piccole dimensioni viene anche definito aggiornamento QFE (Quick Fix Engineering) e un aggiornamento secondario viene definito anche aggiornamento del Service Pack (SP). Un tipico aggiornamento principale rimuove un'applicazione precedente e installa una nuova applicazione. Windows Il programma di installazione può fornire informazioni di manutenzione alle applicazioni come pacchetto di installazione [(file](installation-package.md) .msi) o come [pacchetto di patch](patch-packages.md) (file con estensione msp).

Un Windows di patch del programma di installazione che fornisce informazioni di manutenzione per un piccolo aggiornamento o un aggiornamento secondario è in genere molto più piccolo del pacchetto di installazione equivalente che fornisce le stesse informazioni di manutenzione. È consigliabile usare i pacchetti di patch per la distribuzione di aggiornamenti di piccole e piccole dimensioni. È consigliabile usare un pacchetto di installazione per la distribuzione di un aggiornamento principale.

Windows Le patch del programma di installazione (file con estensione msp) possono essere generate da file completi o da differenze di file (detti anche delta dei file). Una Windows del programma di installazione generata dai differenziali di file può essere molto più piccola della patch di file completo equivalente. Tutte le versioni del Windows installer possono usare patch con file completi o patch differenziali.

A partire da Windows installer versione 3.0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornati. Le informazioni sull'applicazione di base originale (versione RTM) e sull'aggiornamento secondario più recente (Service Pack) vengono salvate in un percorso privato quando l'applicazione viene installata o riceve un aggiornamento secondario.

Il programma di installazione esegue le operazioni seguenti per ridurre al minimo le dimensioni della cache di base:

-   Non vengono mantenute più di due baseline per ogni applicazione: una baseline del file come rilasciato in origine (RTM) e una baseline del file nell'aggiornamento secondario più recente (Service Pack).
-   Un file non viene aggiunto alla cache fino a quando non viene patchato. La cache di base è copy-on-write.
-   Se l'applicazione non è mai stata aggiornata, non sono presenti file nella cache di base.
-   Quando l'ultima manutenzione dell'applicazione è stata un aggiornamento secondario (Service Pack), l'applicazione si trova a un livello di base e al massimo due copie di un file possono essere presenti nel computer. Una copia del file si trova nella directory di destinazione dell'installazione. L'altra copia può essere nella cache della baseline RTM.
-   Quando l'ultima manutenzione dell'applicazione è stata un piccolo aggiornamento (QFE), l'applicazione non è a livello di base e al massimo tre copie di un file possono essere presenti nel computer. La prima copia del file si trova nella directory di destinazione dell'installazione. La seconda copia del file si trova nella cache della baseline RTM. L'ultima copia del file si trova nella cache di base più recente.
-   La cache di base dell'applicazione viene rimossa quando il prodotto viene disinstallato.

A partire da Windows Installer versione 3.0, il programma di installazione può usare la cache di base quando le patch vengono applicate all'applicazione. Le informazioni di base possono essere usate per applicare una patch differenziale o ripristinare una versione precedente di un file durante una disinstallazione della patch. In questo modo gli autori di patch possono trarre vantaggio da patch differenziali più piccole. Se il programma di installazione rileva che la patch differenziale non può essere applicata al file di destinazione, il programma di installazione può tentare di usare un file salvato nella cache di base come punto di partenza. Il programma di installazione richiede solo l'origine di installazione originale dopo aver provato tutte le possibilità nella cache.

L'aderenza alle linee guida seguenti consente agli autori di patch di usare le patch Windows Installer versione 3.0 e la cache di base per creare patch differenziali più piccole:

-   Creare patch che includono la [tabella MsiPatchSequence](msipatchsequence-table.md). Questa tabella è necessaria per usare la cache di base ed è disponibile a partire da Windows Installer versione 3.0.
-   Non impostare criteri che impediscono la memorizzazione nella cache di base. Il valore dei criteri [MaxPatchCacheSize](maxpatchcachesize.md) specifica la percentuale massima di spazio su disco che può essere usata. Se il criterio MaxPatchCacheSize è impostato su 0, non vengono salvati file aggiuntivi nella cache di base. Se il criterio non è impostato, per impostazione predefinita è possibile usare un massimo del 10% dello spazio su disco. Se le dimensioni totali della cache raggiungono la percentuale massima di spazio su disco, non vengono salvati file aggiuntivi. I criteri non influiscono sui file che sono già stati salvati. Anche quando la memorizzazione nella cache è disabilitata, il programma di installazione può usare cache di base del prodotto esistenti.
-   Se la prima patch applicata include la [tabella MsiPatchSequence](msipatchsequence-table.md), la memorizzazione nella cache è abilitata per l'applicazione.
-   Se una patch nella transazione di manutenzione non include la tabella [MsiPatchSequence](msipatchsequence-table.md), la memorizzazione nella cache viene abilitata per l'applicazione solo se al prodotto viene applicata correttamente una patch di aggiornamento secondaria (Service Pack) che include la tabella MsiPatchSequence.
-   Generare il pacchetto patch usando strumenti di creazione delle [ patch, ad ](msimsp-exe.md) esempioMsimsp.exee [PATCHWIZ.DLL](patchwiz-dll.md).
-   Applicare sempre le patch per la versione RTM dell'applicazione o per una versione di aggiornamento secondario (Service Pack) dell'applicazione. Le destinazioni specificate nella tabella [TargetImages](targetimages-table-patchwiz-dll-.md) del file delle proprietà di creazione patch (PCP) devono essere punti di controllo del prodotto definiti dai primi tre campi della [**proprietà ProductVersion.**](productversion.md)
-   Non applicare mai patch a piccole immagini di aggiornamento. Le destinazioni per la compilazione della patch non devono includere le immagini di aggiornamento di piccole dimensioni precedenti.

 

 



