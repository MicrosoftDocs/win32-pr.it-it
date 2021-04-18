---
description: Windows Sockets 2 è un set di funzioni che standardizza il modo in cui le applicazioni accedono e usano i vari servizi di denominazione di rete.
ms.assetid: e245475c-26cc-491f-b335-b1b6a816dc3c
title: Registrazione e risoluzione dei nomi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc8abc778c09fa2c0cc8de00db0edaa846ed2ab0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309940"
---
# <a name="registration-and-name-resolution"></a><span data-ttu-id="6d797-103">Registrazione e risoluzione dei nomi</span><span class="sxs-lookup"><span data-stu-id="6d797-103">Registration and Name Resolution</span></span>

<span data-ttu-id="6d797-104">Windows Sockets 2 è un set di funzioni che standardizza il modo in cui le applicazioni accedono e usano i vari servizi di denominazione di rete.</span><span class="sxs-lookup"><span data-stu-id="6d797-104">Windows Sockets 2 is a set of functions that standardizes the way applications access and use the various network naming services.</span></span> <span data-ttu-id="6d797-105">Quando si usano queste funzioni, le applicazioni non devono distinguere i protocolli molto diversi associati ai servizi nomi, ad esempio DNS, NIS, X. 500, SAP e così via. Per mantenere la compatibilità completa con Windows Sockets 1,1, le funzioni di ricerca di database **getXbyY** e asincrone **WSAAsyncGetXbyY** esistenti continuano a essere supportate, ma sono implementate nell'interfaccia del provider di servizi Windows Sockets in termini di nuove funzionalità di risoluzione dei nomi.</span><span class="sxs-lookup"><span data-stu-id="6d797-105">When using these functions, applications need not distinguish the widely differing protocols associated with name services such as DNS, NIS, X.500, SAP, etc. To maintain full backward compatibility with Windows Sockets 1.1, the existing **getXbyY** and asynchronous **WSAAsyncGetXbyY** database-lookup functions continue to be supported, but are implemented in the Windows Sockets service provider interface in terms of the new name resolution capabilities.</span></span> <span data-ttu-id="6d797-106">Per ulteriori informazioni, vedere le funzioni [**GetServByName**](/windows/desktop/api/winsock/nf-winsock-getservbyname) e [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) .</span><span class="sxs-lookup"><span data-stu-id="6d797-106">For more information, see the [**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname) and [**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport) functions.</span></span> <span data-ttu-id="6d797-107">Vedere anche [risoluzione dei nomi compatibili per TCP/IP in Windows sockets 1,1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span><span class="sxs-lookup"><span data-stu-id="6d797-107">Also, see [Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-spi-2.md).</span></span>

<span data-ttu-id="6d797-108">Questa sezione descrive le funzionalità di registrazione e risoluzione dei nomi disponibili per gli sviluppatori Winsock.</span><span class="sxs-lookup"><span data-stu-id="6d797-108">This section describes registration and name resolution capabilities available to Winsock developers.</span></span> <span data-ttu-id="6d797-109">Nell'elenco seguente vengono descritti gli argomenti di questa sezione:</span><span class="sxs-lookup"><span data-stu-id="6d797-109">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="6d797-110">Risoluzione dei nomi indipendente dal protocollo</span><span class="sxs-lookup"><span data-stu-id="6d797-110">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
-   [<span data-ttu-id="6d797-111">Risoluzione dei nomi compatibile per TCP/IP nell'API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="6d797-111">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>](compatible-name-resolution-for-tcp-ip-in-the-windows-sockets-1-1-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="6d797-112">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6d797-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6d797-113">Informazioni su Winsock</span><span class="sxs-lookup"><span data-stu-id="6d797-113">About Winsock</span></span>](about-winsock.md)
</dt> <dt>

[<span data-ttu-id="6d797-114">Uso di Winsock</span><span class="sxs-lookup"><span data-stu-id="6d797-114">Using Winsock</span></span>](using-winsock.md)
</dt> </dl>

 

 



