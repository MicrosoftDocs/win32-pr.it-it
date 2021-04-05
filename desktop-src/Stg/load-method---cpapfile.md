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
# <a name="load-method---cpapfile"></a>Metodo Load-CPapFile

Quando queste operazioni hanno esito positivo, viene rilasciata l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta. Questa operazione chiude il file e indica che il file non viene mantenuto aperto durante le altre operazioni client. Verrà riaperto quando richiesto.

Questo esempio è il metodo  **Load** di **CPapFile** da Papfile. cpp.


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

Come nel caso del metodo [**Save**](save-method---cpapfile.md) , se viene passato **null** per il parametro *pszFileName* , per il nome file viene usato il contenuto archiviato del membro **m \_ szCurFileName** . Poiché è possibile che venga aperto un file esistente, la funzione **Fileexist** APPUTIL viene innanzitutto utilizzata per verificare che il file esista. Se esiste, viene chiamata la funzione del servizio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) standard per verificare il formato del file per determinare se si tratta di un file composto valido.

Se il file è valido, viene chiamata la funzione di servizio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) standard per aprire il file e restituire un puntatore a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .

Il primo parametro è il nome del file composto da aprire. Come per la chiamata a [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , questa stringa è prevista nel formato Unicode e durante la compilazione ANSI viene usata una macro APPUTIL per assicurarsi che il parametro ANSI venga convertito nel formato Unicode previsto.

Il secondo parametro di archiviazione Priority è **null**, a indicare che non viene usato in questo esempio.

I flag della modalità di accesso vengono passati come terzo parametro per specificare le modalità di accesso consentite nel file aperto. [**STGM \_ READ**](stgm-constants.md) apre il file con l'autorizzazione di sola lettura. [**STGM \_ DIRECT**](stgm-constants.md) apre il file per l'accesso diretto, anziché l'accesso transazionale. [**STGM \_ SHARE \_ Exclusive**](stgm-constants.md) apre il file per l'uso esclusivo e non condiviso da parte del chiamante.

Il quarto parametro di esclusione di elementi in **null**, che indica che non viene utilizzato in questo esempio.

Il quinto parametro è riservato per utilizzi futuri e deve essere zero.

L'indirizzo della variabile puntatore **m \_ pIStorage** viene passato come sesto parametro. Quando la chiamata restituisce correttamente, **m \_ pIStorage** contiene un puntatore a un'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Si tratta dell'interfaccia utilizzata per tutte le operazioni successive sul file aperto.

L'operazione importante in questo caso consiste nel fare in modo che l'oggetto Copaper carichi i dati di disegno dal file. Questa operazione viene eseguita in precedenza utilizzando il metodo **Load** dell'interfaccia [**iPaper**](ipaper-methods.md) di Copaper. Se il Copaper riesce a caricare i dati usando il [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) specificato, il nome del file composto viene copiato in **m \_ szCurFileName** come nuovo nome file corrente.

Quando queste operazioni vengono completate correttamente, viene rilasciata l'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) ottenuta. Questa operazione chiude il file e indica che il file non viene mantenuto aperto durante le altre operazioni client. Verrà riaperto quando richiesto.

 

 




