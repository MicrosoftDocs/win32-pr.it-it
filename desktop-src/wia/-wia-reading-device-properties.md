---
description: Le applicazioni usano l'interfaccia IWiaPropertyStorage di un dispositivo per leggere e scrivere le proprietà del dispositivo. IWiaPropertyStorage eredita tutti i metodi dell'interfaccia Component Object Model (COM) IPropertyStorage.
ms.assetid: 65ca9e71-9a0f-495f-b78c-3b1a8d66ee33
title: Lettura delle proprietà del dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 235ba701ed3356e09070709f3c99f2826c69c8c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966717"
---
# <a name="reading-device-properties"></a><span data-ttu-id="a9c74-104">Lettura delle proprietà del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a9c74-104">Reading Device Properties</span></span>

<span data-ttu-id="a9c74-105">Le applicazioni usano l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) di un dispositivo per leggere e scrivere le proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9c74-105">Applications use a device's [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface to read and write device properties.</span></span> <span data-ttu-id="a9c74-106">**IWiaPropertyStorage** eredita tutti i metodi dell'interfaccia Component Object Model (com) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span><span class="sxs-lookup"><span data-stu-id="a9c74-106">**IWiaPropertyStorage** inherits all of the methods of the Component Object Model (COM) interface [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).</span></span>

<span data-ttu-id="a9c74-107">Le proprietà del dispositivo includono informazioni su un dispositivo che descrivono le funzionalità e le impostazioni del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9c74-107">Device properties include information about a device that describe the device's capabilities and settings.</span></span> <span data-ttu-id="a9c74-108">Per un elenco di queste proprietà, vedere [proprietà del dispositivo](-wia-device-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a9c74-108">For a list of these properties, see [Device Properties](-wia-device-properties.md).</span></span>

<span data-ttu-id="a9c74-109">Tra le proprietà del dispositivo lette usando [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) è l'ID del dispositivo, che viene quindi usato per creare un dispositivo Windows Image Acquisition (WIA).</span><span class="sxs-lookup"><span data-stu-id="a9c74-109">Among the device properties that are read using [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) is the device ID, that is then used to create a Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="a9c74-110">Per ulteriori informazioni, vedere [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span><span class="sxs-lookup"><span data-stu-id="a9c74-110">For more information, see [**IWiaDevMgr::CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (or [**IWiaDevMgr2::CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).</span></span>

<span data-ttu-id="a9c74-111">L'esempio seguente legge l'ID del dispositivo, il nome del dispositivo e la descrizione del dispositivo dalla matrice di proprietà del dispositivo e stampa tali proprietà nella console.</span><span class="sxs-lookup"><span data-stu-id="a9c74-111">The following example reads the device ID, the device name, and the device description from the array of device properties, and prints these properties to the console.</span></span>


```
    HRESULT ReadSomeWiaProperties( IWiaPropertyStorage *pWiaPropertyStorage )
    {
        //
        // Validate arguments
        //
        if (NULL == pWiaPropertyStorage)
        {
            return E_INVALIDARG;
        }

        //
        // Declare PROPSPECs and PROPVARIANTs, and initialize them to zero.
        //
        PROPSPEC PropSpec[3] = {0};
        PROPVARIANT PropVar[3] = {0};

        //
        // How many properties are you querying for?
        //
        const ULONG c_nPropertyCount = sizeof(PropSpec)/sizeof(PropSpec[0]);

        //
        // Define which properties you want to read:
        // Device ID.  This is what you would use to create
        // the device.
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_DIP_DEV_ID;

        //
        // Device Name
        //
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_DIP_DEV_NAME;

        //
        // Device description
        //
        PropSpec[2].ulKind = PRSPEC_PROPID;
        PropSpec[2].propid = WIA_DIP_DEV_DESC;

        //
        // Ask for the property values
        //
        HRESULT hr = pWiaPropertyStorage->ReadMultiple( c_nPropertyCount, PropSpec, PropVar );
        if (SUCCEEDED(hr))
        {
            //
            // IWiaPropertyStorage::ReadMultiple will return S_FALSE if some
            // properties could not be read, so you have to check the return
            // types for each requested item.
            //

            //
            // Check the return type for the device ID
            //
            if (VT_BSTR == PropVar[0].vt)
            {
                //
                // Do something with the device ID
                //
                _tprintf( TEXT("WIA_DIP_DEV_ID: %ws\n"), PropVar[0].bstrVal );
            }

            //
            // Check the return type for the device name
            //
            if (VT_BSTR == PropVar[1].vt)
            {
                //
                // Do something with the device name
                //
                _tprintf( TEXT("WIA_DIP_DEV_NAME: %ws\n"), PropVar[1].bstrVal );
            }

            //
            // Check the return type for the device description
            //
            if (VT_BSTR == PropVar[2].vt)
            {
                //
                // Do something with the device description
                //
                _tprintf( TEXT("WIA_DIP_DEV_DESC: %ws\n"), PropVar[2].bstrVal );
            }

            //
            // Free the returned PROPVARIANTs
            //
            FreePropVariantArray( c_nPropertyCount, PropVar );
        }

        //
        // Return the result of reading the properties
        //
        return hr;
    }
```



<span data-ttu-id="a9c74-112">In questo esempio, l'applicazione imposta le matrici [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (rispettivamente **Campo PROPSPEC** e **PropVar**) in modo da mantenere le informazioni sulle proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9c74-112">In this example, the application sets up [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) arrays (**PropSpec** and **PropVar**, respectively) to hold property information.</span></span> <span data-ttu-id="a9c74-113">Queste matrici vengono passate come parametri nella chiamata al metodo [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del puntatore [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**.</span><span class="sxs-lookup"><span data-stu-id="a9c74-113">These arrays are passed as parameters in the call to [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) method of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pIWiaPropStg**.</span></span> <span data-ttu-id="a9c74-114">Ogni elemento della matrice **Campo PROPSPEC** contiene il tipo e il nome di una proprietà del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a9c74-114">Each element of the **PropSpec** array contains the type and name of a device property.</span></span> <span data-ttu-id="a9c74-115">Al momento della restituzione, ogni elemento di **PropVar** contiene il valore della proprietà Device rappresentata dall'elemento corrispondente della matrice **Campo PROPSPEC** .</span><span class="sxs-lookup"><span data-stu-id="a9c74-115">Upon return, each element of the **PropVar** contains the value of the device property represented by the corresponding element of the **PropSpec** array.</span></span>

<span data-ttu-id="a9c74-116">L'applicazione chiama quindi la proprietà [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del [](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) puntatore IWiaPropertyStorage **pWiaPropertyStorage** per recuperare le informazioni sulla proprietà.</span><span class="sxs-lookup"><span data-stu-id="a9c74-116">The application then calls [IPropertyStorage::ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) property of the [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) pointer **pWiaPropertyStorage** to retrieve the property information.</span></span>

<span data-ttu-id="a9c74-117">La tecnica utilizzata per leggere e impostare le proprietà del dispositivo è identica a quella per le proprietà degli elementi, l'unica differenza è il tipo di elemento WIA su cui vengono chiamati i metodi appropriati.</span><span class="sxs-lookup"><span data-stu-id="a9c74-117">The technique used to read and set device properties is the same as that for item properties, the only difference is the type of the WIA item on which you call the appropriate methods.</span></span> <span data-ttu-id="a9c74-118">Per un elenco delle proprietà degli elementi, vedere [proprietà degli elementi](-wia-item-properties.md).</span><span class="sxs-lookup"><span data-stu-id="a9c74-118">For a list of item properties, see [Item Properties](-wia-item-properties.md).</span></span>

 

 
