---
title: Caricamento IPaper
description: Il codice di esempio C++ seguente mostra come aprire il flusso esistente nella memoria, leggere le nuove proprietà della carta in e quindi impostarle come valori correnti per COPaper.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Caricamento IPaper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b592573f016018d359b5e3e35911d92371892b98ebea70338844b7f8ef4b1f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961381"
---
# <a name="ipaperload"></a>IPaper::Load

Il codice di esempio C++ seguente mostra come aprire il flusso esistente nella memoria, leggere le nuove proprietà della carta in e quindi impostarle come valori correnti per COPaper.

Di seguito è riportato **il metodo IPaper::Load** da Paper.cpp.


```
STDMETHODIMP COPaper::CImpIPaper::Load(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    INKDATA* paInkData;
    ULONG ulToRead, ulReadIn;
    LONG lNewArraySize;
    PAPER_PROPERTIES NewProps;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
       // Open the "PAPERDATA" stream where the paper data is stored.
        hr = pIStorage->OpenStream(
               STREAM_PAPERDATA_USTR,
               0,
               STGM_READ | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained paper data stream. Read the Paper Properties.
          ulToRead = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Read(
                           &NewProps,
                           ulToRead,
                           &ulReadIn);
          if (SUCCEEDED(hr) && ulToRead != ulReadIn)
            hr = E_FAIL;
          if (SUCCEEDED(hr))
          {
            // Handle the different versions of ink data format.
            switch (NewProps.lInkDataVersion)
            {
              case INKDATA_VERSION10:
                // Allocate an ample-sized ink data array.
                lNewArraySize = NewProps.lInkArraySize + 
                                               INKDATA_ALLOC;
                paInkData = new INKDATA[(LONG) lNewArraySize];
                if (NULL != paInkData)
                {
                  // Delete the old ink data array.
                  delete [] m_paInkData;

                  // Assign the new array.
                  m_paInkData = paInkData;
                  m_lInkDataMax = lNewArraySize;

                  // Read the complete array of Ink Data.
                  ulToRead = NewProps.lInkArraySize * sizeof(INKDATA);
                  hr = pIStream->Read(m_paInkData, 
                                      ulToRead, &ulReadIn);
                  if (SUCCEEDED(hr) && ulToRead != ulReadIn)
                    hr = E_FAIL;
                  if (SUCCEEDED(hr))
                  {
                    // Set COPaper to use the new PAPER_PROPERTIES
                    // data.
                    m_lInkDataEnd = NewProps.lInkArraySize-1;
                    m_crWinColor = NewProps.crWinColor;
                    m_WinRect.right = NewProps.WinRect.right;
                    m_WinRect.bottom = NewProps.WinRect.bottom;

                    // Copy the new properties into current 
                    // properties.
                    memcpy(
                      &m_PaperProperties,
                      &NewProps,
                      sizeof(PAPER_PROPERTIES));
                  }
                }
                else
                  hr = E_OUTOFMEMORY;
                break;
              default:
                hr = E_FAIL;  // Bad version.
                break;
            }
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify other connected clients that Paper is now loaded.
    // If Paper not loaded, then erase to a safe, empty ink data 
    // array.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_LOADED, 0, 0, 0, 0);
    else
      Erase(nLockKey);

    return hr;
  }
```



A questo punto, viene chiamato il metodo [**IStorage::OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) per aprire il flusso esistente nella memoria denominata "PAPERDATA". I flag della modalità di accesso sono per l'accesso esclusivo di sola lettura, diretto e non condiviso. Quando il flusso è aperto, viene chiamato [**il metodo IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere la struttura PAPER \_ PROPERTIES. Se la quantità effettivamente letta non è uguale alla quantità richiesta, l'operazione di caricamento viene interrotta e viene restituito E \_ FAIL. Se la versione del formato nella proprietà PAPER appena letta non viene riconosciuta, l'operazione di caricamento viene interrotta e \_ **Load** restituisce E \_ FAIL.

Con una versione valida del formato dati dell'input penna, le dimensioni della nuova matrice di dati dell'input penna dalle proprietà paper lette vengono usate per allocare una nuova matrice di dati dell'input penna delle \_ dimensioni richieste. I dati dell'input penna esistenti vengono eliminati e i relativi dati vengono persi. Se questi dati erano importanti, dovrebbero essere stati salvati prima della **chiamata** a Load. Dopo l'allocazione della nuova matrice, viene chiamato di nuovo [**IStream::Read**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere i dati nella matrice dal flusso. Se questa chiamata ha esito positivo, i valori nelle proprietà del documento appena lette vengono adottati come valori correnti per COPaper.

Durante questa operazione di caricamento è stata usata una struttura PAPER \_ PROPERTIES temporanea, NewProps, per contenere le nuove proprietà lette. Se il caricamento ha esito positivo, NewProps viene copiato nella struttura PAPER \_ PROPERTIES, m \_ PaperProperties. Come in precedenza, dopo il caricamento e [**l'IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non è più necessario, viene **rilasciato il puntatore IStream.**

Se si verifica un errore alla fine di **Load**, la matrice di dati dell'input penna viene cancellata, perché può contenere dati danneggiati.

Se non si verifica alcun errore alla fine di **Load,** viene chiamato il metodo [**IPaperSink::Loaded**](ipapersink-methods.md) del client nel metodo NotifySinks interno di COPaper per notificare al client che l'operazione di caricamento è stata completata. Si tratta di una notifica importante per il client, perché deve visualizzare i nuovi dati input penna caricati. Questa notifica usa in modo significativo le funzionalità degli oggetti collegabili in COPaper.

 

 




