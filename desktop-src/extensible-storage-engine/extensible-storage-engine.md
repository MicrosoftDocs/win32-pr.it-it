---
description: 'Altre informazioni su: Extensible Storage Engine'
title: Motore di archiviazione estendibile
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 0ef85de696f52d2220c11b05ed7ada76a70df871
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049671"
---
# <a name="extensible-storage-engine"></a>Motore di archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine"></a>Motore di archiviazione estendibile

Extensible Storage Engine (ESE) è una tecnologia di archiviazione (ISAM) avanzata indicizzata e sequenziale. ESE consente alle applicazioni di archiviare e recuperare i dati dalle tabelle utilizzando la navigazione indicizzata o sequenziale del cursore. Supporta schemi denormalizzati, tra cui tabelle estese con numerose colonne di tipo sparse, colonne multivalore e indici sparsi e ricchi. Consente alle applicazioni di usufruire di uno stato di dati coerente utilizzando l'aggiornamento e il recupero di dati transazionali. Viene fornito un meccanismo di recupero di arresto anomalo del sistema in modo che la coerenza dei dati venga mantenuta anche in caso di arresto anomalo del sistema Fornisce transazioni ACID (atomiche con isolamento coerente) sui dati e sullo schema tramite un log write-ahead e un modello di isolamento dello snapshot. Le transazioni in ESE sono altamente simultanee e rendono ESE utile per le applicazioni server. I dati vengono memorizzati nella cache per ottimizzare l'accesso ai dati ad alte prestazioni. Inoltre, è leggero, rendendolo utile per le applicazioni che svolgono ruoli ausiliari.

ESE è destinata all'uso in applicazioni che richiedono un archivio dati strutturato rapido e/o leggero, in cui l'accesso ai file non elaborati o il registro di sistema non supporta l'indicizzazione dell'applicazione o i requisiti di dimensione dei dati.

Viene usato da applicazioni che non archiviano mai più di un megabyte di dati ed è stato usato nelle applicazioni con database in casi estremi superiori a 1 terabyte e di solito oltre 50 gigabyte.

Questa documentazione è destinata agli sviluppatori che hanno familiarità con C e C++ e con concetti di base sui database quali tabelle, colonne, indici, ripristino e transazioni. L'unico metodo di accesso per ESE è l'API C descritta in questa documentazione.

Extensible Storage Engine è un componente di Windows introdotto in Windows 2000. Non tutte le funzionalità o le API sono disponibili in tutte le versioni dei sistemi operativi Windows.

ESE fornisce un motore di archiviazione in modalità utente che gestisce i dati all'interno di file binari Flat accessibili tramite le API di Windows. È possibile accedere ad ESE tramite una DLL caricata direttamente nel processo dell'applicazione; Nessun metodo di accesso remoto richiesto o fornito dal motore di database stesso. Sebbene ESE non disponga di un metodo di accesso remoto o tra processi, i file di dati usati possono essere forniti in remoto usando SMB (Server Message Block) tramite le API di Windows, ma questa operazione non è consigliata.

**Nota**  Windows XP 64-bit Edition è identico a quello di Windows Server 2003 allo scopo di determinare il set di funzionalità ESE supportato.

### <a name="notes"></a>Note

ESE era precedentemente noto come Joint Engine Technology (JET) Blue e, di conseguenza, il termine "JET Blue" o "JET" viene usato in modo intercambiabile con il termine ESE al di fuori di questa documentazione. Tuttavia, esistono in realtà due implementazioni completamente separate dell'API JET, denominate JET Blue e JET Red. Il termine "JET" viene spesso usato anche per fare riferimento a JET Red, che è il motore di database usato con Microsoft Office Access. Le due implementazioni JET sono completamente diverse, sono gestite separatamente, hanno un set di funzionalità notevolmente diverso e non sono intercambiabili. Nella documentazione di ESE, "JET" si riferisce ad ESE o all'API JET quando ESE la implementa. Qualsiasi riferimento al rosso JET sarà sempre contrassegnato in modo esplicito come "JET Red".

### <a name="in-this-section"></a>Contenuto della sezione

[Informazioni di riferimento sul motore di archiviazione estendibile](./extensible-storage-engine-reference.md)
