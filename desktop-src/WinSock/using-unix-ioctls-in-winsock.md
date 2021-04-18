---
description: Il comando SIOCGIFCONF fornito dalla maggior parte delle implementazioni di UNIX è supportato sotto forma di funzioni WSAIoctl e WSPIoctl con il comando SIO \_ get \_ Interface \_ List. Questo comando restituisce l'elenco delle interfacce configurate e dei relativi parametri.
ms.assetid: c5028dae-052a-444c-837c-cd8d6d901b6c
title: Uso di IOCTL UNIX in Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0b52c311ea8c5f67dc374503f00c3ca16c5d053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313224"
---
# <a name="using-unix-ioctls-in-winsock"></a><span data-ttu-id="d3b8d-104">Uso di IOCTL UNIX in Winsock</span><span class="sxs-lookup"><span data-stu-id="d3b8d-104">Using UNIX Ioctls in Winsock</span></span>

<span data-ttu-id="d3b8d-105">Il comando **SIOCGIFCONF** fornito dalla maggior parte delle implementazioni di UNIX è supportato sotto forma di funzioni [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) con il comando **sio \_ get \_ Interface \_ List**.</span><span class="sxs-lookup"><span data-stu-id="d3b8d-105">The **SIOCGIFCONF** command provided by most UNIX implementations is supported in the form of [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) functions with the command **SIO\_GET\_INTERFACE\_LIST**.</span></span> <span data-ttu-id="d3b8d-106">Questo comando restituisce l'elenco delle interfacce configurate e dei relativi parametri.</span><span class="sxs-lookup"><span data-stu-id="d3b8d-106">This command returns the list of configured interfaces and their parameters.</span></span>

> [!Note]  
> <span data-ttu-id="d3b8d-107">Il supporto di questo comando è obbligatorio per i provider di servizi TCP/IP conformi a Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="d3b8d-107">Support of this command is mandatory for Windows Sockets 2-compliant TCP/IP service providers.</span></span>

 

<span data-ttu-id="d3b8d-108">Il parametro *lpvOutBuffer* punta al buffer in cui [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) e [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) archiviano le informazioni sulle interfacce.</span><span class="sxs-lookup"><span data-stu-id="d3b8d-108">The parameter *lpvOutBuffer* points to the buffer in which [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) and [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) store the information about interfaces.</span></span> <span data-ttu-id="d3b8d-109">Il numero di interfacce (numero di strutture restituite in *lpvOutBuffer*) può essere determinato in base alla lunghezza effettiva del buffer di output restituito in *lpcbBytesReturned*.</span><span class="sxs-lookup"><span data-stu-id="d3b8d-109">The number of interfaces (number of structures returned in *lpvOutBuffer*) can be determined based on the actual length of the output buffer returned in *lpcbBytesReturned*.</span></span>

 

 
