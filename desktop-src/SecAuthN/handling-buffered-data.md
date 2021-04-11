---
description: Diverse funzioni del provider di rete accettano l'indirizzo e la dimensione di un buffer in cui la funzione inserisce una struttura di dati a dimensione variabile.
ms.assetid: 0029a04d-6cf2-40e1-ae1d-4c349a379ad7
title: Gestione dei dati memorizzati nel buffer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63e123fc1ccccae6120b6db1c9ada554acc5b02a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232839"
---
# <a name="handling-buffered-data"></a>Gestione dei dati memorizzati nel buffer

Diverse funzioni del provider di rete accettano l'indirizzo e la dimensione di un buffer in cui la funzione inserisce una struttura di dati a dimensione variabile.

In ogni caso, il meccanismo usato è lo stesso. Il chiamante alloca un buffer e passa il relativo indirizzo alla funzione. Passa inoltre l'indirizzo di un **DWORD** che specifica la dimensione del buffer, in byte.

La funzione copia quindi la maggior parte della struttura di dati richiesta come può essere nel buffer. Se tutti i dati si integrano nel buffer, la funzione restituisce l' \_ esito positivo. Se i dati non rientrano nel buffer, i dati potrebbero essere incompleti e la funzione imposta l'errore di \_ altri \_ dati. In entrambi i casi, il **valore DWORD** che indica la dimensione del buffer è impostato sul numero di byte effettivamente necessari per la struttura dei dati. In questo modo, se il buffer passato era troppo piccolo e la funzione ha esito negativo, il chiamante può allocare un nuovo buffer della dimensione richiesta e chiamare di nuovo la funzione.

Quando le strutture di dati restituite includono stringhe a lunghezza variabile, le singole strutture di dati contengono in genere puntatori a queste stringhe. Anche le stringhe devono essere posizionate all'interno del buffer. Tuttavia, è importante posizionarli alla fine del buffer. In caso contrario, non sarà possibile eseguire l'indicizzazione dell'ennesima struttura. In altre parole, tutte le strutture si trovano in modo contiguo all'inizio del buffer. I puntatori a stringhe o a dati a lunghezza variabile devono essere puntatori effettivi, non offset nel buffer.

Quando si utilizza un buffer per passare e restituire dati costituiti solo da stringhe, il **valore DWORD** che specifica la dimensione del buffer deve essere impostato sul numero totale di caratteri che si adattano a tali stringhe, non sul numero di byte.

 

 



