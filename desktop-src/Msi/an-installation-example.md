---
description: Questo esempio illustra come creare un semplice pacchetto di Windows Installer per l'installazione di un'applicazione.
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: Esempio di installazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881137"
---
# <a name="an-installation-example"></a>Esempio di installazione

Questo esempio illustra come creare un semplice pacchetto di Windows Installer per l'installazione di un'applicazione. Nell'esempio viene installato il blocco note, un editor di testo incluso in Windows e diversi file di testo che descrivono gli eventi e le ammissioni nell'Arena Red Park immaginaria.

Nell'esempio sono presenti le specifiche seguenti:

-   L'applicazione viene fornita agli utenti come pacchetto di Windows Installer di installazione automatica che installa tutti i file, i collegamenti e le informazioni del registro di sistema necessari.
-   Il pacchetto di installazione può presentare all'utente una procedura guidata dell'interfaccia utente durante l'installazione per raccogliere informazioni sull'utente.
-   Durante l'installazione, gli utenti hanno la possibilità di selezionare le singole funzionalità da installare per l'esecuzione in locale, l'esecuzione dall'origine o l'installazione.
-   Una delle funzionalità può essere presentata agli utenti come una funzionalità di installazione su richiesta.
-   Lo stesso pacchetto Disinstalla l'applicazione e rimuove tutti i file dell'applicazione e le informazioni del registro di sistema dal computer dell'utente.
-   Il pacchetto è pronto a ricevere un aggiornamento principale che include la modifica del codice del prodotto.

Per riprodurre l'esempio, è necessario uno strumento software in grado di creare e modificare un database di Windows Installer vuoto. Sono disponibili diversi strumenti per la creazione di pacchetti di fornitori di software indipendenti. Un editor di database Windows Installer denominato Orca viene fornito nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md).

Per completare l'esempio, seguire questa procedura:

[Pianificazione dell'installazione](planning-the-installation.md)

[Importazione di un database vuoto](importing-a-blank-database.md)

[Specifica della struttura di directory](specifying-directory-structure.md)

[Specifica di componenti](specifying-components.md)

[Specifica di file e attributi di file](specifying-files-and-file-attributes.md)

[Specifica dei supporti di origine](specifying-source-media.md)

[Specifica delle funzionalità](specifying-features.md)

[Specifica di relazioni Feature-Component](specifying-feature-component-relationships.md)

[Aggiunta di informazioni del registro di sistema](adding-registry-information.md)

[Specifica dei collegamenti](specifying-shortcuts.md)

[Specifica delle proprietà](specifying-properties.md)

[Importazione del InstallExecuteSequence](importing-the-installexecutesequence.md)

[Importazione del InstallUISequence](importing-the-installuisequence.md)

[Importazione del AdminExecuteSequence](importing-the-adminexecutesequence.md)

[Importazione del AdminUISequence](importing-the-adminuisequence.md)

[Importazione del AdvtExecuteSequence](importing-the-advtexecutesequence.md)

[Aggiunta di informazioni di riepilogo](adding-summary-information.md)

[Importazione dell'interfaccia utente](importing-the-user-interface.md)

[Convalida di un database di installazione](validating-an-installation-database.md)

 

 



