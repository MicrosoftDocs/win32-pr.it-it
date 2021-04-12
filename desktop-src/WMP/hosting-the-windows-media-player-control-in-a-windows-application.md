---
title: Hosting del controllo Media Player Windows in un'applicazione Windows
description: Hosting del controllo Media Player Windows in un'applicazione Windows
ms.assetid: 8da04160-b9db-4082-aeff-b0107189e33e
keywords:
- Windows Media Player, incorporamento del controllo ActiveX
- Modello a oggetti di Windows Media Player, incorporamento del controllo ActiveX
- modello a oggetti, incorporamento del controllo ActiveX
- Windows Media Player Mobile, incorporamento del controllo ActiveX
- Controllo ActiveX di Windows Media Player, incorporamento
- Controllo ActiveX Windows Media Player Mobile, incorporamento
- Controllo ActiveX, incorporamento
- Windows Media Player, programmi basati su Windows
- Modello a oggetti di Windows Media Player, programmi basati su Windows
- modello a oggetti, programmi basati su Windows
- Windows Media Player Mobile, programmi basati su Windows
- Controllo ActiveX di Windows Media Player, programmi basati su Windows
- Controllo ActiveX Windows Media Player Mobile, programmi basati su Windows
- Controllo ActiveX, programmi basati su Windows
- Incorporamento di programmi basati su Windows
- incorporamento, programmi basati su Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2190f0d0076fe3253c39f583ae7d2c197f8cb11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331452"
---
# <a name="hosting-the-windows-media-player-control-in-a-windows-application"></a><span data-ttu-id="723cb-119">Hosting del controllo Media Player Windows in un'applicazione Windows</span><span class="sxs-lookup"><span data-stu-id="723cb-119">Hosting the Windows Media Player Control in a Windows Application</span></span>

