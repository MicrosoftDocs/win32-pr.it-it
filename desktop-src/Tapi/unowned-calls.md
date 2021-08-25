---
description: Per evitare che le chiamate senza proprietario siano nel sistema di telefonia, TAPI elimina le chiamate segnalate da un provider di servizi se non riesce a identificare un'applicazione come proprietario iniziale della chiamata.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Chiamate senzawned
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ea6fffa2ee65f24d73337980e2a8952157aa5d1000e5c657d75af372f26f00d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991651"
---
# <a name="unowned-calls"></a>Chiamate senzawned

Per evitare che le chiamate senza proprietario siano nel sistema di telefonia, TAPI elimina le chiamate segnalate da un provider di servizi se non riesce a identificare un'applicazione come proprietario iniziale della chiamata. In TAPI versione 2.0 e successive, TAPI chiama la [**funzione \_ lineDrop TSPI**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) per eliminare la chiamata.

Il provider di servizi può sapere in anticipo se è disponibile un'applicazione per assumere la proprietà di una nuova chiamata. TAPI informa sempre il provider di servizi dei tipi di supporti per i quali è disponibile un'applicazione usando la [**funzione \_ lineSetDefaultMediaDetection TSPI.**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)

Ad esempio, se un provider di servizi determina che è presente una chiamata attiva sulla riga con la modalità INTERACTIVEVOICE LINEMEDIAMODE, deve controllare il rilevamento dei supporti predefinito prima di generare i messaggi \_ [**LINE \_ NEWCALL**](line-newcall.md) e [**LINE \_ CALLSTATE.**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) Se il rilevamento dei supporti predefinito indica che nessuna applicazione sta cercando una chiamata LINEMEDIAMODE INTERACTIVEVOICE, il provider di servizi non deve inviare i messaggi perché TAPI lo \_ elimina immediatamente.

 

 
