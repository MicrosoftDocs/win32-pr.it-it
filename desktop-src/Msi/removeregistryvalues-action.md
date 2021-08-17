---
description: L'azione RemoveRegistryValues può rimuovere solo i valori dal Registro di sistema creati nella tabella Registro di sistema o nella tabella RemoveRegistry.
ms.assetid: aa05eb75-15f2-4e2a-a8e2-a770ad078b41
title: Azione RemoveRegistryValues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5fe284043f76cbffe3fe6a6887f46d6ab16ba65e9103efce6e4e62baac31d31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119339661"
---
# <a name="removeregistryvalues-action"></a>Azione RemoveRegistryValues

L'azione RemoveRegistryValues può rimuovere solo i valori dal Registro di sistema creati nella tabella [Del](registry-table.md) Registro di sistema o [nella tabella RemoveRegistry](removeregistry-table.md). Questa azione rimuove un valore del Registro di sistema creato nella tabella Del Registro di sistema se il componente associato è stato installato localmente o come eseguito dall'origine ed è ora impostato per la disinstallazione. Questa azione rimuove un valore del Registro di sistema creato nella tabella RemoveRegistry se il componente associato è impostato per l'installazione locale o l'esecuzione dall'origine.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare RemoveRegistryValues. Se viene [usata un'azione WriteRegistryValues,](writeregistryvalues-action.md) deve essere dopo RemoveRegistryValues. RemoveRegistryValues deve essere prima [di UnregisterMIMEInfo](unregistermimeinfo-action.md) [o UnregisterProgIDInfo](unregisterprogidinfo-action.md).

È possibile usare un'azione personalizzata per aggiungere righe alla tabella [Del](registry-table.md) Registro di sistema durante una transazione di installazione, disinstallazione o ripristino. Queste righe non vengono mantenute nella tabella Registro di sistema e le informazioni sono disponibili solo durante la transazione corrente. L'azione personalizzata deve quindi essere eseguita in ogni transazione di installazione, disinstallazione o ripristino che richiede le informazioni in queste righe aggiuntive. L'azione personalizzata deve essere eseguita prima delle azioni RemoveRegistryValues e [WriteRegistryValues](writeregistryvalues-action.md) nella sequenza di azioni.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                          |
|-------|-----------------------------------------------------|
| \[1\] | Percorso del Registro di sistema alla chiave del valore del Registro di sistema rimosso.     |
| \[2\] | Stringa formattata del nome del valore del Registro di sistema rimosso. |



 

## <a name="remarks"></a>Commenti

Per rimuovere un valore del Registro di sistema, registrare il valore nella colonna Valore della tabella Registro di sistema. Se l'azione WriteRegistryValues ha collegato stringhe REG MULTI SZ al valore nella tabella Registro di sistema , l'azione \_ \_ RemoveRegistryValues [](registry-table.md)rimuove solo tali stringhe dal valore del Registro di sistema.

 

 



