---
description: Poiché il trasferimento dei dati di immagine è basato sul flusso in Windows Image Acquisition (WIA) 2,0, non è necessario specificare un tipo di destinazione, ad esempio
ms.assetid: ebb9fce5-9450-4ffe-b480-b21670b60f90
title: Trasferimento dei dati di immagine in WIA 2,0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85ded5c6cd8fb94b1beccd86c3cd8aef3018aed0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343656"
---
# <a name="transferring-image-data-in-wia-20"></a>Trasferimento dei dati di immagine in WIA 2,0

> [!Note]  
> In questa esercitazione viene illustrato come trasferire i dati delle immagini in applicazioni eseguite in Windows Vista o versioni successive. Per informazioni sul trasferimento di dati immagine in applicazioni eseguite in Windows XP o versioni precedenti, vedere [trasferimento di dati di immagine in WIA 1,0](-wia-transferring-image-data.md) .

 

Poiché il trasferimento dei dati di immagine è basato sul flusso in Windows Image Acquisition (WIA) 2,0, non è necessario specificare un tipo di destinazione (ad esempio memoria o file). L'applicazione fornisce semplicemente a WIA 2,0 il flusso da usare e il driver legge o scrive nel flusso. Il flusso può essere un flusso di file, un flusso di memoria o qualsiasi altro tipo di flusso ed è trasparente per il driver. L'uso dei flussi fornisce anche una facile integrazione con il filtro di elaborazione delle immagini.

Usare i metodi dell'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) per trasferire i dati da un dispositivo WIA 2,0 a un'applicazione. Questa interfaccia è disponibile tramite l'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) . L'interfaccia **IWiaTransfer** dispone di metodi per richiedere il caricamento o il download di dati da e verso un dispositivo. Questi metodi accettano un callback fornito dall'applicazione e usano un [IStream](/windows/win32/api/objidl/nn-objidl-istream) fornito dall'applicazione per la destinazione effettiva del trasferimento dei dati.

Le applicazioni devono eseguire una query su un elemento di immagine per ottenere un puntatore alla relativa interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) , come illustrato nell'esempio di codice seguente:


```
    // Get the IWiaTransfer interface
    //
    IWiaTransfer *pWiaTransfer = NULL;
    hr = pIWiaItem2->QueryInterface(IID_IWiaTransfer,(void**)&pWiaTransfer);
```



Nel codice precedente si presuppone che **pWiaItem2** sia un puntatore valido all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) . La chiamata a [IUnknown:: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) Compila **pWiaTransfer** con un puntatore all'interfaccia [**IWiaTransfer**](-wia-iwiatransfer.md) dell'elemento a cui fa riferimento **pWiaItem2**.

L'applicazione crea quindi un'istanza dell'oggetto callback, come illustrato di seguito.


```
    //   Instantiate the object which receives the callbacks
    //
    CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
```



L'applicazione imposta quindi le proprietà usando l'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) dell'elemento [**IWiaItem2**](-wia-iwiaitem2.md) ed esegue il trasferimento.

Download


```
    // Download   
    hr = pWiaTransfer->Download(0,pWiaClassCallback);
```



Caricamento


```
    //Create child item which eventually will be the uploaded image 
    IWiaItem2* pWiaItemChild = NULL;
    HRESULT hr = pIWiaItem2->CreateChildItem(WiaItemTypeImage|WiaItemTypeFile,0,bzUploadFileName,&pWiaItemChild);
    
    if(SUCCEEDED(hr))
    {
                
        //Set the format for the child item as BMP 
        IWiaPropertyStorage* pWiaChildPropertyStorage = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaPropertyStorage, (void**)&pWiaChildPropertyStorage );
        if(SUCCEEDED(hr))
        {
            WritePropertyGuid(pWiaChildPropertyStorage,WIA_IPA_FORMAT,WiaImgFmt_BMP );

            //release pWiaChildPropertyStorage
            pWiaChildPropertyStorage->Release();
            pWiaChildPropertyStorage = NULL;
        }
        

        //Get the IWiaTransfer interface of the child
        IWiaTransfer* pWiaTransferChild = NULL;
        hr = pWiaItemChild->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransferChild );
        if(SUCCEEDED(hr)){
            IStream* pUploadStream = NULL;
                                        
            //Create stream on test.BMP file
            hr = SHCreateStreamOnFile(L"test.BMP",STGM_READ, &pUploadStream);
            if(SUCCEEDED(hr)){
                pWiaTransferChild->Upload(0,pUploadStream,pWiaClassCallback);
                
            }
         }
   
      }
```



