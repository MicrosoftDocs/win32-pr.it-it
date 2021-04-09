---
description: ICE77 verifica che le azioni personalizzate con il set di bit msidbCustomActionTypeInScript vengano sequenziate dopo l'azione InstallInitialize e prima dell'azione InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129971"
---
# <a name="ice77"></a>ICE77

ICE77 verifica che le azioni personalizzate con il set di bit **msidbCustomActionTypeInScript** vengano sequenziate dopo l' [azione InstallInitialize](installinitialize-action.md) e prima dell' [azione InstallFinalize](installfinalize-action.md). ICE77 verifica la sequenza nella tabella [InstallExecuteSequence](installexecutesequence-table.md) e nella [tabella AdminExecuteSequence](adminexecutesequence-table.md).

## <a name="result"></a>Risultato

ICE77 Invia un errore se un'azione personalizzata nello script viene sequenziata prima dell'azione InstallInitialize o dopo l'azione InstallFinalize.

ICE77 Invia un errore se l'azione InstallInitialize o InstallFinalize è mancante.

## <a name="example"></a>Esempio

ICE77 segnala gli errori seguenti per l'esempio:

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione              | Tipo |
|---------------------|------|
| \_INSCRIPTINSTALL CA | 1025 |
| \_INSCRIPTADMIN CA   | 1026 |



 

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione              | Sequenza |
|---------------------|----------|
| \_INSCRIPTINSTALL CA | 2000     |
| InstallInitialize   | 1500     |



 

[Tabella AdminExecuteSequence](adminexecutesequence-table.md) (parziale)



| Azione            | Sequenza |
|-------------------|----------|
| \_INSCRIPTADMIN CA | 1400     |
| InstallInitialize | 1500     |
| InstallFinalize   | 6600     |



 

Per correggere gli errori, sequenziare le azioni personalizzate nello script dopo l'azione InstallInitialize e prima dell'azione InstallFinalize. Le azioni InstallInitialize e InstallFinalize devono essere presenti nella tabella InstallExecuteSequence e nella tabella AdminExecuteSequence.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



