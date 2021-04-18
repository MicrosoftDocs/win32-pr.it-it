---
description: L'azione SelfRegModules elabora tutti i moduli elencati nella tabella SelfReg e registra tutti i moduli installati con il sistema. Il programma di installazione non registra autonomamente i file EXE.
ms.assetid: b139ae28-e479-4915-909d-2449244e9fd6
title: Azione SelfRegModules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75895b1886fad51f36113ce6e677ba6a534ab0cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318986"
---
# <a name="selfregmodules-action"></a>Azione SelfRegModules

L'azione SelfRegModules elabora tutti i moduli elencati nella tabella [selfreg](selfreg-table.md) e registra tutti i moduli installati con il sistema. Il programma di installazione non registra autonomamente i file EXE.

## <a name="sequence-restrictions"></a>Restrizioni sequenza

Prima di chiamare l'azione SelfRegModules, è necessario chiamare l'azione [InstallValidate](installvalidate-action.md) . Se viene usata un'azione [InstallFiles](installfiles-action.md) , deve essere presente prima dell'azione SelfRegModules nella sequenza. Poiché l'azione SelfRegModules modifica il sistema, SelfRegModules deve essere seguito dall' [azione InstallInitialize](installinitialize-action.md).

## <a name="actiondata-messages"></a>Messaggi ActionData



| Campo | Descrizione dei dati dell'azione                           |
|-------|------------------------------------------------------|
| \[1\] | Identificatore del file di modulo registrato.                |
| \[2\] | Identificatore della cartella che contiene il file del modulo registrato. |



 

## <a name="remarks"></a>Commenti

L'azione SelfRegModules tenta di chiamare la funzione [DllRegisterServer](/windows/win32/api/olectl/nf-olectl-dllregisterserver) del modulo pianificato per la registrazione. Questa azione viene eseguita con privilegi elevati quando l'installazione viene eseguita con privilegi elevati, ad esempio durante un'installazione per computer. Durante un'installazione per utente, il programma di installazione esegue questa azione con i privilegi utente.

Si noti che non è possibile specificare l'ordine in cui il programma di installazione registra la registrazione automatica delle dll usando l' [azione SelfUnRegModules](selfunregmodules-action.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Specifica dell'ordine di registrazione automatica](specifying-the-order-of-self-registration.md)
</dt> </dl>

 

 
