---
description: Sia i writer che i richiedenti gestiscono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.
ms.assetid: 1ce56374-cfbf-4ee4-b942-8a7391911a38
title: Metadati VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e718d3fb0290f8610944180c079e4d615124eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307159"
---
# <a name="vss-metadata"></a>Metadati VSS

Sia i writer che i richiedenti gestiscono le informazioni necessarie per un'operazione di backup o ripristino nei propri documenti di metadati.

Questi documenti, il [*documento di metadati del writer*](vssgloss-w.md) e il [*documento sui componenti di backup*](vssgloss-b.md), vengono usati rispettivamente come base per la comunicazione e il coordinamento del writer e del richiedente durante le attività di backup e ripristino.

I metadati sono rappresentati in formato XML utilizzando uno schema proprietario. I metadati possono essere copiati su disco, nastro o qualsiasi altro dispositivo di archiviazione di massa. Deve essere sempre salvato nei supporti di backup durante un'operazione di backup e deve essere recuperato dal supporto nel corso di un'operazione di ripristino.

**Attenzione:** I dettagli specifici del formato e dello schema sono solo per uso del sistema. Gli sviluppatori non devono tentare di modificare o utilizzare direttamente la rappresentazione XML dei metadati.

Ai writer e ai richiedenti viene offerta un'ampia gamma di metodi di query e set per accedere e modificare i componenti di backup e i documenti di metadati del writer:

-   [Utilizzo del documento di metadati del writer](working-with-the-writer-metadata-document.md)
-   [Utilizzo del documento componenti di backup](working-with-the-backup-components-document.md)
-   [Componenti dei metadati VSS](vss-metadata-components.md)

 

 



