---
description: 'Il gestore della memoria crea i pool di memoria seguenti usati dal sistema per allocare memoria: pool non di paging e pool di paging.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pool di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60987b43347e55d8ee2d01672dbb8173ffc8dd5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319449"
---
# <a name="memory-pools"></a>Pool di memoria

Il gestore della memoria crea i pool di memoria seguenti usati dal sistema per allocare memoria: pool non di paging e pool di paging. Entrambi i pool di memoria si trovano nell'area dello spazio degli indirizzi riservata al sistema e mappati allo spazio degli indirizzi virtuali di ogni processo. Il pool non di paging è costituito da indirizzi di memoria virtuale che devono risiedere nella memoria fisica finché vengono allocati gli oggetti kernel corrispondenti. Il pool di paging è costituito da memoria virtuale di cui è possibile effettuare il paging all'interno e all'esterno del sistema. Per migliorare le prestazioni, i sistemi con un solo processore hanno tre pool di paging e i sistemi multiprocessore hanno cinque pool di paging.

Gli handle per [gli oggetti kernel](../sysinfo/kernel-objects.md) vengono archiviati nel pool di paging, quindi il numero di handle che è possibile creare è basato sulla memoria disponibile.

Il sistema registra i limiti e i valori correnti per il pool non di paging, il pool di paging e l'utilizzo del file di paging. Per ulteriori informazioni, vedere [informazioni sulle prestazioni della memoria](memory-performance-information.md).

 

 
