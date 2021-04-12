---
title: Condivisione di una routine di I/O con altre applicazioni
description: Condivisione di una routine di I/O con altre applicazioni
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- I/O di file multimediali, procedure condivise
- I/O di file, procedure condivise
- input e output (I/O), procedure condivise
- I/O (input e output), procedure condivise
- condivisione di procedure di I/O con altre applicazioni
- mmioInstallIOProc (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398905"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>Condivisione di una routine di I/O con altre applicazioni

Se si desidera condividere una procedura di I/O con altre applicazioni, è necessario scrivere una libreria di collegamento dinamico (DLL) per l'applicazione. È possibile condividere la procedura di I/O eseguendo una delle operazioni seguenti:

-   Includere il codice per la procedura di I/O nella DLL.
-   Creare una funzione nella DLL che chiama la funzione [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) per installare la routine di i/O.
-   Esportare questa funzione nel file delle definizioni dei moduli della DLL.

Per utilizzare la procedura di I/O condivisa, un'applicazione deve prima chiamare la funzione nella DLL per installare la procedura di I/O.

 

 