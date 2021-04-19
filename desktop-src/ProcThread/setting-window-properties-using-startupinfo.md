---
description: Un processo padre può specificare le proprietà associate alla finestra principale del processo figlio.
ms.assetid: 12547da4-8d41-48c5-8efc-f0423f64caa7
title: Impostazione delle proprietà della finestra mediante STARTUPINFO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ff59f9ae4473174325880a863f5b1f2fc4203e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311956"
---
# <a name="setting-window-properties-using-startupinfo"></a>Impostazione delle proprietà della finestra mediante STARTUPINFO

Un processo padre può specificare le proprietà associate alla finestra principale del processo figlio. La funzione [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) accetta un puntatore a una struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) come uno dei relativi parametri. Usare i membri di questa struttura per specificare le caratteristiche della finestra principale del processo figlio. Il membro **dwFlags** contiene un bit che determina quali altri membri della struttura vengono utilizzati. In questo modo è possibile specificare i valori per qualsiasi subset delle proprietà della finestra. Il sistema usa i valori predefiniti per le proprietà non specificate. Il membro **dwFlags** può anche forzare la visualizzazione di un cursore dei commenti durante l'inizializzazione del nuovo processo.

Per i processi GUI, la struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) specifica i valori predefiniti da usare la prima volta che il nuovo processo chiama le funzioni [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) e [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) per creare e visualizzare una finestra sovrapposta. È possibile specificare i valori predefiniti seguenti:

-   Larghezza e altezza, in pixel, della finestra creata da [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Posizione, in coordinate dello schermo della finestra creata da [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa).
-   Parametro *nCmdShow* di [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow).

Per i processi della console, usare la struttura [**STARTUPINFO**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-startupinfoa) per specificare le proprietà della finestra solo quando si crea una nuova console (usando [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) con Create \_ New \_ console o con la funzione [**AllocConsole**](/windows/console/allocconsole) ). La struttura **STARTUPINFO** può essere usata per specificare le proprietà della finestra della console seguenti:

-   Dimensioni della nuova finestra della console, in celle di tipo carattere.
-   Posizione della nuova finestra della console, in coordinate dello schermo.
-   Dimensioni, in celle di tipo carattere, del buffer dello schermo della nuova console.
-   Attributi del colore di sfondo e di testo del buffer dello schermo della nuova console.
-   Titolo della finestra della nuova console.

 

 
