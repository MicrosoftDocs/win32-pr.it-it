---
description: Queste sezioni descrivono l'applicazione di patch a un Windows installazione del programma di installazione.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Applicazione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb90436c2a33495aaa818d0796c5d749e5d76286db4dbdc247ec4ee58c7ea6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926238"
---
# <a name="patching"></a>Applicazione di patch

Un'applicazione installata tramite il programma di installazione di Microsoft Windows può essere aggiornata reinstallando un pacchetto di installazione aggiornato (file .msi) o applicando una patch del programma di installazione di Windows (un file msp) all'applicazione.

Una patch Windows Installer (file msp) è un pacchetto autonomo che contiene gli aggiornamenti dell'applicazione e descrive le versioni dell'applicazione che possono ricevere la patch. Le patch contengono almeno due trasformazioni di database e possono contenere file di patch archiviati nel flusso di file CAB del pacchetto di patch. Per altre informazioni sulle parti di un pacchetto di patch Windows Installer, vedere [Patch Packages](patch-packages.md).

La manutenzione delle applicazioni tramite la distribuzione di una patch Windows Installer, anziché un pacchetto di installazione completo per il prodotto aggiornato, può offrire vantaggi. Una patch può contenere un intero file o solo i bit di file necessari per aggiornare parte del file. In questo modo l'utente può scaricare una patch di aggiornamento molto più piccola rispetto al pacchetto di installazione per l'intero prodotto. Un aggiornamento che usa una patch può mantenere una personalizzazione dell'applicazione da parte dell'utente durante l'aggiornamento.

**Windows Installer 4.5 e versioni successive: **

A partire da Windows Installer 4.5, gli sviluppatori possono contrassegnare i componenti in una patch con il valore **msidbComponentAttributesUninstallOnSupersedence** nella tabella [Component](component-table.md). Se viene installata una patch successiva, contrassegnata con il valore **msidbPatchSequenceSupersedeEarlier** nella tabella [MsiPatchSequence](msipatchsequence-table.md) per la prima patch, il programma di installazione di Windows 4.5 e versioni successive può annullare la registrazione e disinstallare i componenti contrassegnati come **msidbComponentAttributesUninstallOnSupersedence** per evitare di lasciare i componenti inutilizzati nel computer. Se il componente non è contrassegnato con questo bit, l'installazione della patch sostituita può lasciare un componente inutilizzato nel computer. **L'impostazione della proprietà MSIUNINSTALLSUPERSEDEDCOMPONENTS** ha lo stesso effetto dell'impostazione di questo bit per tutti i componenti.

**Windows Installer 3.0 e versioni successive: **

Gli sviluppatori che usano Windows Installer 3.0 e creano pacchetti di patch con la tabella [MsiPatchSequence](msipatchsequence-table.md) possono creare pacchetti di patch che ese possano eseguire le operazioni seguenti:

-   Usare la baseline del prodotto memorizzata nella cache dal programma di installazione per gestire più facilmente le applicazioni con patch delta più piccole. Per altre informazioni sull'uso della baseline del prodotto, vedere [Riduzione delle dimensioni delle patch.](reducing-patch-size.md)
-   Ignorare le azioni associate a tabelle specifiche che non vengono modificati dalla patch. Ciò può ridurre significativamente il tempo necessario per installare la patch. Per altre informazioni sulle tabelle che possono essere ignorate, vedere [Ottimizzazione delle patch.](patch-optimization.md)
-   Creare e installare patch che possono essere disinstallate in modo software e in qualsiasi ordine, senza dover disinstallare e reinstallare l'intera applicazione e altre patch. Per altre informazioni sulla disinstallazione delle patch, vedere [Rimozione di patch.](removing-patches.md)
-   Applicare le patch in un ordine costante indipendentemente dall'ordine in cui le patch vengono fornite al sistema. Per altre informazioni sul modo in cui Windows installer determina la sequenza usata per applicare le patch, vedere [Sequenziazione delle patch.](sequencing-patches.md)
-   Applicare patch a un'applicazione installata in un contesto gestito per utente. Per altre informazioni, vedere [Applicazione di patch Per-User applicazioni gestite.](patching-per-user-managed-applications.md)

**Windows Installer 2.0: **

La [tabella MsiPatchSequence](msipatchsequence-table.md) non è supportata. A partire da Windows Installer 3.0, i pacchetti di patch possono contenere informazioni che descrivono la sequenza di applicazione di patch per la patch rispetto ad altri aggiornamenti e informazioni descrittive aggiuntive.

Il metodo consigliato per la creazione di un pacchetto di patch è l'uso di strumenti per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md). Gli sviluppatori possono generare un file di creazione di patch come descritto nella sezione Creazione [di un pacchetto di patch.](creating-a-patch-package.md) La creazione di una piccola patch di aggiornamento è descritta nella sezione A [Small Update Patching Example](a-small-update-patching-example.md).

Microsoft Windows Installer accetta un Uniform Resource Locator (URL) come origine valida per una patch. Per altre informazioni su come installare una patch in un server Web, vedere Download e installazione di [una patch da Internet.](downloading-and-installing-a-patch-from-the-internet.md)

Quando si installa un'Windows per la prima volta, è possibile applicare una singola patch del programma di installazione (file con estensione msp) al pacchetto di installazione. Per altre informazioni, vedere [Applicazione di patch alle installazioni iniziali.](patching-initial-installations.md)

Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch può richiedere l'accesso all'origine dell'installazione originale. Tuttavia, per ridurre al minimo la possibilità che la patch richieda l'accesso all'origine originale, attenersi ai punti elencati nella sezione seguente: [Impedisci a](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)una patch di richiedere l'accesso all'origine di installazione originale .

Per ridurre al minimo la possibilità che la patch non sia interrotta da una successiva trasformazione di personalizzazione, in genere la patch viene installata per prima, seguita dalla personalizzazione. L'installazione delle trasformazioni di personalizzazione prima e quindi della patch potrebbe interrompere la personalizzazione. Per altre informazioni sull'applicazione di patch alle applicazioni personalizzate, vedere [Applicazione di patch alle applicazioni personalizzate.](patching-customized-applications.md)

 

 



