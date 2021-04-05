---
title: Metodo Load-CPapFile
description: Quando queste operazioni hanno esito positivo, viene rilasciata l'interfaccia IStorage ottenuta. Questa operazione chiude il file e indica che il file non viene mantenuto aperto durante le altre operazioni client. Verrà riaperto quando richiesto.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Metodo Load-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103857005"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="26a17-106">Metodo Load-CPapFile</span><span class="sxs-lookup"><span data-stu-id="26a17-106">Load Method - CPapFile</span></span>

<span data-ttu-id="26a17-107">Quando queste operazioni hanno esito positivo, viene rilasciata l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta.</span><span class="sxs-lookup"><span data-stu-id="26a17-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="26a17-108">Questa operazione chiude il file e indica che il file non viene mantenuto aperto durante le altre operazioni client.</span><span class="sxs-lookup"><span data-stu-id="26a17-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="26a17-109">Verrà riaperto quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="26a17-109">It will be reopened when required.</span></span>

<span data-ttu-id="26a17-110">Questo esempio è il metodo  **Load** di **CPapFile** da Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="26a17-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a><span data-ttu-id="26a17-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="26a17-111">Remarks</span></span>

<span data-ttu-id="26a17-112">Come nel caso del metodo [**Save**](save-method---cpapfile.md) , se viene passato **null** per il parametro *pszFileName* , per il nome file viene usato il contenuto archiviato del membro **m \_ szCurFileName** .</span><span class="sxs-lookup"><span data-stu-id="26a17-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="26a17-113">Poiché è possibile che venga aperto un file esistente, la funzione **Fileexist** APPUTIL viene innanzitutto utilizzata per verificare che il file esista.</span><span class="sxs-lookup"><span data-stu-id="26a17-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="26a17-114">Se esiste, viene chiamata la funzione del servizio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) standard per verificare il formato del file per determinare se si tratta di un file composto valido.</span><span class="sxs-lookup"><span data-stu-id="26a17-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="26a17-115">Se il file è valido, viene chiamata la funzione di servizio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) standard per aprire il file e restituire un puntatore a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="26a17-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="26a17-116">Il primo parametro è il nome del file composto da aprire.</span><span class="sxs-lookup"><span data-stu-id="26a17-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="26a17-117">Come per la chiamata a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , questa stringa è prevista nel formato Unicode e durante la compilazione ANSI viene usata una macro APPUTIL per assicurarsi che il parametro ANSI venga convertito nel formato Unicode previsto.</span><span class="sxs-lookup"><span data-stu-id="26a17-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="26a17-118">Il secondo parametro di archiviazione Priority è **null**, a indicare che non viene usato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="26a17-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="26a17-119">I flag della modalità di accesso vengono passati come terzo parametro per specificare le modalità di accesso consentite nel file aperto.</span><span class="sxs-lookup"><span data-stu-id="26a17-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="26a17-120">[**STGM \_ READ**](stgm-constants.md) apre il file con l'autorizzazione di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="26a17-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="26a17-121">[**STGM \_ DIRECT**](stgm-constants.md) apre il file per l'accesso diretto, anziché l'accesso transazionale.</span><span class="sxs-lookup"><span data-stu-id="26a17-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="26a17-122">[**STGM \_ SHARE \_ Exclusive**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.</span><span class="sxs-lookup"><span data-stu-id="26a17-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="26a17-123">Il quarto parametro di esclusione di elementi in **null**, che indica che non viene utilizzato in questo esempio.</span><span class="sxs-lookup"><span data-stu-id="26a17-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="26a17-124">Il quinto parametro è riservato per utilizzi futuri e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="26a17-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="26a17-125">L'indirizzo della variabile puntatore **m \_ pIStorage** viene passato come sesto parametro.</span><span class="sxs-lookup"><span data-stu-id="26a17-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="26a17-126">Quando la chiamata restituisce correttamente, **m \_ pIStorage** contiene un puntatore a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="26a17-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="26a17-127">Si tratta dell'interfaccia utilizzata per tutte le operazioni successive sul file aperto.</span><span class="sxs-lookup"><span data-stu-id="26a17-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="26a17-128">L'operazione importante in questo caso consiste nel fare in modo che l'oggetto Copaper carichi i dati di disegno dal file.</span><span class="sxs-lookup"><span data-stu-id="26a17-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="26a17-129">Questa operazione viene eseguita in precedenza utilizzando il metodo **Load** dell'interfaccia [**iPaper**](ipaper-methods.md) di Copaper.</span><span class="sxs-lookup"><span data-stu-id="26a17-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="26a17-130">Se il Copaper riesce a caricare i dati usando il [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) specificato, il nome del file composto viene copiato in **m \_ szCurFileName** come nuovo nome file corrente.</span><span class="sxs-lookup"><span data-stu-id="26a17-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="26a17-131">Quando queste operazioni vengono completate correttamente, viene rilasciata l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta.</span><span class="sxs-lookup"><span data-stu-id="26a17-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="26a17-132">Questa operazione chiude il file e indica che il file non viene mantenuto aperto durante le altre operazioni client.</span><span class="sxs-lookup"><span data-stu-id="26a17-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="26a17-133">Verrà riaperto quando richiesto.</span><span class="sxs-lookup"><span data-stu-id="26a17-133">It will be reopened when required.</span></span>

 

 




