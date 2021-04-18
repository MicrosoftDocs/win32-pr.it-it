---
description: Per poter accedere a un'applicazione, è necessario che nel sistema sia installato correttamente un protocollo di trasporto e che sia registrato con Windows Sockets.
ms.assetid: 45b20f66-4e12-44df-b64b-c96cd5b24cd4
title: Accesso simultaneo a più protocolli di trasporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5e4b9d97743691bc527c455881cd0da5803b62b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309932"
---
# <a name="simultaneous-access-to-multiple-transport-protocols"></a><span data-ttu-id="15b26-103">Accesso simultaneo a più protocolli di trasporto</span><span class="sxs-lookup"><span data-stu-id="15b26-103">Simultaneous Access to Multiple Transport Protocols</span></span>

<span data-ttu-id="15b26-104">Per poter accedere a un'applicazione, è necessario che nel sistema sia installato correttamente un protocollo di trasporto e che sia registrato con Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="15b26-104">A transport protocol must be properly installed on the system and registered with Windows Sockets to be accessible to an application.</span></span> <span data-ttu-id="15b26-105">La \_ libreria32.dll WS2 esporta un set di funzioni per facilitare il processo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="15b26-105">The Ws2\_32.dll library exports a set of functions to facilitate the registration process.</span></span> <span data-ttu-id="15b26-106">È inclusa la creazione di una nuova registrazione e la rimozione di una esistente.</span><span class="sxs-lookup"><span data-stu-id="15b26-106">This includes creating a new registration and removing an existing one.</span></span>

<span data-ttu-id="15b26-107">Quando vengono create nuove registrazioni, il chiamante (ovvero lo script di installazione del fornitore dello stack) fornisce una o più strutture di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) contenenti un set completo di informazioni sul protocollo.</span><span class="sxs-lookup"><span data-stu-id="15b26-107">When new registrations are created, the caller (that is, the stack vendor's installation script) supplies one or more filled in [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures containing a complete set of information about the protocol.</span></span> <span data-ttu-id="15b26-108">Per ulteriori informazioni, vedere [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span><span class="sxs-lookup"><span data-stu-id="15b26-108">For more information, see [Windows Sockets 2 SPI](about-the-winsock-spi.md).</span></span> <span data-ttu-id="15b26-109">Qualsiasi stack di trasporto installato in questo modo viene definito provider di servizi Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="15b26-109">Any transport stack installed in this manner is referred to as a Windows Sockets service provider.</span></span>

<span data-ttu-id="15b26-110">In Windows XP con Service Pack 2 (SP2), Windows Server 2003 con Service Pack 1 (SP1) e Windows Vista e versioni successive.</span><span class="sxs-lookup"><span data-stu-id="15b26-110">On Windows XP with Service Pack 2 (SP2), Windows Server 2003 with Service Pack 1 (SP1), and Windows Vista and later.</span></span> <span data-ttu-id="15b26-111">il catalogo Winsock contenente un elenco di provider di trasporto e spazio dei nomi installati può essere visualizzato in un prompt dei comandi con il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="15b26-111">the Winsock catalog that contains a list of installed transport and namespace providers can be displayed in a command prompt with the following command:</span></span>

<span data-ttu-id="15b26-112">**netsh winsock Show Catalog**</span><span class="sxs-lookup"><span data-stu-id="15b26-112">**netsh winsock show catalog**</span></span>

<span data-ttu-id="15b26-113">Il Software Development Kit (SDK) di Microsoft Windows include *Sporder.exe*, che consente all'utente di visualizzare e modificare l'ordine in cui vengono enumerati i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="15b26-113">The Microsoft Windows Software Development Kit (SDK) includes *Sporder.exe*, which enables the user to view and modify the order in which service providers are enumerated.</span></span> <span data-ttu-id="15b26-114">Utilizzando *Sporder.exe*, un utente può stabilire manualmente un particolare stack di protocolli TCP/IP come provider TCP/IP predefinito se è presente più di uno stack di questo tipo.</span><span class="sxs-lookup"><span data-stu-id="15b26-114">Using *Sporder.exe*, a user can manually establish a particular TCP/IP protocol stack as the default TCP/IP provider if more than one such stack is present.</span></span>

<span data-ttu-id="15b26-115">L'applicazione *Sporder.exe* usa le funzioni esportate da *Sporder.dll* per riordinare i provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="15b26-115">The *Sporder.exe* application uses exported functions from *Sporder.dll* to reorder the service providers.</span></span> <span data-ttu-id="15b26-116">Di conseguenza, le applicazioni di installazione possono utilizzare l'interfaccia fornita da *Sporder.dll* per riordinare i provider di servizi a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="15b26-116">As a result, installation applications can use the interface provided by *Sporder.dll* to programmatically reorder service providers.</span></span>

-   [<span data-ttu-id="15b26-117">Protocolli sovrapposti e catene di protocolli</span><span class="sxs-lookup"><span data-stu-id="15b26-117">Layered Protocols and Protocol Chains</span></span>](layered-protocols-and-protocol-chains-2.md)
-   [<span data-ttu-id="15b26-118">Uso di più protocolli</span><span class="sxs-lookup"><span data-stu-id="15b26-118">Using Multiple Protocols</span></span>](using-multiple-protocols-2.md)
-   [<span data-ttu-id="15b26-119">Limitazioni di più provider per Select</span><span class="sxs-lookup"><span data-stu-id="15b26-119">Multiple Provider Restrictions on Select</span></span>](multiple-provider-restrictions-on-select-2.md)

 

 
