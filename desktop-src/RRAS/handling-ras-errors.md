---
title: Gestione degli errori RAS
description: Quando si verifica un errore, la gestione connessione di accesso remoto richiama il gestore di notifiche del client.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- RAS del servizio di accesso remoto, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f37c18a795f5675fc6df80da6027526f81a87010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712868"
---
# <a name="handling-ras-errors"></a>Gestione degli errori RAS

Quando si verifica un errore, la gestione connessione di accesso remoto richiama il gestore di notifiche del client. La notifica indica lo stato della connessione quando si è verificato l'errore e un codice che identifica l'errore. In questi casi, il gestore delle notifiche deve chiamare [**RasHangup**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione RAS.

I codici di errore che identificano gli errori RAS sono definiti nel file raserror. h. Il client RAS può usare la funzione [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) per ottenere una stringa di visualizzazione che descrive l'errore. Per una descrizione di questi errori, vedere [codici di errore di routing e accesso remoto](routing-and-remote-access-error-codes.md) .

 

 




