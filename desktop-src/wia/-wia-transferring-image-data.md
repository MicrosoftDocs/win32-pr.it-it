---
description: Usare i metodi dell'interfaccia IWiaDataTransfer per trasferire i dati da un dispositivo Windows Image Acquisition (WIA) 1,0 a un'applicazione.
ms.assetid: 67fbf3d9-6965-4464-b04c-10989b2fd55d
title: Trasferimento dei dati di immagine in WIA 1,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00fc7ff76576b6c140358f9af3a0f9d17d4b180e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129395"
---
# <a name="transferring-image-data-in-wia-10"></a><span data-ttu-id="4d382-103">Trasferimento dei dati di immagine in WIA 1,0</span><span class="sxs-lookup"><span data-stu-id="4d382-103">Transferring Image Data in WIA 1.0</span></span>

> [!Note]  
> <span data-ttu-id="4d382-104">Questa esercitazione riguarda il trasferimento dei dati immagine nelle applicazioni che eseguiranno Windows XP o versioni precedenti.</span><span class="sxs-lookup"><span data-stu-id="4d382-104">This tutorial is about transferring image data in applications that will run Windows XP or earlier.</span></span> <span data-ttu-id="4d382-105">Per informazioni sul trasferimento di dati di immagini in applicazioni che vengono eseguite in Windows Vista o versioni successive, vedere [trasferimento di dati immagine in WIA 2,0](-wia-transferring-image-data-in-wia2.md) .</span><span class="sxs-lookup"><span data-stu-id="4d382-105">See [Transferring Image Data in WIA 2.0](-wia-transferring-image-data-in-wia2.md) for information about transferring image data in applications that will run on Windows Vista or later.</span></span>

 

<span data-ttu-id="4d382-106">Usare i metodi dell'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) per trasferire i dati da un dispositivo Windows Image Acquisition (WIA) 1,0 a un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4d382-106">Use the methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface to transfer data from a Windows Image Acquisition (WIA) 1.0 device to an application.</span></span> <span data-ttu-id="4d382-107">Questa interfaccia supporta una finestra di memoria condivisa per trasferire i dati dall'oggetto dispositivo all'applicazione ed eliminare le copie di dati non necessarie durante il marshalling.</span><span class="sxs-lookup"><span data-stu-id="4d382-107">This interface supports a shared memory window to transfer data from the device object to the application and eliminate unnecessary data copies during marshalling.</span></span>

<span data-ttu-id="4d382-108">Le applicazioni devono eseguire una query su un elemento di immagine per ottenere un puntatore alla relativa interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) , come nell'esempio di codice seguente:</span><span class="sxs-lookup"><span data-stu-id="4d382-108">Applications must query an image item to obtain a pointer to its [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface, as in the following code sample:</span></span>


```
    // Get the IWiaDataTransfer interface
    //
    IWiaDataTransfer *pWiaDataTransfer = NULL;
    hr = pWiaItem->QueryInterface( IID_IWiaDataTransfer, (void**)&pWiaDataTransfer );
```



<span data-ttu-id="4d382-109">Nel codice precedente si presuppone che **pWiaItem** sia un puntatore valido all'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) .</span><span class="sxs-lookup"><span data-stu-id="4d382-109">In the previous code, it is assumed that **pWiaItem** is a valid pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface.</span></span> <span data-ttu-id="4d382-110">La chiamata a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Compila **pWiaDataTransfer** con un puntatore all'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) dell'elemento a cui fa riferimento **pWiaItem**.</span><span class="sxs-lookup"><span data-stu-id="4d382-110">The call to [IUnknown::QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) fills **pWiaDataTransfer** with a pointer to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface of the item referred to by **pWiaItem**.</span></span>

<span data-ttu-id="4d382-111">L'applicazione imposta quindi i membri della struttura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="4d382-111">The application then sets the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure members.</span></span> <span data-ttu-id="4d382-112">Per informazioni, vedere STGMEDIUM e [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span><span class="sxs-lookup"><span data-stu-id="4d382-112">For information, see STGMEDIUM and [TYMED](/windows/win32/api/objidl/ne-objidl-tymed).</span></span>


