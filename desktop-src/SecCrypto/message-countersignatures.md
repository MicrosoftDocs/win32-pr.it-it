---
description: A volte un messaggio firmato richiede una controfirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Controfirma dei messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d95f9d082a2814501bdb948d1bfebdc5c2699012446c5189c5c3fc18612c1ef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080641"
---
# <a name="message-countersignatures"></a>Controfirma dei messaggi

A volte un messaggio firmato richiede [*una controfirma.*](../secgloss/c-gly.md) Ad esempio, l'utente A può inviare un messaggio di dati firmati all'utente B, prevedendo che B confermi l'accordo con le condizioni contenute nel documento. L'utente B decodifica il messaggio, legge i termini e, in caso di accordo, controfirma il messaggio. Il messaggio controfirmato viene quindi inviato all'utente A. L'utente A ora conosce e può dimostrare che l'utente B ha accettato le condizioni.

Nella tabella seguente sono elencate le sezioni che contengono descrizioni delle procedure o esempi di programmi C di controfirma dei messaggi.



| Sezione                                                                                                                                 | Contenuto                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Funzioni di messaggio](cryptography-functions.md)                                                                       | Elenca le funzioni di firma del contatore.                             |
| [Controfirma di un messaggio](countersigning-a-message.md)                                                                                | Dettagli del processo di controfirizzazione di un messaggio.                  |
| [Verifica di una controfirma](verifying-a-countersignature.md)                                                                        | Illustra in dettaglio la procedura per la verifica di una firma del contatore.           |
| [Verifica di un messaggio firmato](verifying-a-signed-message.md)                                                                            | Dettagli di un processo per la verifica della firma in un messaggio firmato. |
| [Programma C di esempio: codifica e decodifica di un messaggio controfirmato](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Programma C di esempio che codifica e decodifica un messaggio controfirmato. |



 

 

 
