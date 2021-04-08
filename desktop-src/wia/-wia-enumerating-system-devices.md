---
description: 'Usare il metodo IWiaDevMgr:: EnumDeviceInfo (o IWiaDevMgr2:: EnumDeviceInfo) per enumerare i dispositivi Windows Image Acquisition (WIA) installati in un sistema.'
ms.assetid: 6465a33e-1b3b-4142-a58f-b27e9c95cd3e
title: Enumerazione dei dispositivi di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2d65879cd1fc8466f4ada638281ef496636b19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967576"
---
# <a name="enumerating-system-devices"></a>Enumerazione dei dispositivi di sistema

Usare il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) per enumerare i dispositivi Windows Image Acquisition (WIA) installati in un sistema. Questo metodo crea un oggetto di enumerazione per le proprietà dei dispositivi e restituisce un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) supportata dall'oggetto di enumerazione.

È quindi possibile usare i metodi dell'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) per ottenere un puntatore di interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ogni dispositivo installato nel sistema.

Il codice seguente dell'applicazione di esempio WiaSSamp illustra come creare un oggetto di enumerazione per i dispositivi in un sistema ed eseguire l'iterazione su tali dispositivi:


```
    HRESULT EnumerateWiaDevices( IWiaDevMgr *pWiaDevMgr ) //XP or earlier
    HRESULT EnumerateWiaDevices( IWiaDevMgr2 *pWiaDevMgr ) //Vista or later
    
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaDevMgr)
        {
            return E_INVALIDARG;
        }

        //
        // Get a device enumerator interface
        //
        IEnumWIA_DEV_INFO *pWiaEnumDevInfo = NULL;
        HRESULT hr = pWiaDevMgr->EnumDeviceInfo( WIA_DEVINFO_ENUM_LOCAL, &pWiaEnumDevInfo );
        if (SUCCEEDED(hr))
        {
            //
            // Loop until you get an error or pWiaEnumDevInfo->Next returns
            // S_FALSE to signal the end of the list.
            //
            while (S_OK == hr)
            {
                //
                // Get the next device's property storage interface pointer
                //
                IWiaPropertyStorage *pWiaPropertyStorage = NULL;
                hr = pWiaEnumDevInfo->Next( 1, &pWiaPropertyStorage, NULL );

                //
                // pWiaEnumDevInfo->Next will return S_FALSE when the list is
                // exhausted, so check for S_OK before using the returned
                // value.
                //
                if (hr == S_OK)
                {
                    //
                    // Do something with the device's IWiaPropertyStorage*
                    //

                    //
                    // Release the device's IWiaPropertyStorage*
                    //
                    pWiaPropertyStorage->Release();
                    pWiaPropertyStorage = NULL;
                }
            }

            //
            // If the result of the enumeration is S_FALSE (which
            // is normal), change it to S_OK.
            //
            if (S_FALSE == hr)
            {
                hr = S_OK;
            }

            //
            // Release the enumerator
            //
            pWiaEnumDevInfo->Release();
            pWiaEnumDevInfo = NULL;
        }

        //
        // Return the result of the enumeration
        //
        return hr;
    }
```



WIA \_ DEVINFO \_ enum \_ local è una costante WIA che rappresenta l'unico valore valido per questo parametro.

Nell'esempio, il parametro **pWiaDevMgr** punta a un'istanza dell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) dopo una precedente chiamata a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

L'applicazione chiama il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) del puntatore [**IWiaDevMgr (**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) che riempie **PWiaDevMgr** con l'indirizzo di **un puntatore all'** interfaccia [**pWiaEnumDevInfo \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .

Se la chiamata ha esito positivo, l'applicazione chiama il metodo [**IEnumWIA \_ dev \_ info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) del puntatore [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) . La variabile **pWiaEnumDevInfo** garantisce che l'enumerazione venga avviata dall'inizio.

Se la chiamata ha esito positivo, l'applicazione scorre i dispositivi nel sistema chiamando ripetutamente il metodo [**IEnumWIA \_ dev \_ info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) del puntatore [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** finché il metodo non restituisce più \_ OK, a indicare che l'enumerazione è stata completata.

Ogni chiamata a **pWiaEnumDevInfo->successiva** riempie **pWiaPropertyStorage** con un puntatore all'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) che contiene le informazioni sulle proprietà per un dispositivo specifico.

 

 
