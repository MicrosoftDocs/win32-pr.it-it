---
description: 'Gestione memoria crea i pool di memoria seguenti utilizzati dal sistema per allocare memoria: pool non di paging e pool di paging.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pool di memoria
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808998"
---
# <a name="memory-pools"></a>Pool di memoria

Gestione memoria crea i pool di memoria seguenti utilizzati dal sistema per allocare memoria: pool non di paging e pool di paging. Entrambi i pool di memoria si trovano nell'area dello spazio indirizzi riservato al sistema ed è mappato nello spazio indirizzi virtuale di ogni processo. Il pool non di paging è costituito da indirizzi di memoria virtuale che possono risiedere nella memoria fisica purché siano allocati gli oggetti kernel corrispondenti. Il pool di paging è costituito da memoria virtuale che può essere di paging all'esterno del sistema. Per migliorare le prestazioni, i sistemi con un singolo processore hanno tre pool di pagine e i sistemi multiprocessore hanno cinque pool di pagine.

Gli handle per [gli oggetti kernel](../sysinfo/kernel-objects.md) vengono archiviati nel pool di paging, quindi il numero di handle che è possibile creare è basato sulla memoria disponibile.

Il sistema registra i limiti e i valori correnti per il pool non di paging, il pool di paging e l'utilizzo del file di paging. Per altre informazioni, vedere [Informazioni sulle prestazioni della memoria](memory-performance-information.md).

 

 
