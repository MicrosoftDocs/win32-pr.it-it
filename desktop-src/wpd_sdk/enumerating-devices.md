---
title: Enumerazione dei dispositivi (WPD)
description: Informazioni su come un'applicazione enumera i dispositivi usando la funzione EnumerateAllDevices, che ottiene un conteggio dei dispositivi connessi e delle informazioni specifiche del dispositivo.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6cfe1c1b4dee11383a4c36eaea43974f7e0439ae4ff2370a90e99b1702a8e0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083575"
---
# <a name="enumerating-devices-wpd"></a>Enumerazione dei dispositivi (WPD)

La prima attività completata dalla maggior parte delle applicazioni è l'enumerazione dei dispositivi connessi al computer. Questa attività e il recupero delle informazioni sul dispositivo (ad esempio produttore, nome descrittivo e descrizione) sono supportati [**dall'interfaccia IPortableDeviceManager.**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)

La funzione EnumerateAllDevices nel modulo DeviceEnumeration.cpp contiene codice che illustra il recupero del conteggio dei dispositivi connessi e, una volta recuperato il conteggio, il recupero di informazioni specifiche del dispositivo per ogni dispositivo connesso.

La funzione EnumerateAllDevices esegue quattro attività principali:

1.  Crea l'oggetto di gestione dispositivi portabile.
2.  Recupera un conteggio dei dispositivi connessi.
3.  Recupera le informazioni sul dispositivo (per i dispositivi connessi).
4.  Libera la memoria usata durante il recupero delle informazioni sul dispositivo.

Ognuna di queste quattro attività è descritta in modo più dettagliato nelle sezioni seguenti.

Il primo passaggio del processo di enumerazione dei dispositivi è la creazione di un oggetto di gestione dispositivi portabile. Questa operazione viene eseguita chiamando la funzione CoCreateInstance e passando l'identificatore di classe (CLSID) per l'oggetto, specificando il contesto in cui verrà eseguito il codice, specificando un identificatore di riferimento per l'interfaccia IPortableDeviceManager e quindi fornendo una variabile puntatore che riceve il puntatore di interfaccia IPortableDeviceManager.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



Dopo aver ottenuto un [**puntatore a interfaccia IPortableDeviceManager,**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) è possibile iniziare a chiamare metodi su questa interfaccia. Il primo metodo chiamato nella funzione EnumerateAllDevices è [**IPortableDeviceManager::GetDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices) Quando questo metodo viene chiamato con il primo argomento impostato su **NULL,** restituisce il conteggio dei dispositivi connessi.


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



Dopo aver recuperato il numero di dispositivi connessi, è possibile usare questo valore per recuperare le informazioni sul dispositivo per ogni dispositivo connesso. Questo processo inizia passando una matrice di puntatori di stringa come primo argomento e un conteggio del numero di elementi che questa matrice può contenere come secondo argomento (questo conteggio deve essere almeno uguale al numero di dispositivi disponibili).

Le stringhe restituite da questo metodo sono Plug and Play nomi dei dispositivi connessi. Questi nomi, a loro volta, vengono passati ad altri metodi [**nell'interfaccia IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) per recuperare informazioni specifiche del dispositivo, ad esempio il nome descrittivo, il nome del produttore e la descrizione del dispositivo. Questi nomi vengono usati anche per aprire una connessione al dispositivo quando un'applicazione chiama il [**metodo IPortableDevice::Open.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



Dopo aver recuperato le informazioni sul dispositivo, sarà necessario liberare la memoria associata alle stringhe a cui punta la matrice di puntatori di stringa. Sarà anche necessario eliminare questa matrice.


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Interfaccia IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Guida per programmatori**](programming-guide.md)
</dt> </dl>

 

 



