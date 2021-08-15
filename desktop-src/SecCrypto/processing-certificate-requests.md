---
description: Viene illustrato il modo in cui Servizi certificati elabora le richieste di certificato.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Elaborazione delle richieste di certificato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be2c8e8acacbb001803cf3ce8d7e1263e920673eb912a04105ec8bb2772953a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117977406"
---
# <a name="processing-certificate-requests"></a>Elaborazione delle richieste di certificato

Servizi certificati esegue i passaggi seguenti durante l'elaborazione di [*una richiesta di certificato:*](../secgloss/c-gly.md)

1.  Richiedere la ricezione.

    La [*richiesta di*](../secgloss/c-gly.md) certificato viene inviata dal client a un'applicazione intermedia, che la formatta in una richiesta di formato PKCS 10 e la invia al motore del \# server.

2.  Richiedere l'approvazione.

    Il motore del server chiama il [modulo criteri](policy-modules.md), che esegue query sulle proprietà della richiesta, decide se la richiesta è autorizzata o meno e imposta le proprietà facoltative del certificato.

3.  Formazione del certificato.

    Se la richiesta viene approvata, il motore del server accetta la richiesta e tutte le proprietà richieste dal modulo criteri e compila un certificato completo.

4.  Pubblicazione del certificato.

    Il motore del server archivia il certificato completato nel database di Servizi certificati e notifica all'applicazione intermedia lo stato della richiesta. Se il [modulo di uscita](exit-modules.md) lo ha richiesto, il motore del server notificherà un evento di rilascio del certificato. In questo modo il modulo di uscita può eseguire altre operazioni, ad esempio la pubblicazione del certificato in un repository di certificati esterno, ad esempio un servizio directory. Nel frattempo, l'intermediario ottiene il certificato pubblicato da Servizi certificati e lo passa di nuovo al client.

La figura seguente mostra come una [*richiesta di certificato*](../secgloss/c-gly.md) viene elaborata da Servizi certificati.

![elaborazione di una richiesta di certificato](images/certflow.png)

 

 
