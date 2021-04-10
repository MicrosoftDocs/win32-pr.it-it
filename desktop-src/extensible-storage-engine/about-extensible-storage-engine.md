---
description: 'Altre informazioni su: informazioni sul motore di archiviazione estendibile'
title: Informazioni sul motore di archiviazione estendibile
TOCTitle: About Extensible Storage Engine
ms:assetid: 06d1526e-169d-4677-b409-2ed415287de6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269181(v=EXCHG.10)
ms:contentKeyID: 32765484
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 17e2277deaef54c04bf6a53a8464479fd67295a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966418"
---
# <a name="about-extensible-storage-engine"></a>Informazioni sul motore di archiviazione estendibile


_**Si applica a:** Exchange Server 2013 | Windows | Windows Server_

## <a name="about-extensible-storage-engine"></a>Informazioni sul motore di archiviazione estendibile

Extensible Storage Engine (ESE) è un motore di database che archivia le informazioni in una sequenza logica. Le informazioni possono essere recuperate in sequenza oppure accedendo agli indici definiti. Gli aggiornamenti al database vengono implementati con una transazione per garantire operazioni protette. ESE consente l'accesso simultaneo a più database, inclusi i database dei file di log delle transazioni che possono essere utilizzati per il ripristino del sistema. ESE è scalabile per applicazioni di grandi dimensioni o piccole. Le funzionalità seguenti sono disponibili con l'Application Programming Interface ESE (API):

  - Backup e ripristino: un'applicazione può eseguire copie coerenti dello stato dei dati mentre è in linea e modifica attivamente lo stato dei dati.

  - Navigazione del cursore: l'applicazione può spostarsi con il cursore per accedere ai dati in sequenza o usando gli indici.

  - Database: raccolta di tabelle di cui viene eseguito il backup e il ripristino come singola unità.

  - Registrazione e ripristino di arresto anomalo: l'API ESE garantisce che la coerenza dei dati definita dall'applicazione venga rispettata anche in caso di arresto anomalo del sistema.

  - Tables: la struttura di base del database ESE usato per archiviare i dati.

  - Transazione: il motore di database ESE fornisce transazioni ACID (Atomic coerenti) atomiche che consentono alle applicazioni di recuperare i dati solo da Stati di dati affidabili e di mantenere la coerenza dei dati in caso di interruzione imprevista di un processo o di arresto del sistema.

  - Scalabile: l'applicazione può creare database di dimensioni pari a 100 GB o fino a 1 MB.

