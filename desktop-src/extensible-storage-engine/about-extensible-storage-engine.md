---
description: Altre informazioni su Extensible Archiviazione Engine
title: Informazioni su Extensible Archiviazione Engine
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 26a1d4d28f1d5957432202545ff94c4f18c37e5a521e0deadfdabfb72751adec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118983871"
---
# <a name="about-extensible-storage-engine"></a>Informazioni su Extensible Archiviazione Engine


_**Si applica a:** Exchange Server 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Informazioni su Extensible Archiviazione Engine

Il motore di archiviazione estendibile (ESE) è un motore di database che archivia le informazioni in una sequenza logica. Le informazioni possono essere recuperate in sequenza o accedendo agli indici definiti. Gli aggiornamenti al database vengono implementati con una transazione per garantire operazioni sicure. ESE consente l'accesso simultaneo a più database, inclusi i database di file di log delle transazioni che possono essere usati per il ripristino del sistema. ESE è scalabile in applicazioni di grandi o piccole dimensioni. Con l'API (Application Programming Interface) ESE sono disponibili le funzionalità seguenti:

  - Backup e ripristino: un'applicazione può eseguire copie coerenti dello stato dei dati mentre è in linea e modifica attivamente lo stato dei dati.

  - Navigazione con cursore: l'applicazione può spostarsi con il cursore per accedere ai dati in sequenza o tramite indici.

  - Database: raccolta di tabelle di cui viene eseguito il backup e il ripristino come singola unità.

  - Registrazione e ripristino da arresto anomalo del sistema: l'API ESE garantisce che la coerenza dei dati definita dall'applicazione sia rispettata anche in caso di arresto anomalo del sistema.

  - Tabelle: struttura fondamentale del database ESE usato per archiviare i dati.

  - Transazione: il motore di database ESE fornisce transazioni ACID (Atomic Consistent Isolated Durable) che consentono alle applicazioni di recuperare i dati solo da stati di dati affidabili e di mantenere la coerenza dei dati in caso di chiusura imprevista del processo o arresto del sistema.

  - Scalabile: l'applicazione può creare database di dimensioni fino a 100 GB o fino a 1 MB.

