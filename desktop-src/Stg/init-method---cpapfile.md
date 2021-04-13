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
# <a name="init-method---cpapfile"></a><span data-ttu-id="e7141-104">Metodo Init-CPapFile</span><span class="sxs-lookup"><span data-stu-id="e7141-104">Init Method - CPapFile</span></span>

<span data-ttu-id="e7141-105">Nell'esempio di codice seguente viene illustrata la modalità di inizializzazione di **CPapFile** .</span><span class="sxs-lookup"><span data-stu-id="e7141-105">The following code example shows how **CPapFile** is initialized.</span></span>

<span data-ttu-id="e7141-106">Questo esempio è il metodo  **init** di **CPapFile** da Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="e7141-106">This example is the **CPapFile** **Init** method from Papfile.cpp.</span></span>


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



<span data-ttu-id="e7141-107">Il parametro *pszAppFileName* viene usato per inizializzare CPapFile con un nome di file predefinito per tutte le operazioni di caricamento o salvataggio successive.</span><span class="sxs-lookup"><span data-stu-id="e7141-107">The *pszAppFileName* parameter is used to initialize CPapFile with a default file name for any subsequent load or save operations.</span></span> <span data-ttu-id="e7141-108">Una copia viene mantenuta nel membro **m \_ szCurFileName** per il primo carico.</span><span class="sxs-lookup"><span data-stu-id="e7141-108">A copy is kept in member **m\_szCurFileName** for the first load.</span></span> <span data-ttu-id="e7141-109">In **StoClien** viene eseguito un tentativo di caricamento di questo tipo quando l'applicazione viene avviata per la prima volta dopo l'inizializzazione di CPapFile con *PSZAPPFILENAME* assegnato "StoClien. PAP ".</span><span class="sxs-lookup"><span data-stu-id="e7141-109">In **StoClien**, such a load is attempted when the application first starts after CPapFile has been initialized with *pszAppFileName* assigned "STOCLIEN.PAP".</span></span> <span data-ttu-id="e7141-110">Questo nome file è stato creato in un costruttore CGuiPaper ottenendo il nome del modulo corrente in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="e7141-110">This file name was constructed in a CGuiPaper constructor by obtaining the current executing module name.</span></span> <span data-ttu-id="e7141-111">Viene chiamata la funzione Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) .</span><span class="sxs-lookup"><span data-stu-id="e7141-111">(The Win32 [**GetModuleFileName**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulefilenamea) function is called).</span></span>

<span data-ttu-id="e7141-112">Il parametro *pIPaper* è richiesto da CPapFile, perché usa questa interfaccia nell'oggetto Copaper per eseguire le operazioni di caricamento e salvataggio.</span><span class="sxs-lookup"><span data-stu-id="e7141-112">The *pIPaper* parameter is required by CPapFile, because it uses this interface on the COPaper object to perform its load and save operations.</span></span> <span data-ttu-id="e7141-113">**AddRef** viene chiamato in questa copia archiviata di *pIPaper*, in base alle regole com.</span><span class="sxs-lookup"><span data-stu-id="e7141-113">**AddRef** is called on this stored copy of *pIPaper*, in accordance with COM rules.</span></span> <span data-ttu-id="e7141-114">La **versione** corrispondente viene chiamata nel distruttore CPapFile.</span><span class="sxs-lookup"><span data-stu-id="e7141-114">The matching **Release** is called in the CPapFile destructor.</span></span>

 

 