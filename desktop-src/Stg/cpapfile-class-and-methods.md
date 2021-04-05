---
title: Classe e metodi CPapFile
description: StoClien incapsula le operazioni dei file composti in un oggetto C++ CPapFile.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa970aecf275afbf7bc5b6d68c69de3367e48aa5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955344"
---
# <a name="cpapfile-class-and-methods"></a>Classe e metodi CPapFile

**StoClien** incapsula le operazioni dei file composti in un oggetto C++ CPapFile.

Di seguito è riportata la dichiarazione della classe **CPapFile** da Papfile. h.


```C++
class CPapFile
  {
    public:
      CPapFile(void);
      ~CPapFile(void);
      HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
      HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
      HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);

    private:
      TCHAR          m_szCurFileName[MAX_PATH];
      IPaper*        m_pIPaper;
      IStorage*      m_pIStorage;
  };
  
```



L'oggetto CPapFile mantiene un nome file corrente nel membro **m \_ szCurFileName**. Questo nome file viene usato come impostazione predefinita nei metodi [**Load**](load-method---cpapfile.md) e [**Save**](save-method---cpapfile.md) quando non ricevono in modo esplicito un nome file.

Member **m \_ pIPaper** mantiene un puntatore di interfaccia per l'interfaccia [**iPaper**](ipaper-methods.md) di Copaper. Member **m \_ pIStorage** mantiene un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per il file composto corrente usato da **StoClien** per l'archiviazione strutturata.

Di seguito è riportato un riepilogo dei metodi di CPapFile.


```C++
HRESULT Init(TCHAR* pszFileName, IPaper* pIPaper);
    // Initializes CPapFile.

  HRESULT Load(SHORT nLockKey, TCHAR* pszFileName);
    // Loads default or specified paper data file.

  HRESULT Save(SHORT nLockKey, TCHAR* pszFileName);
    // Saves drawing data to the current paper data file or
    // to a specified paper data file.
```



 

 




