---
title: Uso di un'interfaccia COM
description: Uso di un'interfaccia COM
ms.assetid: 44e1aeac-585c-4856-8c4d-1adb5b307b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78b5d402079debf5e0a565c6b91136605cec50fb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104328639"
---
# <a name="using-a-com-interface"></a>Uso di un'interfaccia COM

Il codice client è l'utente dell'interfaccia COM. Per usare qualsiasi interfaccia COM, personalizzata o standard, un client deve conoscerne l'IID. Nell'esempio seguente, il driver che chiama CustomRpt passa il nome dell'oggetto convertito in un formato a caratteri wide. Il nome dell'oggetto viene fornito a [**CreateFileMoniker**](/windows/desktop/api/Objbase/nf-objbase-createfilemoniker) in modo che sia possibile creare un moniker di file e che il client possa essere associato all'oggetto in esecuzione. Dopo l'esecuzione dell'oggetto, CustomRpt può accedere a un puntatore a un'interfaccia nel proxy/stub standard, ad esempio [**IPersistFile**](/windows/desktop/api/ObjIdl/nn-objidl-ipersistfile), o all'interfaccia personalizzata ICustomInterface.


```C++
void CustomRpt(char *pszObject) 
{ 
    HRESULT             hr; 
    WCHAR               wszObject[128]; 
    WCHAR               wszMsg[128] = {L"Your Message Here...\n"}; 
    IMoniker            *pmkObject = NULL; 
    IUnknown            *pIUnk = NULL; 
    IPersistFile        *pIPersistFile = NULL; 
    ICustomInterface    *pICustomInterface = NULL; 
 
    // Create a wide-character version of the object's file name. 
    StringCchPrintf(wszObject, 128, L"%hs", pszObject); 
 
    // Get a file moniker for the object (a *.smp file). 
    hr = CreateFileMoniker(wszObject, &pmkObject); 
 
    if(FAILED(hr)) 
    { 
        printf("Client: CreateFileMoniker for Object failed"); 
        return; 
    } 
 
    // BindMoniker is equivalent to calling CreateBindCtx() followed by 
    // a call to BindToObject(). It has the net result of binding the 
    // interface (specified by the IID) to the moniker. 
 
    hr = BindMoniker(pmkObject, 0, IID_IUnknown, (void **)&pIUnk); 
    if (FAILED(hr)) 
    { 
        printf("Client: BindMoniker failed (%x)\n", hr); 
        return; 
    } 
 
    // Try a couple QueryInterface calls into the object code; first a 
    // QueryInterface to IPersistFile... 
 
    hr = pIUnk->QueryInterface(IID_IPersistFile, (void **)&pIPersistFile); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface IPersistFile failed (%x)\n", hr); 
        pIUnk->Release(); 
        return; 
    } 
 
    // Followed by a QueryInterface to ICustomInterface. 
    hr = pIUnk->QueryInterface(IID_ICustomInterface, (void **)&pICustomInterface); 
 
    if (FAILED(hr)) { 
        printf("Client: QueryInterface failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // CustomReport() is the object function that displays the time and 
    // date information on the object. 
    hr = pICustomInterface->CustomReport(); 
 
    if (FAILED(hr)) 
    { 
        printf("Client: pICustomInterface->CustomReport failed (%x)\n", hr); 
        pIUnk->Release(); 
        pIPersistFile->Release(); 
        return; 
    } 
 
    // Clean up resources by calling release on each of the interfaces. 
    pIPersistFile->Release(); 
    pICustomInterface->Release(); 
    pIUnk->Release(); 
    return; 
} 
```



 

 




