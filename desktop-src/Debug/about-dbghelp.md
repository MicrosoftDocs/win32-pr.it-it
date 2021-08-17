---
description: Negli argomenti seguenti vengono descritti i file di simboli e le funzionalità fornite dalle funzioni DbgHelp.
ms.assetid: 1bae2f0a-94a4-4152-bccc-b4deb1291a09
title: Informazioni su DbgHelp
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 958a139a7dcbffb8ee1b3b3d030d170fc821e6022038cab6a704b3b04f820f33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118162699"
---
# <a name="about-dbghelp"></a>Informazioni su DbgHelp

Negli argomenti seguenti vengono descritti i file di simboli e le funzionalità fornite dalle [funzioni DbgHelp](dbghelp-functions.md).

-   [Versioni di DbgHelp](dbghelp-versions.md)
-   [File di simboli](symbol-files.md)
-   [Gestione dei simboli](symbol-handling.md)
-   [Server di simboli e archivi simboli](symbol-servers-and-symbol-stores.md)
-   [File minidump](minidump-files.md)
-   [Server di origine](source-server-and-source-indexing.md)
-   [Supporto aggiornato della piattaforma](updated-platform-support.md)

Si noti che tutte [le funzioni DbgHelp](dbghelp-functions.md) sono a thread singolo. Pertanto, le chiamate da più thread a questa funzione probabilmente comportano un comportamento imprevisto o un danneggiamento della memoria. Per evitare questo problema, è necessario sincronizzare tutte le chiamate simultanee da più thread a questa funzione.

 

 



