---
title: Enumerazione dei dispositivi (WPD)
description: Informazioni su come un'applicazione enumera i dispositivi usando la funzione EnumerateAllDevices, che ottiene un conteggio dei dispositivi connessi e delle informazioni specifiche del dispositivo.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6465b04e6f1a18a0bdb74f0ce883cf9161371fb6
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068597"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="00871-103">Enumerazione dei dispositivi (WPD)</span><span class="sxs-lookup"><span data-stu-id="00871-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="00871-104">La prima attività completata dalla maggior parte delle applicazioni è l'enumerazione dei dispositivi connessi al computer.</span><span class="sxs-lookup"><span data-stu-id="00871-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="00871-105">Questa attività e il recupero delle informazioni sul dispositivo (ad esempio produttore, nome descrittivo e descrizione) sono supportati [**dall'interfaccia IPortableDeviceManager.**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)</span><span class="sxs-lookup"><span data-stu-id="00871-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="00871-106">La funzione EnumerateAllDevices nel modulo DeviceEnumeration.cpp contiene codice che illustra il recupero del conteggio dei dispositivi connessi e, una volta recuperato il conteggio, il recupero di informazioni specifiche del dispositivo per ogni dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="00871-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="00871-107">La funzione EnumerateAllDevices esegue quattro attività principali:</span><span class="sxs-lookup"><span data-stu-id="00871-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="00871-108">Crea l'oggetto gestione dispositivi portabile.</span><span class="sxs-lookup"><span data-stu-id="00871-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="00871-109">Recupera un conteggio dei dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="00871-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="00871-110">Recupera le informazioni sul dispositivo (per i dispositivi connessi).</span><span class="sxs-lookup"><span data-stu-id="00871-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="00871-111">Libera la memoria usata durante il recupero delle informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00871-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="00871-112">Ognuna di queste quattro attività è descritta in modo più dettagliato nelle sezioni seguenti.</span><span class="sxs-lookup"><span data-stu-id="00871-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="00871-113">Il primo passaggio del processo di enumerazione dei dispositivi è la creazione di un oggetto di gestione dispositivi portabile.</span><span class="sxs-lookup"><span data-stu-id="00871-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="00871-114">Questa operazione viene eseguita chiamando la funzione CoCreateInstance e passando l'identificatore di classe (CLSID) per l'oggetto, specificando il contesto in cui verrà eseguito il codice, specificando un identificatore di riferimento per l'interfaccia IPortableDeviceManager e quindi fornendo una variabile puntatore che riceve il puntatore di interfaccia IPortableDeviceManager.</span><span class="sxs-lookup"><span data-stu-id="00871-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


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



<span data-ttu-id="00871-115">Dopo aver ottenuto un [**puntatore a interfaccia IPortableDeviceManager,**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) è possibile iniziare a chiamare metodi su questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="00871-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="00871-116">Il primo metodo chiamato nella funzione EnumerateAllDevices è [**IPortableDeviceManager::GetDevices.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices)</span><span class="sxs-lookup"><span data-stu-id="00871-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="00871-117">Quando questo metodo viene chiamato con il primo argomento impostato su **NULL,** restituisce il conteggio dei dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="00871-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


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



<span data-ttu-id="00871-118">Dopo aver recuperato il numero di dispositivi connessi, è possibile usare questo valore per recuperare le informazioni sul dispositivo per ogni dispositivo connesso.</span><span class="sxs-lookup"><span data-stu-id="00871-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="00871-119">Questo processo inizia passando una matrice di puntatori di stringa come primo argomento e un conteggio del numero di elementi che questa matrice può contenere come secondo argomento (questo conteggio deve essere almeno uguale al numero di dispositivi disponibili).</span><span class="sxs-lookup"><span data-stu-id="00871-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="00871-120">Le stringhe restituite da questo metodo sono Plug and Play nomi dei dispositivi connessi.</span><span class="sxs-lookup"><span data-stu-id="00871-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="00871-121">Questi nomi, a loro volta, vengono passati ad altri metodi [**nell'interfaccia IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) per recuperare informazioni specifiche del dispositivo, ad esempio il nome descrittivo, il nome del produttore e la descrizione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="00871-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="00871-122">Questi nomi vengono usati anche per aprire una connessione al dispositivo quando un'applicazione chiama il [**metodo IPortableDevice::Open.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open)</span><span class="sxs-lookup"><span data-stu-id="00871-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


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



<span data-ttu-id="00871-123">Dopo aver recuperato le informazioni sul dispositivo, sarà necessario liberare la memoria associata alle stringhe a cui punta la matrice di puntatori di stringa.</span><span class="sxs-lookup"><span data-stu-id="00871-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="00871-124">Sarà anche necessario eliminare questa matrice.</span><span class="sxs-lookup"><span data-stu-id="00871-124">You will also need to delete this array.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="00871-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00871-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00871-126">**Interfaccia IPortableDeviceManager**</span><span class="sxs-lookup"><span data-stu-id="00871-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="00871-127">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="00871-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



