---
description: La resilienza è la capacità di un'applicazione di eseguire correttamente il ripristino da situazioni in cui un componente essenziale è mancante o è stato sostituito da una versione incompatibile.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73565a129c25b19e0fb362e5363626f1acfee0387b2d4e4826f79222e7425b96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810781"
---
# <a name="resiliency"></a>Resilienza

La resilienza è la capacità di un'applicazione di eseguire correttamente il ripristino da situazioni in cui un componente essenziale è mancante o è stato sostituito da una versione incompatibile. Tramite la creazione di un pacchetto di installazione e l'uso delle funzioni del programma di installazione [di](installer-functions.md), gli sviluppatori possono usare il programma di installazione di Windows per produrre applicazioni resilienti in grado di eseguire il ripristino in situazioni di questo tipo.

-   Usare l'elenco di origine del programma di installazione per aumentare la resilienza delle applicazioni che si basano sulle risorse di rete. Per altre informazioni, vedere [Resilienza dell'origine.](source-resiliency.md)
-   Usare l'API del programma di installazione per verificare se è installata una funzionalità essenziale, un componente, un file o una versione del file.
-   Usare l'API del programma di installazione per controllare il percorso di un componente in fase di esecuzione. In questo modo si riduce la dipendenza dell'applicazione dai percorsi di file statici, che in genere differiscono tra computer.
-   Usare il programma di installazione per reinstallare i collegamenti danneggiati, le voci del Registro di sistema e altri componenti senza dover rieseguire l'installazione.
-   Aumentare la resilienza dell'installazione del prodotto lasciando abilitata la funzionalità di rollback del programma di installazione. Per altre informazioni, vedere [Rollback Installation](rollback-installation.md).

 

 



