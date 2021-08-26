---
title: Metodo Load - CPapFile
description: Quando queste operazioni hanno esito positivo, viene rilasciata l'interfaccia IStorage ottenuta. In questo modo il file viene chiuso e viene indicato che il file non viene mantenuto aperto durante altre operazioni client. Verrà riaperto quando necessario.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- Metodo Load - CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49eac23bcb79738a30b18eb87a4d8ef4598aba89de0748c58b433df28d614886
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120034891"
---
# <a name="load-method---cpapfile"></a>Metodo Load - CPapFile

Quando queste operazioni hanno esito positivo, viene rilasciata [**l'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta. In questo modo il file viene chiuso e viene indicato che il file non viene mantenuto aperto durante altre operazioni client. Verrà riaperto quando necessario.

Questo esempio è il **metodo CPapFile** **Load** di Papfile.cpp.


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



### <a name="remarks"></a>Commenti

Come per il [**metodo Save,**](save-method---cpapfile.md) se viene passato **NULL** per il parametro *pszFileName,* per il nome file viene usato il contenuto archiviato del membro **m \_ szCurFileName.** Poiché è possibile aprire un file esistente, la funzione APPUTIL **FileExist** viene prima usata per verificare l'esistenza del file. Se esiste, viene chiamata la funzione del servizio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) standard per verificare il formato del file per determinare se si tratta di un file composto valido.

Se il file è valido, viene chiamata la funzione del servizio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) standard per aprire il file e restituire un puntatore a [**un'interfaccia IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage)

Il primo parametro è il nome del file composto da aprire. Come per la chiamata [**StgCreateDocfile,**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) questa stringa è prevista nel formato Unicode e durante la compilazione ANSI viene usata una macro APPUTIL per assicurarsi che il parametro ANSI sia convertito nel formato Unicode previsto.

Il secondo parametro di archiviazione con priorità **è NULL,** a indicare che non viene usato in questo esempio.

I flag della modalità di accesso vengono passati come terzo parametro per specificare le modalità di accesso consentite nel file aperto. [**STGM \_ READ**](stgm-constants.md) apre il file con autorizzazione di sola lettura. [**STGM \_ DIRECT**](stgm-constants.md) apre il file per l'accesso diretto, anziché per l'accesso transazione. [**STGM \_ SHARE \_ EXCLUSIVE**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.

Quarto parametro di esclusione dell'elemento in **NULL,** che indica che non viene usato in questo esempio.

Il quinto parametro è riservato per un uso futuro e deve essere zero.

L'indirizzo della variabile **puntatore m \_ pIStorage** viene passato come sesto parametro. Quando la chiamata viene restituita correttamente, **m \_ pIStorage** contiene un puntatore a [**un'interfaccia IStorage.**](/windows/desktop/api/Objidl/nn-objidl-istorage) Si tratta dell'interfaccia utilizzata per tutte le operazioni successive sul file aperto.

L'operazione importante in questo caso è fare in modo che l'oggetto COPaper carichi i dati di disegno dal file. Questa operazione viene eseguita in precedenza **usando il metodo Load** dell'interfaccia IPaper di [**COPaper.**](ipaper-methods.md) Se COPaper riesce a caricare i dati usando [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) fornito, il nome del file composto viene copiato in **m \_ szCurFileName** come nuovo nome file corrente.

Al termine di queste operazioni, viene rilasciata [**l'interfaccia IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta. In questo modo il file viene chiuso e significa che il file non viene mantenuto aperto durante altre operazioni client. Verrà riaperto quando necessario.

 

 




