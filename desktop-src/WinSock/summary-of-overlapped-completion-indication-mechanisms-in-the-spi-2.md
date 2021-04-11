---
description: Riepilogo dei meccanismi di indicazione di completamento sovrapposti in Windows Sockets (Winsock) SPI.
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Riepilogo dei meccanismi di indicazione di completamento sovrapposti in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20e78f38e35638f29376cb0807d4eedabbe9164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129115"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Riepilogo dei meccanismi di indicazione di completamento sovrapposti in SPI

Nella tabella seguente viene riepilogata la semantica di completamento per un socket sovrapposto, che mostra le varie combinazioni di *lpOverlapped*, **hEvent** e *il lpCompletionRoutine*.



| *lpOverlapped* | **hEvent**     | *Il lpCompletionRoutine* | Indicazione di completamento                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicabile | Ignorato               | L'operazione viene completata in modo sincrono, ovvero si comporta come se fosse un socket non sovrapposto.                                                                                                                                 |
| NOT NULL       | NULL           | NULL                  | L'operazione è stata completata, ma non è disponibile alcun meccanismo di completamento supportato da Windows Sockets 2. Il meccanismo della porta di completamento (se supportato) può essere usato in questo caso, altrimenti non sarà presente alcuna notifica di completamento. |
| NOT NULL       | NOT NULL       | NULL                  | L'operazione è stata completata e viene eseguita la notifica tramite un oggetto evento di segnalazione.                                                                                                                                                      |
| NOT NULL       | Ignorato        | NOT NULL              | Il completamento dell'operazione è sovrapposto, notifica pianificando la routine di completamento.                                                                                                                                               |



 

 

 



