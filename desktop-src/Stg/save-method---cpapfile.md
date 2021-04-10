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
# <a name="save-method---cpapfile"></a>Metodo Save-CPapFile

Quando **CPapFile** viene inizializzato, può essere usato per salvare i dati di disegno correnti contenuti nell'oggetto Copaper.

## <a name="save-method-papfilecpp"></a>Metodo Save (PAPFILE. CPP

Questo esempio è il metodo di  [**salvataggio**](ipaper--save.md) **CPapFile** da Papfile. cpp.


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



Se viene passato **null** per il parametro *pszFileName* , per il nome file viene usato il contenuto archiviato del membro **m \_ szCurFileName** . *NLockKey* è la chiave di blocco del client ottenuta in una chiamata precedente al metodo [**Lock**](ipaper-methods.md) di Copaper nell'interfaccia **iPaper** .

La funzione del servizio [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) standard com viene chiamata per creare il file composto in cui verranno salvati i dati di disegno.

Il nome del file composto da creare viene passato come primo parametro. Questo comportamento è previsto da [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) come stringa Unicode. Quando **StoClien** viene compilato per le stringhe ANSI (Unicode non è definito, che è l'impostazione predefinita nel makefile), questa chiamata si riduce effettivamente a una chiamata a una funzione APPUTIL interna, ovvero **un \_ StgCreateDocFile**. Questa funzione esegue la conversione corretta del parametro ANSI pszFile in una versione Unicode prima di chiamare **StgCreateDocFile**. Per ulteriori informazioni, vedere apputil. h e Stoserve.htm.

I flag della modalità di accesso vengono passati come secondo parametro e determinano le modalità di accesso consentite nel nuovo file. Il flag [STGM \_ create](stgm-constants.md) Access Mode crea un nuovo file composto o sovrascrive uno esistente con lo stesso nome. [STGM \_ READWRITE](stgm-constants.md) apre il file con l'autorizzazione di lettura/scrittura. [STGM \_ DIRECT](stgm-constants.md) apre il file per l'accesso diretto, anziché l'accesso transazionale. [STGM \_ SHARE \_ Exclusive](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.

Il terzo parametro è riservato e deve essere zero.

L'indirizzo della variabile puntatore **m \_ pIStorage** viene passato a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) come quarto parametro. Quando la chiamata restituisce correttamente, **m \_ pIStorage** contiene un puntatore di interfaccia a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Si tratta dell'interfaccia utilizzata per tutte le operazioni successive sul file.

L'operazione importante in questo caso consiste nel fare in modo che l'oggetto Copaper memorizzi i dati di disegno nel file. Questa operazione viene eseguita sopra usando il metodo [**Save**](ipaper--save.md) dell'interfaccia [**iPaper**](ipaper-methods.md) di Copaper. Se il Copaper riesce a salvare i dati nell'oggetto di archiviazione fornito, il nome del file composto viene copiato in **m \_ szCurFileName** come nuovo nome file corrente.

 

 




