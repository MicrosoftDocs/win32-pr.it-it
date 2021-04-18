---
description: La resilienza è la capacità di un'applicazione di eseguire il ripristino normalmente da situazioni in cui manca un componente essenziale oppure è stato sostituito da una versione incompatibile.
ms.assetid: c0504a84-6d51-4734-a55d-f1d1ebcb3e73
title: Resilienza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d57e5c5a342a8e1c295afd97a69fe2828362a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316743"
---
# <a name="resiliency"></a>Resilienza

La resilienza è la capacità di un'applicazione di eseguire il ripristino normalmente da situazioni in cui manca un componente essenziale oppure è stato sostituito da una versione incompatibile. Con la creazione di un pacchetto di installazione e l'utilizzo delle [funzioni del programma di installazione](installer-functions.md), gli sviluppatori possono utilizzare il Windows Installer per produrre applicazioni resilienti in grado di eseguire il ripristino da tali situazioni.

-   Usare l'elenco di origine del programma di installazione per aumentare la resilienza delle applicazioni che si basano sulle risorse di rete. Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md).
-   Usare l'API del programma di installazione per verificare se è installata una funzionalità vitale, un componente, un file o una versione del file.
-   Usare l'API del programma di installazione per controllare il percorso di un componente in fase di esecuzione. In questo modo si riduce la dipendenza dell'applicazione da percorsi di file statici, che in genere differiscono tra i computer.
-   Utilizzare il programma di installazione per reinstallare i collegamenti danneggiati, le voci del registro di sistema e altri componenti senza dover eseguire di nuovo l'installazione.
-   Aumentare la resilienza dell'installazione del prodotto lasciando abilitata la funzionalità di rollback del programma di installazione. Per ulteriori informazioni, vedere [rollback Installation](rollback-installation.md).

 

 



