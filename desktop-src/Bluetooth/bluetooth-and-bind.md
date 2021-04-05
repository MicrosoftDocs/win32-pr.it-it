---
title: Bluetooth e binding
description: Bluetooth usa la funzione di binding per eseguire il binding a un socket.
ms.assetid: 308d2680-de51-49e6-a0da-7aba494d9572
keywords:
- bind
- Bluetooth
- Bluetooth
- Bluetooth e binding
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12ccbd088ab61edcfa3dfc511ea591593d0cf781
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103872909"
---
# <a name="bluetooth-and-bind"></a><span data-ttu-id="022d4-107">Bluetooth e binding</span><span class="sxs-lookup"><span data-stu-id="022d4-107">Bluetooth and bind</span></span>

<span data-ttu-id="022d4-108">Bluetooth usa la funzione di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) per eseguire il binding a un socket.</span><span class="sxs-lookup"><span data-stu-id="022d4-108">Bluetooth uses the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function to bind to a socket.</span></span> <span data-ttu-id="022d4-109">Per associare un Socket Bluetooth, chiamare la funzione **Bind** usando la [**struttura \_ BTH di SOCKADDR**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) .</span><span class="sxs-lookup"><span data-stu-id="022d4-109">To bind a Bluetooth socket, call the **bind** function using the [**SOCKADDR\_BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) structure.</span></span> <span data-ttu-id="022d4-110">Usare la **struttura \_ BTH di SOCKADDR** con le impostazioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="022d4-110">Use the **SOCKADDR\_BTH** structure with the following settings:</span></span>

``` syntax
name.addressFamily = AF_BTH;
name.btAddr = 0;
name.serviceClassId = GUID_NULL;
name.port = number of service channel, 0 or BT_PORT_ANY;
```

<span data-ttu-id="022d4-111">Nelle applicazioni client, il membro della porta deve essere zero per consentire l'assegnazione di un endpoint locale appropriato.</span><span class="sxs-lookup"><span data-stu-id="022d4-111">On client applications, the port member must be zero to enable an appropriate local endpoint to be assigned.</span></span> <span data-ttu-id="022d4-112">Nelle applicazioni server, il membro di porta deve essere un numero di porta valido o una \_ porta BT \_ qualsiasi; le porte assegnate automaticamente usando \_ la porta BT \_ any possono essere eseguite successivamente con una chiamata alla funzione [**getsockname**](bluetooth-and-getsockname.md) .</span><span class="sxs-lookup"><span data-stu-id="022d4-112">On server applications, the port member must be a valid port number or BT\_PORT\_ANY; ports automatically assigned using BT\_PORT\_ANY may be queried subsequently with a call to the [**getsockname**](bluetooth-and-getsockname.md) function.</span></span> <span data-ttu-id="022d4-113">L'intervallo valido per la richiesta di una porta RFCOMM specifica è compreso tra 1 e 30.</span><span class="sxs-lookup"><span data-stu-id="022d4-113">The valid range for requesting a specific RFCOMM port is 1 through 30.</span></span> <span data-ttu-id="022d4-114">I canali server sono risorse globali e sono disponibili solo 30 canali server per RFCOMM su qualsiasi dispositivo Bluetooth, che deve essere condiviso da tutti i socket di Windows che appartengono alla famiglia di indirizzi Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="022d4-114">Server channels are global resource, and only 30 server channels are available for RFCOMM on any Bluetooth device, which must be shared by all Windows Sockets that belong to the Bluetooth address family.</span></span> <span data-ttu-id="022d4-115">Se non è disponibile alcun canale server o se il canale server specificato è già riservato, la chiamata di [**Binding**](/windows/desktop/api/winsock/nf-winsock-bind) ha esito negativo.</span><span class="sxs-lookup"><span data-stu-id="022d4-115">If no server channel is available, or if the specified server channel is already reserved, the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) call fails.</span></span>

<span data-ttu-id="022d4-116">Al termine della restituzione dal binding, il canale server viene riservato fino alla chiusura del socket.</span><span class="sxs-lookup"><span data-stu-id="022d4-116">Upon successful return from bind, the server channel is reserved until the socket is closed.</span></span> <span data-ttu-id="022d4-117">Usare la funzione [**getsockname**](bluetooth-and-getsockname.md) per recuperare il numero di canale per la registrazione SDP.</span><span class="sxs-lookup"><span data-stu-id="022d4-117">Use the [**getsockname**](bluetooth-and-getsockname.md) function to retrieve the channel number for SDP registration.</span></span>

<span data-ttu-id="022d4-118">Le applicazioni devono utilizzare l'allocazione automatica per il canale server.</span><span class="sxs-lookup"><span data-stu-id="022d4-118">Applications should use auto-allocation for the server channel.</span></span>

<span data-ttu-id="022d4-119">La funzione [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) non annuncia automaticamente l'applicazione server tramite il Bluetooth SDP; le applicazioni devono chiamare la funzione [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) per trovare le applicazioni Bluetooth Remote.</span><span class="sxs-lookup"><span data-stu-id="022d4-119">The [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function does not automatically advertise the server application using the Bluetooth SDP; applications must call the [**WSASetService**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea) function to be found by remote Bluetooth applications.</span></span>

## <a name="related-topics"></a><span data-ttu-id="022d4-120">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="022d4-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="022d4-121">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="022d4-121">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="022d4-122">**associare**</span><span class="sxs-lookup"><span data-stu-id="022d4-122">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)
</dt> </dl>

 

 