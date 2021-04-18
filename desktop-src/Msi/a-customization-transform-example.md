---
description: Questo esempio illustra come è possibile usare una trasformazione di personalizzazione per disabilitare le funzionalità e aggiungere nuove risorse.
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: Esempio di trasformazione della personalizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311106"
---
# <a name="a-customization-transform-example"></a>Esempio di trasformazione della personalizzazione

Questo esempio illustra come è possibile usare una trasformazione di personalizzazione per disabilitare le funzionalità e aggiungere nuove risorse.

Un amministratore può disabilitare definitivamente una funzionalità utilizzando una trasformazione di personalizzazione per immettere un valore 0 nella colonna livello della [tabella delle funzionalità](feature-table.md). L'applicazione della trasformazione personalizzazione impedisce quindi l'installazione e la visualizzazione della funzionalità anche se l'utente seleziona un'installazione completa usando l'interfaccia utente o impostando la proprietà [**ADDLOCAL**](addlocal.md) su All nella riga di comando. Per informazioni sul livello di installazione, vedere [tabella delle funzionalità](feature-table.md) e proprietà [**INSTALLLEVEL**](installlevel.md) .

Le risorse necessarie per personalizzare un'applicazione possono essere distribuite usando una trasformazione di personalizzazione per aggiungere uno o più nuovi componenti. La trasformazione deve aggiungere una o più nuove funzionalità per contenere questi nuovi componenti. Per le regole da seguire quando si distribuiscono risorse, ad esempio file, chiavi del registro di sistema o collegamenti, vedere [uso delle trasformazioni per aggiungere risorse](using-transforms-to-add-resources.md).

Questo esempio illustra come creare una [trasformazione](transforms.md) per personalizzare l'installazione dell'applicazione descritta in [un esempio di installazione](an-installation-example.md). Il pacchetto di installazione originale installa tutte le funzionalità dell'applicazione di esempio, inclusa la funzionalità Gate, che consente agli utenti di visualizzare le informazioni di ammissione per l'Arena di Red Park. Per alcuni gruppi di utenti sono necessarie solo le funzionalità dell'applicazione che forniscono informazioni sulla pianificazione degli eventi e che non necessitano della funzionalità di controllo. Questi gruppi devono anche ottenere un elenco telefonico speciale. La trasformazione deve quindi eseguire due operazioni: 1) personalizzare l'installazione in modo che questo gruppo riceva solo le funzionalità dell'applicazione necessarie e 2) fornisca le risorse necessarie per il nuovo elenco telefonico.

Un esempio di interfaccia utente minima per questo esempio è disponibile nei [componenti Windows SDK per Windows Installer sviluppatori](platform-sdk-components-for-windows-installer-developers.md) come file Uisample.msi. Se si dispone dell'SDK, è possibile accedere a tutti gli strumenti e i dati necessari per riprodurre il pacchetto di installazione di esempio, l'interfaccia utente e la trasformazione di personalizzazione.

La trasformazione personalizzazione presenta le specifiche seguenti:

-   La trasformazione personalizzazione è incorporata all'interno del file MNP2000.msi per garantire che sia sempre disponibile con il database di installazione.
-   L'installazione di MNP2000.msi con la trasformazione personalizzazione non installa la funzionalità di controllo, le funzionalità figlio della funzionalità di controllo o uno dei componenti della funzionalità di controllo, anche se l'utente seleziona il tipo completo di installazione.
-   Altre applicazioni possono condividere alcuni o tutti i componenti della funzionalità di controllo. I pacchetti di installazione di queste applicazioni possono installare tutti i relativi componenti nel computer dell'utente.
-   La rimozione di MNP2000.msi con la trasformazione personalizzazione non comporta la rimozione dei componenti di controllo installati da altre applicazioni.
-   L'installazione di MNP2000.msi con la trasformazione personalizzazione installa anche una nuova funzionalità di primo livello, \_ elenco telefonico e un nuovo componente, telefono, che richiede l'installazione della risorsa, Phone.txt. L'utente accede alla \_ funzionalità elenco telefonico usando un collegamento nella directory dei menu.

[Continua](customizing-an-original-database.md)

 

 



