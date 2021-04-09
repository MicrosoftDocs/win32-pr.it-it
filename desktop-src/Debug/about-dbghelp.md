---
description: Negli argomenti seguenti vengono descritti i file di simboli e la funzionalità fornita dalle funzioni DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informazioni su DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 634633d44d0c9e8202d99fd16140dd0a506453ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126246"
---
# <a name="about-dbghelp"></a>Informazioni su DbgHelp

Negli argomenti seguenti vengono descritti i file di simboli e la funzionalità fornita dalle [funzioni DbgHelp](dbghelp-functions.md).

-   [Versioni di DbgHelp](dbghelp-versions.md)
-   [File di simboli](symbol-files.md)
-   [Gestione dei simboli](symbol-handling.md)
-   [Server di simboli e archivi simboli](symbol-servers-and-symbol-stores.md)
-   [File minidump](minidump-files.md)
-   [Server di origine](source-server-and-source-indexing.md)
-   [Supporto aggiornato della piattaforma](updated-platform-support.md)

Si noti che tutte le [funzioni DbgHelp](dbghelp-functions.md) sono a thread singolo. Pertanto, le chiamate da più thread a questa funzione potrebbero causare un comportamento imprevisto o un danneggiamento della memoria. Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più di un thread a questa funzione.

 

 



