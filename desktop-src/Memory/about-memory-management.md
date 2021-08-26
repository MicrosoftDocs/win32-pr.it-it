---
description: Ogni processo in Microsoft Windows a 32 bit ha un proprio spazio di indirizzi virtuali che consente di indirizzarsi fino a 4 gigabyte di memoria.
ms.assetid: f259f3cb-81c0-4b5f-b6fa-9681a278019a
title: Informazioni sulla gestione della memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b2cc91b2a907fa5f9db24f42393be51bb8795200357eff0b612f8241219361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869971"
---
# <a name="about-memory-management"></a>Informazioni sulla gestione della memoria

Ogni processo in Microsoft Windows a 32 bit ha un proprio spazio di indirizzi virtuali che consente di indirizzarsi fino a 4 gigabyte di memoria. Ogni processo a 64 bit Windows uno spazio di indirizzi virtuali di 8 terabyte. Tutti i thread di un processo possono accedere al relativo spazio di indirizzi virtuali. Tuttavia, i thread non possono accedere alla memoria che appartiene a un altro processo, che protegge un processo dal danneggiamento da parte di un altro processo.

Per informazioni sullo spazio di indirizzi virtuali e sulle funzioni di gestione della memoria, vedere gli argomenti seguenti.

-   [Spazio indirizzi virtuali](virtual-address-space.md)
-   [Pool di memoria](memory-pools.md)
-   [Informazioni sulle prestazioni della memoria](memory-performance-information.md)
-   [Funzioni di memoria virtuale](virtual-memory-functions.md)
-   [Funzioni heap](heap-functions.md)
-   [File Mapping](file-mapping.md)
-   [Supporto di memoria di grandi dimensioni](large-memory-support.md)
-   [Funzioni globali e locali](global-and-local-functions.md)
-   [Funzioni della libreria C standard](standard-c-library-functions.md)
-   [Confronto dei metodi di allocazione di memoria](comparing-memory-allocation-methods.md)

 

 



