---
title: Metodo Init-CPapFile
description: Nell'esempio di codice seguente viene illustrata la modalità di inizializzazione di CPapFile.
ms.assetid: 8312a6b2-6f3f-4a24-8aeb-9461f3b1a905
keywords:
- Metodo Init-CPapFile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4fb5729ddcf20545254e3e461070c3e68f3421
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399501"
---
# <a name="init-method---cpapfile"></a>Metodo Init-CPapFile

Nell'esempio di codice seguente viene illustrata la modalità di inizializzazione di **CPapFile** .

Questo esempio è il metodo  **init** di **CPapFile** da Papfile. cpp.


```C++
HRESULT CPapFile::Init(
                      TCHAR* pszAppFileName,
                      IPaper* pIPaper)
  {
    HRESULT hr = E_FAIL;

    if (NULL != pIPaper)
    {
      // Keep CPapFile copy of pIPaper. Thus AddRef it.
      // Released in Destructor.
      m_pIPaper = pIPaper;
      m_pIPaper->AddRef();

      if (NULL != pszAppFileName)
      {
        // Set the default current file name.
        StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszAppFileName);

        hr = NOERROR;
      }
    }

    return (hr);
  }
  
```



Il parametro *pszAppFileName* viene usato per inizializzare CPapFile con un nome di file predefinito per tutte le operazioni di caricamento o salvataggio successive. Una copia viene mantenuta nel membro **m \_ szCurFileName** per il primo carico. In **StoClien** viene eseguito un tentativo di caricamento di questo tipo quando l'applicazione viene avviata per la prima volta dopo l'inizializzazione di CPapFile con *PSZAPPFILENAME* assegnato "StoClien. PAP ". Questo nome file è stato creato in un costruttore CGuiPaper ottenendo il nome del modulo corrente in esecuzione. Viene chiamata la funzione Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .

Il parametro *pIPaper* è richiesto da CPapFile, perché usa questa interfaccia nell'oggetto Copaper per eseguire le operazioni di caricamento e salvataggio. **AddRef** viene chiamato in questa copia archiviata di *pIPaper*, in base alle regole com. La **versione** corrispondente viene chiamata nel distruttore CPapFile.

 

 