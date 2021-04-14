---
description: Come creare un'applicazione helper IP di base.
ms.assetid: b53f1cf5-3659-407e-8279-5c94333f3017
title: Creazione di un'applicazione helper IP di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baae961f8ffb6aa899e96fd05f0cb9f0c41469ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350266"
---
# <a name="creating-a-basic-ip-helper-application"></a><span data-ttu-id="1923c-103">Creazione di un'applicazione helper IP di base</span><span class="sxs-lookup"><span data-stu-id="1923c-103">Creating a Basic IP Helper Application</span></span>

<span data-ttu-id="1923c-104">**Per creare un'applicazione helper IP di base**</span><span class="sxs-lookup"><span data-stu-id="1923c-104">**To create a basic IP Helper application**</span></span>

1.  <span data-ttu-id="1923c-105">Creare un nuovo progetto vuoto.</span><span class="sxs-lookup"><span data-stu-id="1923c-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="1923c-106">Aggiungere un file di origine C++ vuoto al progetto.</span><span class="sxs-lookup"><span data-stu-id="1923c-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="1923c-107">Verificare che l'ambiente di compilazione faccia riferimento alle directory include, lib e src di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1923c-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="1923c-108">Verificare che l'ambiente di compilazione sia collegato al file della libreria helper IP iphlpapi. lib e al file della libreria WinSock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="1923c-108">Ensure that the build environment links to the IP Helper Library file Iphlpapi.lib and the Winsock Library file WS2\_32.lib.</span></span>
    > [!Note]  
    > <span data-ttu-id="1923c-109">Alcune funzioni Winsock di base vengono utilizzate per restituire i valori degli indirizzi IP e altre informazioni.</span><span class="sxs-lookup"><span data-stu-id="1923c-109">Some basic Winsock functions are used to return IP address values and other information.</span></span>

     

