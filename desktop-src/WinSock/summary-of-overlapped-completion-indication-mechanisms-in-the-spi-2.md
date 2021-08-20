---
description: Riepilogo dei meccanismi di indicazione del completamento sovrapposti Windows Sockets (Winsock) SPI.
ms.assetid: 2306b884-7d3a-4002-928e-54537571e5f8
title: Riepilogo dei meccanismi di indicazione del completamento sovrapposti in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1cb7cc0f354c018ab7a766ea5b71877877fbae6b36cdd86e95f6d1bf9998140
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993251"
---
# <a name="summary-of-overlapped-completion-indication-mechanisms-in-the-spi"></a>Riepilogo dei meccanismi di indicazione del completamento sovrapposti in SPI

La tabella seguente riepiloga la semantica di completamento per un socket sovrapposto, che mostra la combinazione di *lpOverlapped*, **hEvent** e *lpCompletionRoutine*.



| *lpOverlapped* | **hEvent**     | *lpCompletionRoutine* | Indicazione di completamento                                                                                                                                                                                                        |
|----------------|----------------|-----------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| NULL           | Non applicabile | Ignorato               | L'operazione viene completata in modo sincrono, ad esempio si comporta come se fosse un socket non sovrapposto.                                                                                                                                 |
| non NULL       | NULL           | NULL                  | L'operazione viene completata sovrapposta, ma non Windows di completamento supportato da Sockets 2. In questo caso è possibile usare il meccanismo della porta di completamento (se supportato). In caso contrario, non verrà visualizzata alcuna notifica di completamento. |
| non NULL       | non NULL       | NULL                  | L'operazione viene completata sovrapposta, notifica segnalando l'oggetto evento.                                                                                                                                                      |
| non NULL       | Ignorato        | non NULL              | L'operazione viene completata sovrapposta, notifica pianificando la routine di completamento.                                                                                                                                               |



 

 

 



