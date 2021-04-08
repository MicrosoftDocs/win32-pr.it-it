---
title: Registrazione di una funzione hook
description: Le applicazioni client ricevono WinEvents in una funzione di callback WinEventProc. Le azioni eseguite dalla funzione di callback sono definite dall'applicazione, ma la sintassi deve essere quella specificata nel prototipo.
ms.assetid: 7e999335-6a41-4d22-82ef-1a8dd6cb656e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5b1f39a535b366af72b1034cc9344171d253ea0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855778"
---
# <a name="registering-a-hook-function"></a>Registrazione di una funzione hook

Le applicazioni client ricevono WinEvents in una funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) . Le azioni eseguite dalla funzione di callback sono definite dall'applicazione, ma la sintassi deve essere quella specificata nel prototipo.

Prima di poter ricevere gli eventi, la funzione deve essere registrata chiamando [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook). Il client può chiamare **SetWinEventHook** più di una volta per registrare funzioni hook diverse o per impostare eventi aggiuntivi per una funzione hook registrata in precedenza.

Quando si chiama [**SetWinEventHook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) , il client specifica quali eventi ricevere e come riceverli. Il client può scegliere di:

-   Ricevere tutti gli eventi o un set di eventi specifico.
-   Ricevere eventi da tutti i thread o da un thread specifico.
-   Ricevere eventi da tutti i processi o da un processo specifico.
-   Gestione degli eventi in corso o out-of-process.

Quando viene generato un evento che corrisponde ai criteri specificati, il sistema chiama la funzione di callback [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) del client (o "procedura hook"). I parametri ricevuti dalla funzione hook indicano al client la finestra, l'oggetto e il possibile elemento figlio che ha generato l'evento. Un client usa questi parametri in una chiamata di recupero di oggetti, ad esempio [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent).

 

 




