---
description: In due casi era necessario rinominare le funzioni usate nei socket Berkeley per evitare conflitti con altre funzioni dell'API Microsoft Windows.
ms.assetid: b53b1622-cba4-47e3-a371-b3186de6d61b
title: Funzioni rinominate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a8fd2af33bdeb74dd7a4c83fe535bae2a020530
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880458"
---
# <a name="renamed-functions"></a><span data-ttu-id="f04a3-103">Funzioni rinominate</span><span class="sxs-lookup"><span data-stu-id="f04a3-103">Renamed Functions</span></span>

<span data-ttu-id="f04a3-104">In due casi era necessario rinominare le funzioni usate nei socket Berkeley per evitare conflitti con altre funzioni dell'API Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f04a3-104">In two cases it was necessary to rename functions that are used in Berkeley Sockets in order to avoid clashes with other Microsoft Windows API functions.</span></span>

## <a name="close-and-closesocket"></a><span data-ttu-id="f04a3-105">Close e chiamata closesocket</span><span class="sxs-lookup"><span data-stu-id="f04a3-105">Close and Closesocket</span></span>

<span data-ttu-id="f04a3-106">I socket sono rappresentati da descrittori di file standard nei socket Berkeley, quindi è possibile usare la funzione **Close** per chiudere i socket e i file normali.</span><span class="sxs-lookup"><span data-stu-id="f04a3-106">Sockets are represented by standard file descriptors in Berkeley Sockets, so the **close** function can be used to close sockets as well as regular files.</span></span> <span data-ttu-id="f04a3-107">Sebbene nessun elemento in Windows Sockets impedisca a un'implementazione di utilizzare handle di file normali per identificare i socket, non è necessario alcun elemento.</span><span class="sxs-lookup"><span data-stu-id="f04a3-107">While nothing in Windows Sockets prevents an implementation from using regular file handles to identify sockets, nothing requires it either.</span></span> <span data-ttu-id="f04a3-108">In Windows è necessario chiudere i socket usando la routine [**chiamata closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) .</span><span class="sxs-lookup"><span data-stu-id="f04a3-108">On Windows, sockets must be closed by using the [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) routine.</span></span> <span data-ttu-id="f04a3-109">IN Windows, l'utilizzo della funzione **Close** per chiudere un socket non è corretto e gli effetti di tale operazione non sono definiti da questa specifica.</span><span class="sxs-lookup"><span data-stu-id="f04a3-109">ON Windows, using the **close** function to close a socket is incorrect and the effects of doing so are undefined by this specification.</span></span>

## <a name="ioctl-and-ioctlsocketwsaioctl"></a><span data-ttu-id="f04a3-110">IOCTL e ioctlsocket/WSAIoctl</span><span class="sxs-lookup"><span data-stu-id="f04a3-110">Ioctl and Ioctlsocket/WSAIoctl</span></span>

<span data-ttu-id="f04a3-111">Vari sistemi di runtime del linguaggio C utilizzano le IOCTL per scopi non correlati a Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="f04a3-111">Various C language run-time systems use the IOCTLs for purposes unrelated to Windows Sockets.</span></span> <span data-ttu-id="f04a3-112">Di conseguenza, la funzione [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) e la funzione [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) sono state definite per gestire le funzioni socket eseguite da **IOCTL** e **fcntl** nella distribuzione del software Berkeley.</span><span class="sxs-lookup"><span data-stu-id="f04a3-112">As a consequence, the [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) function and the [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) function were defined to handle socket functions that were performed by **IOCTL** and **fcntl** in the Berkeley Software Distribution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f04a3-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f04a3-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f04a3-114">**chiamata closesocket**</span><span class="sxs-lookup"><span data-stu-id="f04a3-114">**closesocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-closesocket)
</dt> <dt>

[<span data-ttu-id="f04a3-115">**ioctlsocket**</span><span class="sxs-lookup"><span data-stu-id="f04a3-115">**ioctlsocket**</span></span>](/windows/desktop/api/winsock/nf-winsock-ioctlsocket)
</dt> <dt>

[<span data-ttu-id="f04a3-116">Porting delle applicazioni socket in Winsock</span><span class="sxs-lookup"><span data-stu-id="f04a3-116">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="f04a3-117">Considerazioni sulla programmazione Winsock</span><span class="sxs-lookup"><span data-stu-id="f04a3-117">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> <dt>

[<span data-ttu-id="f04a3-118">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="f04a3-118">**WSAIoctl**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl)
</dt> </dl>

 

 



