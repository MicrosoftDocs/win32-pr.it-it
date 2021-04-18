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
# <a name="creating-a-device"></a>Creazione di un dispositivo

Quando un'applicazione ha l'ID dispositivo di un determinato dispositivo, può chiamare il metodo [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md), che crea un albero gerarchico di oggetti [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**IWiaItem2**](-wia-iwiaitem2.md) che rappresentano un dispositivo di imaging e i letti per l'analisi delle immagini e le cartelle contenute in tale dispositivo.

Nell'esempio seguente di WiaSSamp dell'applicazione di esempio viene implementata una funzione che accetta un ID dispositivo come parametro. Per informazioni su come ottenere un ID dispositivo per un dispositivo specifico, vedere [lettura delle proprietà dei dispositivi](-wia-reading-device-properties.md).


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



In questo esempio, **pWiaDevMgr** è un puntatore all'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) e **ppWiaDevice** è una variabile che, dopo la chiamata a [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o a [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)), contiene l'indirizzo di un puntatore all'elemento radice dell'albero che rappresenta il dispositivo appena creato.

 

 



