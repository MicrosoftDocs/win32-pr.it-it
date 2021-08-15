---
title: Salvataggio IPaper
description: L'obiettivo principale di questo codice di esempio è il modo in cui COPaper può caricare e salvare i dati cartacei in file compositi. Le implementazioni dei metodi IPaper, Load e Save sono descritte in dettaglio.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52772002fe8f0ed234a4f430eaff4328f96f9d1ef151e83da3f4aa3e255dba09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961371"
---
# <a name="ipapersave"></a>IPaper::Save

L'obiettivo principale di questo codice di esempio è il modo in cui COPaper può caricare e salvare i dati cartacei in file compositi. Le implementazioni dei metodi [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)e **Save** sono descritte in dettaglio.

Di seguito è riportato **il metodo IPaper::Save** da Paper.cpp.


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



In questa relazione client e server, COPaper non crea il file composto usato per archiviare i dati cartacei. Per entrambi i **metodi Save** [**e Load,**](ipaper--load.md) il client passa un puntatore a interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per un file composto esistente. Usa quindi **IStorage** per scrivere e leggere i dati in tale file composto. In **IPaper::Save precedente** vengono archiviati diversi tipi di dati.

Il CLSID per DllPaper, CLSID DllPaper, viene serializzato e archiviato in uno speciale flusso controllato da COM all'interno dell'oggetto di archiviazione denominato \_ \\ "001CompObj". La [**funzione del servizio WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) esegue questa archiviazione. Questi dati CLSID archiviati possono essere usati per associare il contenuto di archiviazione al componente DllPaper che ha creato e può interpretarlo. In questo esempio l'archiviazione radice viene passata da **StoClien** e pertanto l'intero file composto viene associato al componente DllPaper. Questi dati CLSID possono essere recuperati in un secondo momento con una chiamata alla funzione del servizio [**ReadClassStg.**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg)

Poiché DllPaper gestisce i dati modificabili, è anche opportuno registrare un formato degli Appunti nell'archiviazione. La funzione del servizio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) viene chiamata per archiviare sia una designazione del formato degli Appunti che un nome leggibile dall'utente per il formato. Il nome leggibile dall'utente è destinato alla visualizzazione gui negli elenchi di selezione. Il nome passato in precedenza usa una macro, CLIPBDFMT \_ STR, definita come "DllPaper 1.0" in Paper.h. Questi dati degli Appunti archiviati possono essere recuperati in un secondo momento con una chiamata alla funzione del servizio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg). Questa funzione restituisce un valore stringa allocato usando l'allocatore di memoria dell'attività. Il chiamante è responsabile della liberatura della stringa.

**Salva** crea quindi un flusso nell'archivio per i dati cartacei DI COPaper. Il flusso è denominato "PAPERDATA" e viene passato usando la \_ macro STREAM PAPERDATA \_ USTR. Il [**metodo IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) richiede che questa stringa sia in Unicode. Poiché la stringa è fissa in fase di compilazione, la macro è definita come Unicode in Paper.h.

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

La "L" prima della stringa, che indica LONG, ottiene questo risultato.

Il [**metodo CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea e apre un flusso all'interno dell'archiviazione specificata. Un [**puntatore a interfaccia IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per il nuovo flusso viene passato in una variabile di puntatore a interfaccia del chiamante. AddRef viene chiamato su questo puntatore a interfaccia all'interno **di CreateStream** e il chiamante deve rilasciare questo puntatore dopo l'uso. Al **metodo CreateStream** vengono passati numerosi flag della modalità di accesso, come indicato di seguito.

STGM \_ CREATE \| STGM \_ WRITE \| STGM \_ DIRECT \| STGM \_ SHARE \_ EXCLUSIVE

[**STGM \_ CREATE**](stgm-constants.md) crea un nuovo flusso o ne sovrascrive uno esistente con lo stesso nome. [**STGM \_ WRITE**](stgm-constants.md) apre il flusso con autorizzazione di scrittura. [**STGM \_ DIRECT**](stgm-constants.md) apre il flusso per l'accesso diretto, anziché per l'accesso transazione. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.

Dopo aver creato correttamente il flusso PAPERDATA, viene usata [**l'interfaccia IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per scrivere nel flusso. Il **metodo IStream::Write** viene usato per archiviare prima il contenuto della struttura PAPER \_ PROPERTIES. Si tratta essenzialmente di un'intestazione di proprietà nella parte anteriore del flusso. Poiché il numero di versione è la prima cosa nel file, può essere letto in modo indipendente per determinare come gestire i dati seguenti. Se la quantità di dati effettivamente scritti non è uguale alla quantità richiesta, il metodo Save viene interrotto e restituisce STG \_ E \_ CANTSAVE.

Il salvataggio dell'intera matrice di dati di input penna nel flusso è semplice.


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



Poiché il [**metodo IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opera su una matrice di byte, viene calcolato il numero di byte di dati di input penna archiviati nella matrice e l'operazione di scrittura inizia all'inizio della matrice. Se la quantità di dati effettivamente scritti non è uguale alla quantità richiesta, il **metodo Save** restituisce STG \_ E \_ CANTSAVE.

Dopo la scrittura del flusso, il **metodo IPaper::Save** rilascia il puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) in uso.

Il **metodo Save** chiama anche il metodo [**IPaperSink**](ipapersink-methods.md) del client (nel metodo NotifySinks interno di COPaper) per notificare al client che l'operazione di salvataggio è stata completata. A questo punto il **metodo Save** torna al client chiamante, che in genere rilascia il [**puntatore IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage)

 

 




