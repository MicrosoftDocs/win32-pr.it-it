---
description: Descrive i formati di ora supportati per l'utilizzo nella clausola WHERE di WQL.
ms.assetid: d86bd2e3-f5cb-488f-9cd6-5105d82a1842
ms.tgt_platform: multiple
title: Formati di WQL-Supported ora
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b84d9e37de3529060dc3da6277b2cfb40f7cc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310318"
---
# <a name="wql-supported-time-formats"></a>Formati di WQL-Supported ora

Oltre al formato DATETIME WMI, i formati di data seguenti sono supportati per l'utilizzo nella clausola WHERE di WQL.



| Formato                                    | Descrizione                                                                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HH \[ \] {AP} M<br/>                   | Ora, come illustrato in un orario a dodici ore e designazione AM o PM.<br/> 4 PM<br/>                                                                                                             |
| hh:mm<br/>                          | Ora e minuti delimitati da due punti. Nessuna designazione AM o PM.<br/> 3:23<br/>                                                                                                                  |
| HH: mm \[ \] {AP} M<br/>                | Ora e minuti delimitati da due punti, spazio facoltativo e designazione AM o PM.<br/> 3:23 AM<br/>                                                                                              |
| hh:mm:ss<br/>                       | Due punti: ora, minuti e secondi delimitati. Nessuna indicazione AM/PM.<br/> 3:23:00<br/>                                                                                                         |
| HH: mm: SS \[ \] {AP} M<br/>             | Ora, minuti e secondi delimitati da due punti, spazio facoltativo e designazione AM/PM.<br/> 3:23: PM<br/>                                                                                      |
| HH: mm: SS: UUU<br/>                   | Ora, minuti e secondi delimitati da due punti e offset di tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC.<br/>                                    |
| HH: mm: SS: \[ \[ u \] u \] u<br/>           | Due punti: ora, minuti e secondi delimitati; un offset di uno, due o tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC.<br/>                       |
| HH: mm: SS: UUU \[ \] {AP} M<br/>         | Ora, minuti e secondi delimitati da due punti, offset di tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC e la designazione AM o PM.<br/>              |
| HH: mm: SS: \[ \[ u \] u \] u \[ \] {AP} M<br/> | Due punti: ora, minuti e secondi delimitati; offset uno, due o tre cifre che indica il numero di minuti che il fuso orario di origine devia dall'ora UTC; e la designazione AM o PM.<br/> |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Clausola WHERE](where-clause.md)
</dt> </dl>

 

 




