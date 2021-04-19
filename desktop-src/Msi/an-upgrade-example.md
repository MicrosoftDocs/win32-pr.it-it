---
description: Le sezioni seguenti presentano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in un esempio di installazione.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Esempio di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95d1e19173a98f3ddee49c19d0ec10aca7994e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311061"
---
# <a name="an-upgrade-example"></a>Esempio di aggiornamento

Le sezioni seguenti presentano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in [un esempio di installazione](an-installation-example.md). Un esempio di interfaccia utente minima per questo esempio è disponibile nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) come file Uisample.msi. Se si dispone dell'SDK, è possibile accedere a tutti gli strumenti e i dati necessari per riprodurre il pacchetto di installazione di esempio, l'interfaccia utente e il pacchetto di aggiornamento di esempio.

Questo esempio illustra come creare un pacchetto di Windows Installer che aggiorna il prodotto ipotetico MNP2000 a un nuovo prodotto denominato MNP2001. Il pacchetto di aggiornamento di esempio applica un aggiornamento principale al prodotto che richiede la modifica del codice del prodotto. Per ulteriori informazioni sugli aggiornamenti principali, vedere l'argomento relativo agli [aggiornamenti principali](major-upgrades.md) nella sezione applicazione di [patch e aggiornamenti](patching-and-upgrades.md) .

Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:

-   Per qualificarsi per la ricezione dell'aggiornamento a MNP2001, un utente deve avere installato in precedenza le versioni da 1,0 a 1,4 (incluse) della lingua inglese MNP2000 usando Windows Installer.
-   Quando un utente tenta di installare il pacchetto di aggiornamento, la funzionalità di aggiornamento di Windows Installer cerca nel computer dell'utente tutti i prodotti che sono idonei per l'aggiornamento.
-   Windows Installer esegue la migrazione di tutte le impostazioni della funzionalità del prodotto originale al prodotto aggiornato.
-   Il programma di installazione rimuove tutte le funzionalità obsolete dal computer dell'utente.
-   Il programma di installazione installa tutte le nuove funzionalità appartenenti all'aggiornamento.
-   Una disinstallazione del pacchetto di aggiornamento comporta la rimozione del prodotto dal computer dell'utente e non il ripristino della versione precedente del prodotto.
-   L'aggiornamento di esempio aggiorna i collegamenti ai nuovi file e funzionalità.

    [Pianificazione di un aggiornamento principale](planning-a-major-upgrade.md)

    [Importazione del database di installazione originale](importing-original-installation-database.md)

    [Aggiornamento della struttura di directory per un aggiornamento](updating-directory-structure-for-an-upgrade.md)

    [Aggiornamento di file e attributi di file per un aggiornamento](updating-files-and-file-attributes-for-an-upgrade.md)

    [Aggiornamento dei componenti per un aggiornamento](updating-components-for-an-upgrade.md)

    [Aggiornamento delle funzionalità per un aggiornamento](updating-features-for-an-upgrade.md)

    [Aggiornamento dei collegamenti per un aggiornamento](updating-shortcuts-for-an-upgrade.md)

    [Aggiornamento della tabella di aggiornamento per un aggiornamento](updating-upgrade-table-for-an-upgrade.md)

    [Aggiornamento delle proprietà per un aggiornamento](updating-properties-for-an-upgrade.md)

    [Aggiornamento di tabelle di sequenza per un aggiornamento](updating-sequence-tables-for-an-upgrade.md)

    [Aggiornamento delle informazioni di riepilogo per un aggiornamento](updating-summary-information-for-an-upgrade.md)

    [Convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md)

 

 



