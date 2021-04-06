---
description: Trasferimento di un oggetto Properties-Only al dispositivo
ms.assetid: 6305cff9-c0ce-4ef5-a129-bc329b9c563f
title: Trasferimento di un oggetto Properties-Only al dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e20f9bcfecd46ea3047310ea5b946a366b35b9c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758450"
---
# <a name="transferring-a-properties-only-object-to-the-device"></a>Trasferimento di un oggetto Properties-Only al dispositivo

Mentre l'esempio nell'argomento precedente illustra la creazione di contenuto in un dispositivo costituito da proprietà e dati, questo argomento è incentrato sulla creazione di un oggetto solo proprietà.

I trasferimenti di sola proprietà vengono eseguiti utilizzando le interfacce descritte nella tabella seguente.



| Interfaccia                                                          | Descrizione                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [**Interfaccia IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) | Fornisce l'accesso ai metodi specifici del contenuto.       |
| [**Interfaccia IPortableDeviceValues**](iportabledevicevalues.md)   | Utilizzato per recuperare le proprietà che descrivono il contenuto. |



 

La `TransferContactToDevice` funzione nel modulo ContentTransfer. cpp dell'applicazione di esempio illustra come un'applicazione può trasferire le informazioni di contatto da un PC a un dispositivo connesso. In questo particolare esempio, il nome del contatto trasferito è "John Kane" hardcoded e il numero di telefono del contatto trasferito è sempre "425-555-0123".

La prima attività eseguita dalla `TransferContactToDevice` funzione consiste nel richiedere all'utente di immettere un identificatore di oggetto per l'oggetto padre sul dispositivo (in cui verrà trasferito il contenuto).


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the contact will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



Il passaggio successivo è il recupero delle proprietà del contatto, che verrà usato quando l'esempio scrive il nuovo contatto nel dispositivo. Il recupero delle proprietà del contatto viene eseguito dalla `GetRequiredPropertiesForPropertiesOnlyContact` funzione helper.


```C++
// 2) Get the properties that describe the object being created on the device

if (SUCCEEDED(hr))
{
    hr = GetRequiredPropertiesForPropertiesOnlyContact(szSelection,              // Parent to transfer the data under
                                                       &pFinalObjectProperties);  // Returned properties describing the data
    if (FAILED(hr))
    {
        printf("! Failed to get required properties needed to transfer an image file to the device, hr = 0x%lx\n", hr);
    }
}
```



Questa funzione scrive i dati seguenti in un oggetto **IPortableDeviceValues** .

-   Identificatore di oggetto per l'elemento padre del contatto nel dispositivo. (Si tratta della destinazione in cui verrà archiviato l'oggetto dal dispositivo).
-   Tipo di oggetto (contatto).
-   Nome del contatto (una stringa hardcoded di "John Kane").
-   Il numero di telefono del contatto (una stringa hardcoded "425-555-0123").

Il passaggio finale crea l'oggetto solo proprietà nel dispositivo (usando le proprietà impostate dalla `GetRequiredPropertiesForPropertiesOnlyContact` funzione helper). Questa operazione viene eseguita chiamando il metodo **IPortableDeviceContent:: CreateObjectWithPropertiesOnly** .


```C++
if (SUCCEEDED(hr))
{
    PWSTR pszNewlyCreatedObject = NULL;
    hr = pContent->CreateObjectWithPropertiesOnly(pFinalObjectProperties,    // Properties describing the object data
                                                  &pszNewlyCreatedObject);
    if (SUCCEEDED(hr))
    {
        printf("The contact was transferred to the device.\nThe newly created object's ID is '%ws'\n",pszNewlyCreatedObject);
    }

    if (FAILED(hr))
    {
        printf("! Failed to transfer contact object to the device, hr = 0x%lx\n",hr);
    }

    // Free the object identifier string returned from CreateObjectWithPropertiesOnly
    CoTaskMemFree(pszNewlyCreatedObject);
    pszNewlyCreatedObject = NULL;
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

 

 



