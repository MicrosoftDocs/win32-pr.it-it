---
description: Ogni processo in Microsoft Windows a 32 bit dispone di uno spazio degli indirizzi virtuale che consente di indirizzare fino a 4 gigabyte di memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informazioni sulla gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4110bf1d0768f1321fd89ddd1d5a985e3e54aa75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307268"
---
# <a name="about-memory-management"></a>Informazioni sulla gestione della memoria

Ogni processo in Microsoft Windows a 32 bit dispone di uno spazio degli indirizzi virtuale che consente di indirizzare fino a 4 gigabyte di memoria. Ogni processo in Windows a 64 bit ha uno spazio di indirizzi virtuale di 8 terabyte. Tutti i thread di un processo possono accedere al proprio spazio degli indirizzi virtuali. Tuttavia, i thread non possono accedere alla memoria che appartiene a un altro processo, evitando che un processo venga danneggiato da un altro processo.

Per informazioni sullo spazio degli indirizzi virtuali e sulle funzioni di gestione della memoria, vedere gli argomenti seguenti.

-   [Spazio degli indirizzi virtuali](virtual-address-space.md)
-   [Pool di memoria](memory-pools.md)
-   [Informazioni sulle prestazioni della memoria](memory-performance-information.md)
-   [Funzioni di memoria virtuale](virtual-memory-functions.md)
-   [Funzioni heap](heap-functions.md)
-   [Mapping dei file](file-mapping.md)
-   [Supporto per memoria di grandi dimensioni](large-memory-support.md)
-   [Funzioni globali e locali](global-and-local-functions.md)
-   [Funzioni della libreria C standard](standard-c-library-functions.md)
-   [Confronto tra i metodi di allocazione della memoria](comparing-memory-allocation-methods.md)

 

 



