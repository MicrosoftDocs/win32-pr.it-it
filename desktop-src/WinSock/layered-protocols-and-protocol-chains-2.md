---
description: 'Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto.'
ms.assetid: 80e0b229-ebdc-4ac1-8e8e-9e5b7cfc3ab5
title: Protocolli sovrapposti e catene di protocolli
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf74a11dffca9d8c49c61af82132857f5510e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129163"
---
# <a name="layered-protocols-and-protocol-chains"></a><span data-ttu-id="17a49-103">Protocolli sovrapposti e catene di protocolli</span><span class="sxs-lookup"><span data-stu-id="17a49-103">Layered Protocols and Protocol Chains</span></span>

<span data-ttu-id="17a49-104">Windows Sockets 2 incorpora il concetto di protocollo a più livelli: uno che implementa solo funzioni di comunicazione di livello superiore mentre si basa su uno stack di trasporto sottostante per lo scambio effettivo di dati con un endpoint remoto.</span><span class="sxs-lookup"><span data-stu-id="17a49-104">Windows Sockets 2 incorporates the concept of a layered protocol: one that implements only higher-level communications functions while relying on an underlying transport stack for the actual exchange of data with a remote endpoint.</span></span> <span data-ttu-id="17a49-105">Un esempio di questo tipo di protocollo a più livelli è un livello di sicurezza che aggiunge un protocollo al processo di connessione socket per poter eseguire l'autenticazione e stabilire uno schema di crittografia.</span><span class="sxs-lookup"><span data-stu-id="17a49-105">An example of this type of layered protocol is a security layer that adds a protocol to the socket connection process in order to perform authentication and establish an encryption scheme.</span></span> <span data-ttu-id="17a49-106">Un protocollo di sicurezza di questo tipo richiede in genere i servizi di un protocollo di trasporto sottostante e affidabile, ad esempio TCP o SPX.</span><span class="sxs-lookup"><span data-stu-id="17a49-106">Such a security protocol generally requires the services of an underlying and reliable transport protocol such as TCP or SPX.</span></span>

<span data-ttu-id="17a49-107">Il termine *protocollo di base* fa riferimento a un protocollo, ad esempio TCP o SPX, che è completamente in grado di eseguire le comunicazioni dati con un endpoint remoto.</span><span class="sxs-lookup"><span data-stu-id="17a49-107">The term *base protocol* refers to a protocol, such as TCP or SPX, that is fully capable of performing data communications with a remote endpoint.</span></span> <span data-ttu-id="17a49-108">Un *protocollo* a più livelli è un protocollo che non può essere autonomo, mentre una *catena* di protocolli è uno o più protocolli sovrapposti e ancorato da un protocollo di base.</span><span class="sxs-lookup"><span data-stu-id="17a49-108">A *layered protocol* is a protocol that cannot stand alone, while a *protocol chain* is one or more layered protocols strung together and anchored by a base protocol.</span></span>

<span data-ttu-id="17a49-109">È possibile creare una catena di protocolli se si progettano i protocolli a più livelli per supportare Windows Sockets 2 SPI a entrambi i bordi superiore e inferiore.</span><span class="sxs-lookup"><span data-stu-id="17a49-109">You can create a protocol chain if you design the layered protocols to support the Windows Sockets 2 SPI at both their upper and lower edges.</span></span> <span data-ttu-id="17a49-110">Una struttura [**di \_ informazioni WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) speciale si riferisce alla catena di protocolli nel suo complesso e descrive l'ordine esplicito in cui vengono aggiunti i protocolli a più livelli.</span><span class="sxs-lookup"><span data-stu-id="17a49-110">A special [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structure refers to the protocol chain as a whole and describes the explicit order in which the layered protocols are joined.</span></span> <span data-ttu-id="17a49-111">Questa procedura è illustrata nella figura seguente.</span><span class="sxs-lookup"><span data-stu-id="17a49-111">This is illustrated in the figure below.</span></span> <span data-ttu-id="17a49-112">Poiché solo i protocolli di base e le catene di protocollo sono utilizzabili direttamente dalle applicazioni, sono elencate solo quando i protocolli installati vengono enumerati con la funzione [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .</span><span class="sxs-lookup"><span data-stu-id="17a49-112">Since only base protocols and protocol chains are directly usable by applications, they are the only ones listed when the installed protocols are enumerated with the [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) function.</span></span>

![architettura del protocollo a più livelli](images/ovrvw2-3.png)

 

 
