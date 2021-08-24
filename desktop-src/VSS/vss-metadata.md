---
description: Sia i writer che i richiedenti mantengono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadati di VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e69d0a40bbbce2d231573d187843c14bd83fea419a7024940d0fd618838500b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119986581"
---
# <a name="vss-metadata"></a>Metadati di VSS

Sia i writer che i richiedenti mantengono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.

Questi documenti, rispettivamente il documento [*dei metadati*](vssgloss-w.md) del writer e il documento dei componenti di [*backup,*](vssgloss-b.md)vengono usati come base per la comunicazione e il coordinamento del writer e del richiedente durante le attività di backup e ripristino.

I metadati sono rappresentati in formato XML usando uno schema proprietario. I metadati possono essere copiati su disco, nastro o qualsiasi altro dispositivo di archiviazione di massa. Deve sempre essere salvato nel supporto di backup durante un'operazione di backup e dovrà essere recuperato da tale supporto nel corso di un'operazione di ripristino.

**Attenzione:** I dettagli specifici del formato e dello schema sono solo per uso di sistema. Gli sviluppatori non devono tentare di modificare o usare direttamente la rappresentazione XML dei metadati.

I writer e i richiedenti sono forniti con un'ampia gamma di metodi di query e set per accedere ai documenti Componenti di backup e Metadati del writer e modificarli:

-   [Uso del documento dei metadati del writer](working-with-the-writer-metadata-document.md)
-   [Uso del documento Componenti di backup](working-with-the-backup-components-document.md)
-   [Componenti dei metadati di VSS](vss-metadata-components.md)

 

 



