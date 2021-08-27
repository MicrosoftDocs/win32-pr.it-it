---
description: Descrive i formati di ora supportati per l'uso nella clausola WHERE WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: WQL-Supported formati di ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 627b46ef7d01a2eb3e8e40484b37822c9ebca55a9487b1ffb0e1a138ab7378d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049739"
---
# <a name="wql-supported-time-formats"></a>WQL-Supported formati di ora

Oltre al formato WMI DATETIME, nella clausola WHERE WQL sono supportati i formati di data seguenti.



| Formato                                    | Descrizione                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| hh \[ \] {AP}M<br/>                   | Ora come illustrato in un orologio di dodici ore e designazione AM o PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Ora e minuti delimitati da due punti. Nessuna designazione AM o PM.<br/> 3:23<br/>                                                                                                                  |
| hh:mm \[ \] {AP}M<br/>                | Ora e minuti delimitati da due punti, spazio facoltativo e designazione AM o PM.<br/> 03:23<br/>                                                                                              |
| hh:mm:ss<br/>                       | Ora, minuti e secondi delimitati da due punti. Nessuna designazione AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| hh:mm:ss \[ \] {AP}M<br/>             | Ora, minuti e secondi delimitati da due punti, spazio facoltativo e designazione AM/PM.<br/> 15:23:00<br/>                                                                                      |
| hh:mm:ss:uuu<br/>                   | Ora, minuti e secondi delimitati da due punti e offset a tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC.<br/>                                    |
| hh:mm:ss: \[ \[ u u \] \] u<br/>           | Ora, minuti e secondi delimitati da due punti; e offset di una, due o tre cifre che indica il numero di minuti in cui il fuso orario di origine devia dall'ora UTC.<br/>                       |
| hh:mm:ss:uuu \[ \] {AP}M<br/>         | Ora, minuti e secondi delimitati da due punti, offset a tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC e dalla designazione AM o PM.<br/>              |
| hh:mm:ss: \[ \[ u u \] \] \[ \] {AP}M<br/> | Ora, minuti e secondi delimitati da due punti; offset di una, due o tre cifre che indica il numero di minuti in cui il fuso orario di origine devia dall'ora UTC; e la designazione AM o PM.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Clausola WHERE](where-clause.md)
</dt> </dl>

 

 




