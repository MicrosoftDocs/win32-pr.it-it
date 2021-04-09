---
description: Come creare un'applicazione Windows Sockets (Winsock) di base.
ms.assetid: 56af2e95-ea82-49e4-b335-86dcf4c38780
title: Creazione di un'applicazione Winsock di base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0d5b5695ddb3b329bb4f81da6149fcf740a4240
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129207"
---
# <a name="creating-a-basic-winsock-application"></a><span data-ttu-id="743a8-103">Creazione di un'applicazione Winsock di base</span><span class="sxs-lookup"><span data-stu-id="743a8-103">Creating a Basic Winsock Application</span></span>

<span data-ttu-id="743a8-104">**Per creare un'applicazione Winsock di base**</span><span class="sxs-lookup"><span data-stu-id="743a8-104">**To create a basic Winsock application**</span></span>

1.  <span data-ttu-id="743a8-105">Creare un nuovo progetto vuoto.</span><span class="sxs-lookup"><span data-stu-id="743a8-105">Create a new empty project.</span></span>
2.  <span data-ttu-id="743a8-106">Aggiungere un file di origine C++ vuoto al progetto.</span><span class="sxs-lookup"><span data-stu-id="743a8-106">Add an empty C++ source file to the project.</span></span>
3.  <span data-ttu-id="743a8-107">Verificare che l'ambiente di compilazione faccia riferimento alle directory include, lib e src del Software Development Kit (SDK) di Microsoft Windows o della precedente piattaforma Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="743a8-107">Ensure that the build environment refers to the Include, Lib, and Src directories of the Microsoft Windows Software Development Kit (SDK) or the earlier Platform Software Development Kit (SDK).</span></span>
4.  <span data-ttu-id="743a8-108">Verificare che l'ambiente di compilazione sia collegato al file della libreria WinSock WS2 \_ 32. lib.</span><span class="sxs-lookup"><span data-stu-id="743a8-108">Ensure that the build environment links to the Winsock Library file Ws2\_32.lib.</span></span> <span data-ttu-id="743a8-109">Le applicazioni che utilizzano Winsock devono essere collegate al \_ file della libreria WS2 32. lib.</span><span class="sxs-lookup"><span data-stu-id="743a8-109">Applications that use Winsock must be linked with the Ws2\_32.lib library file.</span></span> <span data-ttu-id="743a8-110">Il \# commento pragma indica al linker che è necessario il file *WS2 \_ 32. lib* .</span><span class="sxs-lookup"><span data-stu-id="743a8-110">The \#pragma comment indicates to the linker that the *Ws2\_32.lib* file is needed.</span></span>
5.  <span data-ttu-id="743a8-111">Iniziare a programmare l'applicazione Winsock.</span><span class="sxs-lookup"><span data-stu-id="743a8-111">Begin programming the Winsock application.</span></span> <span data-ttu-id="743a8-112">Usare l'API Winsock includendo i file di intestazione di Winsock 2.</span><span class="sxs-lookup"><span data-stu-id="743a8-112">Use the Winsock API by including the Winsock 2 header files.</span></span> <span data-ttu-id="743a8-113">Il file di intestazione *Winsock2. h* contiene la maggior parte delle funzioni, delle strutture e delle definizioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="743a8-113">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="743a8-114">Il file di intestazione *Ws2tcpip. h* contiene le definizioni introdotte nel documento di allegato WinSock 2 Protocol-Specific per TCP/IP che include funzioni e strutture più recenti utilizzate per recuperare gli indirizzi IP.</span><span class="sxs-lookup"><span data-stu-id="743a8-114">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span>
    > [!Note]  
    > <span data-ttu-id="743a8-115">Stdio. h viene utilizzato per l'input e l'output standard, in particolare la funzione **printf ()** .</span><span class="sxs-lookup"><span data-stu-id="743a8-115">Stdio.h is used for standard input and output, specifically the **printf()** function.</span></span>

     


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



> [!Note]
>
> <span data-ttu-id="743a8-116">Il file di intestazione *iphlpapi. h* è obbligatorio se un'applicazione usa le API helper IP.</span><span class="sxs-lookup"><span data-stu-id="743a8-116">The *Iphlpapi.h* header file is required if an application is using the IP Helper APIs.</span></span> <span data-ttu-id="743a8-117">Quando il file di intestazione *iphlpapi. h* è obbligatorio, la \# riga di inclusione per il file di intestazione *Winsock2. h* deve essere posizionata prima della \# riga di inclusione per il file di intestazione *iphlpapi. h* .</span><span class="sxs-lookup"><span data-stu-id="743a8-117">When the *Iphlpapi.h* header file is required, the \#include line for the *Winsock2.h* header file should be placed before the \#include line for the *Iphlpapi.h* header file.</span></span>
>
> <span data-ttu-id="743a8-118">Il file di intestazione *Winsock2. h* include internamente gli elementi di base del file di intestazione di *Windows. h* , quindi non esiste in genere una \# riga di inclusione per il file di intestazione di *Windows. h* nelle applicazioni Winsock.</span><span class="sxs-lookup"><span data-stu-id="743a8-118">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="743a8-119">Se \# è necessaria una riga di inclusione per il file di intestazione di *Windows. h* , questa operazione deve essere preceduta dalla macro per la \# definizione e la media di Win32 \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="743a8-119">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="743a8-120">Per motivi cronologici, per impostazione predefinita l'intestazione *Windows. h* include il file di intestazione *Winsock. h* per Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="743a8-120">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="743a8-121">Le dichiarazioni nel file di intestazione *Winsock. h* sono in conflitto con le dichiarazioni nel file di intestazione *Winsock2. h* richiesto da Windows Sockets 2,0.</span><span class="sxs-lookup"><span data-stu-id="743a8-121">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.0.</span></span> <span data-ttu-id="743a8-122">La \_ macro Win32 snello \_ e \_ media impedisce che *Winsock. h* venga incluso nell'intestazione *Windows. h* .</span><span class="sxs-lookup"><span data-stu-id="743a8-122">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="743a8-123">Di seguito è riportato un esempio che illustra questo problema.</span><span class="sxs-lookup"><span data-stu-id="743a8-123">An example illustrating this is shown below.</span></span>

 


```C++
#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <iphlpapi.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



<span data-ttu-id="743a8-124">Passaggio successivo: [inizializzazione di Winsock](initializing-winsock.md)</span><span class="sxs-lookup"><span data-stu-id="743a8-124">Next Step: [Initializing Winsock](initializing-winsock.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="743a8-125">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="743a8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="743a8-126">Introduzione con Winsock</span><span class="sxs-lookup"><span data-stu-id="743a8-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="743a8-127">Informazioni su server e client</span><span class="sxs-lookup"><span data-stu-id="743a8-127">About Servers and Clients</span></span>](about-clients-and-servers.md)
</dt> </dl>

 

 



