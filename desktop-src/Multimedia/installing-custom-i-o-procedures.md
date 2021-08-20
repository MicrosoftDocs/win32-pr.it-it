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
- Funzione mmioInstallIOProc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ec92542efe80c24e1e620983d78b4b9a6c246ff003934a1ace1cae159fbd1da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140466"
---
# <a name="installing-custom-io-procedures"></a>Installazione di procedure di I/O personalizzate

Per installare una procedura di I/O associata a . ESTENSIONE ARC, usare la [**funzione mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) come indicato di seguito:


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



Quando si installa una procedura di I/O usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), la procedura rimane installata fino a quando non viene rimosso. La procedura di I/O viene usata per qualsiasi file aperto, purché il file abbia l'estensione di file appropriata.

È anche possibile installare temporaneamente una procedura di I/O usando la funzione [**mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) In questo caso, la procedura di I/O viene usata solo con un file aperto tramite **mmioOpen** e viene rimossa quando il file viene chiuso tramite la funzione [**mmioClose.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) Per specificare una procedura di I/O quando si apre un file usando **mmioOpen,** usare il *parametro lpmmioinfo* per fare riferimento a una [**struttura MMIOINFO**](/previous-versions//dd757322(v=vs.85)) come indicato di seguito:

1.  Impostare il **membro fccIOProc** su **NULL.**
2.  Impostare il **membro pIOProc** sull'indirizzo dell'istanza della procedura di I/O.
3.  Impostare tutti gli altri membri su zero ,a meno che non si aperi un file di memoria o non si leggono o si scrivono direttamente nel buffer di I/O del file.

Assicurarsi di rimuovere tutte le procedure di I/O installate prima di uscire dall'applicazione.

 

 