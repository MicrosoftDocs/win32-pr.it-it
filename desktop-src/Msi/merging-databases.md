---
description: È possibile usare il programma di installazione per aggiungere le informazioni in un database in un altro database eseguendo un'unione.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Unione di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2931bb624037f2f909b99cfeb19a64fcb4abef689fe988a308d35766f50b1dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628707"
---
# <a name="merging-databases"></a>Unione di database

È possibile usare il programma di installazione per aggiungere le informazioni in un database in un altro database eseguendo un'unione. [Le unioni e le trasformazioni](merges-and-transforms.md) operano su un intero database e un'unione combina due database in uno. Le unioni sono utili per i team di sviluppo perché consentono al database di installazione di applicazioni di grandi dimensioni di essere suddivise in parti più piccole e quindi ricombinate nel database di installazione completo in un secondo momento.

**Per unire più database dei componenti in un singolo database completo**

1.  Sviluppare separatamente i database dei componenti parziali.
2.  Unire ogni database dei componenti nel database principale del prodotto chiamando la [**funzione MsiDatabaseMerge.**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea)

 

 



