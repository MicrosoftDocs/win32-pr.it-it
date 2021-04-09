---
description: In ogni sistema è disponibile un numero limitato di oggetti dati privati allo scopo di archiviare le informazioni in modo protetto e crittografato.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Oggetto dati privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccacd1334c9859495acf89075b77a0f10af4cb64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128778"
---
# <a name="private-data-object"></a>Oggetto dati privato

In ogni sistema è disponibile un numero limitato di oggetti dati privati allo scopo di archiviare le informazioni in modo protetto e crittografato.

Gli oggetti dati privati vengono forniti principalmente per supportare l'archiviazione delle password degli account del server. Questa operazione è utile per i server in esecuzione in un account specifico. La password dell'account del server è costituita da dati privati che devono essere protetti, ma necessari per la registrazione del server.

Gli oggetti dati privati possono essere di uso generico oppure possono essere uno dei tre tipi specializzati: locale, globale e computer.

Gli oggetti dati privati locali possono essere letti solo localmente dal computer che archivia l'oggetto. Se si tenta di leggere i dati in modalità remota, si verifica un errore di accesso allo stato \_ \_ negato. Gli oggetti dati privati locali hanno nomi di chiave che iniziano con il prefisso "L $". Oltre agli oggetti privati locali creati, il sistema operativo definisce gli oggetti privati locali seguenti: $machine. ACC, SAC, SAI e SANSC.

Gli oggetti dati privati globali sono globali, nel senso che se vengono creati in un controller di dominio, verranno replicati automaticamente in tutti i controller di dominio del dominio. In altre parole, ogni controller di dominio in tale dominio avrà accesso ai valori contenuti nell'oggetto dati privato globale. Al contrario, gli oggetti dati globali privati creati in un sistema che non è un controller di dominio, nonché oggetti dati privati non globali, non vengono replicati. Gli oggetti dati globali privati hanno nomi di chiave che iniziano con "G $".

È possibile accedere agli oggetti dati privati del computer solo dal sistema operativo. Questi oggetti hanno nomi di chiave che iniziano con "M $".

**Nota**  È possibile impostare, ma non è possibile recuperare gli oggetti dati privati del computer.

Oltre a questi prefissi, i valori seguenti indicano anche oggetti locali o computer. Questi valori sono supportati per la compatibilità con le versioni precedenti e non devono essere usati quando si creano nuovi oggetti locali o computer. Il nome della chiave degli oggetti dati privati locali può iniziare anche con "RasDialParms" o "RasCredentials". Il nome della chiave per gli oggetti computer può anche iniziare con, "NL $" o " \_ SC \_ ".

Gli oggetti dati privati che non sono uno dei tipi specializzati precedenti utilizzano nomi di chiave che non iniziano con un prefisso. Questi oggetti non vengono replicati e possono essere letti in locale o in remoto dalle applicazioni.

 

 



