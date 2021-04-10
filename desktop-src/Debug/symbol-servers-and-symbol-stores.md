---
description: La configurazione corretta dei simboli per il debug può essere un'attività complessa, in particolare per il debug del kernel.
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  Server di simboli e archivi simboli"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225597"
---
# <a name="symbol-server-and-symbol-stores"></a>  Server di simboli e archivi simboli

La configurazione corretta dei simboli per il debug può essere un'attività complessa, in particolare per il debug del kernel. Spesso è necessario che si conoscano i nomi e le versioni di tutti i prodotti nel computer. Il debugger deve essere in grado di individuare i file di simboli che corrispondono a ogni versione del prodotto e Service Pack. Questo può comportare un percorso di simboli estremamente lungo costituito da un lungo elenco di directory.

Per semplificare queste difficoltà nel coordinamento dei file di simboli, usare il *server di simboli*. Il server di simboli consente ai debugger di recuperare automaticamente i file di simboli corretti senza nomi di prodotto, versioni o numeri di Build. Strumenti di debug per Windows contiene il server di simboli SymSrv.

Il server di simboli viene attivato includendo una determinata stringa di testo nel percorso dei simboli. Ogni volta che il debugger deve caricare i simboli per un modulo appena caricato, chiama il server di simboli per individuare i file di simboli appropriati. Il server dei simboli individua i file in un *Archivio di simboli*. Si tratta di una raccolta di file di simboli, di un indice e di uno strumento che può essere utilizzato da un amministratore per aggiungere ed eliminare file. I file vengono indicizzati in base a parametri univoci, ad esempio il timestamp e le dimensioni dell'immagine. Strumenti di debug per Windows contiene uno strumento di archiviazione simboli denominato SymStore.

Per altre informazioni, vedere:

-   [Uso di SymSrv](using-symsrv.md)
-   [Uso di SymStore](using-symstore.md)
-   [Uso di altri archivi simboli](using-other-symbol-stores.md)
-   [Opzioni Command-Line SymStore](symstore-command-line-options.md)
-   [Server di simboli e firewall Internet](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[File di simboli](symbol-files.md)
</dt> </dl>

 

 



