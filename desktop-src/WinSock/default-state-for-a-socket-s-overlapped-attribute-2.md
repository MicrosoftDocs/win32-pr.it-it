---
description: La funzione socket ha creato socket con l'attributo Overlapped impostato per impostazione predefinita nel primo Wsock32.dll, la versione a 32 bit di Windows Sockets 1,1.
ms.assetid: 2ebf71fd-fcb3-4f2f-bf52-14cd13af012f
title: Stato predefinito per l'attributo Overlapped di un socket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bc46fbf08731b0f73d841291f6815b43d02785
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129203"
---
# <a name="default-state-for-a-sockets-overlapped-attribute"></a><span data-ttu-id="b761e-103">Stato predefinito per l'attributo Overlapped di un socket</span><span class="sxs-lookup"><span data-stu-id="b761e-103">Default State for a Socket's Overlapped Attribute</span></span>

<span data-ttu-id="b761e-104">La funzione [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) ha creato socket con l'attributo Overlapped impostato per impostazione predefinita nel primo Wsock32.dll, la versione a 32 bit di Windows sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="b761e-104">The [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function created sockets with the overlapped attribute set by default in the first Wsock32.dll, the 32-bit version of Windows Sockets 1.1.</span></span> <span data-ttu-id="b761e-105">Per garantire la compatibilità con le implementazioni Wsock32.dll attualmente distribuite, questo continuerà a essere il caso anche per Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="b761e-105">In order to ensure backward compatibility with currently deployed Wsock32.dll implementations, this will continue to be the case for Windows Sockets 2 as well.</span></span> <span data-ttu-id="b761e-106">Ovvero nei socket di Windows Sockets 2 creati con la funzione **socket** avrà l'attributo Overlapped.</span><span class="sxs-lookup"><span data-stu-id="b761e-106">That is, in Windows Sockets 2 sockets created with the **socket** function will have the overlapped attribute.</span></span> <span data-ttu-id="b761e-107">Tuttavia, per essere più compatibili con il resto dell'API Windows, i socket creati con [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) non saranno, per impostazione predefinita, hanno l'attributo Overlapped.</span><span class="sxs-lookup"><span data-stu-id="b761e-107">However, in order to be more compatible with the rest of the Windows API, sockets created with [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) will not, default, have the overlapped attribute.</span></span> <span data-ttu-id="b761e-108">Questo attributo verrà applicato solo se \_ è impostato il bit del flag WSA \_ sovrapposto.</span><span class="sxs-lookup"><span data-stu-id="b761e-108">This attribute will only be applied if the WSA\_FLAG\_OVERLAPPED bit is set.</span></span>

 

 



