---
description: Le finestre di dialogo vengono specificate nella colonna finestra di dialogo della tabella della finestra di dialogo. Per ulteriori informazioni sull'aggiunta di una finestra di dialogo o di un Billboard a un'interfaccia utente, vedere Utilizzo dell'interfaccia utente.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Finestre di dialogo (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5695a8d936d0933983407ba52a531ea839137c09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232255"
---
# <a name="dialog-boxes-windows-installer"></a>Finestre di dialogo (Windows Installer)

Le finestre di dialogo vengono specificate nella colonna finestra di dialogo della [tabella della finestra di dialogo](dialog-table.md). Per ulteriori informazioni sull'aggiunta di una finestra di dialogo o di un Billboard a un'interfaccia utente, vedere [utilizzo dell'interfaccia utente](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nomi della finestra di dialogo riservata

I nomi delle finestre di dialogo seguenti sono riservati da Windows Installer e non devono essere utilizzati per le finestre di dialogo personalizzate create dall'utente. Il programma di installazione richiede che tali finestre di dialogo siano elencate nella [tabella della finestra di dialogo](dialog-table.md) utilizzando i nomi riservati seguenti. Ogni finestra di dialogo e il nome possono essere elencati una sola volta. Gli sviluppatori devono creare queste finestre di dialogo nell'interfaccia utente. Per informazioni sull'anteprima delle finestre di dialogo, vedere [importazione dell'interfaccia utente](importing-the-user-interface.md).



| Nome della finestra di dialogo                                      | Breve descrizione della finestra di dialogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Finestra di dialogo filesinus](filesinuse-dialog.md)           | Avvisa l'utente di elaborare la sovrascrittura o l'eliminazione di file.                                                                                                                 |
| [Finestra di dialogo FirstRun](firstrun-dialog.md)               | Raccoglie il nome utente, il nome della società e l'ID prodotto.                                                                                                                       |
| [Finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Avvisa l'utente per la sovrascrittura o l'eliminazione di file e offre all'utente la possibilità di usare [Gestione riavvio](/windows/desktop/RstMgr/restart-manager-portal) per chiudere e riavviare le applicazioni. |



 

## <a name="required-dialog-boxes"></a>Finestre di dialogo obbligatorie

Durante l'installazione, determinati eventi determinano Windows Installer di controllare le [tabelle di sequenza dell'interfaccia utente](using-a-sequence-table.md) nel pacchetto e visualizzare la finestra di dialogo specificata. Ad esempio, in caso di errore irreversibile, Windows Installer Visualizza la finestra di dialogo elencata con un numero di sequenza di-3 nella tabella delle sequenze dell'interfaccia utente indipendentemente dalla finestra di dialogo denominata nella [tabella della finestra di dialogo](dialog-table.md). La tabella seguente elenca gli eventi specifici e il numero di sequenza corrispondente nella tabella sequenza dell'interfaccia utente:



| Tipo di evento                        | Numero di sequenza della tabella sequenza dell'interfaccia utente | Descrizione della finestra di dialogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Errore irreversibile](fatalerror-dialog.md) | -3                                            | L'installazione è stata interrotta da un errore irreversibile.      |
| [Uscita dall'utente](userexit-dialog.md)     | -2                                            | L'installazione è stata terminata in corrispondenza della richiesta dell'utente. |
| [Esci](exit-dialog.md)              | -1                                            | L'installazione è stata completata correttamente.               |



 

Inoltre, l'autore del pacchetto deve creare una finestra di dialogo generica per visualizzare Windows Installer messaggi di [errore](error-dialog.md) . Questa finestra di dialogo può avere un nome qualsiasi, ma questo nome deve essere specificato nella proprietà **ErrorDialog** .

## <a name="typical-dialog-boxes"></a>Finestre di dialogo tipiche

Le finestre di dialogo seguenti sono facoltative e sono comunemente incluse nell'interfaccia utente creata di un pacchetto di installazione. Queste finestre di dialogo sono tipiche della maggior parte delle [procedure guidate dell'interfaccia utente](user-interface-wizard-behavior.md) per l'installazione di file. Queste finestre di dialogo possono avere qualsiasi nome nella tabella della finestra di dialogo. I nomi visualizzati sono consigliati per maggiore chiarezza e possono essere modificati se necessario. È ad esempio possibile utilizzare nel pacchetto due finestre di dialogo **LicenseAgreement** personalizzate e distinguerle in base ai nomi ProfessionalLicenseAgreement e LimitedLicenseAgreement.



| Tipo di finestra di dialogo                                             | Breve descrizione della finestra di dialogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Finestra di dialogo DiskCost](diskcost-dialog.md)                  | Indica uno spazio su disco insufficiente per l'installazione. |
| [Finestra di dialogo Sfoglia](browse-dialog.md)                      | Consente all'utente di selezionare una directory.                     |
| [Finestra di dialogo Annulla](cancel-dialog.md)                      | Conferma la richiesta di terminare l'installazione.       |
| [Finestra di dialogo contratto di licenza](licenseagreement-dialog.md) | Casella modale che Visualizza il contratto di licenza.             |
| [Finestra di dialogo selezione](selection-dialog.md)                | Casella modale che consente all'utente di selezionare gli elementi.            |



 

 

 
