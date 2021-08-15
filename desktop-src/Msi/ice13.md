---
description: ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle AdminUISequence o InstallUISequence. Le finestre di dialogo non devono essere elencate nelle tabelle InstallExecuteSequence, AdminExecuteSequence o AdvtExecuteSequence.
ms.assetid: 51542a8f-2fb6-4021-b52d-6f7a2b0294d6
title: ICE13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fdc11f8254c721d404a65e63fc897aa6e55bc61364c768b48f2d5aded4348d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118946635"
---
# <a name="ice13"></a>ICE13

ICE13 verifica che le finestre di dialogo nelle tabelle di sequenza vengano visualizzate nelle tabelle [AdminUISequence](adminuisequence-table.md)o [InstallUISequence.](installuisequence-table.md) Le finestre di dialogo non devono essere elencate nelle tabelle [InstallExecuteSequence](installexecutesequence-table.md), [AdminExecuteSequence](adminexecutesequence-table.md)o [AdvtExecuteSequence.](advtexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE13 pubblica un messaggio di errore se viene visualizzata una finestra di dialogo in una tabella di sequenza di esecuzione.

## <a name="example"></a>Esempio

Per l'esempio seguente, ICE13 pubblica un messaggio di errore che informa che 'WelcomeDialog' non può essere elencato nella tabella 'InstallExecuteSequence'.

[Tabella InstallExecuteSequence](installexecutesequence-table.md) (parziale)



| Azione          |
|-----------------|
| InstallFinalize |
| CostFinalize    |
| Finestra di dialogo di benvenuto   |



 

[Tabella InstallUISequence](installuisequence-table.md) (parziale)



| Azione         |
|----------------|
| CostFinalize   |
| CostInitialize |
| Finestra di dialogo Sfoglia   |



 

[Tabella delle finestre di](dialog-table.md) dialogo (parziale)



| Finestra di dialogo        |
|---------------|
| Finestra di dialogo Sfoglia  |
| Finestra di dialogo di benvenuto |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



