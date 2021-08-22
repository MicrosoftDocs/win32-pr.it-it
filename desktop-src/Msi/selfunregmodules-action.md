---
description: L'azione SelfUnregModules annulla la registrazione di tutti i moduli elencati nella tabella SelfReg pianificati per la disinstallazione. Il programma di installazione non esegue la registrazione .EXE file.
ms.assetid: fa5a5abb-ecd4-434c-b176-83cdca280a13
title: Azione SelfUnregModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ba95a745716d512a72e9541064f56bdc663e2e6c9658a9c35744449217952f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040331"
---
# <a name="selfunregmodules-action"></a>Azione SelfUnregModules

L'azione SelfUnregModules annulla la registrazione di tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md) pianificati per la disinstallazione. Il programma di installazione non esegue la registrazione .EXE file.

## <a name="sequence-restrictions"></a>Restrizioni relative alle sequenze

[L'azione InstallValidate](installvalidate-action.md) deve essere visualizzata prima dell'azione SelfUnregModules nella sequenza. Se viene [usata un'azione SelfRegModules,](selfregmodules-action.md) deve essere visualizzata dopo l'azione SelfUnregModules nella sequenza. Se viene [usata un'azione RemoveFiles,](removefiles-action.md) deve essere visualizzata dopo l'azione SelfUnregModules nella sequenza.

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                             |
|-------|--------------------------------------------------------|
| \[1\] | Identificatore del file di modulo non registrato.                |
| \[2\] | Identificatore della cartella contenente il file di modulo non registrato. |



 

## <a name="remarks"></a>Commenti

L'azione SelfUnregModules tenta di chiamare la funzione [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver) del modulo di cui annullare la registrazione. Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer. Durante un'installazione per utente, il programma di installazione esegue questa azione con privilegi utente.

Si noti che non è possibile specificare l'ordine in cui il programma di installazione annulla la registrazione delle DLL con registrazione automatica usando l'azione SelfUnRegModules.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
