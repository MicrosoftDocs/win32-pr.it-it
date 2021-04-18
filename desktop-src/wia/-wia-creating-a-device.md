---
description: "Quando un'applicazione ha l'ID dispositivo di un determinato dispositivo, può chiamare IWiaDevMgr:: CreateDevice o IWiaDevMgr2:: CreateDevicemethod, che crea un albero gerarchico di oggetti IWiaItem o IWiaItem2 che rappresentano un dispositivo di imaging e i letti per l'analisi delle immagini e le cartelle contenute in tale dispositivo."
ms.assetid: 807695c2-4c42-4318-9a5d-d34ac9014f0f
title: Creazione di un dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2622d22a55c4273dcc13cc1421537b94037a3bb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312448"
---
# <a name="creating-a-device"></a><span data-ttu-id="ed4ef-103">Creazione di un dispositivo</span><span class="sxs-lookup"><span data-stu-id="ed4ef-103">Creating a Device</span></span>

<span data-ttu-id="ed4ef-104">Quando un'applicazione ha l'ID dispositivo di un determinato dispositivo, può chiamare il metodo [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), che crea un albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) che rappresentano un dispositivo di imaging e i letti per l'analisi delle immagini e le cartelle contenute in tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ed4ef-104">Once an application has the device ID of a given device, it can call the [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)method, which creates a hierarchical tree of [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) objects that represent an imaging device and the image scanning beds, and folders contained on that device.</span></span>

<span data-ttu-id="ed4ef-105">Nell'esempio seguente di WiaSSamp dell'applicazione di esempio viene implementata una funzione che accetta un ID dispositivo come parametro.</span><span class="sxs-lookup"><span data-stu-id="ed4ef-105">The following example from the sample application WiaSSamp implements a function that takes a device ID as a parameter.</span></span> <span data-ttu-id="ed4ef-106">Per informazioni su come ottenere un ID dispositivo per un dispositivo specifico, vedere [lettura delle proprietà dei dispositivi](-wia-reading-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ed4ef-106">For information about how to obtain a device ID for a particular device, see [Reading Device Properties](-wia-reading-device-properties.md).</span></span>


```
    //XP or earlier:
    HRESULT CreateWiaDevice( IWiaDevMgr *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem **ppWiaDevice ) 
    //Vista or later:
    HRESULT CreateWiaDevice( IWiaDevMgr2 *pWiaDevMgr, BSTR bstrDeviceID, IWiaItem2 **ppWiaDevice ) 
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr || NULL == bstrDeviceID || NULL == ppWiaDevice)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevice = NULL;

        //
        // Create the WIA Device
        //
        HRESULT hr = pWiaDevMgr->CreateDevice( bstrDeviceID, ppWiaDevice );

        //
        // Return the result of creating the device
        //
        return hr;
    }
```



<span data-ttu-id="ed4ef-107">In questo esempio, **pWiaDevMgr** è un puntatore all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e **ppWiaDevice** è una variabile che, dopo la chiamata a [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o a [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contiene l'indirizzo di un puntatore all'elemento radice dell'albero che rappresenta il dispositivo appena creato.</span><span class="sxs-lookup"><span data-stu-id="ed4ef-107">In this example, **pWiaDevMgr** is a pointer to the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interface, and **ppWiaDevice** is a variable that, after the call to [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or to [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contains the address of a pointer to the root item of the tree that represents the newly created device.</span></span>

 

 



