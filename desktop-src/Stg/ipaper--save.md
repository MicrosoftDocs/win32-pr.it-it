---
title: Salva IPaper
description: Lo stato attivo principale in questo esempio di codice è il modo in cui il Copaper può caricare e salvare i dati cartacei nei file composti. Le implementazioni del metodo IPaper, Load e Save sono descritte in dettaglio.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298687"
---
# <a name="ipapersave"></a>IPaper:: Save

Lo stato attivo principale in questo esempio di codice è il modo in cui il Copaper può caricare e salvare i dati cartacei nei file composti. Le implementazioni del metodo [**iPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)e **Save** sono descritte in dettaglio.

Di seguito è riportato il metodo **iPaper:: Save** di paper. cpp.


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



In questa relazione tra client e server, il Copaper non crea il file composto usato per archiviare i dati cartacei. Per entrambi i metodi **Save** e [**Load**](ipaper--load.md) , il client passa un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per un file composto esistente. USA quindi **IStorage** per scrivere e leggere i dati nel file composto. In **iPaper:: Save** sopra sono archiviati diversi tipi di dati.

Il CLSID per DllPaper, CLSID \_ DllPaper, viene serializzato e archiviato in un flusso speciale controllato a com all'interno dell'oggetto di archiviazione denominato " \\ 001CompObj". La funzione del servizio [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) esegue questa archiviazione. Questi dati CLSID archiviati possono essere usati per associare il contenuto di archiviazione al componente DllPaper che ha creato e può interpretarlo. In questo esempio, l'archiviazione radice viene passata da **StoClien**, quindi l'intero file composto viene associato al componente DllPaper. Questi dati CLSID possono essere recuperati in un secondo momento con una chiamata alla funzione del servizio [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .

Poiché DllPaper gestisce i dati modificabili, è anche opportuno registrare un formato degli Appunti nell'archivio. La funzione del servizio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) viene chiamata per archiviare una designazione di formato degli Appunti e un nome leggibile dall'utente per il formato. Il nome leggibile dall'utente è destinato alla visualizzazione GUI negli elenchi di selezione. Il nome passato usa una macro, CLIPBDFMT \_ Str, definita come "DllPaper 1,0" in paper. h. È possibile recuperare i dati degli Appunti archiviati in un secondo momento con una chiamata alla funzione del servizio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Questa funzione restituisce un valore stringa allocato usando l'allocatore di memoria dell'attività. Il chiamante è responsabile della liberazione della stringa.

**Salva** successivo consente di creare un flusso nell'archivio per i dati cartacei del documento. Il flusso è denominato "PAPERDATA" e viene passato utilizzando la \_ macro PAPERDATA \_ USTR di Stream. Il metodo [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) richiede che la stringa sia in Unicode. Poiché la stringa viene fissata in fase di compilazione, la macro viene definita come Unicode in paper. h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

Il valore di "L" prima della stringa, che indica LONG, raggiunge questo oggetto.

Il metodo [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea e apre un flusso all'interno dell'archiviazione specificata. Un puntatore di interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per il nuovo flusso viene passato in una variabile del puntatore a interfaccia del chiamante. AddRef viene chiamato su questo puntatore di interfaccia all'interno di **CreateStream** e il chiamante deve rilasciare il puntatore dopo averlo utilizzato. Al metodo **CreateStream** vengono passati diversi flag della modalità di accesso, come indicato di seguito.

STGM \_ creare \| STGM \_ scrivere \| STGM \_ Direct \| STGM \_ share \_ Exclusive

[**STGM \_ Crea**](stgm-constants.md) crea un nuovo flusso o sovrascrive uno esistente con lo stesso nome. [**STGM \_ WRITE**](stgm-constants.md) apre il flusso con l'autorizzazione di scrittura. [**STGM \_ DIRECT**](stgm-constants.md) apre il flusso per l'accesso diretto, anziché l'accesso transazionale. [**STGM \_ SHARE \_ Exclusive**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.

Dopo la creazione del flusso PAPERDATA, l'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) viene usata per scrivere nel flusso. Il metodo **IStream:: Write** viene usato per archiviare prima di tutto il contenuto della \_ struttura della proprietà paper. Si tratta essenzialmente di un'intestazione Properties all'inizio del flusso. Poiché il numero di versione è il primo elemento del file, può essere letto in modo indipendente per determinare come gestire i dati seguenti. Se la quantità di dati effettivamente scritti non equivale alla quantità richiesta, il metodo Save viene interrotto e restituisce STG \_ e \_ CANTSAVE.

Il salvataggio dell'intera matrice di dati Ink nel flusso è semplice.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Poiché il metodo [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opera su una matrice di byte, il numero di byte dei dati di input penna archiviati nella matrice viene calcolato e l'operazione di scrittura inizia all'inizio della matrice. Se la quantità di dati effettivamente scritti non equivale alla quantità richiesta, il metodo **Save** restituisce STG \_ E \_ CANTSAVE.

Dopo la scrittura del flusso, il metodo **iPaper:: Save** rilascia il puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) usato.

Il metodo **Save** chiama anche il client [**IPaperSink**](ipapersink-methods.md) (nel metodo NotifySinks interno della carta) per notificare al client che l'operazione di salvataggio è stata completata. A questo punto il metodo **Save** viene restituito al client chiamante, che in genere rilascia il puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

 

 




