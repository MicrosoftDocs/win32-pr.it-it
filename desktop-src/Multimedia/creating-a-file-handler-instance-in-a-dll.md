---
title: Creazione di un'istanza di File-Handler in una DLL
description: Creazione di un'istanza di File-Handler in una DLL
ms.assetid: 0cf7ef72-c675-4a67-97b3-18cccfb7ddc1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c95a462d9c2f56abb5985904c4acc1fb12d10877
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103726303"
---
# <a name="creating-a-file-handler-instance-in-a-dll"></a><span data-ttu-id="e6526-103">Creazione di un'istanza di File-Handler in una DLL</span><span class="sxs-lookup"><span data-stu-id="e6526-103">Creating a File-Handler Instance in a DLL</span></span>

<span data-ttu-id="e6526-104">Quando un'applicazione specifica la DLL del gestore di file o il gestore del flusso, il sistema lo cerca nel registro di sistema in base all'identificatore di classe e caricato.</span><span class="sxs-lookup"><span data-stu-id="e6526-104">When an application specifies your file-handler DLL or stream handler, the system looks it up in the registry by its class identifier and loaded.</span></span> <span data-ttu-id="e6526-105">Il sistema chiama quindi la funzione [**DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) della dll per creare un'istanza del gestore di file o di flusso.</span><span class="sxs-lookup"><span data-stu-id="e6526-105">The system then calls the [**DllGetClassObject**](/previous-versions//dd797891(v=vs.85)) function of the DLL to create an instance of the file or stream handler.</span></span> <span data-ttu-id="e6526-106">Nell'esempio seguente (scritto in C++) viene illustrato il modo in cui un gestore di file crea un'istanza.</span><span class="sxs-lookup"><span data-stu-id="e6526-106">The following example (written in C++) shows how a file handler creates an instance.</span></span>


```C++
// Main DLL entry point. 
STDAPI DllGetClassObject(const CLSID FAR& rclsid, 
    const IID FAR& riid, void FAR* FAR* ppv) 
{ 
    HRESULT hresult; 
    hresult = CAVIFileCF::Create(rclsid, riid, ppv); 
    return hresult; 
} 
HRESULT CAVIFileCF::Create(const CLSID FAR&   rclsid, 
    const IID FAR& riid, void FAR* FAR*   ppv) 
{ 
// The following is the class factory creation and not an 
// actual PAVIFile. 
    CAVIFileCF FAR*   pAVIFileCF; 
    IUnknown FAR*   pUnknown; 
    HRESULT hresult; 
 
// Create the instance. 
    pAVIFileCF = new FAR CAVIFileCF(rclsid, &pUnknown); 
    if (pAVIFileCF == NULL) 
        return ResultFromScode(E_OUTOFMEMORY); 
 
// Set the interface pointer. 
    hresult = pUnknown->QueryInterface(riid, ppv); 
    if (FAILED(GetScode(hresult))) 
        delete pAVIFileCF; 
    return hresult; 
} 

```



 

 