Di seguito è riportato l'esempio completo di trasferimento dei dati:


```
HRESULT TransferWiaItem( IWiaItem2 *pIWiaItem2)
{
    // Validate arguments
    if (NULL == pIWiaItem2)
    {
        _tprintf(TEXT("\nInvalid parameters passed"));
        return E_INVALIDARG;
    }
    
    // Get the IWiaTransfer interface
    IWiaTransfer *pWiaTransfer = NULL;
    HRESULT hr = pIWiaItem2->QueryInterface( IID_IWiaTransfer, (void**)&pWiaTransfer );
    if (SUCCEEDED(hr))
    {
        // Create our callback class
        CWiaTransferCallback *pWiaClassCallback = new CWiaTransferCallback;
        if (pWiaClassCallback)
        {
            
              LONG lItemType = 0;
              hr = pIWiaItem2->GetItemType( &lItemType );

              //download all items which have WiaItemTypeTransfer flag set
              if(lItemType & WiaItemTypeTransfer)
              {

                  // If it is a folder, do folder download . Hence with one API call, all the leaf nodes of this folder 
                  // will be transferred
                  if ((lItemType & WiaItemTypeFolder))
                  {
                        _tprintf ( L"\nI am a folder item");
                        hr = pWiaTransfer->Download(WIA_TRANSFER_ACQUIRE_CHILDREN, pWiaClassCallback);
                        if(S_OK == hr)
                        {
                            _tprintf(TEXT("\npWiaTransfer->Download() on folder item SUCCEEDED"));
                        }
                        else if(S_FALSE == hr)
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item returned S_FALSE. Folder may not be having child items"),hr);
                        }
                        else if(FAILED(hr))
                        {
                            ReportError(TEXT("\npWiaTransfer->Download() on folder item failed"),hr);
                        }
                   }

                  
                  // If this is an file type, do file download
                  else if (lItemType & WiaItemTypeFile )
                  {
                      hr = pWiaTransfer->Download(0,pWiaClassCallback);
                      if(S_OK == hr)
                      {
                          _tprintf(TEXT("\npWiaTransfer->Download() on file item SUCCEEDED"));
                      }
                      else if(S_FALSE == hr)
                      {
                          ReportError(TEXT("\npWiaTransfer->Download() on file item returned S_FALSE. File may be empty"),hr);
                      }
                      else if(FAILED(hr))
                      {
                         ReportError(TEXT("\npWiaTransfer->Download() on file item failed"),hr);
                      }
                  }                     
                }
                
                // Release our callback.  It should now delete itself.
                pWiaClassCallback->Release();
                pWiaClassCallback = NULL;
        }
        else
        {
            ReportError( TEXT("\nUnable to create CWiaTransferCallback class instance") );
        }
            
        // Release the IWiaTransfer
        pWiaTransfer->Release();
        pWiaTransfer = NULL;
    }
    else
    {
        ReportError( TEXT("\npIWiaItem2->QueryInterface failed on IID_IWiaTransfer"), hr );
    }
    return hr;
}

// Callback Class should be something like this:

class CWiaTransferCallback : public IWiaTransferCallback
{
public: // Constructors, destructor
    CWiaTransferCallback () : m_cRef(1) {};
    ~ CWiaTransferCallback () {};

public: // IWiaTransferCallback
    HRESULT __stdcall TransferCallback(
        LONG                lFlags,
        WiaTransferParams   *pWiaTransferParams)
    {
        HRESULT hr = S_OK;

        switch (pWiaTransferParams->lMessage)
        {
            case WIA_TRANSFER_MSG_STATUS:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_STREAM:
                ...
                break;
            case WIA_TRANSFER_MSG_END_OF_TRANSFER:
                ...
                break;
            default:
                break;
        }

        return hr;
    }

    HRESULT __stdcall GetNextStream(
        LONG    lFlags,
        BSTR    bstrItemName,
        BSTR    bstrFullItemName,
        IStream **ppDestination)
    {

        HRESULT hr = S_OK;

        //  Return a new stream for this item's data.
        //
        hr = CreateDestinationStream(bstrItemName, ppDestination);
        return hr;
    }

public: // IUnknown
        .
        .
        . // Etc.

private:
    /// For ref counting implementation
    LONG                m_cRef;
};

```



 

 
