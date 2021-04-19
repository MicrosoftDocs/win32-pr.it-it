---
description: Le funzioni di messaggio CryptoAPI rispettano lo \# standard CMS (Cryptographic Message Syntax) PKCS 7. Gli sviluppatori devono acquisire familiarità con questa specifica per utilizzare in modo più efficace le funzioni dei messaggi di basso livello. Alcune delle definizioni sono evidenziate qui.
ms.assetid: 99b633fe-9898-4570-ba8b-16ee78d351da
title: '\#Concetti sulla sintassi della messaggistica crittografica PKCS 7'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ead1c5e75737db80adbca725a30cb730b547be4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315377"
---
# <a name="pkcs-7-cryptographic-messaging-syntax-concepts"></a>\#Concetti sulla sintassi della messaggistica crittografica PKCS 7

Le funzioni di messaggio CryptoAPI rispettano lo [standard CMS (Cryptographic Message Syntax)](https://www.ietf.org/rfc/rfc3369.txt) [*PKCS \# 7*](../secgloss/p-gly.md) . Gli sviluppatori devono acquisire familiarità con questa specifica per utilizzare in modo più efficace le [*funzioni dei messaggi di basso livello*](../secgloss/l-gly.md). Alcune delle definizioni sono evidenziate qui.

Lo \# standard PKCS 7 descrive una sintassi generale per i dati a cui è possibile applicare la [*crittografia*](../secgloss/c-gly.md) , ad esempio le [*firme digitali*](../secgloss/d-gly.md) e le [*buste digitali*](../secgloss/d-gly.md). La sintassi ammette la ricorsione, in modo che, ad esempio, una busta possa essere annidata all'interno di un'altra oppure un'entità possa firmare i dati digitali che sono già stati inseriti in una busta. Consente inoltre di eseguire l'autenticazione degli attributi arbitrari, ad esempio l'ora di firma, insieme al contenuto di un messaggio. Inoltre, fornisce altri attributi, ad esempio [*controfirme*](../secgloss/c-gly.md), da associare a una firma.

Il tipo di dati contenuti in un \# messaggio PKCS 7 viene definito tipo di contenuto. Sono disponibili due classi di tipi di contenuto: base e migliorata.

-   I tipi di contenuto di base contengono solo dati senza miglioramenti per la crittografia. Attualmente esiste un solo tipo di contenuto in questa classe, il [*tipo di contenuto dei dati*](../secgloss/d-gly.md).
-   I [*tipi di contenuto avanzati*](../secgloss/e-gly.md) contengono dati di alcuni tipi (probabilmente crittografati) e altri miglioramenti crittografici (ad esempio hash o firme).

Il contenuto della classe avanzata usa l'incapsulamento, dando luogo a termini di [*contenuto esterno*](../secgloss/o-gly.md) (quello contenente i miglioramenti) e al [*contenuto interno*](../secgloss/i-gly.md) (quello che viene migliorato). Una classe avanzata, ad esempio, può contenere il [*tipo di contenuto dei dati*](../secgloss/d-gly.md) (classe base) con una firma inclusa. In questo caso, il tipo di contenuto dei dati è il *contenuto interno* e la combinazione del tipo di contenuto dei dati e la firma formano il contenuto esterno.

I tipi di contenuto definiti nello \# standard PKCS 7 sono i seguenti.



| Tipo di contenuto              | Descrizione                                                                                                                                                                                                                                                                                                           |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Data                      | Stringa ottetto (**byte**).                                                                                                                                                                                                                                                                                           |
| Dati firmati               | Contenuto di qualsiasi tipo e [*hash*](../secgloss/h-gly.md) di messaggi crittografati ([*digest*](../secgloss/m-gly.md)) del contenuto per zero o più firmatari.                                                                           |
| Dati in busta            | Contenuto crittografato di qualsiasi tipo e chiavi di crittografia del contenuto crittografate per uno o più destinatari. La combinazione di contenuto crittografato e chiave di crittografia del contenuto crittografata per un destinatario è una [*busta digitale*](../secgloss/d-gly.md) per tale destinatario. |
| Dati firmati e in busta | Contenuto crittografato di qualsiasi tipo, chiavi di crittografia del contenuto crittografate per uno o più destinatari e digest di messaggi crittografati in forma doppia per uno o più firmatari. La crittografia doppia è costituita da una crittografia con la chiave privata di un firmatario seguita da una crittografia con la chiave di crittografia del contenuto.                     |
| Dati digest             | Contenuto di qualsiasi tipo e un [*hash*](../secgloss/h-gly.md) del messaggio (digest) del contenuto.                                                                                                                                                                                             |
| Dati crittografati            | Contenuto crittografato di qualsiasi tipo. A differenza del [*tipo di contenuto dati*](../secgloss/d-gly.md)in busta, il tipo di contenuto dati crittografati non ha né destinatari né chiavi di crittografia del contenuto crittografate. Si presuppone che le chiavi siano gestite in altri modi.               |



 

> [!Note]  
> In tutta la \# specifica PKCS 7, i termini *digest* e [*digested*](../secgloss/d-gly.md) fanno riferimento al valore prodotto dall'applicazione di un [*algoritmo hash*](../secgloss/h-gly.md) ai dati. Questa documentazione usa i termini [*hash*](../secgloss/h-gly.md) e *Hashed* per lo stesso scopo. Ad esempio, il tipo di dati utilizzato con le [*funzioni di messaggio di basso livello*](../secgloss/l-gly.md) viene chiamato Hashed anziché digested. Ai fini di questa documentazione, i due set di termini possono essere usati in modo intercambiabile.

 

 

 
