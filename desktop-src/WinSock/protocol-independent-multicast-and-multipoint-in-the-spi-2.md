---
description: Windows Sockets (Winsock) e funzionalità multipoint e multicast indipendenti dal protocollo dei trasporti.
ms.assetid: 861f457c-fe7e-4128-a3f3-786424a96ea5
title: Protocol-Independent multicast e MultiPoint in SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bda9e5cab1b790a1e2d2c64c4451063a94dd8bc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131175"
---
# <a name="protocol-independent-multicast-and-multipoint-in-the-spi"></a><span data-ttu-id="0a66d-103">Protocol-Independent multicast e MultiPoint in SPI</span><span class="sxs-lookup"><span data-stu-id="0a66d-103">Protocol-Independent Multicast and Multipoint in the SPI</span></span>

<span data-ttu-id="0a66d-104">Così come Windows Sockets 2 consente di accedere alle funzionalità di base di trasporto dei dati di numerosi protocolli di trasporto in modo generico, fornisce anche un modo generico per usare le funzionalità multipoint e multicast dei trasporti che implementano queste funzionalità.</span><span class="sxs-lookup"><span data-stu-id="0a66d-104">Just as Windows Sockets 2 allows the basic data transport capabilities of numerous transport protocols to be accessed in a generic manner, it also provides a generic way to use multipoint and multicast capabilities of transports that implement these features.</span></span> <span data-ttu-id="0a66d-105">Per semplificare, il termine *multipoint* viene usato in seguito per fare riferimento alle comunicazioni multicast e MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="0a66d-105">To simplify, the term *multipoint* is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="0a66d-106">Le implementazioni multipoint correnti (ad esempio, multicast IP, ST-II, T. 120, ATM UNI) variano notevolmente in base al modo in cui i nodi si uniscono a una sessione MultiPoint, a seconda che un determinato nodo sia designato come nodo centrale o radice e che i dati vengano scambiati tra tutti i nodi o solo tra un nodo radice e vari nodi foglia.</span><span class="sxs-lookup"><span data-stu-id="0a66d-106">Current multipoint implementations (for example, IP multicast, ST-II, T.120, ATM UNI) vary widely with respect to how nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and various leaf nodes.</span></span> <span data-ttu-id="0a66d-107">La struttura delle [**\_ informazioni**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) di Windows Sockets 2 WSAPROTOCOL viene usata per dichiarare gli attributi MultiPoint di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="0a66d-107">The Windows Sockets 2 [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure is used to declare the multipoint attributes of a protocol.</span></span> <span data-ttu-id="0a66d-108">Esaminando questi attributi, il programmatore saprà le convenzioni da seguire per l'uso delle funzioni Winsock applicabili per configurare, usare e rimuovere le sessioni multipoint.</span><span class="sxs-lookup"><span data-stu-id="0a66d-108">By examining these attributes the programmer will know what conventions to follow in using the applicable Winsock functions to set up, use, and tear down multipoint sessions.</span></span>

<span data-ttu-id="0a66d-109">Le funzionalità di Windows Sockets 2 che supportano il multicast possono essere riepilogate come segue:</span><span class="sxs-lookup"><span data-stu-id="0a66d-109">The features of Windows Sockets 2 that support multicast can be summarized as follows:</span></span>

-   <span data-ttu-id="0a66d-110">Tre bit di attributo nella struttura di [**\_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="0a66d-110">Three attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="0a66d-111">Quattro flag definiti per il parametro *dwFlags* di [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span><span class="sxs-lookup"><span data-stu-id="0a66d-111">Four flags defined for the *dwFlags* parameter of [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket)</span></span>
-   <span data-ttu-id="0a66d-112">Una funzione, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint.</span><span class="sxs-lookup"><span data-stu-id="0a66d-112">One function, [**WSPJoinLeaf**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspjoinleaf), for adding leaf nodes into a multipoint session.</span></span>
-   <span data-ttu-id="0a66d-113">Due codici di comando di [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) per il controllo di loopback multipoint e la definizione dell'ambito per trasmissioni multicast.</span><span class="sxs-lookup"><span data-stu-id="0a66d-113">Two [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="0a66d-114">(Quest'ultimo corrisponde al parametro TTL (time-to-Live) del multicast IP.</span><span class="sxs-lookup"><span data-stu-id="0a66d-114">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="0a66d-115">L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non impedisce a un provider di servizi di supportare anche un'interfaccia dipendente dal protocollo esistente, ad esempio le opzioni socket di Deering per il multicast IP.</span><span class="sxs-lookup"><span data-stu-id="0a66d-115">The inclusion of these multipoint features in Windows Sockets 2 does not preclude a service provider from also supporting an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

 

 
