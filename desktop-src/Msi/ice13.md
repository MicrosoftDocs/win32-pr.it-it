---
description: ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle AdminUISequence o InstallUISequence. Le finestre di dialogo non devono essere elencate nelle tabelle InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fff440217ccffe41d5e4036f4ea0d03d1eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967792"
---
# <a name="ice13"></a>ICE13

ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle [AdminUISequence](adminuisequence-table.md)o [InstallUISequence](installuisequence-table.md) . Le finestre di dialogo non devono essere elencate nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence](advtexecutesequence-table.md) .

## <a name="result"></a>Risultato

ICE13 Invia un messaggio di errore se viene visualizzata una finestra di dialogo in una tabella di sequenza di esecuzione.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE13 Invia un messaggio di errore che informa che non è possibile elencare ' WelcomeDialog ' nella tabella ' InstallExecuteSequence '.

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione          |
|-----------------|
| InstallFinalize |
| CostFinalize secondo    |
| WelcomeDialog   |



 

[Tabella InstallUISequence](installuisequence-table.md) (parziale)



| Azione         |
|----------------|
| CostFinalize secondo   |
| CostInitialize |
| BrowseDialog   |



 

[Tabella finestra di dialogo](dialog-table.md) (parziale)



| Finestra di dialogo        |
|---------------|
| BrowseDialog  |
| WelcomeDialog |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