```
    // Set storage medium
    //
    STGMEDIUM StgMedium = {0};
    StgMedium.tymed = TYMED_FILE;
```



<span data-ttu-id="4d382-113">Se si specifica un nome file, deve includere l'estensione di file appropriata; WIA 1,0 non fornisce estensioni di file.</span><span class="sxs-lookup"><span data-stu-id="4d382-113">If you supply a filename, it should include the proper file extension; WIA 1.0 does not provide file extensions.</span></span> <span data-ttu-id="4d382-114">Se il membro **lpszFileName** di **StgMedium** è **null**, WIA 1,0 genera un percorso e un nome file casuali per i dati trasferiti.</span><span class="sxs-lookup"><span data-stu-id="4d382-114">If the **lpszFileName** member of **StgMedium** is **NULL**, WIA 1.0 generates a random file name and path for the transferred data.</span></span> <span data-ttu-id="4d382-115">Spostare o copiare questo file prima di chiamare ReleaseStgMedium, perché questa funzione eliminerà il file.</span><span class="sxs-lookup"><span data-stu-id="4d382-115">Move or copy this file before calling ReleaseStgMedium, because this function will delete the file.</span></span>

<span data-ttu-id="4d382-116">L'applicazione chiama quindi il metodo [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) per eseguire il trasferimento dei dati:</span><span class="sxs-lookup"><span data-stu-id="4d382-116">The application then calls the [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata) method to run the data transfer:</span></span>


```
    // Perform the transfer
    //
    hr = pWiaDataTransfer->idtGetData( &stgMedium, pWiaDataCallback );
```



<span data-ttu-id="4d382-117">Nella chiamata a [**IWiaDataTransfer:: idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), il secondo parametro specifica un puntatore all'interfaccia [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) .</span><span class="sxs-lookup"><span data-stu-id="4d382-117">In the call to [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), the second parameter specifies a pointer to the [**IWiaDataCallback**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatacallback) interface.</span></span> <span data-ttu-id="4d382-118">Le applicazioni devono implementare questa interfaccia per ricevere callback durante i trasferimenti di dati.</span><span class="sxs-lookup"><span data-stu-id="4d382-118">Applications must implement this interface to receive callbacks during data transfers.</span></span> <span data-ttu-id="4d382-119">Per informazioni sull'implementazione di questa interfaccia, vedere [**IWiaDataCallback:: BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="4d382-119">For information about implementing this interface, see [**IWiaDataCallback::BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

<span data-ttu-id="4d382-120">L'applicazione rilascia quindi i puntatori all'interfaccia [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) e libera tutti i dati allocati nella struttura [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) .</span><span class="sxs-lookup"><span data-stu-id="4d382-120">The application then releases the pointers to the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface and frees any data allocated in the [STGMEDIUM](/windows/win32/api/objidl/ns-objidl-ustgmedium-r1) structure.</span></span>

<span data-ttu-id="4d382-121">L'applicazione può anche trasferire l'immagine usando i trasferimenti di dati in memoria invece dei trasferimenti di file.</span><span class="sxs-lookup"><span data-stu-id="4d382-121">The application can also transfer the image using in-memory data transfers instead of file transfers.</span></span> <span data-ttu-id="4d382-122">In questo caso, l'applicazione usa il metodo idtGetBandedData al posto del metodo idtGetData.</span><span class="sxs-lookup"><span data-stu-id="4d382-122">In this case, the application uses the idtGetBandedData method in place of the idtGetData method.</span></span>

<span data-ttu-id="4d382-123">Di seguito è riportato l'esempio completo di trasferimento dei dati:</span><span class="sxs-lookup"><span data-stu-id="4d382-123">Here is the complete data transfer sample:</span></span>


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



 

 
