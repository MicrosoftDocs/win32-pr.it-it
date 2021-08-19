---
description: L'azione SelfRegModules elabora tutti i moduli elencati nella tabella SelfReg e registra tutti i moduli installati nel sistema. Il programma di installazione non registra automaticamente i file EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Azione SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf137dc63baa72a3d5b93370e40911af93691eaa911c4081990656c84091870
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119630041"
---
# <a name="selfregmodules-action"></a>Azione SelfRegModules

L'azione SelfRegModules elabora tutti i moduli elencati nella [tabella SelfReg](selfreg-table.md) e registra tutti i moduli installati nel sistema. Il programma di installazione non registra automaticamente i file EXE.

## <a name="sequence-restrictions"></a>Restrizioni di sequenza

[L'azione InstallValidate](installvalidate-action.md) deve essere chiamata prima di chiamare l'azione SelfRegModules. Se si [usa un'azione InstallFiles,](installfiles-action.md) deve essere visualizzata prima dell'azione SelfRegModules nella sequenza. Poiché l'azione SelfRegModules modifica il sistema, SelfRegModules dovrebbe venire dopo [l'azione InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                           |
|-------|------------------------------------------------------|
| \[1\] | Identificatore del file di modulo registrato.                |
| \[2\] | Identificatore della cartella che contiene il file di modulo registrato. |



 

## <a name="remarks"></a>Commenti

L'azione SelfRegModules tenta di chiamare la [funzione DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) del modulo pianificato per la registrazione. Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer. Durante un'installazione per utente, il programma di installazione esegue questa azione con privilegi utente.

Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra le DLL autoregistrate usando [l'azione SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
