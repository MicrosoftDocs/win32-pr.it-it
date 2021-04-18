---
description: Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti.
ms.assetid: 75cd8f21-a391-4626-b909-0760d12db995
title: Protocol-Independent multicast e MultiPoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e409c18752b32af7cf65b4a55862ec75cec7a3e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309945"
---
# <a name="protocol-independent-multicast-and-multipoint"></a><span data-ttu-id="6c608-103">Protocol-Independent multicast e MultiPoint</span><span class="sxs-lookup"><span data-stu-id="6c608-103">Protocol-Independent Multicast and Multipoint</span></span>

<span data-ttu-id="6c608-104">Windows Sockets 2 fornisce un metodo generico per l'utilizzo delle funzionalità multipoint e multicast dei trasporti.</span><span class="sxs-lookup"><span data-stu-id="6c608-104">Windows Sockets 2 provides a generic method for utilizing the multipoint and multicast capabilities of transports.</span></span> <span data-ttu-id="6c608-105">Questo metodo generico implementa queste funzionalità così come consente l'accesso alle funzionalità di trasporto dei dati di base di numerosi protocolli di trasporto.</span><span class="sxs-lookup"><span data-stu-id="6c608-105">This generic method implements these features just as it allows the basic data transport capabilities of numerous transport protocols to be accessed.</span></span> <span data-ttu-id="6c608-106">Il termine multipoint viene usato in seguito per fare riferimento alle comunicazioni multicast e MultiPoint.</span><span class="sxs-lookup"><span data-stu-id="6c608-106">The term, multipoint, is used hereafter to refer to both multicast and multipoint communications.</span></span>

<span data-ttu-id="6c608-107">Le implementazioni multipoint correnti (ad esempio, multicast IP, ST-II, T. 120 e ATM UNI) variano notevolmente.</span><span class="sxs-lookup"><span data-stu-id="6c608-107">Current multipoint implementations (for example, IP multicast, ST-II, T.120, and ATM UNI) vary widely.</span></span> <span data-ttu-id="6c608-108">Il modo in cui i nodi vengono aggiunti a una sessione MultiPoint, se un determinato nodo viene designato come nodo centrale o radice e se i dati vengono scambiati tra tutti i nodi o solo tra un nodo radice e i vari nodi foglia sono diversi tra le implementazioni.</span><span class="sxs-lookup"><span data-stu-id="6c608-108">How nodes join a multipoint session, whether a particular node is designated as a central or root node, and whether data is exchanged between all nodes or only between a root node and the various leaf nodes differ among implementations.</span></span> <span data-ttu-id="6c608-109">La struttura delle [**\_ informazioni di WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) per Windows Sockets 2 viene usata per dichiarare i vari attributi MultiPoint di un protocollo.</span><span class="sxs-lookup"><span data-stu-id="6c608-109">The [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure for Windows Sockets 2 is used to declare the various multipoint attributes of a protocol.</span></span> <span data-ttu-id="6c608-110">Esaminando questi attributi, il programmatore sa quali convenzioni seguire con le funzioni di Windows Sockets 2 applicabili per configurare, utilizzare e rimuovere le sessioni multipoint.</span><span class="sxs-lookup"><span data-stu-id="6c608-110">By examining these attributes, the programmer knows what conventions to follow with the applicable Windows Sockets 2 functions to set up, utilize, and tear down multipoint sessions.</span></span>

<span data-ttu-id="6c608-111">Di seguito sono riepilogate le funzionalità Winsock che supportano multipoint:</span><span class="sxs-lookup"><span data-stu-id="6c608-111">The following summarizes Winsock features that support multipoint:</span></span>

-   <span data-ttu-id="6c608-112">Bit a due attributi nella struttura [**di \_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) .</span><span class="sxs-lookup"><span data-stu-id="6c608-112">Two-attribute bits in the [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure.</span></span>
-   <span data-ttu-id="6c608-113">Quattro flag definiti per il parametro *dwFlags* della funzione [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) .</span><span class="sxs-lookup"><span data-stu-id="6c608-113">Four flags defined for the *dwFlags* parameter of the [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) function.</span></span>
-   <span data-ttu-id="6c608-114">Una funzione, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), per l'aggiunta di nodi foglia in una sessione multipoint</span><span class="sxs-lookup"><span data-stu-id="6c608-114">One function, [**WSAJoinLeaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf), for adding leaf nodes into a multipoint session</span></span>
-   <span data-ttu-id="6c608-115">Due codici di comando di [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) per il controllo di loopback multipoint e la definizione dell'ambito per trasmissioni multicast.</span><span class="sxs-lookup"><span data-stu-id="6c608-115">Two [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) command codes for controlling multipoint loopback and establishing the scope for multicast transmissions.</span></span> <span data-ttu-id="6c608-116">(Quest'ultimo corrisponde al parametro TTL (time-to-Live) del multicast IP.</span><span class="sxs-lookup"><span data-stu-id="6c608-116">(The latter corresponds to the IP multicast time-to-live or TTL parameter.)</span></span>

> [!Note]  
> <span data-ttu-id="6c608-117">L'inclusione di queste funzionalità multipoint in Windows Sockets 2 non impedisce a un'applicazione di usare un'interfaccia dipendente dal protocollo esistente, ad esempio le opzioni dei socket di cervo per il multicast IP.</span><span class="sxs-lookup"><span data-stu-id="6c608-117">The inclusion of these multipoint features in Windows Sockets 2 does not preclude an application from using an existing protocol-dependent interface, such as the Deering socket options for IP multicast.</span></span>

 

<span data-ttu-id="6c608-118">Vedere [semantica multipoint e multicast](multipoint-and-multicast-semantics-2.md) per informazioni dettagliate sul modo in cui vengono caratterizzati i diversi schemi multipoint e sulle modalità di utilizzo delle funzionalità applicabili di Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="6c608-118">See [Multipoint and Multicast Semantics](multipoint-and-multicast-semantics-2.md) for detailed information on how the various multipoint schemes are characterized and how the applicable features of Windows Sockets 2 are utilized.</span></span>

 

 
