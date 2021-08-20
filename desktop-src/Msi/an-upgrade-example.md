---
description: Le sezioni seguenti illustrano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in Esempio di installazione.
ms.assetid: 233302ea-abc3-4879-b868-425f2b10e02e
title: Esempio di aggiornamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a148c8d66c09ae2ce033d3ad2440040734a2b1301b2e9e1b9bb1b79e44beb06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066351"
---
# <a name="an-upgrade-example"></a>Esempio di aggiornamento

Le sezioni seguenti illustrano un esempio di creazione di un pacchetto di aggiornamento per l'applicazione descritta in [An Installation Example](an-installation-example.md). Un esempio di un'interfaccia utente minima per questo esempio è disponibile in componenti [dell'SDK](platform-sdk-components-for-windows-installer-developers.md) di Windows per sviluppatori di Windows Installer come file Uisample.msi. Se si dispone dell'SDK, è possibile accedere a tutti gli strumenti e i dati necessari per riprodurre il pacchetto di installazione di esempio, l'interfaccia utente e il pacchetto di aggiornamento di esempio.

Questo esempio illustra come creare un pacchetto Windows Installer che aggiorna l'ipotetico prodotto MNP2000 a un nuovo prodotto denominato MNP2001. Il pacchetto di aggiornamento di esempio applica un aggiornamento principale al prodotto che richiede la modifica del codice del prodotto. Per altre informazioni sugli aggiornamenti principali, vedere l'argomento sugli aggiornamenti [principali](major-upgrades.md) nella sezione [Applicazione di patch e](patching-and-upgrades.md) aggiornamenti.

Il pacchetto di aggiornamento di esempio presenta le specifiche seguenti:

-   Per ricevere questo aggiornamento a MNP2001, un utente deve aver installato in precedenza le versioni da 1.0 a 1.4 (inclusi) di MNP2000 in lingua inglese usando il programma di installazione Windows.
-   Quando un utente tenta di installare il pacchetto di aggiornamento, la funzionalità di aggiornamento di Windows Installer cerca nel computer dell'utente tutti i prodotti idonei per l'aggiornamento.
-   Windows Il programma di installazione esegue la migrazione di tutte le impostazioni delle funzionalità del prodotto originale al prodotto aggiornato.
-   Il programma di installazione rimuove tutte le funzionalità obsolete dal computer dell'utente.
-   Il programma di installazione installa tutte le nuove funzionalità appartenenti all'aggiornamento.
-   Una disinstallazione del pacchetto di aggiornamento rimuove il prodotto dal computer dell'utente e non ripristina la versione precedente del prodotto.
-   L'aggiornamento di esempio aggiorna i collegamenti a nuovi file e funzionalità.

    [Pianificazione di un aggiornamento principale](planning-a-major-upgrade.md)

    [Importazione del database di installazione originale](importing-original-installation-database.md)

    [Aggiornamento della struttura di directory per un aggiornamento](updating-directory-structure-for-an-upgrade.md)

    [Aggiornamento di file e attributi di file per un aggiornamento](updating-files-and-file-attributes-for-an-upgrade.md)

    [Aggiornamento dei componenti per un aggiornamento](updating-components-for-an-upgrade.md)

    [Aggiornamento delle funzionalità per un aggiornamento](updating-features-for-an-upgrade.md)

    [Aggiornamento dei collegamenti per un aggiornamento](updating-shortcuts-for-an-upgrade.md)

    [Aggiornamento della tabella di aggiornamento per un aggiornamento](updating-upgrade-table-for-an-upgrade.md)

    [Aggiornamento delle proprietà per un aggiornamento](updating-properties-for-an-upgrade.md)

    [Aggiornamento delle tabelle di sequenza per un aggiornamento](updating-sequence-tables-for-an-upgrade.md)

    [Aggiornamento delle informazioni di riepilogo per un aggiornamento](updating-summary-information-for-an-upgrade.md)

    [Convalida di un aggiornamento dell'installazione](validating-an-installation-upgrade.md)

 

 



