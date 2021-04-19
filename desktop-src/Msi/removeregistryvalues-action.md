---
description: L'azione RemoveRegistryValues può rimuovere solo i valori dal registro di sistema che sono stati creati nella tabella del registro di sistema o nella tabella RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Azione RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e6e7473be344faa08ed456e72e3b9c80c4aa8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313803"
---
# <a name="removeregistryvalues-action"></a>Azione RemoveRegistryValues

L'azione RemoveRegistryValues può rimuovere solo i valori dal registro di sistema che sono stati creati nella [tabella del registro](registry-table.md) di sistema o nella [tabella RemoveRegistry](removeregistry-table.md). Questa azione rimuove un valore del registro di sistema che è stato creato nella tabella del registro di sistema se il componente associato è stato installato localmente o come eseguito dall'origine ed è ora impostato per la disinstallazione. Questa azione rimuove un valore del registro di sistema che è stato creato nella tabella RemoveRegistry se il componente associato è impostato per essere installato localmente o come eseguito dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveRegistryValues. Se viene usata un'azione [WriteRegistryValori consente](writeregistryvalues-action.md) , deve provenire dopo RemoveRegistryValues. RemoveRegistryValues deve essere precedente a [UnregisterMIMEInfo](unregistermimeinfo-action.md) o [UnregisterProgIDInfo](unregisterprogidinfo-action.md).

È possibile utilizzare un'azione personalizzata per aggiungere righe alla [tabella del registro di sistema](registry-table.md) durante un'installazione, una disinstallazione o una transazione di ripristino. Queste righe non vengono mantenute nella tabella del registro di sistema e le informazioni sono disponibili solo durante la transazione corrente. L'azione personalizzata deve pertanto essere eseguita in ogni installazione, disinstallazione o ripristino della transazione che richiede le informazioni contenute in queste righe aggiuntive. L'azione personalizzata deve precedere le azioni RemoveRegistryValues e [WriteRegistryValori consente](writeregistryvalues-action.md) nella sequenza di azione.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                          |
|-------|-----------------------------------------------------|
| \[1\] | Percorso del registro di sistema della chiave del valore del registro di sistema rimosso.     |
| \[2\] | Stringa formattata di nome del valore del registro di sistema rimosso. |



 

## <a name="remarks"></a>Commenti

Per rimuovere un valore del registro di sistema, registrare il valore nella colonna valore della tabella del registro di sistema. Se l'azione WriteRegistryValori consente ha collegato le \_ \_ stringhe reg multisz al valore nella [tabella del registro di sistema](registry-table.md), l'azione RemoveRegistryValues rimuove solo le stringhe dal valore del registro di sistema.

 

 



