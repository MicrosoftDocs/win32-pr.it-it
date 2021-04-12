---
description: ICE75 verifica che tutte le azioni personalizzate 17 (DLL), tipo di azione personalizzata 18 (EXE), tipo di azione personalizzata 21 (JScript) e tipo di azione personalizzata 22 (VBScript) vengano sequenziate dopo l'azione CostFinalize secondo.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347356"
---
# <a name="ice75"></a>ICE75

ICE75 verifica che tutte le azioni personalizzate [17](custom-action-type-17.md) (dll), tipo [di azione personalizzata 18](custom-action-type-18.md) (exe), [tipo](custom-action-type-21.md) di azione personalizzata 21 (JScript) e [tipo di azione personalizzata 22](custom-action-type-22.md) (VBScript) vengano sequenziate dopo l' [azione CostFinalize secondo](costfinalize-action.md). Questi tipi di azione personalizzata utilizzano un file installato come origine. ICE75 controlla la tabella [InstallUISequence](installuisequence-table.md), la tabella [InstallExecuteSequence](installexecutesequence-table.md), la tabella [AdminUISequence](adminuisequence-table.md)e la [tabella AdminExecuteSequence](adminexecutesequence-table.md). Si noti che l'azione CostFinalize secondo è obbligatoria in queste tabelle di sequenza.

## <a name="result"></a>Risultato

ICE75 Invia un errore se trova un'azione personalizzata usando un file installato come file di origine che non è sequenziato dopo l'azione CostFinalize secondo.

## <a name="example"></a>Esempio

ICE75 segnala gli errori seguenti per l'esempio illustrato:

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

[Tabella CustomAction](customaction-table.md) (parziale)



| Azione      | Tipo | Source (Sorgente)  |
|-------------|------|---------|
| \_FILEEXE CA | 18   | FileExe |
| \_FILEDLL CA | 17   | FileDLL |



 

[Tabella AdminUISequence](adminuisequence-table.md) (parziale)



| Azione      | Sequenza |
|-------------|----------|
| \_FILEEXE CA | 1100     |



 

[Tabella AdminExecuteSequence](adminexecutesequence-table.md) (parziale)



| Azione       | Sequenza |
|--------------|----------|
| \_FILEDLL CA  | 800      |
| CostFinalize secondo | 1000     |



 

Per correggere gli errori, sequenziare le azioni personalizzate dopo l'azione CostFinalize secondo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



