---
description: Il primo passaggio per l'utilizzo dei servizi Windows Image Acquisition (WIA) consiste nell'ottenere un puntatore a interfaccia IWiaDevMgr (se si sta programmando per Windows XP o versione precedente) o un puntatore all'interfaccia IWiaDevMgr2 (se si sta programmando per Windows Vista o versione successiva).
ms.assetid: 8f20c64a-db79-4c3c-a544-685ed82143bb
title: Creazione di un Gestione dispositivi WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e315939566eea6fe8a4acabeb5fd8afe247c30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312449"
---
# <a name="creating-a-wia-device-manager"></a>Creazione di un Gestione dispositivi WIA

Il primo passaggio per l'utilizzo dei servizi Windows Image Acquisition (WIA) consiste nell'ottenere un puntatore a interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (se si sta programmando per Windows XP o versione precedente) o un puntatore all'interfaccia [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) (se si sta programmando per Windows Vista o versione successiva). A tale scopo, chiamare [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) con i parametri appropriati. L'applicazione di esempio WiaSSamp crea una gestione dispositivi in una funzione globale implementata dal codice seguente:


```
    HRESULT CreateWiaDeviceManager( IWiaDevMgr **ppWiaDevMgr ) //XP or earlier
    HRESULT CreateWiaDeviceManager( IWiaDevMgr2 **ppWiaDevMgr ) //Vista or later
    {
        //
        // Validate arguments
        //
        if (NULL == ppWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Initialize out variables
        //
        *ppWiaDevMgr = NULL;

        //
        // Create an instance of the device manager
        //
        
        //XP or earlier:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr, (void**)ppWiaDevMgr );

        //Vista or later:
        HRESULT hr = CoCreateInstance( CLSID_WiaDevMgr2, NULL, CLSCTX_LOCAL_SERVER, IID_IWiaDevMgr2, (void**)ppWiaDevMgr ); 

        //
        // Return the result of creating the device manager
        //
        return hr;
    }
```



In questo esempio CLSID \_ WiaDevMgr e IID \_ IWiaDevMgr sono costanti WIA che rappresentano rispettivamente l'ID della classe e l'ID di interfaccia di [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr). CLSID \_ WiaDevMgr2 ed IID \_ IWiaDevMgr2 sono costanti WIA che rappresentano rispettivamente l'ID della classe e l'ID di interfaccia di [**IWiaDevMgr2**](-wia-iwiadevmgr2.md).

Il valore dell'argomento *dwClsContext* della chiamata [COCREATEINSTANCE](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) deve essere CLSCTX \_ Local \_ Server. Nessun altro tipo di server è supportato e Component Object Model (COM) rifiuta qualsiasi altro valore per questo parametro.

 

 
