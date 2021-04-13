---
title: IPaper ridisegnato
description: Il metodo di riestrazione IPaper si basa sulla tecnologia del punto di connessione.
ms.assetid: d0126a47-d616-4cc0-b270-75779a51c843
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968d2cf545296f8413d613410d9cbb759cb2b897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331591"
---
# <a name="ipaperredraw"></a>IPaper:: redisegnato

Il metodo **iPaper:: redisegnato** si basa sulla tecnologia del punto di connessione.

Il codice di esempio seguente è il metodo di **riestrazione** da Paper. cpp.


```C++
STDMETHODIMP COPaper::CImpIPaper::Redraw(
                 SHORT nLockKey)
  {
    HRESULT hr = E_FAIL;
    IConnectionPoint* pIConnectionPoint;
    IEnumConnections* pIEnum;
    CONNECTDATA ConnData;
    IPaperSink* pIPaperSink;
    SHORT nInkType;
    LONG i;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey)
      {
        // Broadcast InkData notifications to all Sinks connected to
        // each connection point.

        // Here is the section for the PaperSink connection point -- 
        // this is currently the only connection point offered by
        // COPaper objects.
        pIConnectionPoint =
          m_pBackObj->m_aConnectionPoints[CONNPOINT_PAPERSINK];
        if (NULL != pIConnectionPoint)
        {
          pIConnectionPoint->AddRef();
          hr = pIConnectionPoint->EnumConnections(&pIEnum);
          if (SUCCEEDED(hr))
          {
            // Loop through the connection point connections and if the
            // listening connection supports IPaperSink (ie, PaperSink
            // events) then send all the current Paper Ink Data to 
            // it.
            while (NOERROR == pIEnum->Next(1, &ConnData, NULL))
            {
              hr = ConnData.pUnk->QueryInterface(
                                    IID_IPaperSink,
                                    (PPVOID)&pIPaperSink);
              if (SUCCEEDED(hr))
              {
                // Loop through all the Ink Data and send it to this 
                // connected client sink.
                for (i=0; i<m_lInkDataEnd+1; i++)
                {
                  nInkType = m_paInkData[i].nType;
                  switch (nInkType)
                  {
                    case INKTYPE_START:
                      pIPaperSink->InkStart(
                                     m_paInkData[i].nX,
                                     m_paInkData[i].nY,
                                     m_paInkData[i].nWidth,
                                     m_paInkData[i].crColor);
                      break;
                    case INKTYPE_DRAW:
                      pIPaperSink->InkDraw(
                                     m_paInkData[i].nX,
                                     m_paInkData[i].nY);
                      break;
                    case INKTYPE_STOP:
                      pIPaperSink->InkStop(
                                     m_paInkData[i].nX,
                                     m_paInkData[i].nY);
                      break;
                    default:
                      break;
                  }
                }
                pIPaperSink->Release();
              }
              ConnData.pUnk->Release();
            }
            pIEnum->Release();
          }
          pIConnectionPoint->Release();
        }
      }

      UnOwnThis();
    }

    return hr;
  }
```



Per ulteriori informazioni, vedere metodo [**IPaperSink**](ipapersink-methods.md) .

 

 




