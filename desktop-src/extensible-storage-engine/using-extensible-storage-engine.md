---
description: Altre informazioni sull'uso di Extensible Archiviazione Engine
title: Uso del motore Archiviazione estendibile
TOCTitle: Using Extensible Storage Engine
ms:assetid: d0249519-4c7c-49c1-9c80-b3cae2537d61
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294096(v=EXCHG.10)
ms:contentKeyID: 32765711
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: e994b423b56b092e8865ad2440829aecfe3832b5a36d015869e0b700c2579a86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118070441"
---
# <a name="using-extensible-storage-engine"></a>Uso del motore Archiviazione estendibile


_**Si applica a:** Windows | Windows Server_

## <a name="using-extensible-storage-engine"></a>Uso del motore Archiviazione estendibile

Questa sezione contiene informazioni generali su come usare le parti seguenti dell'API ESE.

  - [Colonne](./columns.md)

  - [Indicizzazione nella tabella](./indexing-in-the-table.md)

  - [Creazione di database](./creating-databases.md)

  - [Transazioni](./transactions.md)

  - [Errori ESE](./extensible-storage-engine-errors.md)

  - [File ESE](./extensible-storage-engine-files.md)

I file di origine del programma devono includere il file di intestazione esent.h per accedere ai prototipi di funzione e alle definizioni di struttura per l'API Extensible Archiviazione Engine. Gli sviluppatori possono usare il file di libreria esent.lib per compilare applicazioni che usano l'API Extensible Archiviazione Engine. In fase di esecuzione, le applicazioni si collegano al esent.dll.
