---
description: Per liberare tutta la memoria usata dal gestore di simboli per un processo, usare la funzione SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Pulizia del gestore dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6db42f1fedfe68af4ab6eab885aefff0e8eb56e4ac9262f79adef8733f7ee7d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956960"
---
# <a name="symbol-handler-cleanup"></a>Pulizia del gestore dei simboli

Per liberare tutta la memoria usata dal gestore di simboli per un processo, usare la [**funzione SymCleanup.**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) Questa funzione enumera tutti i moduli caricati, libera ogni modulo e libera la memoria allocata per l'elenco di moduli. Dopo aver chiamato **SymCleanup,** non è possibile usare l'handle del processo nelle funzioni di gestione dei simboli finché non si chiama la [**funzione SymInitialize.**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize)

 

 



