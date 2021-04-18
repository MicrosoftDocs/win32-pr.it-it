---
description: Elementi dell'interfaccia Windows Sockets 2 (Winsock) per MultiPoint e multicast.
ms.assetid: c6f704cf-031b-4714-9f07-2d7715a157a0
title: Elementi dell'interfaccia Windows Sockets 2 per MultiPoint e multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad86905fe19c5c4c603db488874039b7cc8a0b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308868"
---
# <a name="windows-sockets-2-interface-elements-for-multipoint-and-multicast"></a><span data-ttu-id="8b812-103">Elementi dell'interfaccia Windows Sockets 2 per MultiPoint e multicast</span><span class="sxs-lookup"><span data-stu-id="8b812-103">Windows Sockets 2 Interface Elements for Multipoint and Multicast</span></span>

<span data-ttu-id="8b812-104">I meccanismi incorporati in Windows Sockets 2 per l'uso delle funzionalità multipoint possono essere riepilogati come segue:</span><span class="sxs-lookup"><span data-stu-id="8b812-104">The mechanisms that have been incorporated into Windows Sockets 2 for utilizing multipoint capabilities can be summarized as follows:</span></span>

-   <span data-ttu-id="8b812-105">Tre bit di attributo nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="8b812-105">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="8b812-106">Quattro flag definiti per il parametro *dwFlags* di [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span><span class="sxs-lookup"><span data-stu-id="8b812-106">Four flags defined for the *dwFlags* parameter of [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa).</span></span>
-   <span data-ttu-id="8b812-107">Una funzione, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="8b812-107">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="8b812-108">Due codici di comando di [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo di loopback multipoint e l'ambito delle trasmissioni multicast.</span><span class="sxs-lookup"><span data-stu-id="8b812-108">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and the scope of multicast transmissions.</span></span>

<span data-ttu-id="8b812-109">Le sezioni seguenti descrivono questi elementi dell'interfaccia in modo più dettagliato:</span><span class="sxs-lookup"><span data-stu-id="8b812-109">The following sections describe these interface elements in more detail:</span></span>

-   [<span data-ttu-id="8b812-110">Semantica per l'Unione di foglie multipoint</span><span class="sxs-lookup"><span data-stu-id="8b812-110">Semantics for Joining Multipoint Leaves</span></span>](semantics-for-joining-multipoint-leaves-2.md)
-   [<span data-ttu-id="8b812-111">Supporto di queste estensioni da protocolli multipoint esistenti</span><span class="sxs-lookup"><span data-stu-id="8b812-111">How Existing Multipoint Protocols Support These Extensions</span></span>](how-existing-multipoint-protocols-support-these-extensions-2.md)

 

 
