---
description: Per liberare tutta la memoria usata dal gestore di simboli per un processo, usare la funzione SymCleanup.
ms.assetid: d442b2f2-9225-43fd-bd25-274322857834
title: Pulitura gestore simboli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0daea96e780f7e3a685b408c7c774e91b2795b84
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877569"
---
# <a name="symbol-handler-cleanup"></a>Pulitura gestore simboli

Per liberare tutta la memoria usata dal gestore di simboli per un processo, usare la funzione [**SymCleanup**](/windows/desktop/api/Dbghelp/nf-dbghelp-symcleanup) . Questa funzione enumera tutti i moduli caricati, libera ogni modulo e libera la memoria allocata per l'elenco di moduli. Dopo aver chiamato **SymCleanup**, non è possibile usare l'handle di processo nelle funzioni di gestione dei simboli fino a quando non si chiama la funzione [**SymInitialize**](/windows/desktop/api/Dbghelp/nf-dbghelp-syminitialize) .

 

 



