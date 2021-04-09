---
title: Metodo InkStart
description: I metodi InkStart, InkDraw e InkStop usano tutti costrutti GUI Win32, ad esempio contesti di dispositivo e oggetti penna.
ms.assetid: a639e1d2-6d81-472b-b639-d237e202020f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93e25d02c4490106180298b6977ec539bd96fd03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955707"
---
# <a name="inkstart-method"></a><span data-ttu-id="4fe18-103">Metodo InkStart</span><span class="sxs-lookup"><span data-stu-id="4fe18-103">InkStart Method</span></span>

<span data-ttu-id="4fe18-104">I metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**INKSTOP**](cguipaper-methods.md) usano tutti costrutti GUI Win32, ad esempio contesti di dispositivo e oggetti penna.</span><span class="sxs-lookup"><span data-stu-id="4fe18-104">**InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods all use Win32 GUI constructs such as device contexts and pen objects.</span></span> <span data-ttu-id="4fe18-105">Viene illustrato il motivo per cui CGuiPaper è necessario come livello separato di incapsulamento.</span><span class="sxs-lookup"><span data-stu-id="4fe18-105">This illustrates why CGuiPaper is needed as a separate level of encapsulation.</span></span> <span data-ttu-id="4fe18-106">Gli aspetti dell'interfaccia utente grafica del paper di disegno vengono gestiti in CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="4fe18-106">The GUI aspects of the drawing paper are handled in CGuiPaper.</span></span> <span data-ttu-id="4fe18-107">L'oggetto Copaper viene inviato solo ai dati di input penna.</span><span class="sxs-lookup"><span data-stu-id="4fe18-107">The COPaper object is sent only ink data.</span></span>

<span data-ttu-id="4fe18-108">Un altro motivo di progettazione per il livello di incapsulamento CGuiPaper è la doppia natura dei metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe18-108">Another design reason for the CGuiPaper level of encapsulation is the dual nature of its **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods.</span></span> <span data-ttu-id="4fe18-109">Non solo la chiamata a un documento per registrare i dati di input penna come si verificano, disegnano anche un'immagine visiva del disegno quando si verifica.</span><span class="sxs-lookup"><span data-stu-id="4fe18-109">They not only call on COPaper to record the ink data as it occurs, they also paint a visual image of the drawing as it occurs.</span></span> <span data-ttu-id="4fe18-110">CGuiPaper mantiene un \_ flag m bInkSaving per gestire questa duplice natura.</span><span class="sxs-lookup"><span data-stu-id="4fe18-110">CGuiPaper keeps an m\_bInkSaving flag to manage this dual nature.</span></span> <span data-ttu-id="4fe18-111">Quando m \_ bInkSaving è false, l'immagine viene disegnata sullo schermo, ma i dati non vengono inviati al documento per la registrazione.</span><span class="sxs-lookup"><span data-stu-id="4fe18-111">When m\_bInkSaving is FALSE, the image is drawn on screen but the data is not sent to COPaper for recording.</span></span>

