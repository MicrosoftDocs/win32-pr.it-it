---
description: A volte un messaggio firmato richiede un controfirma.
ms.assetid: de83a9ad-4e88-4477-8c9e-6dd7d5ec9e8f
title: Controfirme messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8dff2920217dd9a79f917f7b625da3919747d7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752127"
---
# <a name="message-countersignatures"></a>Controfirme messaggi

A volte un messaggio firmato richiede un [*controfirma*](../secgloss/c-gly.md). Ad esempio, l'utente A può inviare un messaggio di dati firmato all'utente B, in attesa di B per confermare l'accordo con i termini contenuti nel documento. L'utente B decodifica il messaggio, legge i termini e, se il contratto, controfirma il messaggio. Il messaggio controfirmato viene quindi inviato di nuovo all'utente A. l'utente A ora sa e può dimostrare che l'utente B ha accettato le condizioni.

Nella tabella seguente sono elencate le sezioni che contengono le descrizioni delle procedure o esempi di programmi C del messaggio controfirma.



| Sezione                                                                                                                                 | Contenuto                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [Funzioni di messaggio](cryptography-functions.md)                                                                       | Elenca le funzioni di firma del contatore.                             |
| [Controfirma un messaggio](countersigning-a-message.md)                                                                                | Descrive il processo di contatore della firma di un messaggio.                  |
| [Verifica di un controfirma](verifying-a-countersignature.md)                                                                        | Descrive la procedura per la verifica di una firma del contatore.           |
| [Verifica di un messaggio firmato](verifying-a-signed-message.md)                                                                            | Descrive in dettaglio un processo per la verifica della firma in un messaggio firmato. |
| [Esempio di programma C: codifica e decodifica di un messaggio controfirmato](example-c-program-encoding-and-decoding-a-countersigned-message.md) | Programma C di esempio che codifica e decodifica un messaggio controfirmato. |



 

 

 
