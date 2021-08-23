---
description: Per risparmiare tempo e memoria quando si usano molti file di simboli, usare la funzione SymSetOptions per impostare l'opzione deferred symbol loading (SYMOPT \_ DEFERRED \_ LOADS).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Caricamento dei simboli posticipato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8682de9ac8eaea78e037bf85ea8a17cd88e63bb56468ab39df3d1887fcc66801
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957150"
---
# <a name="deferred-symbol-loading"></a>Caricamento dei simboli posticipato

Per risparmiare tempo e memoria quando si usano molti file di simboli, usare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per impostare l'opzione deferred symbol loading (SYMOPT DEFERRED LOADS), quindi usare la funzione \_ \_ [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) per caricare i simboli posticipati per tutti i moduli. Il gestore dei simboli elarnerà i simboli disponibili per i moduli, ma non eseguirà il mapping delle informazioni di debug in memoria fino a quando non vengono richieste. Questo è il metodo preferito per usare in modo efficiente i simboli di debug. Tutte le funzioni che usano simboli sono interessate dal caricamento posticipato dei simboli.

 

 