<span data-ttu-id="4fe18-112">Questo schema viene utilizzato per il ridisegno quando l'utente non sta muovendo il mouse ma i dati di input penna del documento vengono inviati a CGuiPaper per il ridisegno automatico.</span><span class="sxs-lookup"><span data-stu-id="4fe18-112">This scheme is used in repainting when the user is not moving the mouse but COPaper's ink data is being resent to CGuiPaper for automatic repainting.</span></span> <span data-ttu-id="4fe18-113">CGuiPaper può essere indicato per impostare il flag m bInkSaving chiamando il \_ relativo metodo [**InkSaving**](cguipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe18-113">CGuiPaper can be told to set the m\_bInkSaving flag by calling its [**InkSaving**](cguipaper-methods.md) method.</span></span>

<span data-ttu-id="4fe18-114">I frammenti di codice di esempio seguenti illustrano i metodi **InkStart** di GUIPAPER. CPP E SINK. CPP.</span><span class="sxs-lookup"><span data-stu-id="4fe18-114">The following sample code snippets illustrate the **InkStart** methods of GUIPAPER.CPP AND SINK.CPP.</span></span>

## <a name="inkstart-method-guipapercpp"></a><span data-ttu-id="4fe18-115">Metodo InkStart (GUIPAPER. CPP</span><span class="sxs-lookup"><span data-stu-id="4fe18-115">InkStart Method (GUIPAPER.CPP)</span></span>


```C++
HRESULT CGuiPaper::InkStart(
                       SHORT nX,
                       SHORT nY)
  {
    HRESULT hr = E_FAIL;

    if (m_nLockKey || (!m_nLockKey && !m_bInkSaving))
    {
      // Start an ink drawing sequence only if one is not in progress.
      if (!m_bInking)
      {
        // Remember start position.
        m_OldPos.x = nX;
        m_OldPos.y = nY;

        // Delete old pen.
        if (m_hPen)
          DeleteObject(m_hPen);

        // Create and select the new drawing pen.
        m_hPen = CreatePen(PS_SOLID, m_nInkWidth, m_crInkColor);
        SelectObject(m_hDC, m_hPen);

        hr = NOERROR;

        // Ask the Paper object to mark the start of the ink drawing
        // sequence in the current ink color.
        if (m_pIPaper && m_bInkSaving)
        {
          hr = m_pIPaper->InkStart(
                            m_nLockKey,
                            nX,
                            nY,
                            m_nInkWidth,
                            m_crInkColor);
          // Capture the Mouse.
          SetCapture(m_hWnd);

          // We've modified the ink data--it is now "dirty" with
          // respect to the compound file image. Set dirty flag.
          m_bDirty = TRUE;
        }

        // Set inking flag to TRUE.
        m_bInking = TRUE;
      }
    }

    return hr;
  }
```



## <a name="inkstart-method-sinkcpp"></a><span data-ttu-id="4fe18-116">Metodo InkStart (SINK. CPP</span><span class="sxs-lookup"><span data-stu-id="4fe18-116">InkStart Method (SINK.CPP)</span></span>

<span data-ttu-id="4fe18-117">**StoClien** riceve i dati di disegno sotto forma di chiamate all'interfaccia **IPaperSink** connessa nell'oggetto COPaperSink.</span><span class="sxs-lookup"><span data-stu-id="4fe18-117">**StoClien** receives the drawing data in the form of calls to the connected **IPaperSink** interface in its COPaperSink object.</span></span> <span data-ttu-id="4fe18-118">Questi metodi corrispondono ai metodi **InkStart**, [**InkDraw**](inkdraw-method.md)e [**InkStop**](cguipaper-methods.md) simili in CGuiPaper.</span><span class="sxs-lookup"><span data-stu-id="4fe18-118">These methods correspond to the similar **InkStart**, [**InkDraw**](inkdraw-method.md), and [**InkStop**](cguipaper-methods.md) methods in CGuiPaper.</span></span>


```C++
STDMETHODIMP COPaperSink::CImpIPaperSink::InkStart(
                                              SHORT nX,
                                              SHORT nY,
                                              SHORT nWidth,
                                              COLORREF crInkColor)
  {
    // Turn off ink saving to the COPaper object.
    m_pBackObj->m_pGuiPaper->InkSaving(FALSE);

    // Play the data back to the CGuiPaper for display only.
    m_pBackObj->m_pGuiPaper->InkWidth(nWidth);
    m_pBackObj->m_pGuiPaper->InkColor(crInkColor);
    m_pBackObj->m_pGuiPaper->InkStart(nX, nY);

    return NOERROR;
  }
```



<span data-ttu-id="4fe18-119">Quando **InkStart** viene chiamato nel sink, chiama CGuiPaper per disattivare il salvataggio dell'input penna in un documento.</span><span class="sxs-lookup"><span data-stu-id="4fe18-119">When **InkStart** is called in the sink, it calls CGuiPaper to turn off ink saving to COPaper.</span></span> <span data-ttu-id="4fe18-120">Non è necessario che il documento riceva una copia con echi dei dati inviati.</span><span class="sxs-lookup"><span data-stu-id="4fe18-120">COPaper does not need to receive an echoed copy of the data it is sending.</span></span> <span data-ttu-id="4fe18-121">Quando [**InkDraw**](inkdraw-method.md) viene chiamato nel sink, passa semplicemente la chiamata a **CGuiPaper:: InkDraw**.</span><span class="sxs-lookup"><span data-stu-id="4fe18-121">When [**InkDraw**](inkdraw-method.md) is called in the sink, it simply passes the call on to **CGuiPaper::InkDraw**.</span></span> <span data-ttu-id="4fe18-122">Quando [**InkStop**](cguipaper-methods.md) viene chiamato nel sink, viene chiamato CGuiPaper per riattivare l'input penna.</span><span class="sxs-lookup"><span data-stu-id="4fe18-122">When [**InkStop**](cguipaper-methods.md) is called in the sink, CGuiPaper is called to turn ink saving back on.</span></span> <span data-ttu-id="4fe18-123">Il risultato è la riproduzione dei dati dell'input penna di un documento in CGuiPaper solo per la visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="4fe18-123">The result is a playback of COPaper's ink data to CGuiPaper for display only.</span></span>

<span data-ttu-id="4fe18-124">È possibile testare il comportamento di **StoClien** quando il relativo **IPaperSink** è disconnesso scegliendo l'opzione Disconnetti dal menu sink.</span><span class="sxs-lookup"><span data-stu-id="4fe18-124">You can test the behavior of **StoClien** when its **IPaperSink** is disconnected by choosing the Disconnect choice on the Sink menu.</span></span> <span data-ttu-id="4fe18-125">Come esperimento, dopo la disconnessione del sink scegliere About dal menu?.</span><span class="sxs-lookup"><span data-stu-id="4fe18-125">As an experiment, after disconnecting the sink, choose About from the Help menu.</span></span> <span data-ttu-id="4fe18-126">Verrà visualizzata la finestra di dialogo informazioni su, che coprirà parte del disegno di **StoClien**.</span><span class="sxs-lookup"><span data-stu-id="4fe18-126">This will show the About dialog box, which will cover part of the **StoClien**'s drawing.</span></span> <span data-ttu-id="4fe18-127">Fare clic su OK nella finestra di dialogo informazioni su.</span><span class="sxs-lookup"><span data-stu-id="4fe18-127">Click OK in the About dialog box.</span></span> <span data-ttu-id="4fe18-128">Si noti che la parte del disegno che è stata analizzata è ora finita.</span><span class="sxs-lookup"><span data-stu-id="4fe18-128">Notice that the portion of the drawing that was covered is now gone.</span></span> <span data-ttu-id="4fe18-129">I dati di disegno non vengono persi, ma parte dell'immagine è.</span><span class="sxs-lookup"><span data-stu-id="4fe18-129">The drawing data is not lost, but part of the image is.</span></span> <span data-ttu-id="4fe18-130">Il client ha ricevuto il \_ messaggio di disegno WM ed ha emesso il metodo [**iPaper:: redisegna**](ipaper--redraw.md) .</span><span class="sxs-lookup"><span data-stu-id="4fe18-130">The client received the WM\_PAINT message and issued the [**IPaper::Redraw**](ipaper--redraw.md) method.</span></span> <span data-ttu-id="4fe18-131">Tuttavia, poiché il sink non era connesso, non ha ricevuto le chiamate **IPaperSink** per ridisegnare il disegno.</span><span class="sxs-lookup"><span data-stu-id="4fe18-131">But because the sink was not connected, it did not receive the **IPaperSink** calls to repaint the drawing.</span></span>

<span data-ttu-id="4fe18-132">È anche possibile testare questo comportamento riducendo al minimo **StoClien** e quindi ripristinarlo.</span><span class="sxs-lookup"><span data-stu-id="4fe18-132">You can also test this behavior by minimizing **StoClien** and then restoring it.</span></span> <span data-ttu-id="4fe18-133">In questo caso, l'intera immagine del disegno viene persa e deve essere ridisegnata.</span><span class="sxs-lookup"><span data-stu-id="4fe18-133">In this case, the entire drawing image is lost and needs repainting.</span></span> <span data-ttu-id="4fe18-134">Per ridisegnare l'immagine del disegno dopo uno di questi test, utilizzare il menu sink per riconnettersi, quindi scegliere [**ridisegna**](ipaper--redraw.md) dal menu Disegna.</span><span class="sxs-lookup"><span data-stu-id="4fe18-134">To repaint the drawing image after either of these tests, use the Sink menu to reconnect, and then choose [**Redraw**](ipaper--redraw.md) from the Draw menu.</span></span>

 

 




