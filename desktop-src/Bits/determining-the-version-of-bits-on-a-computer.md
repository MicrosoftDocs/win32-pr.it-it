---
title: Determinazione della versione di BITS in un computer
description: Per determinare la versione di BITS nel computer client, controllare la versione di QMgr.dll.
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caa2c501fd5f37d44becf11679debb1390aeeb9ee47bee02b43a97788493cd7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120005311"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>Determinazione della versione di BITS in un computer

Per determinare la versione di BITS nel computer client, controllare la versione di QMgr.dll. Per trovare il numero di versione della DLL:

-   Individuare QMgr.dll in %windir% \\ System32.
-   Fare clic con il pulsante destro QMgr.dll e scegliere **Proprietà**.
-   Fare clic **sulla scheda** Versione.
-   Annotare il numero di versione.

È anche possibile usare il codice di PowerShell seguente per determinare la versione del .dll nel sistema:

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

Se la DLL esiste anche in %windir% \\ System32 \\ Bits, ripetere i passaggi precedenti. BITS usa la DLL con il numero di versione più alto.

Nella tabella seguente sono elencate le versioni di BITS e i corrispondenti QMgr.dll di versione del file.



| Versione bits | QMgr.dll versione del file |
|--------------|------------------------------|
| BITS 10.1    | 7.8.xxxx.xxxx                |
| BITS 5.0     | 7.7.xxxx.xxxx                |
| BITS 4.0     | 7.5.xxxx.xxxx                |
| BITS 3.0     | 7.0.xxxx.xxxx                |
| BITS 2.5     | 6.7.xxxx.xxxx                |
| BITS 2.0     | 6.6.xxxx.xxxx                |
| BITS 1.5     | 6.5.xxxx.xxxx                |
| BITS 1.2     | 6.2.xxxx.xxxx                |
| BITS 1.0     | 6.0.xxxx.xxxx                |



 

È anche possibile usare gli identificatori di classe simbolici per determinare la versione di BITS registrata nel computer. Nella tabella seguente sono elencate le versioni di BITS e gli identificatori di classe simbolici corrispondenti. La **funzione CoCreateInstance** restituisce **REGDB E \_ \_ CLASSNOTREG** se la classe non è registrata.



| Versione bits  | Identificatore di classe simbolico         |
|---------------|-----------------------------------|
| BITS 10.1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5.0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4.0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3.0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | ClSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2.0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1.5      | ClSID \_ BackgroundCopyManager1 \_ 5  |
| BITS 1.2, 1.0 | CLSID \_ BackgroundCopyManager      |



 

 

 




