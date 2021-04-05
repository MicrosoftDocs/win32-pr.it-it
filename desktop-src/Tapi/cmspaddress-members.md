---
description: L'elenco seguente contiene i membri dell'indirizzo CMSP.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Membri di CMSPAddress
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103885828"
---
# <a name="cmspaddress-members"></a>Membri di CMSPAddress



| Tipi di membri                    | Nome                    | Descrizione                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Iunknown                        | \*\_pFTM m               | Puntatore al marshaller a thread libero.                                                         |
| HANDLE                          | \_htEvent m              | Handle per l'evento Tapi3.dll, che viene utilizzato per notificare a TAPI che il MSP desidera inviare dati. |
| \_voce elenco                     | \_evento m            | Elenco di eventi.                                                                                  |
| CMSPCritSection                 | \_EventDataLock m        | Blocco che protegge i dati correlati alla gestione degli eventi con TAPI.                             |
| ITTerminalManager               | \*\_pITTerminalManager m | Puntatore all'oggetto di gestione terminal.                                                      |
| CMSPArray <ITTerminal \*> | \_terminali m            | Elenco di terminali statici che è possibile utilizzare per l'indirizzo.                                    |
| BOOL                            | \_fTerminalsUpToDate m   | Questo flag è **true** se l'elenco di terminali è aggiornato.                                        |
| CMSPCritSection                 | \_TerminalDataLock m     | Blocco che protegge i membri dati correlati al terminale.                                        |



 

 

 