5.  <span data-ttu-id="1923c-110">Iniziare a programmare l'applicazione helper IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-110">Begin programming the IP Helper application.</span></span> <span data-ttu-id="1923c-111">Usare l'API helper IP includendo il file di intestazione dell'helper IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-111">Use the IP Helper API by including the IP Helper header file.</span></span>

    ```C++
    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="1923c-112">Il file di intestazione *iphlpapi. h* è necessario per le applicazioni che usano le funzioni di supporto IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-112">The *Iphlpapi.h* header file is required for applications that use the IP Helper functions.</span></span> <span data-ttu-id="1923c-113">Il file di intestazione *iphlpapi. h* include automaticamente altri file di intestazioni con strutture ed enumerazioni usate dalle funzioni helper IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-113">The *Iphlpapi.h* header file automatically includes other headers files with structures and enumerations used by the IP Helper functions.</span></span>
    >
    > <span data-ttu-id="1923c-114">Le nuove funzioni helper IP introdotte in Windows Vista e versioni successive sono definite nel file di intestazione *Netioapi. h* , incluso automaticamente nel file di intestazione *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-114">The new IP Helper functions introduced in Windows Vista and later are defined in the *Netioapi.h* header file which is automatically included by the *Iphlpapi.h* header file.</span></span> <span data-ttu-id="1923c-115">Il file di intestazione *Netioapi. h* non deve mai essere utilizzato direttamente.</span><span class="sxs-lookup"><span data-stu-id="1923c-115">The *Netioapi.h* header file should never be used directly.</span></span>
    >
    > <span data-ttu-id="1923c-116">Molte strutture ed enumerazioni usate dalle funzioni helper IP sono definite nei file di intestazione *Iprtrmib. h*, *Ipexport. h* e *Iptypes. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-116">Many of the structures and enumerations used by IP Helper functions are defined in the *Iprtrmib.h*, *Ipexport.h*, and *Iptypes.h* header files.</span></span> <span data-ttu-id="1923c-117">Questi file di intestazione vengono inclusi automaticamente nel file di intestazione *iphlpapi. h* e non devono mai essere usati direttamente.</span><span class="sxs-lookup"><span data-stu-id="1923c-117">These header files are automatically included in the *Iphlpapi.h* header file and should never be used directly.</span></span>
    >
    > <span data-ttu-id="1923c-118">In Microsoft Windows Software Development Kit (SDK) rilasciato per Windows Vista e versioni successive, l'organizzazione dei file di intestazione è cambiata.</span><span class="sxs-lookup"><span data-stu-id="1923c-118">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed.</span></span> <span data-ttu-id="1923c-119">Alcune strutture sono ora definite nei file di intestazione *Ipmib. h*, *tcpmib. h* e *Udpmib. h* , non nel file di intestazione *Iprtrmib. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-119">Some of the structures are now defined in the *Ipmib.h*, *Tcpmib.h*, and *Udpmib.h* header files, not in the *Iprtrmib.h* header file.</span></span> <span data-ttu-id="1923c-120">Il file di intestazione *Ipmib. h* include automaticamente il file di intestazione *ifmib. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-120">The *Ipmib.h* header file automatically includes the *Ifmib.h* header file.</span></span> <span data-ttu-id="1923c-121">Si noti che questi file di intestazione vengono inclusi automaticamente in *Iprtrmib. h*, che viene automaticamente incluso nel file di intestazione *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-121">Note that these header files are automatically included in *Iprtrmib.h*, which is automatically included in the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="1923c-122">Il file di intestazione *Winsock2. h* per Windows sockets 2,0 è richiesto dalla maggior parte delle applicazioni che usano le API helper IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-122">The *Winsock2.h* header file for Windows Sockets 2.0 is required by most applications using the IP Helper APIs.</span></span> <span data-ttu-id="1923c-123">Quando il file di intestazione *Winsock2. h* è obbligatorio, la \# riga di inclusione per questo file deve essere posizionata prima della \# riga di inclusione per il file di intestazione *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-123">When the *Winsock2.h* header file is required, the \#include line for this file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
    >
    > <span data-ttu-id="1923c-124">Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione *Windows. h* nelle applicazioni helper IP.</span><span class="sxs-lookup"><span data-stu-id="1923c-124">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for *Windows.h* header file in IP Helper applications.</span></span> <span data-ttu-id="1923c-125">Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1923c-125">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="1923c-126">Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="1923c-126">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="1923c-127">Le dichiarazioni nel file di intestazione *Winsock. h* per Windows sockets 1,1 sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="1923c-127">The declarations in the *Winsock.h* header file for Windows Sockets 1.1 will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="1923c-128">La \_ macro Win32 snello \_ e \_ media impedisce che il file di intestazione *Winsock. h* venga incluso nel file di intestazione di *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="1923c-128">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* header file from being included by the *Windows.h* header file.</span></span> <span data-ttu-id="1923c-129">Di seguito è riportato un esempio che illustra questo problema.</span><span class="sxs-lookup"><span data-stu-id="1923c-129">An example illustrating this is shown below.</span></span>

     

    ```C++
    #ifndef WIN32_LEAN_AND_MEAN
    #define WIN32_LEAN_AND_MEAN
    #endif

    #include <windows.h>

    #include <winsock2.h>
    #include <iphlpapi.h>
    #include <stdio.h>

    int main() {
      return 0;
    }
    
    ```

    

    > [!Note]
    >
    > <span data-ttu-id="1923c-130">Questa applicazione helper IP di base usa solo alcune strutture di dati degli indirizzi IP e l'indirizzo IP per le funzioni di conversione di stringhe da Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="1923c-130">This basic IP Helper application only uses some IP address data structures and IP address to string conversion functions from Windows Sockets 2.0.</span></span> <span data-ttu-id="1923c-131">Queste funzioni di Windows Sockets possono essere utilizzate senza chiamare [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare le risorse di Windows Sockets e [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando vengono eseguite utilizzando queste risorse.</span><span class="sxs-lookup"><span data-stu-id="1923c-131">These Windows Sockets functions can be used without calling [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) to initialize Windows Sockets resources and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) when done using these resources.</span></span>
    >
    > <span data-ttu-id="1923c-132">Nelle applicazioni helper IP che usano altre funzioni Winsock diverse da questo indirizzo IP alle funzioni di stringa, è necessario chiamare la funzione [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) per inizializzare le risorse di Windows Sockets prima di chiamare qualsiasi funzione Windows Sockets ed è necessario chiamare [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) quando l'applicazione viene eseguita usando le risorse di Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="1923c-132">In IP Helper applications that use other Winsock functions other than these IP address to string functions, the [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function must be called to initialize Windows Sockets resources before calling any Windows Sockets functions and [**WSACleanup**](/windows/desktop/api/winsock/nf-winsock-wsacleanup) should be called when the application is done using Windows Sockets resources.</span></span>

     

    > [!Note]
    >
    > <span data-ttu-id="1923c-133">Il file di intestazione *stdio. h* è necessario per l'uso di varie funzioni C standard in questa applicazione helper IP di base.</span><span class="sxs-lookup"><span data-stu-id="1923c-133">The *Stdio.h* header file is required for the use of various standard C functions in this basic IP Helper application.</span></span>

     

    <span data-ttu-id="1923c-134">Passaggio successivo: [recupero di informazioni tramite GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span><span class="sxs-lookup"><span data-stu-id="1923c-134">Next Step: [Retrieving Information Using GetNetworkParams](retrieving-information-using-getnetworkparams.md)</span></span>

 

 
