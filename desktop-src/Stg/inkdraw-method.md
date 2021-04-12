---
title: Metodo InkDraw
description: CGuiPaper mantiene anche un \_ flag m bInking. InkStart lo imposta su TRUE per segnalare che una sequenza di disegno è in corso. Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati di input penna.
ms.assetid: 0fe9d029-1522-4caf-8efb-0a4eb2b59958
keywords:
- InkDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41973d3f8560f25a81ac1deb782bada51b015239
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396535"
---
# <a name="inkdraw-method"></a><span data-ttu-id="522ad-106">Metodo InkDraw</span><span class="sxs-lookup"><span data-stu-id="522ad-106">InkDraw Method</span></span>

<span data-ttu-id="522ad-107">CGuiPaper mantiene anche un \_ flag m bInking.</span><span class="sxs-lookup"><span data-stu-id="522ad-107">CGuiPaper also keeps an m\_bInking flag.</span></span> <span data-ttu-id="522ad-108">[InkStart](inkstart-method.md) lo imposta su **true** per segnalare che una sequenza di disegno è in corso.</span><span class="sxs-lookup"><span data-stu-id="522ad-108">[InkStart](inkstart-method.md) sets it to **TRUE** to signal that a drawing sequence is in process.</span></span> <span data-ttu-id="522ad-109">Ad esempio, il metodo InkDraw usa questo flag per determinare se deve disegnare e salvare i dati di input penna.</span><span class="sxs-lookup"><span data-stu-id="522ad-109">For example, the InkDraw method uses this flag to determine whether it should paint and save ink data.</span></span>

<span data-ttu-id="522ad-110">Di seguito è riportato il metodo InkDraw di GUIPAPER. CPP.</span><span class="sxs-lookup"><span data-stu-id="522ad-110">The following is the InkDraw method from GUIPAPER.CPP.</span></span>


```C++
HRESULT CGuiPaper::InkDraw(
                       SHORT nX,
                       SHORT nY)
  {
    if (m_bInking)
    {
      // Start this ink line at previous old position.
      MoveToEx(m_hDC, m_OldPos.x, m_OldPos.y, NULL);

      // Assign new old position and draw the new line.
      LineTo(m_hDC, m_OldPos.x = nX, m_OldPos.y = nY);

      // Ask the Paper object to save this data.
      if (m_bInkSaving)
        m_pIPaper->InkDraw(m_nLockKey, nX, nY);
    }

    return NOERROR;
  }
```



<span data-ttu-id="522ad-111">Questo metodo non esegue alcuna operazione se m \_ bInking è **false**.</span><span class="sxs-lookup"><span data-stu-id="522ad-111">This method does nothing if m\_bInking is **FALSE**.</span></span> <span data-ttu-id="522ad-112">Questa condizione si verifica quando l'utente passa semplicemente il puntatore del mouse sulla finestra del client senza premere il pulsante sinistro del mouse.</span><span class="sxs-lookup"><span data-stu-id="522ad-112">This is the condition when the user is simply moving the mouse over the client window without pressing the left mouse button.</span></span>

<span data-ttu-id="522ad-113">InkDraw ha chiaramente una duplice responsabilità.</span><span class="sxs-lookup"><span data-stu-id="522ad-113">InkDraw clearly has a dual responsibility.</span></span> <span data-ttu-id="522ad-114">Le chiamate Win32 MoveToEx e LineTo vengono effettuate per creare immagini linea sulla schermata GUI (usando l'handle del contesto di dispositivo mantenuto in m \_ HDC).</span><span class="sxs-lookup"><span data-stu-id="522ad-114">The Win32 MoveToEx and LineTo calls are made to draw line images on the GUI screen (using the device context handle kept in m\_hDC).</span></span> <span data-ttu-id="522ad-115">I dati Ink vengono anche passati all'oggetto Copaper per la registrazione tramite il metodo InkDraw dell'interfaccia [iPaper](ipaper-methods.md) .</span><span class="sxs-lookup"><span data-stu-id="522ad-115">The ink data is also passed to the COPaper object for recording using the [IPaper](ipaper-methods.md) interface's InkDraw method.</span></span> <span data-ttu-id="522ad-116">Quando m \_ bInkSaving è **false**, InkDraw disegna l'immagine della linea, ma non archivia i dati in un documento.</span><span class="sxs-lookup"><span data-stu-id="522ad-116">When m\_bInkSaving is **FALSE**, InkDraw paints the line image but does not store the data in COPaper.</span></span> <span data-ttu-id="522ad-117">Questa condizione viene utilizzata durante il ridisegno.</span><span class="sxs-lookup"><span data-stu-id="522ad-117">This condition is used during repainting.</span></span>

 

 




