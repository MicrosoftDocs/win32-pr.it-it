---
description: Per ridurre il tempo e la memoria quando si utilizzano molti file di simboli, utilizzare la funzione SymSetOptions per impostare l'opzione di caricamento posticipato dei simboli ( \_ caricamenti posticipati SYMOPT \_ ).
ms.assetid: 40c9384f-00ed-40cd-9687-b76b69e74f87
title: Caricamento posticipato dei simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64d05a3ad7ad0fe4017f1ba6fa99625af33c2cc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965888"
---
# <a name="deferred-symbol-loading"></a>Caricamento posticipato dei simboli

Per conservare il tempo e la memoria quando si utilizzano molti file di simboli, utilizzare la funzione [**SymSetOptions**](/windows/desktop/api/Dbghelp/nf-dbghelp-symsetoptions) per impostare l'opzione di caricamento posticipato dei simboli (SYMOPT \_ rinviati \_ ), quindi utilizzare la funzione [**SymLoadModuleEx**](/windows/desktop/api/Dbghelp/nf-dbghelp-symloadmoduleex) o [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) per caricare i simboli rinviati per tutti i moduli. Il gestore dei simboli elenca i simboli disponibili per i moduli, ma non esegue il mapping delle informazioni di debug in memoria fino a quando non viene richiesto. Si tratta del metodo preferito per utilizzare in modo efficiente i simboli di debug. Tutte le funzioni che utilizzano simboli sono interessate dal caricamento posticipato dei simboli.

 

 



