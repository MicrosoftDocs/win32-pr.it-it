---
description: Esistono due modi per creare il database di installazione di Windows Installer in modo che un'azione venga chiamata solo quando il pacchetto viene disinstallato.
ms.assetid: 67b205bb-11d8-454f-b5d5-93330219f6cc
title: Esecuzione delle azioni di condizionamento durante la rimozione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad0e84f21b42f569744af9b8a7a46bb1e3df7a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528645"
---
# <a name="conditioning-actions-to-run-during-removal"></a>Esecuzione delle azioni di condizionamento durante la rimozione

Esistono due modi per creare il database di installazione in modo che un'azione venga chiamata solo quando il pacchetto viene disinstallato:

-   Se l'azione viene sequenziata dopo l' [azione InstallValidate](installvalidate-action.md) nella [tabella InstallExecuteSequence](installexecutesequence-table.md), l'autore del pacchetto può specificare una condizione di Remove = "All" per l'azione nella colonna condizione. Si noti che non è garantita l'impostazione della proprietà [**Remove**](remove.md) su All durante una disinstallazione prima che il programma di installazione esegua l'azione InstallValidate. Si noti che in questo caso sono necessarie le virgolette per tutto il valore.
-   Se l'azione viene sequenziata dopo l' [azione CostFinalize secondo](costfinalize-action.md) e tutte le azioni che potrebbero modificare lo stato della funzionalità, ad esempio l'azione [MigrateFeatureStates](migratefeaturestates-action.md), l'azione può essere condizionata sullo stato di una particolare funzionalità o componente. Vedere [sintassi dell'istruzione condizionale](conditional-statement-syntax.md). Usare questa opzione per chiamare un'azione durante la rimozione di una funzionalità o di un componente specifico, che può verificarsi al di fuori della rimozione completa dell'applicazione.

Si noti che la proprietà [**installata**](installed.md) può essere utilizzata nelle espressioni condizionali per determinare se un prodotto è installato per computer o per l'utente corrente. Per determinare se il prodotto è installato per un utente diverso, controllare la proprietà [**ProductState**](productstate.md) .

Si noti che le versioni precedenti di un prodotto possono essere rimosse durante un aggiornamento mediante l' [azione RemoveExistingProducts](removeexistingproducts-action.md). La [tabella di aggiornamento](upgrade-table.md) può inoltre impostare la proprietà [**Remove**](remove.md) su All in questo caso. Per determinare se un prodotto è stato rimosso da un aggiornamento, controllare la proprietà [**UPGRADINGPRODUCTCODE**](upgradingproductcode.md) . Il programma di installazione imposta questa proprietà solo quando RemoveExistingProducts rimuove il prodotto. Il programma di installazione non imposta la proprietà durante una normale disinstallazione, ad esempio la rimozione con installazione applicazioni.

 

 



