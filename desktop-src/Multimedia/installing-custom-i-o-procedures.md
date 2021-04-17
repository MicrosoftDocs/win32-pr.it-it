---
title: Installazione di procedure di I/O personalizzate
description: Installazione di procedure di I/O personalizzate
ms.assetid: 7b26a062-fa52-4de3-b8c8-b9f9167068fc
keywords:
- I/O di file multimediali, procedure personalizzate
- I/O di file, procedure personalizzate
- input e output (I/O), procedure personalizzate
- I/O (input e output), procedure personalizzate
- installazione di procedure di I/O personalizzate
- I/O personalizzato
- mmioInstallIOProc (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1574b7076e7344fa8e800ef1f18ad13fcfd3f3af
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104399015"
---
# <a name="installing-custom-io-procedures"></a>Installazione di procedure di I/O personalizzate

Per installare una routine di I/O associata a. Estensione del nome file ARC, usare la funzione [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) come segue:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Quando si installa una procedura di I/O tramite [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), la procedura rimane installata finché non viene rimossa. La procedura di I/O viene utilizzata per tutti i file aperti purché il file abbia l'estensione del nome file appropriata.

È anche possibile installare temporaneamente una routine di I/O tramite la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . In questo caso, la procedura di I/O viene utilizzata solo con un file aperto utilizzando **mmioOpen** e viene rimosso quando il file viene chiuso utilizzando la funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) . Per specificare una routine di I/O quando si apre un file usando **mmioOpen**, usare il parametro *lpmmioinfo* per fare riferimento a una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) come indicato di seguito:

1.  Impostare il membro **fccIOProc** su **null**.
2.  Impostare il membro **pIOProc** sull'indirizzo dell'istanza di routine della procedura di i/O.
3.  Impostare tutti gli altri membri su zero (a meno che non si stia aprendo un file di memoria o leggendo o scrivendo direttamente nel buffer di I/O di file).

Assicurarsi di rimuovere tutte le procedure di I/O installate prima di uscire dall'applicazione.

 

 