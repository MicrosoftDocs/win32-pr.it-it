---
description: Per impedire che le chiamate non possedute siano presenti nel sistema di telefonia, TAPI rilascia le chiamate segnalate da un provider di servizi se non è in grado di identificare un'applicazione come proprietario iniziale della chiamata.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chiamate non possedute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307809"
---
# <a name="unowned-calls"></a>Chiamate non possedute

Per impedire che le chiamate non possedute siano presenti nel sistema di telefonia, TAPI rilascia le chiamate segnalate da un provider di servizi se non è in grado di identificare un'applicazione come proprietario iniziale della chiamata. In TAPI versione 2,0 e successive, TAPI chiama la funzione [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) per eliminare la chiamata.

Il provider di servizi può sapere in anticipo se un'applicazione è disponibile o meno per la proprietà di una nuova chiamata. TAPI informa sempre il provider di servizi dei tipi di supporto per i quali è disponibile un'applicazione tramite la funzione [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .

Se, ad esempio, un provider di servizi determina la presenza di una chiamata attiva sulla riga con la \_ modalità LINEMEDIAMODE INTERACTIVEVOICE, deve controllare il rilevamento dei supporti predefiniti prima di generare i messaggi della [**riga \_ NEWCALL**](line-newcall.md) e [**\_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) . Se il rilevamento del supporto predefinito indica che nessuna applicazione sta cercando una \_ chiamata LINEMEDIAMODE INTERACTIVEVOICE, il provider di servizi non deve inviare i messaggi perché TAPI lo eliminerà immediatamente.

 

 
