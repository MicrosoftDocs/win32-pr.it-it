---
description: È possibile utilizzare il programma di installazione per aggiungere le informazioni di un database in un altro database eseguendo un'operazione di merge.
ms.assetid: c53ef3d2-b3dc-4cd1-bd98-a856a223917f
title: Unione di database
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8212355f37a12aa3b92bc10e6e3e41abdcf361dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968097"
---
# <a name="merging-databases"></a>Unione di database

È possibile utilizzare il programma di installazione per aggiungere le informazioni di un database in un altro database eseguendo un'operazione di merge. Le [unioni e le trasformazioni](merges-and-transforms.md) operano su un intero database e un'Unione combina due database in uno. Le unioni sono utili per i team di sviluppo perché consentono al database di installazione di applicazioni di grandi dimensioni di essere divise in parti più piccole e quindi ricombinate nel database di installazione completo in un secondo momento.

**Per unire più database di componenti in un unico database completo**

1.  Sviluppare separatamente i database dei componenti parziali.
2.  Unire ogni database componente nel database principale del prodotto chiamando la funzione [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) .

 

 



