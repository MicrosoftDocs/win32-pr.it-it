---
title: Guida alla programmazione per Windows a 64 bit
description: Microsoft ha rilasciato versioni a 64 bit del Windows operativo.
ms.assetid: eb31408a-549d-427e-9f8e-9ae96bf6f854
keywords:
- Guida alla programmazione Windows a 64 bit a 64 bit Windows programmazione
- Guida alla programmazione Windows a 64 bit Windows programmazione home page
- Guida alla programmazione per la programmazione Windows a 64 bit Windows vedere Guida alla programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8af8c2cb6340bd7617dd7e712f89cb5d9485c65d3d56258850c1a885df1f77
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743468"
---
# <a name="programming-guide-for-64-bit-windows"></a>Guida alla programmazione per Windows a 64 bit

Microsoft ha rilasciato versioni a 64 bit del Windows operativo. Il Windows a 64 bit è stato progettato in base alla compatibilità. Gli sviluppatori possono garantire che le applicazioni a 32 bit esistenti siano eseguite in un Windows a 64 bit o sfruttare i vantaggi delle applicazioni Windows a 64 bit eseguendo la migrazione delle applicazioni.

## <a name="benefits-of-64-bit-windows"></a>Vantaggi della versione a 64 bit Windows

Un sistema operativo a 64 bit supporta molto più memoria fisica rispetto a un sistema operativo a 32 bit. Ad esempio, la maggior parte dei sistemi Windows a 32 bit supporta un massimo di 4 gigabyte di memoria fisica, con fino a 3 gigabyte di spazio indirizzi per ogni processo, mentre il Windows a 64 bit supporta fino a 2 terabyte di memoria fisica con 8 terabyte di spazio indirizzi per ogni processo. La memoria fisica aumentata include i vantaggi seguenti per le applicazioni:

-   Ogni applicazione può supportare più utenti. È necessario replicare tutta o parte di ogni applicazione per ogni utente, che richiede memoria aggiuntiva.
-   Ogni applicazione ha prestazioni migliori. L'aumento della memoria fisica consente l'esecuzione simultanea di più applicazioni e di rimanere completamente residenti nella memoria principale del sistema. In questo modo si riduce o si elimina la riduzione delle prestazioni dello scambio di pagine da e verso il disco.
-   Ogni applicazione ha più memoria per l'archiviazione e la manipolazione dei dati. I database possono archiviare più dati nella memoria fisica del sistema. L'accesso ai dati è più veloce perché le operazioni di lettura su disco non sono necessarie.
-   Le applicazioni possono modificare grandi quantità di dati in modo semplice e affidabile. La composizione video per il lavoro con immagini in movimento richiede Windows a 64 bit per questo motivo. La modellazione per applicazioni scientifiche e finanziarie trae vantaggio notevolmente dalle strutture di dati residenti in memoria che non sono possibili nelle applicazioni a 32 bit Windows.

Esistono anche vantaggi importanti per le aziende:

-   Maggiore produttività. I knowledge worker possono dedicare tempo a pensare e produrre, invece di attendere che il software finisca le attività.
-   Costo di proprietà inferiore. Ogni server può supportare un numero maggiore di utenti e applicazioni, quindi l'azienda richiederà meno server. Ciò si traduce direttamente in un overhead di gestione minore, uno dei costi più elevati in qualsiasi ambiente informatico.
-   Nuove opportunità di applicazione. Le nuove applicazioni possono essere progettate senza le barriere imposte dalle applicazioni a 32 bit Windows. Le nuove applicazioni grafiche semplificano e semplificano il lavoro. Le attività a elevato utilizzo di dati attualmente impossibili possono essere eseguite con la Windows a 64 bit.

## <a name="in-this-section"></a>Contenuto della sezione

-   [Getting Ready for 64-bit Windows](getting-ready-for-64-bit-windows.md)
-   [Progettazione di interfacce compatibili a 64 bit](designing-64-bit-compatible-interfaces.md)
-   [Esecuzione di applicazioni a 32 bit](running-32-bit-applications.md)
-   [Suggerimenti sulla migrazione](migration-tips.md)

 

 




