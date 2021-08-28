---
title: Metodi e classe CPapFile
description: StoClien incapsula le operazioni sui file composti in un oggetto CPapFile C++.
ms.assetid: 21a3e170-0a73-4744-8cfc-3a04e0571792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36eaa46b9e675be2da699ed6f2fb0e2a2d8dd6db1e25cf0afba0f216f75a59e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117962377"
---
# <a name="cpapfile-class-and-methods"></a>Metodi e classe CPapFile

**StoClien incapsula** le operazioni sui file composti in un oggetto CPapFile C++.

Di seguito è riportata la dichiarazione di classe **CPapFile** da Papfile.h.


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



L'oggetto CPapFile mantiene un nome file corrente nel **membro m \_ szCurFileName**. Questo nome file viene usato come impostazione predefinita nei metodi [**Load**](load-method---cpapfile.md) e [**Save**](save-method---cpapfile.md) quando non ricevono in modo esplicito un nome file.

Il **membro m \_ pIPaper** mantiene un puntatore a interfaccia all'interfaccia [**COPaper IPaper.**](ipaper-methods.md) Il **membro m \_ pIStorage** mantiene un puntatore all'interfaccia [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) per il file composto corrente che **StoClien** usa per l'archiviazione strutturata.

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



 

 




