---
description: ICE26 convalida le tabelle di sequenza in un database Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bbf63e0efeec79de35122f7a210c32746af9de50f27ac3e47ad1f88984a6ec77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528861"
---
# <a name="ice26"></a>ICE26

ICE26 verifica che ognuna [](s-gly.md) delle tabelle di sequenza seguenti contenga le azioni richieste dalla tabella e non contenga azioni non consentite nella tabella:

-   [Tabella AdminUISequence](adminuisequence-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE26 invia un messaggio di errore se il pacchetto di installazione ha una tabella di sequenza che non dispone di un'azione necessaria o che contiene un'azione non consentita per la tabella.

## <a name="example"></a>Esempio



| Errore ICE26                                                                   | Descrizione                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione: 'Action1' è obbligatorio nella tabella InstallExecuteSequence Sequence.   | Un'azione obbligatoria non è presente nella tabella di sequenza indicata. Vedere la template.msi o le tabelle di sequenza suggerite in [Uso di una tabella di sequenza](using-a-sequence-table.md). |
| Azione: 'Action2' non è consentito nella tabella InstallExecuteSequence Sequence. | Questa azione non può essere nella tabella di sequenza indicata. Rimuovere questa azione dalla tabella di sequenza.                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



