---
description: La \_ tabella ForceCodepage è una tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione. È possibile determinare o impostare la tabella codici esportando o importando un file di archivio di testo denominato \_ ForceCodepage. IDT.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 132843fa092409b26811afd6a4c1f3e7cf0544f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311116"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

La \_ tabella ForceCodepage è una tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione. È possibile determinare o impostare la tabella codici esportando o importando un [file di archivio di testo](text-archive-files.md) denominato \_ ForceCodepage. IDT.

Il formato della \_ tabella ForceCodepage è 2 righe vuote seguite da una terza riga che indica la tabella codici numerici. Ad esempio, un \_ file table. IDT di ForceCodepage per un database giapponese avrà un aspetto simile al seguente. La tabella codici numerici in questo caso è 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Per ulteriori informazioni sull'utilizzo di \_ ForceCodepage per ottenere o impostare la tabella codici di un database, vedere gli argomenti seguenti.

-   [Gestione della tabella codici (Windows Installer)](code-page-handling-windows-installer-.md)
-   [Determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md)
-   [Impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md)

La \_ tabella ForceCodepage è una pseudo-tabella speciale utilizzata per modificare la tabella codici di un pacchetto di installazione. Utilizzando la \_ tabella ForceCodepage, il database viene impostato in modo incondizionato sulla tabella codici senza eseguire alcuna convalida per determinare se i dati attualmente presenti nel database possono essere convertiti nella nuova tabella codici. È sempre consigliabile che la modifica della tabella codici di un database inizi con un database indipendente dalla lingua.

 

 



