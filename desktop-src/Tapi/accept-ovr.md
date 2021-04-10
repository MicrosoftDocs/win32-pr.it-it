---
description: In alcuni ambienti, un utente non viene avvisato automaticamente di una chiamata a un'offerta, ad esempio tramite suoneria o un messaggio sullo schermo del computer.
ms.assetid: 50684e2a-0799-458b-9402-0958e35026d7
title: Accetta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dd23d8ca1ed483b23d1b56fe98721b9fc53fb3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226002"
---
# <a name="accept"></a>Accetta

In alcuni ambienti, un utente non viene avvisato automaticamente di una chiamata a un'offerta, ad esempio tramite suoneria o un messaggio sullo schermo del computer. L'operazione Accept avvia il processo di avviso (in genere squillante) e l'operazione di [risposta](answer-ovr.md) viene eseguita in seguito. L'applicazione può [eliminare](drop-ovr.md) la sessione, [reindirizzarla](redirect-ovr.md) o accettarla.

Se il provider di servizi corrente lo supporta, l'applicazione ha la possibilità di inviare informazioni utente utente al momento dell'accettazione. Non esiste alcuna garanzia che la rete fornisca tali informazioni alla parte chiamante.

Non tutti i provider di servizi supportano l'utilizzo di questa operazione.

**TAPI 2. x:** Vedere [**lineAccept**](/windows/win32/api/tapi/nf-tapi-lineaccept).

 

 
