---
description: Le finestre di dialogo vengono specificate nella colonna Finestra di dialogo della tabella Finestra di dialogo. Per altre informazioni sull'aggiunta di una finestra di dialogo o di un manifesto a un'interfaccia utente, vedere Using the Interfaccia utente.
ms.assetid: 7cecb1c6-3dc3-48a1-94b9-1976c72b7764
title: Finestre di dialogo (Windows programma di installazione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38da0e4d562854abc32064eee06a303747c2587591a5526ae98177a13e0462a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764061"
---
# <a name="dialog-boxes-windows-installer"></a>Finestre di dialogo (Windows programma di installazione)

Le finestre di dialogo vengono specificate nella colonna Finestra di dialogo della [tabella Finestra di dialogo](dialog-table.md). Per altre informazioni sull'aggiunta di una finestra di dialogo o di un manifesto a un'interfaccia utente, vedere [Using the Interfaccia utente](using-the-user-interface.md).

## <a name="reserved-dialog-box-names"></a>Nomi delle finestre di dialogo riservate

I nomi delle finestre di dialogo seguenti sono riservati Windows Programma di installazione e non devono essere usati per le finestre di dialogo personalizzate scritte dall'utente. Il programma di installazione richiede che queste finestre di dialogo siano elencate nella [tabella Dialog usando](dialog-table.md) i nomi riservati seguenti. Ogni finestra di dialogo e ogni nome possono essere elencati una sola volta. Gli sviluppatori devono creare queste finestre di dialogo nell'interfaccia utente. Per informazioni su come visualizzare in anteprima le finestre di dialogo, vedere [Importazione del Interfaccia utente](importing-the-user-interface.md).



| Nome della finestra di dialogo                                      | Breve descrizione della finestra di dialogo                                                                                                                                         |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Finestra di dialogo FileInUse](filesinuse-dialog.md)           | Avvisa l'utente di elaborare la sovrascrittura o l'eliminazione di file.                                                                                                                 |
| [Finestra di dialogo FirstRun](firstrun-dialog.md)               | Raccoglie il nome utente, il nome della società e l'ID prodotto.                                                                                                                       |
| [Finestra di dialogo MsiRMFilesInUse](msirmfilesinuse-dialog.md) | Avvisa l'utente di elaborare la sovrascrittura o l'eliminazione di file e offre all'utente la possibilità di usare Gestione riavvio [per](/windows/desktop/RstMgr/restart-manager-portal) chiudere e riavviare le applicazioni. |



 

## <a name="required-dialog-boxes"></a>Finestre di dialogo obbligatorie

Durante l'installazione, alcuni eventi Windows installer [](using-a-sequence-table.md) controllano le tabelle di sequenza dell'interfaccia utente nel pacchetto e visualizzano la finestra di dialogo specificata. Ad esempio, in caso di errore irreversibile, nel programma di installazione di Windows viene visualizzata la finestra di dialogo elencata con un numero di sequenza -3 nella tabella della sequenza dell'interfaccia utente indipendentemente dal nome della finestra di dialogo nella tabella Finestra di [dialogo](dialog-table.md). Nella tabella seguente sono elencati gli eventi specifici e il numero di sequenza corrispondente nella tabella della sequenza dell'interfaccia utente:



| Tipo di evento                        | Numero di sequenza della tabella della sequenza dell'interfaccia utente | Descrizione della finestra di dialogo                              |
|--------------------------------------|-----------------------------------------------|--------------------------------------------------------|
| [Errore irreversibile](fatalerror-dialog.md) | -3                                            | L'installazione è stata terminata da un errore irreversibile.      |
| [Uscita dell'utente](userexit-dialog.md)     | -2                                            | L'installazione è stata terminata su richiesta dell'utente. |
| [Esci](exit-dialog.md)              | -1                                            | L'installazione è stata completata correttamente.               |



 

Inoltre, l'autore del pacchetto deve creare una finestra di dialogo generica per visualizzare Windows di [errore del programma di](error-dialog.md) installazione. Questa finestra di dialogo può essere denominata qualsiasi elemento, ma questo nome deve essere specificato nella **proprietà ErrorDialog.**

## <a name="typical-dialog-boxes"></a>Finestre di dialogo tipiche

Le finestre di dialogo seguenti sono facoltative e sono in genere incluse nell'interfaccia utente di creazione di un pacchetto di installazione. Queste finestre di dialogo sono tipiche della maggior parte [delle procedure guidate dell'interfaccia utente per](user-interface-wizard-behavior.md) l'installazione di file. Queste finestre di dialogo possono avere qualsiasi nome nella tabella Finestra di dialogo. I nomi visualizzati sono consigliati solo per maggiore chiarezza e possono essere modificati in base alle esigenze. Ad esempio, è possibile usare due diverse finestre di dialogo **personalizzate LicenseAgreement** nel pacchetto e distinguersi nella tabella Dialog dai nomi ProfessionalLicenseAgreement e LimitedLicenseAgreement.



| Tipo di finestra di dialogo                                             | Breve descrizione della finestra di dialogo                         |
|-------------------------------------------------------------|---------------------------------------------------------|
| [Finestra di dialogo DiskCost](diskcost-dialog.md)                  | Indica spazio su disco insufficiente per l'installazione. |
| [Finestra di dialogo Sfoglia](browse-dialog.md)                      | Consente all'utente di selezionare una directory.                     |
| [Finestra di dialogo Annulla](cancel-dialog.md)                      | Conferma una richiesta di interruzione dell'installazione.       |
| [Finestra di dialogo Contratto di licenza](licenseagreement-dialog.md) | Casella modale che visualizza il contratto di licenza.             |
| [Finestra di dialogo Selezione](selection-dialog.md)                | Casella modale che consente all'utente di selezionare gli elementi.            |



 

 

 
