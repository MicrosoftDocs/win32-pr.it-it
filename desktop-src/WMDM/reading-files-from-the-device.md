---
title: Lettura di file dal dispositivo
description: Lettura di file dal dispositivo
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Gestione dispositivi multimediali, lettura di file dai dispositivi
- Gestione dispositivi, lettura di file dai dispositivi
- guida alla programmazione, lettura di file dai dispositivi
- applicazioni desktop, lettura di file dai dispositivi
- creazione Windows applicazioni di Gestione dispositivi multimediali, lettura di file dai dispositivi
- lettura di file dai dispositivi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904001"
---
# <a name="reading-files-from-the-device"></a>Lettura di file dal dispositivo

Dopo aver trovato un file che si vuole copiare dal dispositivo, è possibile copiare il file dal dispositivo al computer in un'unica chiamata o usare un callback per fare in modo che i byte del file leggono direttamente nell'applicazione, che può quindi elaborare o archiviare i dati nel modo più adatto.

La procedura seguente illustra il modo di base per copiare un file da un dispositivo in un'unica chiamata:

1.  Ottenere un handle per il file nel dispositivo. È possibile ottenere l'handle usando una ricerca ricorsiva di file o, se si conosce l'ID permanente della risorsa di archiviazione, chiamando [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage). In entrambi i casi, è necessaria [**l'interfaccia IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) dell'oggetto.
2.  Determinare se l'archiviazione è un file o una cartella. Solo i file possono essere copiati dal dispositivo. Chiamare [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) per ottenere gli attributi di archiviazione, che indica se l'archiviazione è un file o una cartella.
3.  Eseguire una query **su IWMDMStorage** per [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)e chiamare [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) per leggere il file dal dispositivo e salvarlo in un percorso specificato.

Se invece si vuole leggere il file blocco per blocco dal dispositivo, è necessario implementare l'interfaccia di callback [**IWMDMOperation.**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) Passare questa interfaccia alla chiamata **IWMDMStorageControl::Read** e Windows Media Device Manager invierà blocchi di dati di file in sequenza al callback. La procedura seguente illustra come leggere un file del dispositivo blocco per blocco:

1.  Ottenere **l'interfaccia IWMDMStorage per** l'archiviazione e determinare se si tratta di un file, come descritto in precedenza.
2.  Preparare eventuali handle di file o altri handle necessari per contenere i dati ricevuti.
3.  Eseguire una query per **l'interfaccia IWMDMStorageControl dell'archiviazione**
4.  Chiamare **IWMDMStorageControl::Read** per iniziare l'operazione di lettura, passando **l'interfaccia IWMDMOperation** implementata.
5.  Windows Gestione dispositivi multimediali invierà il blocco di dati al dispositivo come descritto in [Gestione manuale dei trasferimenti di file.](handling-file-transfers-manually.md)

La funzione di esempio C++ seguente legge un oggetto di archiviazione da un dispositivo. La funzione accetta un puntatore di **interfaccia IWMDMOperation** facoltativo. Se inviata, la funzione creerà un file in modo esplicito e gestirà la scrittura dei dati nel file nell'implementazione di **IWMDMOperation::TransferObjectData**; In caso contrario, leggerà il file e lo salverà nella destinazione specificata da *pwszDestName*.


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Creazione di un'Windows Gestione dispositivi multimediali**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




