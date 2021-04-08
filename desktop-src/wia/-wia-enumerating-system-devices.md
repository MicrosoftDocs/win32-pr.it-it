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
# <a name="enumerating-system-devices"></a><span data-ttu-id="49fe3-103">Enumerazione dei dispositivi di sistema</span><span class="sxs-lookup"><span data-stu-id="49fe3-103">Enumerating System Devices</span></span>

<span data-ttu-id="49fe3-104">Usare il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) per enumerare i dispositivi Windows Image Acquisition (WIA) installati in un sistema.</span><span class="sxs-lookup"><span data-stu-id="49fe3-104">Use the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method to enumerate the Windows Image Acquisition (WIA) devices installed on a system.</span></span> <span data-ttu-id="49fe3-105">Questo metodo crea un oggetto di enumerazione per le proprietà dei dispositivi e restituisce un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) supportata dall'oggetto di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="49fe3-105">This method creates an enumeration object for the properties of the devices, and returns a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface that the enumeration object supports.</span></span>

<span data-ttu-id="49fe3-106">È quindi possibile usare i metodi dell'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) per ottenere un puntatore di interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) per ogni dispositivo installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="49fe3-106">You can then use the methods of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface to obtain an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface pointer for each device installed on the system.</span></span>

<span data-ttu-id="49fe3-107">Il codice seguente dell'applicazione di esempio WiaSSamp illustra come creare un oggetto di enumerazione per i dispositivi in un sistema ed eseguire l'iterazione su tali dispositivi:</span><span class="sxs-lookup"><span data-stu-id="49fe3-107">The following code from the WiaSSamp sample application demonstrates how to create an enumeration object for the devices on a system and iterate through those devices:</span></span>


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



<span data-ttu-id="49fe3-108">WIA \_ DEVINFO \_ enum \_ local è una costante WIA che rappresenta l'unico valore valido per questo parametro.</span><span class="sxs-lookup"><span data-stu-id="49fe3-108">WIA\_DEVINFO\_ENUM\_LOCAL is a WIA constant that represents the only valid value for this parameter.</span></span>

<span data-ttu-id="49fe3-109">Nell'esempio, il parametro **pWiaDevMgr** punta a un'istanza dell'interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) dopo una precedente chiamata a [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="49fe3-109">In the example, the parameter **pWiaDevMgr** points to an instance of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) interface after a previous call to [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span>

<span data-ttu-id="49fe3-110">L'applicazione chiama il metodo [**IWiaDevMgr:: EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (o [**IWiaDevMgr2:: EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) del puntatore [**IWiaDevMgr (**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) che riempie **PWiaDevMgr** con l'indirizzo di **un puntatore all'** interfaccia [**pWiaEnumDevInfo \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="49fe3-110">The application calls the [**IWiaDevMgr::EnumDeviceInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-enumdeviceinfo) (or [**IWiaDevMgr2::EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)) method of the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) (or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md)) pointer **pWiaDevMgr** that fills **pWiaEnumDevInfo** with the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

<span data-ttu-id="49fe3-111">Se la chiamata ha esito positivo, l'applicazione chiama il metodo [**IEnumWIA \_ dev \_ info:: Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) del puntatore [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="49fe3-111">If the call succeeds, the application then calls the [**IEnumWIA\_DEV\_INFO::Reset**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-reset) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer.</span></span> <span data-ttu-id="49fe3-112">La variabile **pWiaEnumDevInfo** garantisce che l'enumerazione venga avviata dall'inizio.</span><span class="sxs-lookup"><span data-stu-id="49fe3-112">The **pWiaEnumDevInfo** variable ensures that the enumeration starts at the beginning.</span></span>

<span data-ttu-id="49fe3-113">Se la chiamata ha esito positivo, l'applicazione scorre i dispositivi nel sistema chiamando ripetutamente il metodo [**IEnumWIA \_ dev \_ info:: Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) del puntatore [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) **pWiaEnumDevInfo** finché il metodo non restituisce più \_ OK, a indicare che l'enumerazione è stata completata.</span><span class="sxs-lookup"><span data-stu-id="49fe3-113">If this call succeeds, the application iterates through the devices on the system by repeatedly calling the [**IEnumWIA\_DEV\_INFO::Next**](/windows/desktop/api/wia_xp/nf-wia_xp-ienumwia_dev_info-next) method of the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) pointer **pWiaEnumDevInfo** until the method no longer returns S\_OK, indicating that the enumeration is complete.</span></span>

<span data-ttu-id="49fe3-114">Ogni chiamata a **pWiaEnumDevInfo->successiva** riempie **pWiaPropertyStorage** con un puntatore all'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) che contiene le informazioni sulle proprietà per un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="49fe3-114">Each call to **pWiaEnumDevInfo->Next** fills **pWiaPropertyStorage** with a pointer to the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface that contains property information for a specific device.</span></span>

 

 
