---
description: Usare i metodi dell'interfaccia IWiaDataTransfer per trasferire dati da un dispositivo wi-Windows Image Acquisition (WIA) 1.0 a un'applicazione.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Trasferimento di dati immagine in WIA 1.0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e2c1dfce551f105b0df1627f11e9b4ccb7ee8a420e395f3fd0cc1ba932f136
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813671"
---
# <a name="transferring-image-data-in-wia-10"></a>Trasferimento di dati immagine in WIA 1.0

> [!Note]  
> Questa esercitazione riguarda il trasferimento di dati immagine in applicazioni che verranno eseguite Windows XP o versioni precedenti. Per informazioni sul trasferimento dei dati immagine nelle applicazioni che verranno eseguite in Windows Vista o versioni successive, vedere Trasferimento di dati immagine in [WIA 2.0.](-wia-transferring-image-data-in-wia2.md)

 

Usare i metodi [**dell'interfaccia IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) per trasferire dati da un dispositivo wi-Windows Image Acquisition (WIA) 1.0 a un'applicazione. Questa interfaccia supporta una finestra di memoria condivisa per trasferire i dati dall'oggetto dispositivo all'applicazione ed eliminare le copie di dati non necessarie durante il marshalling.

Le applicazioni devono eseguire query su un elemento immagine per ottenere un puntatore alla relativa [**interfaccia IWiaDataTransfer,**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) come nell'esempio di codice seguente:


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



Nel codice precedente si presuppone che **pWiaItem** sia un puntatore valido [**all'interfaccia IWiaItem.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) La chiamata a [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) riempie **pWiaDataTransfer** con un puntatore all'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) dell'elemento a cui fa riferimento **pWiaItem**.

L'applicazione imposta quindi i [membri della struttura STGMEDIUM.](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) Per informazioni, vedere STGMEDIUM e [TYMED.](/windows/win32/api/objidl/ne-objidl-tymed)


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



Se si specifica un nome file, deve includere l'estensione di file appropriata. WIA 1.0 non fornisce estensioni di file. Se il membro **lpszFileName** di **StgMedium** è **NULL,** WIA 1.0 genera un nome file casuale e un percorso per i dati trasferiti. Spostare o copiare questo file prima di chiamare ReleaseStgMedium, perché questa funzione eliminerà il file.

L'applicazione chiama quindi il [**metodo IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) per eseguire il trasferimento dei dati:


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



Nella chiamata a [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)il secondo parametro specifica un puntatore [**all'interfaccia IWiaDataCallback.**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) Le applicazioni devono implementare questa interfaccia per ricevere callback durante i trasferimenti di dati. Per informazioni sull'implementazione di questa interfaccia, vedere [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).

L'applicazione rilascia quindi i puntatori [**all'interfaccia IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) e libera tutti i dati allocati nella [struttura STGMEDIUM.](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1)

L'applicazione può anche trasferire l'immagine usando i trasferimenti di dati in memoria anziché i trasferimenti di file. In questo caso, l'applicazione usa il metodo idtGetBandedData al posto del metodo idtGetData.

Ecco l'esempio completo di trasferimento dei dati:


```
HRESULT TransferWiaItem( IWiaItem *pWiaItem )
{
    //
    // Validate arguments
    //
    if (NULL == pWiaItem)
    {
        return E_INVALIDARG;
    }

    //
    // Get the IWiaPropertyStorage interface so you can set required properties.
    //
    IWiaPropertyStorage *pWiaPropertyStorage = NULL;
    HRESULT hr = pWiaItem->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaPropertyStorage );
    if (SUCCEEDED(hr))
    {
        //
        // Prepare PROPSPECs and PROPVARIANTs for setting the
        // media type and format
        //
        PROPSPEC PropSpec[2] = {0};
        PROPVARIANT PropVariant[2] = {0};
        const ULONG c_nPropCount = sizeof(PropVariant)/sizeof(PropVariant[0]);

        //
        // Use BMP as the output format
        //
        GUID guidOutputFormat = WiaImgFmt_BMP;

        //
        // Initialize the PROPSPECs
        //
        PropSpec[0].ulKind = PRSPEC_PROPID;
        PropSpec[0].propid = WIA_IPA_FORMAT;
        PropSpec[1].ulKind = PRSPEC_PROPID;
        PropSpec[1].propid = WIA_IPA_TYMED;

        //
        // Initialize the PROPVARIANTs
        //
        PropVariant[0].vt = VT_CLSID;
        PropVariant[0].puuid = &guidOutputFormat;
        PropVariant[1].vt = VT_I4;
        PropVariant[1].lVal = TYMED_FILE;

        //
        // Set the properties
        //
        hr = pWiaPropertyStorage->WriteMultiple( c_nPropCount, PropSpec, PropVariant, WIA_IPA_FIRST );
        if (SUCCEEDED(hr))
        {
            //
            // Get the IWiaDataTransfer interface
            //
            IWiaDataTransfer *pWiaDataTransfer = NULL;
            hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
            if (SUCCEEDED(hr))
            {
                //
                // Create our callback class
                //
                CWiaDataCallback *pCallback = new CWiaDataCallback;
                if (pCallback)
                {
                    //
                    // Get the IWiaDataCallback interface from our callback class.
                    //
                    IWiaDataCallback *pWiaDataCallback = NULL;
                    hr = pCallback->QueryInterface( IID_IWiaDataCallback, (void**)&pWiaDataCallback );
                    if (SUCCEEDED(hr))
                    {
                        //
                        // Perform the transfer using default settings
                        //
                        STGMEDIUM stgMedium = {0};
                        StgMedium.tymed = TYMED_FILE;
                        hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
                        if (S_OK == hr)
                        {
                            //
                            // Print the filename (note that this filename is always
                            // a WCHAR string, not TCHAR).
                            //
                            _tprintf( TEXT("Transferred filename: %ws\n"), stgMedium.lpszFileName );

                            //
                            // Release any memory associated with the stgmedium
                            // This will delete the file stgMedium.lpszFileName.
                            //
                            ReleaseStgMedium( &stgMedium );
                        }

                        //
                        // Release the callback interface
                        //
                        pWiaDataCallback->Release();
                        pWiaDataCallback = NULL;
                    }

                    //
                    // Release our callback.  It should now delete itself.
                    //
                    pCallback->Release();
                    pCallback = NULL;
                }

                //
                // Release the IWiaDataTransfer
                //
                pWiaDataTransfer->Release();
                pWiaDataTransfer = NULL;
            }
        }

        //
        // Release the IWiaPropertyStorage
        //
        pWiaPropertyStorage->Release();
        pWiaPropertyStorage = NULL;
    }

    return hr;
}
```



 

 
