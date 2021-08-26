---
title: Server-Side'implementazione della pipe
description: I programmi server per le applicazioni distribuite che usano pipe non devono implementare alcuna funzione push, pull o alloc.
ms.assetid: de733075-5767-4d46-b294-089c7e3cc695
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf5cf7a928c58890e618c9a62cf1df77fe3d00a7ef9d013240d66e57e88a1584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017693"
---
# <a name="server-side-pipe-implementation"></a>Server-Side'implementazione della pipe

I programmi server per le applicazioni distribuite che usano pipe non devono implementare alcuna funzione push, pull o alloc. Devono contenere procedure che i client possono richiamare in remoto per avviare i trasferimenti di dati. Negli argomenti seguenti questa sezione illustra come possono essere implementate le procedure remote del server.

-   [Implementazione di pipe di input nel server](implementing-input-pipes-on-the-server.md)
-   [Implementazione di pipe di output nel server](implementing-output-pipes-on-the-server.md)

 

 




