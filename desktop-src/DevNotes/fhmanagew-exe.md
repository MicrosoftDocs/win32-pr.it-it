---
description: Il FhManagew.exe elimina le versioni dei file che superano una data di validità specificata dal dispositivo di destinazione Cronologia file attualmente assegnato.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2570da9b2b874b723b28917028fab3c58ecdf772
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481517"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

Il FhManagew.exe elimina le versioni dei file che superano una data di validità specificata dal dispositivo di destinazione Cronologia file attualmente assegnato.

Questo programma è disponibile in Windows 8 e Windows Server 2012 e versioni successive.

Per eseguire questo programma, passare al menu **Start,** fare clic **su Esegui** e digitare il comando seguente.

**FhManagew.exe -cleanup** *age*




| Parametro | Descrizione | 
|-----------|-------------|
| <span id="age"></span><span id="AGE"></span><em>Età</em><br /> | Questo parametro specifica la durata minima, in giorni, delle versioni dei file che possono essere eliminate. Una versione del file viene eliminata se si verificano entrambe le condizioni seguenti:<br /><ul><li>La versione del file è precedente alla data di validità specificata.</li><li>Il file non è più incluso nell'ambito di protezione o nel dispositivo di destinazione è disponibile una versione più recente dello stesso file.</li></ul>Se il <em>parametro age</em> è impostato su zero, vengono eliminate tutte le versioni dei file, ad eccezione della versione più recente di ogni file attualmente presente nell'ambito di protezione.<br /> | 




 

Per eliminare tutto l'output di questo programma, usare l'opzione della riga di comando **-quiet** come indicato di seguito.

**FhManagew.exe -cleanup** *age* **-quiet**

## <a name="examples"></a>Esempi



| Esempio                                                                                                                                                                                                      | Descrizione                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**FhManagew.exe -cleanup 30**<br/>                                 | Eliminare tutte le versioni di file precedenti a un mese.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe -cleanup 365 -quiet**<br/> | Eliminare tutte le versioni dei file precedenti a un anno ed eliminare tutto l'output.<br/> |



 

 

 




