---
title: Fornire controlli per il ritaglio e l'estensione delle immagini
description: Fornire controlli per il ritaglio e l'estensione delle immagini
ms.assetid: cc62d70d-3f5f-477c-bc09-ab8ab0a9dce3
keywords:
- Macro MCIWndGetSource
- Macro MCIWndPutSource
- Macro MCIWndGetDest
- Macro MCIWndPutDest
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dddf0d022b63bccb3c64157df796585569b72604dc82746417d725c4135dd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805751"
---
# <a name="providing-controls-for-cropping-and-stretching-images"></a>Fornire controlli per il ritaglio e l'estensione delle immagini

MCIWnd consente di ritagliare ed estendere le immagini di un clip video. Per comprendere queste funzionalità, è necessario comprendere le relazioni tra le dimensioni del *frame,* il rettangolo di *origine,* il rettangolo *di destinazione* e l'area *di riproduzione.*

Un clip video è costituito da diversi fotogrammi, ognuno dei quali contiene un'immagine. Le dimensioni del fotogramma di un clip video sono le dimensioni dell'immagine nel fotogramma corrente. In genere, un clip video ha una dimensione di fotogramma perché tutte le immagini nel clip hanno le stesse dimensioni.

Il rettangolo di origine è un'area rettangolare che sovrappone i fotogrammi di un clip video. Il rettangolo di origine definisce la parte di ogni fotogramma visualizzata durante la riproduzione. Quando un clip video viene caricato con MCIWnd, il rettangolo di origine viene inizializzato con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

Il rettangolo di destinazione è un'area rettangolare che definisce una finestra di riproduzione virtuale. Il rettangolo di destinazione riceve i dati dell'immagine dal rettangolo di origine per ogni fotogramma del clip video. Quando le dimensioni del rettangolo di origine e di destinazione sono diverse, MCIWnd regola i dati dell'immagine orizzontalmente e verticalmente in base alle esigenze per riempire il rettangolo di destinazione. Quando un clip video viene caricato con MCIWnd, il rettangolo di destinazione viene inizializzato con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

L'area di riproduzione è la parte di una finestra MCIWnd utilizzata da un'applicazione per visualizzare il clip video. L'area di riproduzione è l'area client di una finestra MCIWnd o la parte dell'area client che esclude la barra degli strumenti MCIWnd. Quando un clip video viene caricato con MCIWnd, l'area di riproduzione viene inizializzata con le stesse dimensioni e la stessa posizione del fotogramma iniziale del clip video.

È possibile ritagliare un clip video usando le macro [**MCIWndGetSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetsource) e [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) per modificare il rettangolo di origine. Il ritaglio di un'immagine determina solo la parte dei fotogrammi da visualizzare durante la riproduzione. non modifica il contenuto del file riprodotto. Prima di ritagliare un'immagine, è possibile recuperare le dimensioni correnti del rettangolo di origine usando **MCIWndGetSource.** Dopo aver calcolato le nuove dimensioni e posizione del rettangolo di origine, è possibile impostare i limiti di ritaglio del rettangolo di origine usando **MCIWndPutSource**.

È possibile estendere un clip video usando le macro [**MCIWndGetDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdest) e [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) per modificare il rettangolo di destinazione. Quando si estende un clip video, si allungano o si riducono le dimensioni del fotogramma di un clip video verticalmente, orizzontalmente o in entrambe le direzioni. Prima di estendere un'immagine, è possibile recuperare le dimensioni e la posizione correnti del rettangolo di destinazione usando **MCIWndGetDest.** La macro **MCIWndPutDest** consente di ridefinire il rettangolo di destinazione. L'estensione può distorcere l'immagine durante la riproduzione, ma non modifica il contenuto del file riprodotto.

Se le dimensioni del rettangolo di destinazione diventano maggiori dell'area di riproduzione, è possibile specificare quale parte dell'area di riproduzione visualizza il clip video usando **MCIWndPutDest.**

> [!Note]  
> La macro [**MCIWndPutDest**](/windows/desktop/api/Vfw/nf-vfw-mciwndputdest) non modifica le dimensioni dell'area di riproduzione. Per estendere la finestra MCIWnd insieme al rettangolo di destinazione, è necessario conoscere le dimensioni correnti della finestra MCIWnd ed eseguire nuove dimensioni della finestra in base al rettangolo di destinazione. È possibile recuperare le dimensioni della finestra MCIWnd usando la [funzione GetWindowRect](/windows/win32/api/winuser/nf-winuser-getwindowrect) e ridimensionare la finestra MCIWnd usando la [funzione SetWindowPos.](/windows/win32/api/winuser/nf-winuser-setwindowpos)

 

 

 