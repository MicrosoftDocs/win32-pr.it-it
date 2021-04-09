---
description: L'architettura Windows Sockets 2 (Winsock) è conforme all'architettura di Windows Open System (WOSA).
ms.assetid: d4cf1462-2e83-49a5-b698-350ff37aa497
title: Architettura di Windows Sockets 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ae85ad58a4206d75144e47662bd563fb3235eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130415"
---
# <a name="windows-sockets-2-architecture"></a><span data-ttu-id="ba7d4-103">Architettura di Windows Sockets 2</span><span class="sxs-lookup"><span data-stu-id="ba7d4-103">Windows Sockets 2 Architecture</span></span>

<span data-ttu-id="ba7d4-104">L'architettura Windows Sockets 2 è conforme all'architettura di Windows Open System (WOSA), come illustrato di seguito:</span><span class="sxs-lookup"><span data-stu-id="ba7d4-104">The Windows Sockets 2 architecture is compliant with the Windows Open System Architecture (WOSA), as illustrated below:</span></span>

![architettura di Windows Sockets 2](images/ovrvw2-1.png)

<span data-ttu-id="ba7d4-106">Winsock definisce un'interfaccia del provider di servizi (SPI) standard tra il Application Programming Interface (API), con le funzioni esportate da WS2 \_32.dll e gli stack di protocolli.</span><span class="sxs-lookup"><span data-stu-id="ba7d4-106">Winsock defines a standard service provider interface (SPI) between the application programming interface (API), with its functions exported from WS2\_32.dll and the protocol stacks.</span></span> <span data-ttu-id="ba7d4-107">Di conseguenza, il supporto Winsock non è limitato agli stack di protocolli TCP/IP come nel caso di Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="ba7d4-107">Consequently, Winsock support is not limited to TCP/IP protocol stacks as is the case for Windows Sockets 1.1.</span></span>

<span data-ttu-id="ba7d4-108">Con l'architettura Windows Sockets 2, non è necessario o auspicabile, perché i fornitori di stack forniscano una propria implementazione di WS2 \_32.dll, dal momento che un singolo WS2 \_32.dll deve funzionare in tutti gli stack.</span><span class="sxs-lookup"><span data-stu-id="ba7d4-108">With the Windows Sockets 2 architecture, it is not necessary or desirable, for stack vendors to supply their own implementation of WS2\_32.dll, since a single WS2\_32.dll must work across all stacks.</span></span> <span data-ttu-id="ba7d4-109">Gli WS2 \_32.dll e gli shim di compatibilità devono essere visualizzati allo stesso modo di un componente del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="ba7d4-109">The WS2\_32.dll and compatibility shims should be viewed in the same way as an operating system component.</span></span>

 

 



