---
description: L'azione SelfUnregModules Annulla la registrazione di tutti i moduli elencati nella tabella SelfReg che sono pianificati per la disinstallazione. Il programma di installazione non esegue la registrazione automatica. File EXE.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Azione SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3a0d98d8a8afe45b9b78f5c8af8ca2f84b2244
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318987"
---
# <a name="selfunregmodules-action"></a>Azione SelfUnregModules

L'azione SelfUnregModules Annulla la registrazione di tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md) che sono pianificati per la disinstallazione. Il programma di installazione non esegue la registrazione automatica. File EXE.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

L'azione [InstallValidate](installvalidate-action.md) deve essere presente prima dell'azione SelfUnregModules nella sequenza. Se viene utilizzata un'azione [SelfRegModules](selfregmodules-action.md) , deve comparire dopo l'azione SelfUnregModules nella sequenza. Se viene utilizzata un' [azione RemoveFiles](removefiles-action.md) , deve comparire dopo l'azione SelfUnregModules nella sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                             |
|-------|--------------------------------------------------------|
| \[1\] | Identificatore del file di modulo non registrato.                |
| \[2\] | Identificatore della cartella che contiene il file del modulo non registrato. |



 

## <a name="remarks"></a>Commenti

L'azione SelfUnregModules tenta di chiamare la funzione [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) del modulo di cui deve essere annullata la registrazione. Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer. Durante un'installazione per utente, il programma di installazione esegue questa azione con i privilegi utente.

Si noti che non è possibile specificare l'ordine in cui il programma di installazione Annulla la registrazione automatica delle dll usando l'azione SelfUnRegModules.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
