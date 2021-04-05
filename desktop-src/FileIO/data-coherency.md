---
description: Se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati. Un tipo di sistema software che fornisce dati coerenza è un sistema di controllo delle revisioni (RCS).
ms.assetid: cd33d20e-bf25-4a50-9b20-344495554434
title: Coerenza dati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f300296ff0fdc807beb95e2c03662814957bedb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884342"
---
# <a name="data-coherency"></a>Coerenza dati

I dati *coerenti* sono dati identici in tutta la rete. In altre parole, se i dati sono coerenti, i dati nel server e in tutti i client vengono sincronizzati. Un tipo di sistema software che fornisce dati coerenza è un sistema di controllo delle revisioni (RCS). Un sistema di questo tipo è in genere abbastanza semplice, con un solo utente autorizzato a modificare un file specificato alla volta. Altri utenti possono leggere il file, ma non modificarlo.

Si dice che l'utente che può modificare un file è stato estratto. L'utente quindi archivia il file modificato in modo che altri utenti possano visualizzare le modifiche. Solo dopo che l'utente ha controllato un file di nuovo, è possibile estrarlo da un altro utente.

Un RCS richiede l'intervento attivo degli utenti per operare in modo utile. Un file system che opera in una rete deve gestire automaticamente il problema.

La memorizzazione nella cache locale dei dati coerenti è piuttosto semplice quando si dispone di un thread in un client che accede a un file in rete alla volta. Nella maggior parte dei casi, tuttavia, molti thread diversi in uno o più computer potrebbero leggere lo stesso file. Questa situazione è ancora piuttosto semplice. Poiché i dati nel file sono statici, ogni computer client può avere la propria copia locale senza alcuna implicazione per i dati coerenza.

Una situazione più comune è costituita da un thread che modifica il file e da numerosi altri thread che la leggono. Nel momento in cui si verifica un'operazione di scrittura, tutte le cache locali del file sono obsolete. Il server deve notificare a ogni client di abbandonare la cache. Tutte le operazioni di lettura successive per il file devono essere eseguite attraverso la rete.

In un'altra situazione comune, più thread in uno o più client di rete potrebbero provare a scrivere nello stesso file. Questa situazione è simile a quella in cui più utenti RCS desiderano apportare modifiche allo stesso file. Ogni utente in sequenza deve estrarre il file, apportare modifiche e quindi riprovare a eseguire il file. Allo stesso modo, in uno schema di memorizzazione nella cache locale, il server deve consegnare il privilegio di scrivere in un file in un solo thread client alla volta.

 

 



