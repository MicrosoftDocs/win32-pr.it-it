---
description: Per semplificare e ridurre la quantità di codice necessario per eseguire le normali attività di manipolazione dei messaggi, è disponibile un gruppo di funzioni di alto livello.
ms.assetid: 7c1a4d6e-9b9d-43c8-b094-3c98b9a68490
title: Messaggi semplificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1dbacaac4dd8ef32b7bab1ff4e57ad04aa1263c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129659"
---
# <a name="simplified-messages"></a>Messaggi semplificati

Per semplificare e ridurre la quantità di codice necessario per eseguire le normali attività di manipolazione dei messaggi, è disponibile un gruppo di funzioni di alto livello. Queste funzioni sono denominate "funzioni di messaggio semplificate". I nomi di tutte le funzioni di messaggio semplificate contengono la parola "message".

Le [*funzioni di messaggio semplificate*](../secgloss/s-gly.md) sono a un livello superiore rispetto alle funzioni di crittografia di base o alle funzioni dei messaggi di basso livello. Eseguono il wrapping di diverse funzioni di crittografia, messaggio di basso livello e di certificato di base in una singola funzione che esegue un'attività specifica in modo specifico, ad esempio la crittografia di un \# messaggio PKCS 7 o la firma di un messaggio. Le funzioni di messaggio semplificate forniscono un modo rapido per iniziare a usare CryptoAPI riducendo il numero di chiamate di funzione necessarie per eseguire un'attività.

Nella tabella seguente sono elencate le sezioni che contengono descrizioni dettagliate delle procedure o esempi di programmi C sull'utilizzo delle funzioni di messaggio semplificate.



| Sezione                                                                                                                                         | Contenuto                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [Funzioni di messaggio semplificate](cryptography-functions.md)                                                         | Elenca le funzioni di messaggio semplificate.                                                     |
| [Creazione di un messaggio firmato](creating-a-signed-message.md)                                                                                      | Descrive in dettaglio il processo di creazione di un messaggio firmato.                                           |
| [Procedura per la firma dei dati](procedure-for-signing-data.md)                                                                                    | Fornisce una procedura per l'utilizzo delle funzioni di messaggio semplificate per creare un messaggio firmato. |
| [Verifica di un messaggio firmato](verifying-a-signed-message.md)                                                                                    | Descrive in dettaglio un processo per la verifica della firma in un messaggio firmato.                          |
| [Crittografia di un messaggio](../secauthn/encrypting-a-message.md)                                                                                           | Descrive le attività necessarie per crittografare e decrittografare un messaggio.                                  |
| [Decrittografia di un messaggio](../secauthn/decrypting-a-message.md)                                                                                           | Descrive le attività necessarie per decrittografare un messaggio.                                              |
| [Esempio di programma C: uso di CryptEncryptMessage e CryptDecryptMessage](example-c-program-using-cryptencryptmessage-and-cryptdecryptmessage.md) | Fornisce una procedura e un codice di esempio per la crittografia e la decrittografia di un messaggio.               |



 

 

 
