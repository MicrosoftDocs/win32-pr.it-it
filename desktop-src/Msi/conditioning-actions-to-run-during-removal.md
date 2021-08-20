---
description: Esistono due modi per creare il database di installazione Windows Installer, in modo che un'azione viene chiamata solo quando il pacchetto viene disinstallato.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Azioni di condizionamento da eseguire durante la rimozione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18fa9596dd6868b105f87c795ad70b6edc5ebac96381ffcc2b8b951947c87568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144324"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Azioni di condizionamento da eseguire durante la rimozione

Esistono due modi per creare il database di installazione in modo che un'azione viene chiamata solo quando il pacchetto viene disinstallato:

-   Se l'azione viene sequenziata dopo l'azione [InstallValidate](installvalidate-action.md) nella tabella [InstallExecuteSequence](installexecutesequence-table.md), l'autore del pacchetto può specificare una condizione REMOVE="ALL" per l'azione nella colonna Condizione . Si noti che [**non è**](remove.md) garantito che la proprietà REMOVE venga impostata su ALL durante una disinstallazione prima che il programma di installazione ese venga eseguita l'azione InstallValidate. Si noti che le virgolette intorno al valore ALL sono necessarie in questo caso.
-   Se l'azione viene sequenziata dopo l'azione [CostFinalize](costfinalize-action.md) ed eventuali azioni che potrebbero modificare lo stato della funzionalità, ad esempio [l'azione MigrateFeatureStates](migratefeaturestates-action.md), l'azione può essere condizionata in base allo stato di una particolare funzionalità o componente. Vedere [Sintassi delle istruzioni condizionali.](conditional-statement-syntax.md) Usare questa opzione per chiamare un'azione durante la rimozione di una particolare funzionalità o componente, che può verificarsi al di fuori della rimozione completa dell'applicazione.

Si noti che [**la proprietà Installed**](installed.md) può essere usata nelle espressioni condizionali per determinare se un prodotto è installato per computer o per l'utente corrente. Per determinare se il prodotto è installato per un utente diverso, controllare la [**proprietà ProductState.**](productstate.md)

Si noti che le versioni precedenti di un prodotto possono essere rimosse durante un aggiornamento [dall'azione RemoveExistingProducts](removeexistingproducts-action.md). In [questo caso,](upgrade-table.md) la tabella Upgrade [**può anche**](remove.md) impostare la proprietà REMOVE su ALL. Per determinare se un prodotto viene rimosso da un aggiornamento, controllare la [**proprietà UPGRADINGPRODUCTCODE.**](upgradingproductcode.md) Il programma di installazione imposta questa proprietà solo quando RemoveExistingProducts rimuove il prodotto. Il programma di installazione non imposta la proprietà durante una normale disinstallazione, ad esempio la rimozione con Installazione applicazioni.

 

 