<span data-ttu-id="723cb-120">Per utilizzare il controllo ActiveX di Windows Media Player (inclusa l'interfaccia utente) in un programma basato su Windows, è necessario specificare un contenitore di controlli ActiveX.</span><span class="sxs-lookup"><span data-stu-id="723cb-120">To use the Windows Media Player ActiveX control (including the user interface) in a Windows-based program, you must provide an ActiveX control container.</span></span> <span data-ttu-id="723cb-121">ATL fornisce la classe **CAxWindow** per fornire la funzionalità della finestra host ActiveX.</span><span class="sxs-lookup"><span data-stu-id="723cb-121">ATL provides the **CAxWindow** class to provide ActiveX host window functionality.</span></span>

<span data-ttu-id="723cb-122">Per ospitare il controllo Media Player Windows utilizzando la classe **CAxWindow** , attenersi alla seguente procedura:</span><span class="sxs-lookup"><span data-stu-id="723cb-122">To host the Windows Media Player control using the **CAxWindow** class, follow these steps:</span></span>

1.  <span data-ttu-id="723cb-123">Includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="723cb-123">Include the following headers:</span></span>
    ```C++
    #include "wmp.h"
    #include <atlbase.h>
    #include <atlcom.h>
    #include <atlhost.h>
    #include <atlctl.h>
    ```

    

2.  <span data-ttu-id="723cb-124">Dichiarare le variabili membro, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="723cb-124">Declare member variables, as follows:</span></span>
    ```C++
    CAxWindow  m_wndView;  // ActiveX host window class.
    CComPtr<IWMPPlayer>  m_spWMPPlayer;  // Smart pointer to IWMPPlayer interface.
    
    ```

    

3.  <span data-ttu-id="723cb-125">Quando viene creata la finestra dell'applicazione, chiamare **AtlAxWinInit**, che è necessario quando si utilizza la finestra host ActiveX ATL.</span><span class="sxs-lookup"><span data-stu-id="723cb-125">When your application window is created, call **AtlAxWinInit**, which is required when using the ATL ActiveX host window.</span></span>
    ```C++
    AtlAxWinInit();
    
    ```

    

4.  <span data-ttu-id="723cb-126">Dichiarare le variabili locali per i codici restituiti e per contenere il puntatore all'interfaccia della finestra host:</span><span class="sxs-lookup"><span data-stu-id="723cb-126">Declare local variables for return codes and to contain the pointer to the host window interface:</span></span>
    ```C++
    CComPtr<IAxWinHostWindow>  spHost;
    HRESULT  hr;
    
    ```

    

5.  <span data-ttu-id="723cb-127">Creare la finestra host:</span><span class="sxs-lookup"><span data-stu-id="723cb-127">Create the host window:</span></span>
    ```C++
    GetClientRect(&rcClient);
    m_wndView.Create(m_hWnd, rcClient, NULL, WS_CHILD | WS_VISIBLE | WS_CLIPCHILDREN, WS_EX_CLIENTEDGE);
    
    ```

    

6.  <span data-ttu-id="723cb-128">Recuperare il puntatore all'interfaccia della finestra host:</span><span class="sxs-lookup"><span data-stu-id="723cb-128">Retrieve the host window interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryHost(&spHost);
    
    ```

    

7.  <span data-ttu-id="723cb-129">Creare il controllo Media Player Windows nella finestra host usando l'ID classe:</span><span class="sxs-lookup"><span data-stu-id="723cb-129">Create the Windows Media Player control in the host window using the class ID:</span></span>
    ```C++
    hr = spHost->CreateControl(CComBSTR(_T("{6BF52A52-394A-11d3-B153-00C04F79FAA6}")), m_wndView, 0);
    
    ```

    

8.  <span data-ttu-id="723cb-130">Recuperare il puntatore all'interfaccia **IWMPPlayer** :</span><span class="sxs-lookup"><span data-stu-id="723cb-130">Retrieve the **IWMPPlayer** interface pointer:</span></span>
    ```C++
    hr = m_wndView.QueryControl(&m_spWMPPlayer);
    
    ```

    

<span data-ttu-id="723cb-131">Quando si scrive codice personalizzato, assicurarsi di controllare ogni codice restituito **HRESULT** per individuare eventuali errori.</span><span class="sxs-lookup"><span data-stu-id="723cb-131">When you write your own code, be sure to check each **HRESULT** return code for errors.</span></span>

<span data-ttu-id="723cb-132">Per un esempio completo in cui viene illustrato come ospitare il controllo ActiveX di Windows Media Player usando la classe **CAxWindow** , vedere l'esempio WMPHost.</span><span class="sxs-lookup"><span data-stu-id="723cb-132">For a complete sample that illustrates how to host the Windows Media Player ActiveX control by using the **CAxWindow** class, see the WMPHost sample.</span></span>

## <a name="hosting-the-windows-media-player-10-mobile-control-in-windows-ce"></a><span data-ttu-id="723cb-133">Hosting del controllo Windows Media Player 10 mobile in Windows CE</span><span class="sxs-lookup"><span data-stu-id="723cb-133">Hosting the Windows Media Player 10 Mobile control in Windows CE</span></span>

<span data-ttu-id="723cb-134">Microsoft eMbedded Visual C++ 4,0 e Pocket PC 2003 SDK o lo Smartphone 2003 SDK devono essere installati quando si sviluppano applicazioni basate su Windows CE che ospitano un controllo Windows Media Player 10 Mobile.</span><span class="sxs-lookup"><span data-stu-id="723cb-134">Microsoft eMbedded Visual C++ 4.0 and the Pocket PC 2003 SDK or the Smartphone 2003 SDK must be installed when developing Windows CE-based applications that host a Windows Media Player 10 Mobile control.</span></span> <span data-ttu-id="723cb-135">Inoltre, a differenza di ATL per Windows, ATL per Windows CE non supporta il modello di threading dell'Apartment.</span><span class="sxs-lookup"><span data-stu-id="723cb-135">Also, unlike ATL for Windows, ATL for Windows CE does not support the apartment threading model.</span></span> <span data-ttu-id="723cb-136">Pertanto, è necessario trovare tutte le istanze del threading Apartment nel progetto ATL e modificarle in modo da utilizzare il threading libero.</span><span class="sxs-lookup"><span data-stu-id="723cb-136">Therefore, you must find all instances of apartment threading in your ATL project and change them to use free threading.</span></span>

## <a name="related-topics"></a><span data-ttu-id="723cb-137">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="723cb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="723cb-138">**Esempi**</span><span class="sxs-lookup"><span data-stu-id="723cb-138">**Samples**</span></span>](samples.md)
</dt> <dt>

[<span data-ttu-id="723cb-139">**Uso del controllo Media Player di Windows in un programma C++**</span><span class="sxs-lookup"><span data-stu-id="723cb-139">**Using the Windows Media Player Control in a C++ Program**</span></span>](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




