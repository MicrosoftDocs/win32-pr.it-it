---
description: Trasferimento di contenuto dal dispositivo a un PC
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Trasferimento di contenuto dal dispositivo a un PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a8695f8158040e75a4aae40f95386ed70af45df56a137dabc944ab6d1771e69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806521"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a>Trasferimento di contenuto dal dispositivo a un PC

Un'operazione comune eseguita da un'applicazione WPD è il trasferimento del contenuto da un dispositivo connesso al PC.

I trasferimenti di contenuto vengono evasi usando le interfacce descritte nella tabella seguente.



| Interfaccia                                                                | Descrizione                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Fornisce l'accesso **all'interfaccia IPortableDeviceProperties.** |
| [**Interfaccia IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Fornisce l'accesso ai metodi specifici della proprietà.                   |
| [**Interfaccia IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | Usato per archiviare le chiavi delle proprietà per il profilo specificato.          |
| Interfaccia IStream                                                        | Usato per leggere e scrivere i dati.                                |



 

La `TransferContentFromDevice` funzione nel modulo ContentTransfer.cpp dell'applicazione di esempio illustra come un'applicazione potrebbe trasferire le informazioni di contatto da un dispositivo connesso a un PC.

La prima attività eseguita dalla funzione è richiedere all'utente di immettere un identificatore di oggetto per l'oggetto padre nel dispositivo (in cui verrà trasferito `TransferContentFromDevice` il contenuto).


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



Il passaggio successivo consiste nel recupero di **un oggetto IPortableDeviceContent** utilizzato dall'esempio per accedere ai metodi specifici del contenuto.


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Il passaggio successivo consiste nel recupero di **un oggetto IPortableDeviceResources** utilizzato dall'esempio per accedere ai metodi specifici della risorsa.


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



Il passaggio successivo è il recupero di un oggetto IStream utilizzato dall'esempio per leggere i dati trasferiti dal dispositivo.


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



Il passaggio successivo consiste nel recupero del nome file dell'oggetto nel dispositivo. Questa stringa viene usata per creare il nome file corrispondente nel PC. Se l'oggetto non ha un nome file nel dispositivo, l'identificatore dell'oggetto viene convertito in una stringa e usato per creare il nome del file di destinazione.


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



Successivamente, l'esempio crea un oggetto IStream di destinazione.


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



Infine, l'oggetto IStream di origine viene copiato nella destinazione nel PC.


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



