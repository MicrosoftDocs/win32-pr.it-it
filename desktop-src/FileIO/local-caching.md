---
description: La memorizzazione nella cache locale dei dati è una tecnica usata per velocizzare l'accesso di rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Impostazioni Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d60fa71274bfcbf559ff57a3ab1a6fceba13d47315d80d9c3722a2a206b611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927621"
---
# <a name="local-caching"></a>Impostazioni Caching

*La memorizzazione nella cache* locale dei dati è una tecnica usata per velocizzare l'accesso di rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.

L'effetto della memorizzazione nella cache locale è che consente di combinare più operazioni di scrittura nella stessa area di un file in un'unica operazione di scrittura in rete. La memorizzazione nella cache locale riduce il traffico di rete perché i dati vengono scritti una sola volta. Tale memorizzazione nella cache migliora il tempo di risposta apparente delle applicazioni perché le applicazioni non attendono che i dati siano inviati attraverso la rete al server.

La memorizzazione nella cache locale dei dati da leggere può sembrare velocizzare le operazioni tramite la lettura in anticipo. Un esempio semplice è un'applicazione che accede ai dati in sequenza, ad esempio il preprocessore di un compilatore. In questi casi, il livello di rete del sistema operativo legge i dati attraverso la rete prima che l'applicazione richiede i dati. Idealmente, la rete recapita i dati prima che l'applicazione lo file system, con conseguente risposta quasi istantanea. In pratica, questo accade raramente, ma spesso la lettura anticipata velocizza le applicazioni anticipando la richiesta successiva.

La memorizzazione nella cache locale consente anche di ridurre il traffico di rete leggendo una parte di un file in rete una sola volta e mantenendolo nella cache locale. Operazioni di lettura successive su tale parte da parte dell'applicazione lette dalla cache locale.

Un tipo di applicazione che può trarre vantaggio dalla memorizzazione nella cache locale è i file batch. I processori dei comandi leggono ed eseguono un file batch una riga alla volta. Per ogni riga, il processore di comandi apre il file, cerca all'inizio della riga, legge quanto necessario, chiude il file e quindi esegue la riga. Ogni riga comporta una grande quantità di traffico di rete. Il traffico di rete può essere notevolmente ridotto memorizzando nella cache l'intero file batch in un client.

La memorizzazione nella cache locale consente anche di risolvere un altro problema associato alle reti, in particolare le reti che eseguono operazioni su modem e altri thin pipe: tempo di risposta lento. Gli utenti non vogliono attendere che i dati vengono recuperati in rete, modificati e quindi scritti. Con la lettura in anticipo e la memorizzazione nella cache in scrittura, spesso sembra che queste funzionino molto più velocemente di quanto non facciano effettivamente.

Un rischio della memorizzazione nella cache locale è che i dati scritti hanno solo la stessa integrità del client, purché i dati vengono memorizzati nella cache del client. In generale, i dati memorizzati nella cache locale devono essere scaricati nel server appena possibile. Con i sistemi operativi moderni e il supporto hardware, ad esempio alimentatori ininterrotti, il rischio di perdita di dati memorizzati nella cache locale è ridotto. Tuttavia, il rischio esiste ancora ed è necessario considerare sia il compromesso tra l'integrità dei dati e la velocità di risposta apparente sia il compromesso tra l'integrità dei dati e la riduzione del traffico di rete.

 

 



