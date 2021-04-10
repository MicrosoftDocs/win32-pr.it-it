---
title: Evitare il polimorfismo
description: I nuovi tipi di dati includono due tipi polimorfici, INT \_ ptr e Long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- polimorfismo-programmazione Windows a 64 bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332100"
---
# <a name="avoiding-polymorphism"></a>Evitare il polimorfismo

I nuovi tipi di dati includono due tipi polimorfici, **int \_ ptr** e **Long \_ ptr**. Nelle finestre a 32 bit, il **\_ ptr int** esegue il mapping a **int** e il **Long \_ ptr** viene mappato a **Long**. Nelle finestre a 64 bit entrambi i tipi sono mappati al tipo intrinseco **\_ \_ Int64** . Il compilatore MIDL supporta questi tipi per le chiamate di procedure remote, ma esiste una limitazione intrinseca che è necessario tenere presente quando si usano in un ambiente distribuito. Assicurarsi di commentare il codice di conseguenza.

Indipendentemente dalle dimensioni della piattaforma, le dimensioni del Wire di questi tipi polimorfici sono sempre di 32 bit. Quando si esegue l'unmarshalling in Windows a 64 bit, il segno della libreria di Runtime estende i valori firmati e assegna zero ai byte più significativi per un valore senza segno. Quando si inserisce un valore a 64 bit in rete, il runtime tronca i byte più ordinati. Sono pertanto utilizzabili solo i valori a 32 bit di ordine inferiore.

Usare i tipi polimorfici solo quando necessario per il porting. Per le nuove interfacce, usare i tipi Integer intrinseci **\_ \_ MIDL e** **\_ \_ Int64** oppure usare un tipo di puntatore o un handle di contesto, a seconda del tipo di dati che si desidera trasferire.

Il compilatore a 64 bit supporta un nuovo **\_ \_ int3264** intrinseco polimorfico. Anche in questo caso, questo tipo è stato sviluppato per supportare le attività di porting, in questo caso per supportare in modo trasparente i tipi **uint \_ ptr** . (Un'altra funzione intrinseca, **\_ \_ long3264**, supporterà il tipo **ULONG \_ ptr** ). Non utilizzare direttamente **\_ \_ int3264** . utilizzare il tipo **\_ ptr int** quando è necessario un tipo polimorfico per i motivi di portabilità.

 

 




