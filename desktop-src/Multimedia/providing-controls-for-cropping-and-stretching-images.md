---
title: Fornire controlli per il ritaglio e l'allungamento delle immagini
description: Fornire controlli per il ritaglio e l'allungamento delle immagini
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- MCIWndGetSource (macro)
- MCIWndPutSource (macro)
- MCIWndGetDest (macro)
- MCIWndPutDest (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd0889b40204e7c99ec782e454dba2cdeebfe79
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724810"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Fornire controlli per il ritaglio e l'allungamento delle immagini

MCIWnd consente di ritagliare e allungare le immagini di un clip video. Per comprendere queste funzionalità, è necessario comprendere le relazioni tra le *dimensioni del frame*, il *rettangolo di origine*, il rettangolo di *destinazione* e l' *area di riproduzione*.

Un clip video è costituito da diversi frame, ognuno dei quali contiene un'immagine. La dimensione del fotogramma di un clip video corrisponde alla dimensione dell'immagine nel frame corrente. In genere, un clip video ha una dimensione del fotogramma, perché tutte le immagini nella clip hanno le stesse dimensioni.

Il rettangolo di origine è un'area rettangolare che sovrappone i frame di un clip video. Il rettangolo di origine definisce la parte di ogni frame visualizzata durante la riproduzione. Quando un clip video viene caricato con MCIWnd, il rettangolo di origine viene inizializzato con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

Il rettangolo di destinazione è un'area rettangolare che definisce una finestra di riproduzione virtuale. Il rettangolo di destinazione riceve i dati dell'immagine dal rettangolo di origine per ogni fotogramma del clip video. Quando le dimensioni del rettangolo di origine e di destinazione sono diverse, MCIWnd regola orizzontalmente e verticalmente i dati dell'immagine in base alle esigenze per riempire il rettangolo di destinazione. Quando un clip video viene caricato con MCIWnd, il rettangolo di destinazione viene inizializzato con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

L'area di riproduzione è la parte di una finestra MCIWnd utilizzata da un'applicazione per visualizzare il clip video. L'area di riproduzione è l'area client di una finestra MCIWnd o la parte dell'area client che esclude la barra degli strumenti MCIWnd. Quando un clip video viene caricato con MCIWnd, l'area di riproduzione viene inizializzata con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

È possibile ritagliare un clip video usando le macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) e [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) per modificare il rettangolo di origine. Il ritaglio di un'immagine determina solo la parte dei frame che vengono visualizzati durante la riproduzione. non modifica il contenuto del file riprodotto. Prima di ritagliare un'immagine, è possibile recuperare le dimensioni correnti del rettangolo di origine usando **MCIWndGetSource**. Una volta calcolate le nuove dimensioni e la posizione del rettangolo di origine, è possibile impostare i limiti di ritaglio del rettangolo di origine utilizzando **MCIWndPutSource**.

È possibile estendere un clip video usando le macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) e [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) per modificare il rettangolo di destinazione. Quando si allunga un clip video, si allunga o si abbreviano le dimensioni del frame di un clip video verticalmente, orizzontalmente o in entrambe le direzioni. Prima di estendere un'immagine, è possibile recuperare le dimensioni e la posizione correnti del rettangolo di destinazione usando **MCIWndGetDest**. La macro **MCIWndPutDest** consente di ridefinire il rettangolo di destinazione. L'estensione può comtorcere l'immagine durante la riproduzione, ma non modifica il contenuto del file riprodotto.

Se le dimensioni del rettangolo di destinazione diventano maggiori dell'area di riproduzione, è possibile specificare quale parte dell'area di riproduzione visualizzerà il clip video usando **MCIWndPutDest**.

> [!Note]  
> La macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) non modifica le dimensioni dell'area di riproduzione. Per estendere la finestra MCIWnd insieme al rettangolo di destinazione, è necessario ottenere informazioni sulle dimensioni correnti della finestra MCIWnd e rilasciare nuove dimensioni della finestra in base al rettangolo di destinazione. È possibile recuperare le dimensioni della finestra MCIWnd usando la funzione [GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) e ridimensionare la finestra MCIWnd usando la funzione [SetWindowPos](/windows/win32/api/winuser/nf-winuser-setwindowpos) .

 

 

 