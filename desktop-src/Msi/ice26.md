---
description: ICE26 convalida le tabelle di sequenza in un database Windows Installer.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882937"
---
# <a name="ice26"></a>ICE26

ICE26 verifica che ognuna delle [*tabelle di sequenza*](s-gly.md) seguenti contenga le azioni necessarie per la tabella e non contenga alcuna azione non consentita nella tabella:

-   [Tabella AdminUISequence](adminuisequence-table.md)
-   [Tabella AdminExecuteSequence](adminexecutesequence-table.md)
-   [Tabella InstallUISequence](installuisequence-table.md)
-   [Tabella InstallExecuteSequence](installexecutesequence-table.md)

## <a name="result"></a>Risultato

ICE26 Invia un messaggio di errore se il pacchetto di installazione dispone di una tabella di sequenza in cui manca un'azione obbligatoria o che contiene un'azione non consentita per la tabella.

## <a name="example"></a>Esempio



| Errore ICE26                                                                   | Descrizione                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Azione:' action1' è obbligatorio nella tabella di sequenza InstallExecuteSequence.   | Manca un'azione obbligatoria nella tabella di sequenza indicata. Vedere l'template.msi o le tabelle di sequenza suggerite in [uso di una tabella di sequenza](using-a-sequence-table.md). |
| Azione:' Action2' non è consentito nella tabella di sequenza InstallExecuteSequence. | Questa azione non può essere inclusa nella tabella di sequenza indicata. Rimuovere questa azione dalla tabella di sequenza.                                                                             |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



