---
description: In ogni sistema è disponibile un numero limitato di oggetti dati privati allo scopo di archiviare le informazioni in modo protetto, crittografato.
ms.assetid: 927473d7-b5bc-4b6f-b303-8a0f8680731d
title: Oggetto dati privato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481f3641a7195c68a2955cc2cf302e25aa0b5a48a1ef901bec4e056ee536b375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118893680"
---
# <a name="private-data-object"></a>Oggetto dati privato

In ogni sistema è disponibile un numero limitato di oggetti dati privati allo scopo di archiviare le informazioni in modo protetto, crittografato.

Gli oggetti dati privati vengono forniti principalmente per supportare l'archiviazione delle password dell'account server. Ciò è utile per i server eseguiti in un account specifico. La password dell'account del server è un dato privato che deve essere protetto, ma necessario per accedere al server.

Gli oggetti dati privati possono essere per utilizzo generico oppure possono essere di tre tipi specializzati: locale, globale e computer.

Gli oggetti dati privati locali possono essere letti solo localmente dal computer in cui è archiviato l'oggetto. Se si tenta di leggerli in modalità remota, viene restituito un errore STATUS \_ ACCESS \_ DENIED. Gli oggetti dati privati locali hanno nomi di chiave che iniziano con il prefisso "L$". Oltre agli oggetti privati locali creati, il sistema operativo definisce i seguenti oggetti privati locali: $machine.acc, SAC, SAI e SANSC.

Gli oggetti dati privati globali sono globali, nel senso che se vengono creati in un controller di dominio, verranno replicati automaticamente in tutti i controller di dominio in tale dominio. In altre parole, ogni controller di dominio in tale dominio avrà accesso ai valori contenuti nell'oggetto dati privato globale. Al contrario, gli oggetti dati privati globali creati in un sistema che non è un controller di dominio, nonché gli oggetti dati privati non globali, non vengono replicati. Gli oggetti dati privati globali hanno nomi di chiave che iniziano con "G$".

Gli oggetti dati privati del computer sono accessibili solo dal sistema operativo. Questi oggetti hanno nomi di chiave che iniziano con "M$".

**Nota**  È possibile impostare, ma non recuperare, oggetti dati privati del computer.

Oltre a questi prefissi, i valori seguenti indicano anche oggetti locali o del computer. Questi valori sono supportati per la compatibilità con le versioni precedenti e non devono essere usati quando si creano nuovi oggetti locali o del computer. Il nome della chiave degli oggetti dati privati locali può anche iniziare con "RasDialParms" o "RasCredentials". Anche il nome della chiave per gli oggetti computer può iniziare con "NL$" o " \_ sc \_ ".

Gli oggetti dati privati che non sono uno dei tipi specializzati precedenti usano nomi di chiave che non iniziano con un prefisso. Questi oggetti non vengono replicati e possono essere letti in locale o in remoto dalle applicazioni.

 

 



