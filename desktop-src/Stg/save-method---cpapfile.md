---
title: Metodo Save-CPapFile
description: Quando CPapFile viene inizializzato, può essere usato per salvare i dati di disegno correnti contenuti nell'oggetto Copaper.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- Metodo Save-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955848"
---
# <a name="save-method---cpapfile"></a><span data-ttu-id="2be0a-104">Metodo Save-CPapFile</span><span class="sxs-lookup"><span data-stu-id="2be0a-104">Save Method - CPapFile</span></span>

<span data-ttu-id="2be0a-105">Quando **CPapFile** viene inizializzato, può essere usato per salvare i dati di disegno correnti contenuti nell'oggetto Copaper.</span><span class="sxs-lookup"><span data-stu-id="2be0a-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="2be0a-106">Metodo Save (PAPFILE. CPP</span><span class="sxs-lookup"><span data-stu-id="2be0a-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="2be0a-107">Questo esempio è il metodo di  [**salvataggio**](ipaper--save.md) **CPapFile** da Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="2be0a-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



<span data-ttu-id="2be0a-108">Se viene passato **null** per il parametro *pszFileName* , per il nome file viene usato il contenuto archiviato del membro **m \_ szCurFileName** .</span><span class="sxs-lookup"><span data-stu-id="2be0a-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="2be0a-109">*NLockKey* è la chiave di blocco del client ottenuta in una chiamata precedente al metodo [**Lock**](ipaper-methods.md) di Copaper nell'interfaccia **iPaper** .</span><span class="sxs-lookup"><span data-stu-id="2be0a-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="2be0a-110">La funzione del servizio [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) standard com viene chiamata per creare il file composto in cui verranno salvati i dati di disegno.</span><span class="sxs-lookup"><span data-stu-id="2be0a-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="2be0a-111">Il nome del file composto da creare viene passato come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="2be0a-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="2be0a-112">Questo comportamento è previsto da [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) come stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="2be0a-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="2be0a-113">Quando **StoClien** viene compilato per le stringhe ANSI (Unicode non è definito, che è l'impostazione predefinita nel makefile), questa chiamata si riduce effettivamente a una chiamata a una funzione APPUTIL interna, ovvero **un \_ StgCreateDocFile**.</span><span class="sxs-lookup"><span data-stu-id="2be0a-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="2be0a-114">Questa funzione esegue la conversione corretta del parametro ANSI pszFile in una versione Unicode prima di chiamare **StgCreateDocFile**.</span><span class="sxs-lookup"><span data-stu-id="2be0a-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="2be0a-115">Per ulteriori informazioni, vedere apputil. h e Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="2be0a-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="2be0a-116">I flag della modalità di accesso vengono passati come secondo parametro e determinano le modalità di accesso consentite nel nuovo file.</span><span class="sxs-lookup"><span data-stu-id="2be0a-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="2be0a-117">Il flag [STGM \_ create](stgm-constants.md) Access Mode crea un nuovo file composto o sovrascrive uno esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="2be0a-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="2be0a-118">[STGM \_ READWRITE](stgm-constants.md) apre il file con l'autorizzazione di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="2be0a-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="2be0a-119">[STGM \_ DIRECT](stgm-constants.md) apre il file per l'accesso diretto, anziché l'accesso transazionale.</span><span class="sxs-lookup"><span data-stu-id="2be0a-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="2be0a-120">[STGM \_ SHARE \_ Exclusive](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.</span><span class="sxs-lookup"><span data-stu-id="2be0a-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="2be0a-121">Il terzo parametro è riservato e deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="2be0a-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="2be0a-122">L'indirizzo della variabile puntatore **m \_ pIStorage** viene passato a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) come quarto parametro.</span><span class="sxs-lookup"><span data-stu-id="2be0a-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="2be0a-123">Quando la chiamata restituisce correttamente, **m \_ pIStorage** contiene un puntatore di interfaccia a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="2be0a-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="2be0a-124">Si tratta dell'interfaccia utilizzata per tutte le operazioni successive sul file.</span><span class="sxs-lookup"><span data-stu-id="2be0a-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="2be0a-125">L'operazione importante in questo caso consiste nel fare in modo che l'oggetto Copaper memorizzi i dati di disegno nel file.</span><span class="sxs-lookup"><span data-stu-id="2be0a-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="2be0a-126">Questa operazione viene eseguita sopra usando il metodo [**Save**](ipaper--save.md) dell'interfaccia [**iPaper**](ipaper-methods.md) di Copaper.</span><span class="sxs-lookup"><span data-stu-id="2be0a-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="2be0a-127">Se il Copaper riesce a salvare i dati nell'oggetto di archiviazione fornito, il nome del file composto viene copiato in **m \_ szCurFileName** come nuovo nome file corrente.</span><span class="sxs-lookup"><span data-stu-id="2be0a-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




