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
# <a name="reading-device-properties"></a>Lettura delle proprietà del dispositivo

Le applicazioni usano l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) di un dispositivo per leggere e scrivere le proprietà del dispositivo. **IWiaPropertyStorage** eredita tutti i metodi dell'interfaccia Component Object Model (com) [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage).

Le proprietà del dispositivo includono informazioni su un dispositivo che descrivono le funzionalità e le impostazioni del dispositivo. Per un elenco di queste proprietà, vedere [proprietà del dispositivo](-wia-device-properties.md).

Tra le proprietà del dispositivo lette usando [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) è l'ID del dispositivo, che viene quindi usato per creare un dispositivo Windows Image Acquisition (WIA). Per ulteriori informazioni, vedere [**IWiaDevMgr:: CreateDevice**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-createdevice) (o [**IWiaDevMgr2:: CreateDevice**](-wia-iwiadevmgr2-createdevice.md)).

L'esempio seguente legge l'ID del dispositivo, il nome del dispositivo e la descrizione del dispositivo dalla matrice di proprietà del dispositivo e stampa tali proprietà nella console.


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



In questo esempio, l'applicazione imposta le matrici [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) (rispettivamente **Campo PROPSPEC** e **PropVar**) in modo da mantenere le informazioni sulle proprietà. Queste matrici vengono passate come parametri nella chiamata al metodo [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del puntatore [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) **pIWiaPropStg**. Ogni elemento della matrice **Campo PROPSPEC** contiene il tipo e il nome di una proprietà del dispositivo. Al momento della restituzione, ogni elemento di **PropVar** contiene il valore della proprietà Device rappresentata dall'elemento corrispondente della matrice **Campo PROPSPEC** .

L'applicazione chiama quindi la proprietà [IPropertyStorage:: ReadMultiple](/windows/win32/api/propidlbase/nf-propidlbase-ipropertystorage-readmultiple) del [](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) puntatore IWiaPropertyStorage **pWiaPropertyStorage** per recuperare le informazioni sulla proprietà.

La tecnica utilizzata per leggere e impostare le proprietà del dispositivo è identica a quella per le proprietà degli elementi, l'unica differenza è il tipo di elemento WIA su cui vengono chiamati i metodi appropriati. Per un elenco delle proprietà degli elementi, vedere [proprietà degli elementi](-wia-item-properties.md).

 

 
