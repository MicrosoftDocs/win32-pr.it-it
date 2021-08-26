---
description: La \_ tabella ForceCodepage è una tabella speciale usata per modificare la tabella codici di un pacchetto di installazione. È possibile determinare o impostare la tabella codici esportando o importando un file di archivio di testo denominato \_ ForceCodepage.idt.
ms.assetid: d95c205f-a800-4a63-a712-6f06675e4a8a
title: _ForceCodepage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee252260b0aaee9713c28af5a6d810a3f6a8ed1c1b376b52bd82472cebfd0853
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119979601"
---
# <a name="_forcecodepage"></a>\_ForceCodepage

La \_ tabella ForceCodepage è una tabella speciale usata per modificare la tabella codici di un pacchetto di installazione. È possibile determinare o impostare la tabella codici esportando o importando un file di archivio [di testo](text-archive-files.md) denominato \_ ForceCodepage.idt.

Il formato della tabella ForceCodepage è 2 righe vuote seguite da \_ una terza riga che indica la tabella codici numerica. Ad esempio, un file con estensione idt della tabella \_ ForceCodepage per un database giapponese sarà simile al seguente. La tabella codici numerica in questo caso è 932.

``` syntax
<- this line blank
<- this line blank
932 _ForceCodepage
```

Per altre informazioni su come usare ForceCodepage per ottenere o impostare la tabella codici \_ di un database, vedere gli argomenti seguenti.

-   [Gestione della tabella codici (Windows programma di installazione)](code-page-handling-windows-installer-.md)
-   [Determinazione della tabella codici di un database di installazione](determining-an-installation-database-s-code-page.md)
-   [Impostazione della tabella codici di un database](setting-the-code-page-of-a-database.md)

La \_ tabella ForceCodepage è una pseudo-tabella speciale usata per modificare la tabella codici di un pacchetto di installazione. L'uso della tabella ForceCodepage imposta in modo incondizionato il database sulla tabella codici senza eseguire alcuna convalida per stabilire se i dati attualmente presenti nel database possono essere convertiti nella nuova \_ tabella codici. È sempre consigliabile che la modifica della tabella codici di un database inizi con un database indipendente dal linguaggio.

 

 



