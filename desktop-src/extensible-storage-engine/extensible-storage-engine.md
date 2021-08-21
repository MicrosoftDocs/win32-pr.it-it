---
description: 'Altre informazioni su: Extensible Archiviazione Engine'
title: Motore Archiviazione estendibile
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: d1ec139cf947cb2d95bfccf3737c1f6559bf01ffbfa55f2e9a7d1e890efd6a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980821"
---
# <a name="extensible-storage-engine"></a>Motore Archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="extensible-storage-engine"></a>Motore Archiviazione estendibile

Extensible Archiviazione Engine (ESE) è una tecnologia avanzata di archiviazione ISAM (Indexed And Sequential Access Method). ESE consente alle applicazioni di archiviare e recuperare dati dalle tabelle usando la navigazione indicizzata o sequenziale del cursore. Supporta schemi denormalizzati, tra cui tabelle wide con numerose colonne di tipo sparse, colonne multivalore e indici di tipo sparse e rtf. Consente alle applicazioni di usufruire di uno stato dei dati coerente usando l'aggiornamento e il recupero dei dati transazionati. Viene fornito un meccanismo di ripristino di arresto anomalo del sistema in modo che la coerenza dei dati sia mantenuta anche in caso di arresto anomalo del sistema. Fornisce transazioni ACID (Atomic Consistent Isolated Durable) su dati e schema tramite un log write-ahead e un modello di isolamento dello snapshot. Le transazioni in ESE sono altamente simultanee e questo rende ESE utile per le applicazioni server. Memorizza i dati nella cache per ottimizzare l'accesso a prestazioni elevate ai dati. Inoltre, è leggero e risulta utile per le applicazioni che fungono da ruoli ausiliari.

ESE è per l'uso in applicazioni che richiedono un'archiviazione dei dati strutturata veloce e/o leggera, in cui l'accesso ai file non elaborati o il Registro di sistema non supporta i requisiti di indicizzazione o dimensioni dei dati dell'applicazione.

Viene usato dalle applicazioni che non archiviano mai più di 1 megabyte di dati ed è stato usato in applicazioni con database in casi estremi superiori a 1 terabyte e in genere più di 50 gigabyte.

Questa documentazione è destinata agli sviluppatori che hanno familiarità con C e C++ e ai concetti di base del database, ad esempio tabelle, colonne, indici, ripristino e transazioni. L'unico metodo di accesso per ESE è l'API C descritta in questa documentazione.

Extensible Archiviazione Engine è un Windows che è stato introdotto nel Windows 2000. Non tutte le funzionalità o le API sono disponibili in tutte le versioni Windows sistemi operativi.

ESE offre un motore di archiviazione in modalità utente che gestisce i dati all'interno di file binari flat accessibili tramite le API Windows dati. ESE è accessibile tramite una DLL caricata direttamente nel processo dell'applicazione. non sono necessari metodi di accesso remoto di o forniti dal motore di database stesso. Anche se ESE non dispone di un metodo di accesso remoto o inter-processo, i file di dati che usa possono essere forniti in modalità remota usando SMB (Server Message Block) tramite le API Windows, ma questa operazione non è consigliata.

**Si** Windows XP 64-Bit Edition è lo stesso di Windows Server 2003 allo scopo di determinare il set di funzionalità ESE supportato.  

### <a name="notes"></a>Note

ESE era noto in precedenza come Joint Engine Technology (JET) Blue e così spesso il termine "JET Blue" o "JET" viene usato in modo intercambiabile con il termine ESE al di fuori di questa documentazione. Esistono tuttavia due implementazioni completamente separate dell'API JET, denominate JET Blue e JET Red. Il termine "JET" viene spesso usato anche per fare riferimento a JET Red, ovvero il motore di database usato con Microsoft Office Access. Le due implementazioni JET sono completamente diverse, vengono gestite separatamente, hanno un set di funzionalità notevolmente diverso e non sono intercambiabili. Nella documentazione di ESE, "JET" si riferisce all'API ESE o JET perché viene implementata da ESE. Tutti i riferimenti a JET Red verranno sempre etichettati in modo esplicito come "JET Red".

### <a name="in-this-section"></a>Contenuto della sezione

[Informazioni di riferimento sul motore Archiviazione estendibile](./extensible-storage-engine-reference.md)
