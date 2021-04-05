---
description: La memorizzazione nella cache locale dei dati è una tecnica che consente di velocizzare l'accesso alla rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Caching locale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884878"
---
# <a name="local-caching"></a>Caching locale

La *memorizzazione nella cache locale* dei dati è una tecnica che consente di velocizzare l'accesso alla rete ai file di dati. Comporta la memorizzazione nella cache dei dati nei client anziché nei server, quando possibile.

L'effetto della memorizzazione nella cache locale è che consente di combinare più operazioni di scrittura nella stessa area di un file in un'unica operazione di scrittura in rete. La memorizzazione nella cache locale riduce il traffico di rete perché i dati vengono scritti una volta. Questo tipo di memorizzazione nella cache consente di migliorare il tempo di risposta apparente delle applicazioni perché le applicazioni non attendono che i dati vengano inviati attraverso la rete al server.

La memorizzazione nella cache locale dei dati da leggere può comparire per velocizzare le operazioni per mezzo della lettura in anticipo. Un semplice esempio è un'applicazione che accede ai dati in sequenza, ad esempio il preprocessore di un compilatore. In questi casi, il livello di rete del sistema operativo legge i dati attraverso la rete prima che l'applicazione richieda i dati. Idealmente, la rete recapita i dati prima che vengano richiesti dall'applicazione dalla file system, ottenendo una risposta quasi immediata. In pratica, questa situazione si verifica raramente, ma spesso la lettura in avanti consente di velocizzare le applicazioni anticipando la richiesta successiva.

La memorizzazione nella cache locale consente inoltre di ridurre il traffico di rete leggendo una parte di un file in rete e quindi mantenendola nella cache locale. Operazioni di lettura successive sulla parte dell'applicazione lette dalla cache locale.

Un tipo di applicazione che può trarre vantaggio dalla memorizzazione nella cache locale è costituito da file batch. I processori di comandi leggono ed eseguono un file batch una riga alla volta. Per ogni riga, il processore del comando apre il file, Cerca all'inizio della riga, legge il più necessario, chiude il file, quindi esegue la riga. Ogni riga comporta una grande quantità di traffico di rete. È possibile ridurre considerevolmente il traffico di rete memorizzando nella cache l'intero file batch su un client.

La memorizzazione nella cache locale consente anche di un altro problema associato alle reti, in particolare le reti che eseguono il lavoro sui modem e altre Thin pipe, ovvero rallentamento del tempo di risposta. Gli utenti non desiderano attendere mentre i dati vengono recuperati sulla rete, modificati e quindi riscritti. Con la lettura e la memorizzazione nella cache di scrittura, spesso sembra che queste funzioni funzionino molto più velocemente di quanto effettivamente.

Un rischio di memorizzazione nella cache locale è che i dati scritti hanno solo la stessa integrità del client per tutto il tempo in cui i dati vengono memorizzati nella cache del client. In generale, i dati memorizzati localmente nella cache devono essere scaricati sul server il prima possibile. Con i sistemi operativi e il supporto hardware moderni, ad esempio gli alimentatori di continuità, il rischio di perdere i dati memorizzati nella cache locale è ridotto. Tuttavia, il rischio esiste ancora ed è necessario considerare sia il compromesso tra l'integrità dei dati che la velocità di risposta apparente e il compromesso tra l'integrità dei dati e il traffico di rete ridotto.

 

 



