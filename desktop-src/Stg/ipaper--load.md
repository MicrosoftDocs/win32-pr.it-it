---
title: Carico IPaper
description: Nel codice di esempio C++ riportato di seguito viene illustrato come aprire il flusso esistente nell'archiviazione, leggere le nuove proprietà della carta in e impostarle come valori correnti per la cocarta.
ms.assetid: a1559d97-387f-4d1a-8a9d-fa5c27abd545
keywords:
- Carico IPaper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16b5f16b8fe649d08226b2cff5a4b1a5234bddb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955706"
---
# <a name="ipaperload"></a>IPaper:: Load

Nel codice di esempio C++ riportato di seguito viene illustrato come aprire il flusso esistente nell'archiviazione, leggere le nuove proprietà della carta in e impostarle come valori correnti per la cocarta.

Di seguito è riportato il metodo **iPaper:: Load** da Paper. cpp.


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



A questo punto, viene chiamato il metodo [**IStorage:: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) per aprire il flusso esistente nello spazio di archiviazione denominato "PAPERDATA". I flag della modalità di accesso sono per l'accesso esclusivo in sola lettura, diretto e non condiviso. Quando il flusso è aperto, viene chiamato il metodo [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) per leggere la \_ struttura della proprietà paper. Se la quantità effettivamente letta non è uguale a quella richiesta, l'operazione di caricamento viene interrotta e \_ viene restituito e fail. Se la versione del formato nelle proprietà della carta appena letta \_ non è riconosciuta, l'operazione di caricamento è stata interrotta e il **caricamento** restituisce e ha \_ esito negativo.

Con una versione valida del formato dati Ink, le dimensioni della nuova matrice di dati di input penna dalle proprietà della carta \_ lette in vengono utilizzate per allocare una nuova matrice di dati di input penna della dimensione richiesta. I dati di input penna esistenti vengono eliminati e i relativi dati andranno perduti. Se questi dati sono preziosi, dovrebbero essere stati salvati prima della chiamata al metodo **Load** . Dopo che la nuova matrice è stata allocata, [**IStream:: Read**](/windows/desktop/api/Objidl/nn-objidl-istream) viene chiamato nuovamente per leggere i dati nella matrice dal flusso. Se la chiamata ha esito positivo, i valori nelle proprietà della carta appena letta vengono adottati come valori correnti per il Copaper.

Durante questa operazione di caricamento, \_ è stata usata una struttura di proprietà della carta temporanea, NewProps, per conservare le nuove proprietà lette in. Se il metodo ha esito positivo, NewProps viene copiato nella struttura delle \_ proprietà della carta, m \_ PaperProperties. Come prima, al termine del caricamento e l'oggetto [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) non è più necessario, viene rilasciato il puntatore **IStream** .

Se si verifica un errore alla fine del **caricamento**, la matrice di dati Ink viene cancellata perché potrebbe contenere dati danneggiati.

Se non si verificano errori alla fine del **caricamento**, viene chiamato il metodo client [**IPaperSink:: Loaded**](ipapersink-methods.md) , nel metodo NotifySinks interno del documento, per notificare al client che l'operazione di caricamento è stata completata. Si tratta di una notifica importante per il client, perché deve visualizzare i nuovi dati di input penna caricati. Questa notifica consente di usare in modo significativo le funzionalità degli oggetti collegabili in un documento.

 

 




