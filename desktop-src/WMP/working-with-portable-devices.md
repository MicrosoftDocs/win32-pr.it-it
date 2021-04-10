---
title: Uso dei dispositivi portatili
description: Uso dei dispositivi portatili
ms.assetid: 145ede07-a23b-486b-a561-9c87a48b72a8
keywords:
- Windows Media Player, dispositivi portatili
- Modello a oggetti di Windows Media Player, dispositivi portatili
- modello a oggetti, dispositivi portatili
- Controllo ActiveX Windows Media Player, dispositivi portatili
- Controllo ActiveX, dispositivi portatili
- Controllo ActiveX Windows Media Player Mobile, dispositivi portatili
- Dispositivi portatili Windows Media Player Mobile
- dispositivi portatili, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64c6e7047864b899a2d7dca2ba4754cc7cb5dc2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332380"
---
# <a name="working-with-portable-devices"></a><span data-ttu-id="50e47-111">Uso dei dispositivi portatili</span><span class="sxs-lookup"><span data-stu-id="50e47-111">Working with Portable Devices</span></span>

<span data-ttu-id="50e47-112">Questa sezione descrive come usare un controllo ActiveX di Windows Media Player remoto per lavorare con i dispositivi portatili.</span><span class="sxs-lookup"><span data-stu-id="50e47-112">This section describes how to use a remoted Windows Media Player ActiveX control to work with portable devices.</span></span>

<span data-ttu-id="50e47-113">Gli esempi di codice in questa sezione usano le classi Active Template Library (ATL), ad esempio **CComPtr**.</span><span class="sxs-lookup"><span data-stu-id="50e47-113">The code examples in this section use Active Template Library (ATL) classes, such as **CComPtr**.</span></span>

## <a name="included-headers"></a><span data-ttu-id="50e47-114">Intestazioni incluse</span><span class="sxs-lookup"><span data-stu-id="50e47-114">Included Headers</span></span>

<span data-ttu-id="50e47-115">Per usare il codice in questa sezione, includere le intestazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="50e47-115">To use the code in this section, include the following headers:</span></span>


```C++
#include <atlbase.h>
#include <atlcom.h>
#include <atlwin.h>
#include <commctrl.h>
#include "wmp.h"
#include "wmpids.h"
```



## <a name="iwmpplayer-pointer"></a><span data-ttu-id="50e47-116">Puntatore IWMPPlayer</span><span class="sxs-lookup"><span data-stu-id="50e47-116">IWMPPlayer Pointer</span></span>

<span data-ttu-id="50e47-117">Il puntatore **IWMPPlayer** viene archiviato in una variabile membro.</span><span class="sxs-lookup"><span data-stu-id="50e47-117">The **IWMPPlayer** pointer is stored in a member variable.</span></span>


```C++
CComPtr<IWMPPlayer> m_spPlayer;
```



## <a name="devices-are-stored-in-an-array"></a><span data-ttu-id="50e47-118">I dispositivi vengono archiviati in una matrice</span><span class="sxs-lookup"><span data-stu-id="50e47-118">Devices are Stored in an Array</span></span>

<span data-ttu-id="50e47-119">Il codice di esempio accede alla variabile membro seguente, da dichiarare nell'intestazione del progetto:</span><span class="sxs-lookup"><span data-stu-id="50e47-119">The example code accesses the following member variable, to be declared in the project header:</span></span>


```C++
IWMPSyncDevice **m_ppWMPDevices; // Points to the custom device array.
```



<span data-ttu-id="50e47-120">Il numero di dispositivi viene archiviato in una variabile membro.</span><span class="sxs-lookup"><span data-stu-id="50e47-120">The device count is stored in a member variable.</span></span>


```C++
int m_cDevices; // Count of devices.
```



## <a name="retrieving-a-device-pointer"></a><span data-ttu-id="50e47-121">Recupero di un puntatore a dispositivo</span><span class="sxs-lookup"><span data-stu-id="50e47-121">Retrieving a Device Pointer</span></span>

<span data-ttu-id="50e47-122">Un puntatore a un particolare dispositivo viene recuperato tramite il relativo indice di matrice utilizzando codice simile al seguente:</span><span class="sxs-lookup"><span data-stu-id="50e47-122">A pointer to a particular device is retrieved through its array index by using code similar to the following:</span></span>


```C++
CComPtr<IWMPSyncDevice> spSyncDevice(m_ppWMPDevices[lIndex]);
```



<span data-ttu-id="50e47-123">Si noti che l'indice illustrato negli esempi precedenti non è l'indice di relazione per il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="50e47-123">Note that the index shown in the preceding examples is not the partnership index for the device.</span></span> <span data-ttu-id="50e47-124">Si tratta dell'indice del dispositivo nella matrice di dispositivi personalizzata.</span><span class="sxs-lookup"><span data-stu-id="50e47-124">It is the index to the device in the custom array of devices.</span></span>

