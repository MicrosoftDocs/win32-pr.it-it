---
title: Determinazione della versione dei bit in un computer
description: Per determinare la versione dei bit nel computer client, controllare la versione di QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707861"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Determinazione della versione dei bit in un computer

Per determinare la versione dei bit nel computer client, controllare la versione di QMgr.dll. Per trovare il numero di versione della DLL:

-   Individuare QMgr.dll in% windir% \\ system32.
-   Fare clic con il pulsante destro del mouse su QMgr.dll e scegliere **Proprietà**.
-   Fare clic sulla scheda **Version** .
-   Annotare il numero di versione.

È anche possibile usare il codice PowerShell seguente per determinare la versione del file dll nel sistema:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Se la DLL esiste anche in% windir% \\ system32 \\ bit, ripetere i passaggi precedenti. BITS usa la DLL con il numero di versione superiore.

Nella tabella seguente sono elencate le versioni di BITS e i numeri di versione del file QMgr.dll corrispondenti.



| Versione BITS | Numero di versione del file di QMgr.dll |
|--------------|------------------------------|
| BITS 10,1    | 7.8. xxxx. xxxx                |
| BITS 5,0     | 7.7. xxxx. xxxx                |
| BITS 4,0     | 7.5. xxxx. xxxx                |
| BITS 3,0     | 7.0. xxxx. xxxx                |
| BITS 2.5     | 6.7. xxxx. xxxx                |
| BITS 2,0     | 6.6. xxxx. xxxx                |
| BITS 1,5     | 6.5. xxxx. xxxx                |
| BITS 1,2     | 6.2. xxxx. xxxx                |
| BITS 1,0     | 6.0. xxxx. xxxx                |



 

È inoltre possibile utilizzare gli identificatori di classe simbolici per determinare la versione di bit registrata nel computer. La tabella seguente elenca le versioni di BITS e i corrispondenti identificatori di classe simbolici. La funzione **CoCreateInstance** restituisce **REGDB \_ E \_ CLASSNOTREG** se la classe non è registrata.



| Versione BITS  | Identificatore di classe simbolico         |
|---------------|-----------------------------------|
| BITS 10,1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5,0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4,0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3,0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2,0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1,5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1,2, 1,0 | \_BACKGROUNDCOPYMANAGER CLSID      |



 

 

 




