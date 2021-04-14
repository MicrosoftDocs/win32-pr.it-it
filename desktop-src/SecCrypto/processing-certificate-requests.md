---
description: Viene illustrato come Servizi certificati elabora le richieste di certificati.
ms.assetid: 40641167-12de-4008-80e4-2fb758146421
title: Elaborazione delle richieste di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f70a25d9ca633247c3995677825dc011b2b38d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104555696"
---
# <a name="processing-certificate-requests"></a>Elaborazione delle richieste di certificati

Durante l'elaborazione di una [*richiesta di certificato*](../secgloss/c-gly.md), Servizi certificati esegue i passaggi seguenti:

1.  Richiedere la ricezione.

    La [*richiesta di certificato*](../secgloss/c-gly.md) viene inviata dal client a un'applicazione intermedia, che la formatta in una \# richiesta di formato PKCS 10 e la invia al motore del server.

2.  Richiedi l'approvazione.

    Il motore del server chiama il [modulo criteri](policy-modules.md), che esegue query sulle proprietà della richiesta, decide se la richiesta è autorizzata o meno e imposta le proprietà facoltative del certificato.

3.  Formazione del certificato.

    Se la richiesta viene approvata, il motore del server accetta la richiesta e tutte le proprietà richieste dal modulo criteri e compila un certificato completo.

4.  Pubblicazione del certificato.

    Il motore Server archivia il certificato completato nel database di Servizi certificati e notifica all'applicazione intermedia lo stato della richiesta. Se il [modulo di uscita](exit-modules.md) è stato richiesto, il motore del server invierà una notifica di un evento di rilascio del certificato. Ciò consente al modulo di uscita di eseguire ulteriori operazioni, ad esempio la pubblicazione del certificato in un repository di certificati esterno, ad esempio un servizio directory. Nel frattempo, l'intermediario ottiene il certificato pubblicato da Servizi certificati e lo passa nuovamente al client.

Nella figura seguente viene illustrato come una [*richiesta di certificato*](../secgloss/c-gly.md) viene elaborata da Servizi certificati.

![elaborazione di una richiesta di certificato](images/certflow.png)

 

 
