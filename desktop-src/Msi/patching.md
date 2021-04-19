---
description: Queste sezioni descrivono l'applicazione di patch a un'installazione Windows Installer.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Applicazione di patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3117723bda1699eeae341fc75db201421f6ae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318997"
---
# <a name="patching"></a>Applicazione di patch

È possibile aggiornare un'applicazione che è stata installata utilizzando il Microsoft Windows Installer installando un pacchetto di installazione aggiornato (file con estensione msi) o applicando una patch Windows Installer (un file con estensione msp) all'applicazione.

Una patch Windows Installer (file con estensione msp) è un pacchetto autonomo che contiene gli aggiornamenti dell'applicazione e descrive quali versioni dell'applicazione possono ricevere la patch. Le patch contengono almeno due trasformazioni di database e possono contenere file di patch archiviati nel flusso di file CAB del pacchetto di patch. Per ulteriori informazioni sulle parti di un pacchetto Windows Installer patch, vedere la pagina relativa ai [pacchetti di patch](patch-packages.md).

Il servizio di applicazioni tramite la distribuzione di un Windows Installer patch, anziché un pacchetto di installazione completo per il prodotto aggiornato, può presentare dei vantaggi. Una patch può contenere un intero file o solo i bit di file necessari per aggiornare una parte del file. In questo modo l'utente può scaricare una patch di aggiornamento che è molto più piccola del pacchetto di installazione per l'intero prodotto. Un aggiornamento che usa una patch può mantenere una personalizzazione dell'applicazione dell'applicazione durante l'aggiornamento.

* * Windows Installer 4,5 e versioni successive: * *

A partire da Windows Installer 4,5, gli sviluppatori possono contrassegnare i componenti in una patch con il valore **msidbComponentAttributesUninstallOnSupersedence** nella [tabella Component](component-table.md). Se è installata una patch successiva, contrassegnata con il valore **msidbPatchSequenceSupersedeEarlier** nella [tabella MsiPatchSequence](msipatchsequence-table.md) per sostituire la prima patch, Windows Installer 4,5 e versioni successive possono annullare la registrazione e la disinstallazione dei componenti contrassegnati come **msidbComponentAttributesUninstallOnSupersedence** per evitare di lasciare i componenti inutilizzati nel computer. Se il componente non è contrassegnato con questo bit, l'installazione della patch sostitutiva può lasciare un componente inutilizzato nel computer. L'impostazione della proprietà **MSIUNINSTALLSUPERSEDEDCOMPONENTS** ha lo stesso effetto dell'impostazione di questo bit per tutti i componenti.

* * Windows Installer 3,0 e versioni successive: * *

Gli sviluppatori che usano Windows Installer 3,0 e creano pacchetti di patch con la [tabella MsiPatchSequence](msipatchsequence-table.md) possono creare pacchetti di patch che eseguono le operazioni seguenti:

-   Usare la baseline del prodotto memorizzata nella cache dal programma di installazione per semplificare il servizio di applicazioni con patch Delta più piccole. Per ulteriori informazioni sull'utilizzo della linea di base del prodotto, vedere [riduzione delle dimensioni delle patch](reducing-patch-size.md).
-   Ignorare le azioni associate a tabelle specifiche che non sono state modificate dalla patch. Questo può ridurre significativamente il tempo necessario per installare la patch. Per ulteriori informazioni sulle tabelle che è possibile ignorare, vedere [ottimizzazione della patch](patch-optimization.md).
-   Creare e installare patch che possono essere disinstallate singolarmente e in qualsiasi ordine senza dover disinstallare e reinstallare l'intera applicazione e altre patch. Per ulteriori informazioni sulla disinstallazione delle patch, vedere [rimozione di patch](removing-patches.md).
-   Applicare le patch in un ordine costante indipendentemente dall'ordine con cui le patch vengono fornite al sistema. Per ulteriori informazioni sul modo in cui il Windows Installer determina la sequenza utilizzata per applicare le patch, vedere [sequenziazione delle patch](sequencing-patches.md).
-   Applicare patch a un'applicazione installata in un contesto gestito per utente. Per altre informazioni, vedere [applicazione di patch Per-User applicazioni gestite](patching-per-user-managed-applications.md).

* * Windows Installer 2,0: * *

La [tabella MsiPatchSequence](msipatchsequence-table.md) non è supportata. A partire da Windows Installer 3,0, i pacchetti di patch possono contenere informazioni che descrivono la sequenza di patch per la patch rispetto ad altri aggiornamenti e informazioni descrittive aggiuntive.

Il metodo consigliato per la creazione di un pacchetto di patch consiste nell'usare strumenti per la creazione di patch, ad esempio [Msimsp.exe](msimsp-exe.md) e [Patchwiz.dll](patchwiz-dll.md). Gli sviluppatori possono generare un file di creazione patch, come descritto nella sezione [creazione di un pacchetto di patch](creating-a-patch-package.md). La creazione di una patch di aggiornamento di piccole dimensioni è descritta nella sezione: esempio di applicazione di [patch per un piccolo aggiornamento](a-small-update-patching-example.md).

Microsoft Windows Installer accetta una Uniform Resource Locator (URL) come origine valida per una patch. Per ulteriori informazioni su come installare una patch che si trova in un server Web, vedere [download e installazione di una patch da Internet](downloading-and-installing-a-patch-from-the-internet.md).

Quando si installa un'applicazione per la prima volta, è possibile applicare una singola patch di Windows Installer (file con estensione msp) al pacchetto di installazione. Per ulteriori informazioni, vedere applicazione di [patch alle installazioni iniziali](patching-initial-installations.md).

Non è possibile eliminare tutte le circostanze in cui l'applicazione di una patch potrebbe richiedere l'accesso all'origine dell'installazione originale. Tuttavia, per ridurre al minimo la possibilità che la patch richieda l'accesso all'origine originale, attenersi ai punti elencati nella sezione seguente: [impedire a una patch di richiedere l'accesso all'origine dell'installazione originale](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Per ridurre al minimo la possibilità che la patch non venga interruppe da una trasformazione di personalizzazione successiva, in genere la patch viene installata per prima, seguita dalla personalizzazione. Prima di installare le trasformazioni di personalizzazione e quindi la patch, è possibile che la personalizzazione venga interrotta. Per ulteriori informazioni sull'applicazione di patch alle applicazioni personalizzate, vedere [applicazione di patch alle applicazioni personalizzate](patching-customized-applications.md).

 

 



