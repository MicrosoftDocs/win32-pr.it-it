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
# <a name="installing-custom-io-procedures"></a><span data-ttu-id="b5ace-110">Installazione di procedure di I/O personalizzate</span><span class="sxs-lookup"><span data-stu-id="b5ace-110">Installing Custom I/O Procedures</span></span>

<span data-ttu-id="b5ace-111">Per installare una routine di I/O associata a. Estensione del nome file ARC, usare la funzione [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) come segue:</span><span class="sxs-lookup"><span data-stu-id="b5ace-111">To install an I/O procedure associated with the .ARC filename extension, use the [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) function as follows:</span></span>


```C++
mmioInstallIOProc (mmioFOURCC('A', 'R', 'C', ' '), 
    (LPMMIOPROC)lpmmioproc, MMIO_INSTALLPROC); 
```



<span data-ttu-id="b5ace-112">Quando si installa una procedura di I/O tramite [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), la procedura rimane installata finché non viene rimossa.</span><span class="sxs-lookup"><span data-stu-id="b5ace-112">When you install an I/O procedure using [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc), the procedure remains installed until you remove it.</span></span> <span data-ttu-id="b5ace-113">La procedura di I/O viene utilizzata per tutti i file aperti purché il file abbia l'estensione del nome file appropriata.</span><span class="sxs-lookup"><span data-stu-id="b5ace-113">The I/O procedure is used for any file you open as long as the file has the appropriate filename extension.</span></span>

<span data-ttu-id="b5ace-114">È anche possibile installare temporaneamente una routine di I/O tramite la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) .</span><span class="sxs-lookup"><span data-stu-id="b5ace-114">You can also temporarily install an I/O procedure by using the [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) function.</span></span> <span data-ttu-id="b5ace-115">In questo caso, la procedura di I/O viene utilizzata solo con un file aperto utilizzando **mmioOpen** e viene rimosso quando il file viene chiuso utilizzando la funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) .</span><span class="sxs-lookup"><span data-stu-id="b5ace-115">In this case, the I/O procedure is used only with a file opened by using **mmioOpen** and is removed when the file is closed by using the [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) function.</span></span> <span data-ttu-id="b5ace-116">Per specificare una routine di I/O quando si apre un file usando **mmioOpen**, usare il parametro *lpmmioinfo* per fare riferimento a una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="b5ace-116">To specify an I/O procedure when you open a file by using **mmioOpen**, use the *lpmmioinfo* parameter to reference an [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) structure as follows:</span></span>

1.  <span data-ttu-id="b5ace-117">Impostare il membro **fccIOProc** su **null**.</span><span class="sxs-lookup"><span data-stu-id="b5ace-117">Set the **fccIOProc** member to **NULL**.</span></span>
2.  <span data-ttu-id="b5ace-118">Impostare il membro **pIOProc** sull'indirizzo dell'istanza di routine della procedura di i/O.</span><span class="sxs-lookup"><span data-stu-id="b5ace-118">Set the **pIOProc** member to the procedure-instance address of the I/O procedure.</span></span>
3.  <span data-ttu-id="b5ace-119">Impostare tutti gli altri membri su zero (a meno che non si stia aprendo un file di memoria o leggendo o scrivendo direttamente nel buffer di I/O di file).</span><span class="sxs-lookup"><span data-stu-id="b5ace-119">Set all other members to zero (unless you are opening a memory file, or directly reading or writing to the file I/O buffer).</span></span>

<span data-ttu-id="b5ace-120">Assicurarsi di rimuovere tutte le procedure di I/O installate prima di uscire dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b5ace-120">Be sure to remove any I/O procedures you have installed before you exit your application.</span></span>

 

 