## <a name="cleaning-up"></a><span data-ttu-id="50e47-125">Pulizia</span><span class="sxs-lookup"><span data-stu-id="50e47-125">Cleaning Up</span></span>

<span data-ttu-id="50e47-126">Gli esempi usano la funzione seguente per liberare la memoria nell'array del dispositivo e rilasciare i puntatori di interfaccia:</span><span class="sxs-lookup"><span data-stu-id="50e47-126">The examples use the following function to free the memory in the device array and to release the interface pointers:</span></span>


```C++
void CMainDlg::FreeDeviceArray()
{
    if(m_ppWMPDevices)
    {
        for(long i = 0; i < m_cDevices; i++)
        {
            m_ppWMPDevices[i]->Release();
        }
 
        delete[] m_ppWMPDevices;
        m_ppWMPDevices = NULL;        
    }
}
```



## <a name="devices-are-displayed-in-a-list-box"></a><span data-ttu-id="50e47-127">I dispositivi vengono visualizzati in una casella di riepilogo</span><span class="sxs-lookup"><span data-stu-id="50e47-127">Devices are Displayed in a List Box</span></span>

<span data-ttu-id="50e47-128">La funzione GetSelectedDeviceIndex restituisce l'indice del dispositivo selezionato dall'utente in una casella di riepilogo usando il codice seguente:</span><span class="sxs-lookup"><span data-stu-id="50e47-128">The GetSelectedDeviceIndex function returns the index of the device the user selected in a list box by using the following code:</span></span>


```C++
long CMainDlg::GetSelectedDeviceIndex()
{
    return (long)SendMessage(GetDlgItem(IDC_DEVICES), LB_GETCURSEL, 0, 0);
}
```



## <a name="user-interface-state-is-managed-by-a-single-function"></a><span data-ttu-id="50e47-129">Lo stato dell'interfaccia utente è gestito da un'unica funzione</span><span class="sxs-lookup"><span data-stu-id="50e47-129">User Interface State is Managed by a Single Function</span></span>

<span data-ttu-id="50e47-130">La funzione SetUIState gestisce l'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="50e47-130">The SetUIState function manages the user interface.</span></span>


```C++
SetUIState(UIState 
NewState, BOOL 
bConnected)
```



<span data-ttu-id="50e47-131">I dettagli di questa funzione non sono rilevanti per le discussioni in questa sezione, ma tenere presente che questa funzione esegue attività quali l'abilitazione o la disabilitazione dei controlli e la modifica del testo visualizzato nell'interfaccia utente.</span><span class="sxs-lookup"><span data-stu-id="50e47-131">The details of this function are not relevant to the discussions in this section, but be aware that this function performs tasks like enabling or disabling controls and changing display text in the user interface.</span></span>

<span data-ttu-id="50e47-132">L'enumerazione UIState è stata definita nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="50e47-132">The UIState enumeration was defined as follows:</span></span>


```C++
enum UIState
{
    Partnership,
    NoPartnership,
    Synchronizing
};
```



<span data-ttu-id="50e47-133">Il parametro *bConnected* specifica se configurare l'interfaccia utente per un dispositivo connesso (true indica che il dispositivo è connesso).</span><span class="sxs-lookup"><span data-stu-id="50e47-133">The *bConnected* parameter specifies whether to configure the user interface for a connected device (TRUE means the device is connected).</span></span> <span data-ttu-id="50e47-134">I parametri *NewState* e *bConnected* contengono le informazioni necessarie per la funzione per svolgere il proprio lavoro.</span><span class="sxs-lookup"><span data-stu-id="50e47-134">The *NewState* and *bConnected* parameters convey the information needed for the function to do its work.</span></span>

<span data-ttu-id="50e47-135">Le sezioni seguenti forniscono spiegazioni del codice di esempio:</span><span class="sxs-lookup"><span data-stu-id="50e47-135">The following sections provide explanations of the example code:</span></span>

-   [<span data-ttu-id="50e47-136">Enumerazione dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="50e47-136">Enumerating Devices</span></span>](enumerating-devices.md)
-   [<span data-ttu-id="50e47-137">Recupero degli attributi del dispositivo</span><span class="sxs-lookup"><span data-stu-id="50e47-137">Retrieving Device Attributes</span></span>](retrieving-device-attributes.md)
-   [<span data-ttu-id="50e47-138">Visualizzazione dello stato di avanzamento della sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="50e47-138">Showing Synchronization Progress</span></span>](showing-synchronization-progress.md)
-   [<span data-ttu-id="50e47-139">Gestione delle playlist di sincronizzazione</span><span class="sxs-lookup"><span data-stu-id="50e47-139">Managing Synchronization Playlists</span></span>](managing-synchronization-playlists.md)

## <a name="related-topics"></a><span data-ttu-id="50e47-140">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="50e47-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50e47-141">**Guida al controllo del lettore**</span><span class="sxs-lookup"><span data-stu-id="50e47-141">**Player Control Guide**</span></span>](player-control-guide.md)
</dt> </dl>

 

 




