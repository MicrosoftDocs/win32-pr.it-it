---
title: Gestione degli errori RAS
description: Quando si verifica un errore, il Gestione connessioni remoto richiama il gestore di notifica del client.
ms.assetid: 73595fa9-9548-49bf-bcce-d023bc1351d5
keywords:
- Servizio di accesso remoto RAS, errori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b870678eb2dbe95c190bc67415b9abb5481c33918429194404893349c0d7f7a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791279"
---
# <a name="handling-ras-errors"></a>Gestione degli errori RAS

Quando si verifica un errore, il Gestione connessioni remoto richiama il gestore di notifica del client. La notifica indica lo stato della connessione quando si è verificato l'errore e un codice che identifica l'errore. In questi casi, il gestore delle notifiche deve chiamare [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa) per terminare la connessione RAS.

I codici di errore che identificano gli errori RAS sono definiti nel file raserror.h. Il client RAS può usare la [**funzione RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa) per ottenere una stringa di visualizzazione che descrive l'errore. Per [una descrizione di questi errori,](routing-and-remote-access-error-codes.md) vedere Codici di errore di Routing e Accesso remoto.

 

 




