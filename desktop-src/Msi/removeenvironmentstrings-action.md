---
description: L'azione RemoveEnvironmentStrings modifica i valori delle variabili di ambiente.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Azione RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319963"
---
# <a name="removeenvironmentstrings-action"></a>Azione RemoveEnvironmentStrings

L'azione RemoveEnvironmentStrings modifica i valori delle variabili di ambiente.

Si noti che le variabili di ambiente non cambiano per l'installazione in corso quando viene eseguita l'azione [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o RemoveEnvironmentStrings. In Windows 2000 queste informazioni vengono archiviate nel registro di sistema e viene inviato un messaggio per notificare al sistema le modifiche apportate al completamento dell'installazione. Un nuovo processo o un altro processo che verifica la presenza di questi messaggi utilizzerà le nuove variabili di ambiente.

Il programma di installazione esegue l' [azione WriteEnvironmentStrings](writeenvironmentstrings-action.md) solo durante l'installazione o la reinstallazione di un componente ed esegue l'azione RemoveEnvironmentStrings solo durante la rimozione di un componente.

I valori vengono scritti o rimossi in base alla selezione di azioni e modificatori primari. Questi elementi sono descritti nella sezione messaggi ActionData seguenti. Si noti che, a seconda dell'azione specificata, WriteEnvironmentStrings può rimuovere le variabili e RemoveEnvironmentStrings può aggiungerle in base alla creazione della [tabella dell'ambiente](environment-table.md).

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L' [azione InstallValidate](installvalidate-action.md) deve essere eseguita prima dell'azione RemoveEnvironmentStrings. Poiché l'azione WriteEnvironmentStrings e l'azione RemoveEnvironmentStrings non vengono mai applicate durante l'installazione o la rimozione di un componente, la relativa sequenza relativa non è limitata.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Nome della variabile di ambiente da modificare.                                                                                                                                                                               |
| \[2\] | Valore della variabile di ambiente.                                                                                                                                                                                           |
| \[3\] | Si tratta di un campo di flag di bit che specificano l'azione da eseguire. Includere solo un bit per un'azione primaria. In questo campo può essere incluso più di un bit del modificatore. Vedere le seguenti descrizioni dei flag di bit. |



 



| Valore bit | Descrizione delle azioni primarie                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Ai posti. Imposta il valore della variabile di ambiente in tutti i casi.<br/> Se questo bit è combinato con un bit di modificatore Append o prefix, l'azione aggiunge il valore a qualsiasi valore esistente nella variabile.<br/> |
| 0x2       | Ai posti. Imposta il valore se la variabile è assente.<br/> Se questo bit è combinato con un bit di modificatore Append o prefix, l'azione aggiunge il valore a qualsiasi valore esistente nella variabile.<br/>                |
| 0x4       | Rimuovi. Rimuove il valore dalla variabile.<br/> Se questo bit è combinato con un bit di modificatore Append o prefix, il valore viene rimosso dalla stringa esistente, se il valore esiste.<br/>               |



 



| Valore bit  | Descrizione del modificatore                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Se questo bit è impostato, le azioni vengono applicate alle variabili di ambiente del computer.<br/> Se questo bit non è impostato, le azioni vengono applicate alle variabili di ambiente dell'utente.<br/> |
| 0x40000000 | Append. Questo bit è facoltativo. Non impostare i modificatori Append e prefix.<br/>                                                                                            |
| 0x80000000 | Prefisso. Questo bit è facoltativo. Non impostare i modificatori Append e prefix.<br/>                                                                                            |



 

 

 




