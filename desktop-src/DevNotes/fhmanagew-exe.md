---
description: Il programma FhManagew.exe Elimina le versioni dei file che superano la validità specificata dal dispositivo di destinazione della cronologia file attualmente assegnato.
ms.assetid: 31A6E1AC-492A-4080-9095-3180FD60A575
title: FhManagew.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f7c7cdaa5ddba46dc2ead3e4e9a462416758e1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483244"
---
# <a name="fhmanagewexe"></a>FhManagew.exe

Il programma FhManagew.exe Elimina le versioni dei file che superano la validità specificata dal dispositivo di destinazione della cronologia file attualmente assegnato.

Questo programma è disponibile in Windows 8 e Windows Server 2012 e versioni successive.

Per eseguire questo programma, andare al menu **Start** , fare clic su **Esegui** e digitare il comando seguente.

*Tempo* **di puliziaFhManagew.exe**



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parametro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="age"></span><span id="AGE"></span><em>età</em><br/></td>
<td>Questo parametro specifica la durata minima, in giorni, delle versioni dei file che possono essere eliminate. Una versione del file viene eliminata se si verificano entrambe le condizioni seguenti:<br/>
<ul>
<li>La versione del file è precedente alla data di validità specificata.</li>
<li>Il file non è più incluso nell'ambito di protezione oppure è presente una versione più recente dello stesso file nel dispositivo di destinazione.</li>
</ul>
Se il parametro <em>Age</em> è impostato su zero, tutte le versioni dei file vengono eliminate, ad eccezione della versione più recente di ogni file attualmente presente nell'ambito di protezione.<br/></td>
</tr>
</tbody>
</table>



 

Per disattivare tutti gli output di questo programma, usare l'opzione della riga di comando **-quiet** come indicato di seguito.

**FhManagew.exe-pulizia** *età* **-non interattiva**

## <a name="examples"></a>Esempi



| Esempio                                                                                                                                                                                                      | Descrizione                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="FhManagew.exe_-cleanup_30"></span><span id="fhmanagew.exe_-cleanup_30"></span><span id="FHMANAGEW.EXE_-CLEANUP_30"></span>**PuliziaFhManagew.exe 30**<br/>                                 | Elimina tutte le versioni di file che hanno più di un mese.<br/>                        |
| <span id="FhManagew.exe_-cleanup_365_-quiet"></span><span id="fhmanagew.exe_-cleanup_365_-quiet"></span><span id="FHMANAGEW.EXE_-CLEANUP_365_-QUIET"></span>**FhManagew.exe-Cleanup 365-quiet**<br/> | Eliminare tutte le versioni dei file precedenti a un anno ed eliminare tutti gli output.<br/> |



 

 

 




