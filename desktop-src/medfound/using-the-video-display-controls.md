---
description: Uso dei controlli schermo video
ms.assetid: 09501d67-effb-41ce-a7b7-d2415acdf3ac
title: Uso dei controlli schermo video
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbb9c83485faebc873b3e92502122c5497b4bb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753826"
---
# <a name="using-the-video-display-controls"></a>Uso dei controlli schermo video

L'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) controlla il modo in cui il renderer video avanzato (EVR) Visualizza il video all'interno di una finestra dell'applicazione. Questa interfaccia può essere utilizzata sia in DirectShow che in Media Foundation. Internamente, i controlli schermo video sono forniti dal Presenter predefinito di EVR. Se si scrive un presentatore personalizzato, è possibile specificare la stessa interfaccia o definire un'interfaccia personalizzata.

Il modo corretto per ottenere un puntatore all'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) varia a seconda che si usi la versione DIRECTSHOW di EVR o la versione Media Foundation. Per il Media Foundation EVR, dipende anche dal fatto che il EVR venga usato direttamente o usato attraverso la sessione multimediale, che è più comune.

Per ottenere un puntatore all'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) , eseguire le operazioni seguenti:

1.  Ottenere un puntatore all'interfaccia [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .

    -   Se si usa il filtro EVR DirectShow, chiamare **QueryInterface** sul filtro.

    -   Se si usa direttamente il sink di supporto EVR, chiamare **QueryInterface** sul sink multimediale.

    -   Se si usa la sessione multimediale, chiamare **QueryInterface** nella sessione multimediale.

2.  Se si usa la sessione multimediale, attendere che la sessione multimediale invii l'evento [MESessionTopologyStatus](mesessiontopologystatus.md) con un valore di stato MF \_ TOPOSTATUS \_ Ready. Ignorare questo passaggio in caso contrario.

3.  Chiamare [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) per ottenere l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) . L'identificatore del servizio è \_ il \_ servizio di rendering video \_ .

È possibile utilizzare l'interfaccia [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) per eseguire le attività seguenti:

-   Impostare la finestra di ridimensionamento.

-   Impostare i rettangoli di origine e di destinazione.

-   Aggiornare la finestra video in risposta ai messaggi della finestra.

-   Abilitare o disabilitare la modalità schermo intero.

## <a name="clipping-window"></a>Finestra di ritaglio

L'applicazione deve fornire una finestra in cui EVR disegna il video. Per impostare la finestra di ridimensionamento, chiamare [**IMFVideoDisplayControl:: SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) con un handle per la finestra dell'applicazione.

Se si crea il sink del supporto EVR tramite il relativo oggetto Activation, questo passaggio non è necessario. L'oggetto Activation chiama automaticamente [**SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow), usando l'handle della finestra fornito nella funzione [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .

## <a name="source-and-destination-rectangles"></a>Rettangoli di origine e di destinazione

Durante la riproduzione, il Presenter acquisisce una parte dell'immagine video composita e la disegna su un'area della finestra video. La parte dell'immagine composita è il *rettangolo di origine* e l'area della finestra video è il rettangolo di *destinazione*.

Il rettangolo di origine viene definito usando le coordinate normalizzate in cui il punto (0,0, 0,0) corrisponde all'angolo superiore sinistro del video e (1,0, 1,0) corrisponde all'angolo inferiore destro del video. Il rettangolo di origine può essere qualsiasi area all'interno di questo rettangolo. Il rettangolo di destinazione viene specificato in pixel rispetto all'area client della finestra. Il rettangolo di origine predefinito è l'intera immagine e il rettangolo di destinazione predefinito è un rettangolo vuoto.

Per impostare i rettangoli di origine e di destinazione, chiamare [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Se si crea il sink del supporto EVR tramite il relativo oggetto Activation, questo passaggio non è necessario. L'oggetto Activation imposta automaticamente il rettangolo di destinazione uguale all'intera area client della finestra. Tuttavia, è necessario chiamare [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) se si desidera modificare il rettangolo di origine o impostare un rettangolo di destinazione diverso.

## <a name="window-messages"></a>Messaggi finestra

Durante la riproduzione, l'applicazione deve rispondere a determinati messaggi della finestra, come indicato di seguito:

-   \_Disegno WM: chiamare [**IMFVideoDisplayControl:: RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) per ridisegnare il video. Evitare inoltre di disegnare sul rettangolo di destinazione durante la riproduzione del video, perché ciò può causare lo sfarfallio.

-   \_Dimensioni WM: potrebbe essere necessario chiamare [**SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) per ridimensionare il rettangolo di destinazione.

Diversamente dal filtro VMR (video Mixing Renderer) in DirectShow, non è necessario inviare una notifica al EVR quando si riceve un messaggio WM \_ DISPLAYCHANGE.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Renderer video migliorato](enhanced-video-renderer.md)
</dt> </dl>

 

 



