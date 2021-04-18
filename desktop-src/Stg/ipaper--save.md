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
# <a name="ipapersave"></a><span data-ttu-id="db38f-104">IPaper:: Save</span><span class="sxs-lookup"><span data-stu-id="db38f-104">IPaper::Save</span></span>

<span data-ttu-id="db38f-105">Lo stato attivo principale in questo esempio di codice è il modo in cui il Copaper può caricare e salvare i dati cartacei nei file composti.</span><span class="sxs-lookup"><span data-stu-id="db38f-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="db38f-106">Le implementazioni del metodo [**iPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)e **Save** sono descritte in dettaglio.</span><span class="sxs-lookup"><span data-stu-id="db38f-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="db38f-107">Di seguito è riportato il metodo **iPaper:: Save** di paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="db38f-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


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



<span data-ttu-id="db38f-108">In questa relazione tra client e server, il Copaper non crea il file composto usato per archiviare i dati cartacei.</span><span class="sxs-lookup"><span data-stu-id="db38f-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="db38f-109">Per entrambi i metodi **Save** e [**Load**](ipaper--load.md) , il client passa un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per un file composto esistente.</span><span class="sxs-lookup"><span data-stu-id="db38f-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="db38f-110">USA quindi **IStorage** per scrivere e leggere i dati nel file composto.</span><span class="sxs-lookup"><span data-stu-id="db38f-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="db38f-111">In **iPaper:: Save** sopra sono archiviati diversi tipi di dati.</span><span class="sxs-lookup"><span data-stu-id="db38f-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="db38f-112">Il CLSID per DllPaper, CLSID \_ DllPaper, viene serializzato e archiviato in un flusso speciale controllato a com all'interno dell'oggetto di archiviazione denominato " \\ 001CompObj".</span><span class="sxs-lookup"><span data-stu-id="db38f-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="db38f-113">La funzione del servizio [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) esegue questa archiviazione.</span><span class="sxs-lookup"><span data-stu-id="db38f-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="db38f-114">Questi dati CLSID archiviati possono essere usati per associare il contenuto di archiviazione al componente DllPaper che ha creato e può interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="db38f-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="db38f-115">In questo esempio, l'archiviazione radice viene passata da **StoClien**, quindi l'intero file composto viene associato al componente DllPaper.</span><span class="sxs-lookup"><span data-stu-id="db38f-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="db38f-116">Questi dati CLSID possono essere recuperati in un secondo momento con una chiamata alla funzione del servizio [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .</span><span class="sxs-lookup"><span data-stu-id="db38f-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="db38f-117">Poiché DllPaper gestisce i dati modificabili, è anche opportuno registrare un formato degli Appunti nell'archivio.</span><span class="sxs-lookup"><span data-stu-id="db38f-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="db38f-118">La funzione del servizio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) viene chiamata per archiviare una designazione di formato degli Appunti e un nome leggibile dall'utente per il formato.</span><span class="sxs-lookup"><span data-stu-id="db38f-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="db38f-119">Il nome leggibile dall'utente è destinato alla visualizzazione GUI negli elenchi di selezione.</span><span class="sxs-lookup"><span data-stu-id="db38f-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="db38f-120">Il nome passato usa una macro, CLIPBDFMT \_ Str, definita come "DllPaper 1,0" in paper. h.</span><span class="sxs-lookup"><span data-stu-id="db38f-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="db38f-121">È possibile recuperare i dati degli Appunti archiviati in un secondo momento con una chiamata alla funzione del servizio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span><span class="sxs-lookup"><span data-stu-id="db38f-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="db38f-122">Questa funzione restituisce un valore stringa allocato usando l'allocatore di memoria dell'attività.</span><span class="sxs-lookup"><span data-stu-id="db38f-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="db38f-123">Il chiamante è responsabile della liberazione della stringa.</span><span class="sxs-lookup"><span data-stu-id="db38f-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="db38f-124">**Salva** successivo consente di creare un flusso nell'archivio per i dati cartacei del documento.</span><span class="sxs-lookup"><span data-stu-id="db38f-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="db38f-125">Il flusso è denominato "PAPERDATA" e viene passato utilizzando la \_ macro PAPERDATA \_ USTR di Stream.</span><span class="sxs-lookup"><span data-stu-id="db38f-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="db38f-126">Il metodo [**IStorage:: CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) richiede che la stringa sia in Unicode.</span><span class="sxs-lookup"><span data-stu-id="db38f-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="db38f-127">Poiché la stringa viene fissata in fase di compilazione, la macro viene definita come Unicode in paper. h.</span><span class="sxs-lookup"><span data-stu-id="db38f-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="db38f-128">Il valore di "L" prima della stringa, che indica LONG, raggiunge questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="db38f-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="db38f-129">Il metodo [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea e apre un flusso all'interno dell'archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="db38f-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="db38f-130">Un puntatore di interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) per il nuovo flusso viene passato in una variabile del puntatore a interfaccia del chiamante.</span><span class="sxs-lookup"><span data-stu-id="db38f-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="db38f-131">AddRef viene chiamato su questo puntatore di interfaccia all'interno di **CreateStream** e il chiamante deve rilasciare il puntatore dopo averlo utilizzato.</span><span class="sxs-lookup"><span data-stu-id="db38f-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="db38f-132">Al metodo **CreateStream** vengono passati diversi flag della modalità di accesso, come indicato di seguito.</span><span class="sxs-lookup"><span data-stu-id="db38f-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="db38f-133">STGM \_ creare \| STGM \_ scrivere \| STGM \_ Direct \| STGM \_ share \_ Exclusive</span><span class="sxs-lookup"><span data-stu-id="db38f-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="db38f-134">[**STGM \_ Crea**](stgm-constants.md) crea un nuovo flusso o sovrascrive uno esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="db38f-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="db38f-135">[**STGM \_ WRITE**](stgm-constants.md) apre il flusso con l'autorizzazione di scrittura.</span><span class="sxs-lookup"><span data-stu-id="db38f-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="db38f-136">[**STGM \_ DIRECT**](stgm-constants.md) apre il flusso per l'accesso diretto, anziché l'accesso transazionale.</span><span class="sxs-lookup"><span data-stu-id="db38f-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="db38f-137">[**STGM \_ SHARE \_ Exclusive**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.</span><span class="sxs-lookup"><span data-stu-id="db38f-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="db38f-138">Dopo la creazione del flusso PAPERDATA, l'interfaccia [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) viene usata per scrivere nel flusso.</span><span class="sxs-lookup"><span data-stu-id="db38f-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="db38f-139">Il metodo **IStream:: Write** viene usato per archiviare prima di tutto il contenuto della \_ struttura della proprietà paper.</span><span class="sxs-lookup"><span data-stu-id="db38f-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="db38f-140">Si tratta essenzialmente di un'intestazione Properties all'inizio del flusso.</span><span class="sxs-lookup"><span data-stu-id="db38f-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="db38f-141">Poiché il numero di versione è il primo elemento del file, può essere letto in modo indipendente per determinare come gestire i dati seguenti.</span><span class="sxs-lookup"><span data-stu-id="db38f-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="db38f-142">Se la quantità di dati effettivamente scritti non equivale alla quantità richiesta, il metodo Save viene interrotto e restituisce STG \_ e \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="db38f-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="db38f-143">Il salvataggio dell'intera matrice di dati Ink nel flusso è semplice.</span><span class="sxs-lookup"><span data-stu-id="db38f-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="db38f-144">Poiché il metodo [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) opera su una matrice di byte, il numero di byte dei dati di input penna archiviati nella matrice viene calcolato e l'operazione di scrittura inizia all'inizio della matrice.</span><span class="sxs-lookup"><span data-stu-id="db38f-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="db38f-145">Se la quantità di dati effettivamente scritti non equivale alla quantità richiesta, il metodo **Save** restituisce STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="db38f-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="db38f-146">Dopo la scrittura del flusso, il metodo **iPaper:: Save** rilascia il puntatore [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) usato.</span><span class="sxs-lookup"><span data-stu-id="db38f-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="db38f-147">Il metodo **Save** chiama anche il client [**IPaperSink**](ipapersink-methods.md) (nel metodo NotifySinks interno della carta) per notificare al client che l'operazione di salvataggio è stata completata.</span><span class="sxs-lookup"><span data-stu-id="db38f-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="db38f-148">A questo punto il metodo **Save** viene restituito al client chiamante, che in genere rilascia il puntatore [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="db38f-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




