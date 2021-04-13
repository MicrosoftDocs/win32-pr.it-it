---
title: Guida alla programmazione per Windows a 64 bit
description: Microsoft ha rilasciato versioni a 64 bit del sistema operativo Windows.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guida per programmatori Windows a 64 bit-programmazione Windows a 64 bit
- Guida per programmatori Windows a 64 bit-programmazione Windows a 64 bit, home page
- Guida per programmatori per la programmazione Windows a 64 bit di Windows a 64 bit vedere la guida per programmatori Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb1fa906510d3d9909c5cf888b562deaccb3496
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396178"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guida alla programmazione per Windows a 64 bit

Microsoft ha rilasciato versioni a 64 bit del sistema operativo Windows. Windows a 64 bit è stato progettato tenendo presente la compatibilità. Gli sviluppatori possono garantire che le applicazioni a 32 bit esistenti siano eseguite correttamente in Windows a 64 bit o sfruttare i vantaggi di Windows a 64 bit eseguendo la migrazione delle applicazioni.

## <a name="benefits-of-64-bit-windows"></a>Vantaggi di Windows a 64 bit

Un sistema operativo a 64 bit supporta una quantità di memoria fisica molto maggiore rispetto a un sistema operativo a 32 bit. Ad esempio, la maggior parte dei sistemi Windows a 32 bit supporta un massimo di 4 gigabyte di memoria fisica, con un massimo di 3 gigabyte di spazio di indirizzi per ogni processo, mentre Windows a 64 bit supporta fino a 2 terabyte di memoria fisica con 8 terabyte di spazio di indirizzi per ogni processo. L'aumento della memoria fisica include i vantaggi seguenti per le applicazioni:

-   Ogni applicazione può supportare più utenti. È necessario replicare tutte le applicazioni o parte di esse per ogni utente, che richiede memoria aggiuntiva.
-   Ogni applicazione offre prestazioni migliori. Una maggiore quantità di memoria fisica consente l'esecuzione simultanea di più applicazioni e rimane completamente residente nella memoria principale del sistema. In questo modo è possibile ridurre o eliminare la riduzione delle prestazioni dello scambio di pagine da e verso il disco.
-   Ogni applicazione dispone di più memoria per l'archiviazione e la manipolazione dei dati. I database possono archiviare più dati nella memoria fisica del sistema. L'accesso ai dati è più veloce perché le letture del disco non sono necessarie.
-   Le applicazioni possono modificare grandi quantità di dati in modo semplice e affidabile. Per questo motivo, la composizione video per il lavoro di Motion Picture richiede Windows a 64 bit. La modellazione per le applicazioni scientifiche e finanziarie è molto vantaggiosa dalle strutture di dati residenti in memoria che non sono possibili in Windows a 32 bit.

Sono inoltre disponibili importanti vantaggi per le aziende:

-   Maggiore produttività. I Knowledge Worker possono dedicare tempo a pensare e produrre, anziché attendere il completamento delle attività del software.
-   Costo inferiore della proprietà. Ogni server può supportare un numero maggiore di utenti e applicazioni, quindi l'azienda richiede un minor numero di server. Questo si traduce direttamente in un sovraccarico di gestione inferiore, uno dei costi più elevati in qualsiasi ambiente informatico.
-   Nuove opportunità di applicazione. Le nuove applicazioni possono essere progettate senza gli ostacoli imposti da Windows a 32 bit. Le nuove applicazioni grafiche renderanno il lavoro più semplice e più gradevole. Le attività che richiedono un utilizzo intensivo di dati oggi possono essere eseguite con Windows a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Preparazione per Windows a 64 bit](getting-ready-for-64-bit-windows.md)
-   [Progettazione di interfacce compatibili a 64 bit](designing-64-bit-compatible-interfaces.md)
-   [Esecuzione di applicazioni a 32 bit](running-32-bit-applications.md)
-   [Suggerimenti sulla migrazione](migration-tips.md)

 

 




