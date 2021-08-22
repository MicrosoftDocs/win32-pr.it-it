---
description: Recupero dei puntatori di interfaccia DVD
ms.assetid: 3d9315fc-dcfb-483a-9437-55c440813dc2
title: Recupero dei puntatori di interfaccia DVD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d965dff48813800fa76821c72fa06a2d2f652e623c8aaeb7c0b44f9f9fafc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072942"
---
# <a name="obtaining-the-dvd-interface-pointers"></a>Recupero dei puntatori di interfaccia DVD

Dopo aver compilato il grafico dei filtri, l'applicazione può ottenere i puntatori di cui ha bisogno per controllare lo strumento di navigazione DVD, Il gestore Graph filtri e la finestra video. I passaggi di base, con il controllo degli errori e altro codice lasciato per semplicità, sono illustrati nell'esempio di codice seguente. Il codice completo è disponibile nell'applicazione DVD Sample nel metodo CDvdCore::BuildGraph. Per altre informazioni, vedere esempi [DirectShow.](directshow-samples.md)


```C++
// Create an instance of the DVD Graph Builder object.
HRESULT hr;
hr = CoCreateInstance(CLSID_DvdGraphBuilder,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IDvdGraphBuilder,
                          reinterpret_cast<void**>(&m_pIDvdGB));

// Build the DVD filter graph.
AM_DVD_RENDERSTATUS buildStatus;
hr = m_pIDvdGB->RenderDvdVideoVolume(pszwDiscPath, m_dwRenderFlags, &buildStatus);

// Get the pointers to the DVD Navigator interfaces.
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdInfo2, reinterpret_cast<void**>(&m_pIDvdI2));
hr = m_pIDvdGB->GetDvdInterface(IID_IDvdControl2, reinterpret_cast<void**>(&m_pIDvdC2));
   ...    
// Get a pointer to the filter graph manager.
hr = m_pDvdGB->GetFiltergraph(&m_pGraph);
...   
// Use the graph pointer to get a pointer to IMediaControl,
// for controlling the filter graph as a whole.
hr = m_pGraph->QueryInterface(IID_IMediaControl, reinterpret_cast<void**>(&m_pIMC));
...   
// Get a pointer to IMediaEventEx,
// used for handling DVD and other filter graph events.
hr = m_pGraph->QueryInterface(IID_IMediaEventEx, reinterpret_cast<void**>(&m_pME)); 
...                
// Use the graph builder pointer again to get the IVideoWindow interface,
// to set the window style and message-handling behavior of the video renderer filter.
hr = m_pIDvdGB->GetDvdInterface(IID_IVideoWindow, reinterpret_cast<void**>(&m_pIVW));
  
hr = m_pDvdGB->GetDvdInterface(IID_IAMLine21Decoder, reinterpret_cast<void**>(&pL21Dec));
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 



