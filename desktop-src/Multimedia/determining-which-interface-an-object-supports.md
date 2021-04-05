---
title: Determinazione dell'interfaccia supportata da un oggetto
description: Determinazione dell'interfaccia supportata da un oggetto
ms.assetid: cf2aacb7-5315-4907-a49b-3eb3bbfd13d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 066523503232926f5c031efa2cee5ad7a2b05d24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713792"
---
# <a name="determining-which-interface-an-object-supports"></a><span data-ttu-id="ec949-103">Determinazione dell'interfaccia supportata da un oggetto</span><span class="sxs-lookup"><span data-stu-id="ec949-103">Determining Which Interface an Object Supports</span></span>

<span data-ttu-id="ec949-104">Il metodo **QueryInterface** consente a un'applicazione di eseguire una query su un oggetto per determinare quali interfacce sono supportate.</span><span class="sxs-lookup"><span data-stu-id="ec949-104">The **QueryInterface** method lets an application query an object to determine which interfaces it supports.</span></span> <span data-ttu-id="ec949-105">L'applicazione di esempio imposta il puntatore *PPV* sull'interfaccia corrente.</span><span class="sxs-lookup"><span data-stu-id="ec949-105">The sample application sets the *ppv* pointer to the current interface.</span></span>


```C++
STDMETHODIMP CAVIFileCF::QueryInterface( 
    const IID FAR& iid, 
    void FAR* FAR* ppv) 
{ 
    if (iid == IID_IUnknown) 
        *ppv = this;                     // set the interface pointer 
                                         // to this instance 
    else if (iid == IID_IClassFactory) 
        *ppv = this;                     // second chance to set the 
                                         // interface pointer to this 
                                         // instance 
    else 
        return ResultFromScode(E_NOINTERFACE); 
    AddRef();  //Increment the reference count 
    return NULL; 
} 

```



 

 




