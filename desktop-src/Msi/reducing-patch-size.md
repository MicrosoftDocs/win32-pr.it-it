---
description: A partire da Windows Installer versione 3,0, gli autori delle patch possono usare la baseline del prodotto memorizzata nella cache dal programma di installazione per semplificare il servizio di applicazioni con patch Delta più piccole.
ms.assetid: ab5b193d-79ce-4ed4-af53-89a4197197c1
title: Riduzione delle dimensioni delle patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fa365e831ab8685073347dc254bac58269135f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311717"
---
# <a name="reducing-patch-size"></a>Riduzione delle dimensioni delle patch

A partire da Windows Installer versione 3,0, gli autori delle patch possono usare la baseline del prodotto memorizzata nella cache dal programma di installazione per semplificare il servizio di applicazioni con patch Delta più piccole. In molti casi, una [*patch Delta*](d-gly.md) che fornisce informazioni sul servizio a un'applicazione può essere notevolmente più piccola rispetto a una patch di file completo o a un pacchetto di installazione che fornisce le stesse informazioni.

**Windows Installer 2,0:** Non supportato. A partire da Windows Installer 3,0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornate.

In Windows Installer sono disponibili tre metodi per l'aggiornamento e la manutenzione di applicazioni: [piccoli aggiornamenti](small-updates.md), aggiornamenti [secondari](minor-upgrades.md)e [aggiornamenti principali](major-upgrades.md). Un aggiornamento di piccole dimensioni è noto anche come aggiornamento QFE (Quick Fix Engineering) e un aggiornamento secondario viene definito anche aggiornamento di Service Pack (SP). Un tipico aggiornamento principale rimuove un'applicazione precedente e installa una nuova applicazione. Windows Installer possibile recapitare le informazioni di manutenzione alle applicazioni come [pacchetto di installazione](installation-package.md) (file con estensione msi) o come [pacchetto di patch](patch-packages.md) (file con estensione msp).

Un pacchetto Windows Installer patch che fornisce informazioni di manutenzione per un aggiornamento di piccole dimensioni o un aggiornamento secondario è in genere molto più piccolo del pacchetto di installazione equivalente che fornisce le stesse informazioni di manutenzione. È consigliabile usare i pacchetti di patch per la distribuzione di aggiornamenti piccoli e secondari. Per la distribuzione di un aggiornamento principale è consigliabile usare un pacchetto di installazione.

Windows Installer patch (file con estensione msp) possono essere generate da file completi o da differenze di file, denominate anche Delta di file. Una patch Windows Installer generata da Delta di file può essere molto più piccola della patch di file completo equivalente. Tutte le versioni del Windows Installer possono usare sia patch di file completi che patch Delta.

A partire da Windows Installer versione 3,0, il programma di installazione salva in modo selettivo le informazioni di base sui file quando vengono aggiornate. Le informazioni sull'applicazione di base originale (versione RTM) e l'aggiornamento secondario più recente (Service Pack) vengono salvate in un percorso privato quando l'applicazione viene installata o riceve un aggiornamento secondario.

Il programma di installazione esegue le operazioni seguenti per ridurre al minimo le dimensioni della cache di base:

-   Non vengono mantenute più di due linee di base per ogni applicazione: una linea di base del file come originariamente rilasciata (RTM) e una linea di base del file nell'aggiornamento secondario più recente (Service Pack).
-   Un file non viene aggiunto alla cache finché non viene patchato. La cache di base è copy-on-Write.
-   Se l'applicazione non è mai stata aggiornata, non sono presenti file nella cache di base.
-   Quando l'ultima manutenzione dell'applicazione era un aggiornamento secondario (Service Pack), l'applicazione è a livello di base e al massimo due copie di un file possono essere presenti nel computer. Una copia del file si trova nella directory di destinazione dell'installazione. L'altra copia può trovarsi nella cache Baseline RTM.
-   Quando l'ultima manutenzione dell'applicazione era un piccolo aggiornamento (QFE), l'applicazione non si trova a un livello di base e al massimo tre copie di un file possono essere presenti nel computer. La prima copia del file si trova nella directory di destinazione dell'installazione. La seconda copia del file si trova nella cache di base RTM. L'ultima copia del file si trova nella cache di base più recente.
-   La cache di base dell'applicazione viene rimossa quando il prodotto viene disinstallato.

A partire da Windows Installer versione 3,0, il programma di installazione può usare la cache di base quando le patch vengono applicate all'applicazione. È possibile usare le informazioni di base per applicare una patch Delta o per ripristinare un file a una versione precedente durante la disinstallazione di una patch. In questo modo gli autori delle patch possono trarre vantaggio dalle patch Delta più piccole. Se il programma di installazione rileva che non è possibile applicare la patch Delta al file di destinazione, il programma di installazione può tentare di usare un file salvato nella cache di base come punto di partenza. Il programma di installazione ricorre solo alla richiesta dell'origine di installazione originale dopo aver provato tutte le possibilità nella cache.

L'adesione alle linee guida seguenti può aiutare gli autori di patch a usare Patch Windows Installer versione 3,0 e la cache di base per creare patch Delta più piccole:

-   Creare patch che includano la [tabella MsiPatchSequence](msipatchsequence-table.md). Questa tabella è necessaria per usare la cache Baseline ed è disponibile a partire dalla versione Windows Installer 3,0.
-   Non impostare criteri che impediscono la memorizzazione nella cache di base. Il valore del criterio [MaxPatchCacheSize](maxpatchcachesize.md) specifica la percentuale massima di spazio su disco che è possibile utilizzare. Se il criterio MaxPatchCacheSize è impostato su 0, non viene salvato alcun file aggiuntivo nella cache di base. Se il criterio non è impostato, il valore predefinito è che è possibile utilizzare un massimo del 10% dello spazio su disco. Se la dimensione totale della cache raggiunge la percentuale massima di spazio su disco, non viene salvato alcun file aggiuntivo. Il criterio non influisce sui file che sono già stati salvati. Anche quando la memorizzazione nella cache è disabilitata, il programma di installazione può usare le cache di base del prodotto esistenti.
-   Se la prima patch applicata include la [tabella MsiPatchSequence](msipatchsequence-table.md), la memorizzazione nella cache è abilitata per l'applicazione.
-   Se una patch nella transazione di manutenzione non include la [tabella MsiPatchSequence](msipatchsequence-table.md), la memorizzazione nella cache è abilitata per l'applicazione solo se una patch di aggiornamento secondaria (Service Pack) che include la tabella MsiPatchSequence è stata applicata correttamente al prodotto.
-   Generare il pacchetto di patch usando gli strumenti di creazione della patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [PATCHWIZ.DLL](patchwiz-dll.md).
-   Usare sempre le patch per la versione RTM dell'applicazione o per una versione di aggiornamento secondaria (Service Pack) dell'applicazione. Le destinazioni specificate nella [tabella TargetImages](targetimages-table-patchwiz-dll-.md) del file PCP (Patch Creation Properties) devono essere punti di controllo del prodotto definiti dai primi tre campi della proprietà [**ProductVersion**](productversion.md) .
-   Non utilizzare mai patch per le immagini di aggiornamento di piccole dimensioni. Le destinazioni per la compilazione della patch non devono includere le immagini di aggiornamento di piccole dimensioni precedenti.

 

 



