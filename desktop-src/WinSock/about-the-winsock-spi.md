---
description: Winsock fornisce un'interfaccia del provider di servizi per la creazione di servizi Winsock, comunemente noti come Winsock SPI.
ms.assetid: e3d21dd8-2b58-4108-857d-a075b8be68b0
title: Informazioni su Winsock SPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe70d5d381505085e2794a57a1183e8bec505917
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129231"
---
# <a name="about-the-winsock-spi"></a><span data-ttu-id="79b34-103">Informazioni su Winsock SPI</span><span class="sxs-lookup"><span data-stu-id="79b34-103">About the Winsock SPI</span></span>

<span data-ttu-id="79b34-104">Winsock fornisce un'interfaccia del provider di servizi per la creazione di servizi Winsock, comunemente noti come Winsock SPI.</span><span class="sxs-lookup"><span data-stu-id="79b34-104">Winsock provides a Service Provider Interface for creating Winsock services, commonly referred to as the Winsock SPI.</span></span> <span data-ttu-id="79b34-105">Esistono due tipi di provider di servizi: provider di trasporto e provider dello spazio dei nomi.</span><span class="sxs-lookup"><span data-stu-id="79b34-105">Two types of service providers exist: transport providers and namespace providers.</span></span> <span data-ttu-id="79b34-106">Esempi di provider di trasporto includono gli stack di protocolli, ad esempio TCP/IP o IPX/SPX, mentre un esempio di provider dello spazio dei nomi è un'interfaccia per il DNS (Domain Naming System) di Internet.</span><span class="sxs-lookup"><span data-stu-id="79b34-106">Examples of transport providers include protocol stacks such as TCP/IP or IPX/SPX, while an example of a namespace provider would be an interface to the Internet's Domain Naming System (DNS).</span></span> <span data-ttu-id="79b34-107">Le sezioni separate della specifica dell'interfaccia del provider di servizi si applicano a ogni tipo di provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="79b34-107">Separate sections of the service provider interface specification apply to each type of service provider.</span></span>

<span data-ttu-id="79b34-108">I provider di servizi di [trasporto](transport-service-providers-2.md) e [spazio dei nomi](name-space-service-providers-2.md) devono essere registrati con WS2 \_32.dll al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="79b34-108">[Transport](transport-service-providers-2.md) and [namespace](name-space-service-providers-2.md) service providers must be registered with the Ws2\_32.dll at the time they are installed.</span></span> <span data-ttu-id="79b34-109">Questa registrazione deve essere eseguita una sola volta per ogni provider, in quanto le informazioni necessarie vengono conservate nell'archivio permanente.</span><span class="sxs-lookup"><span data-stu-id="79b34-109">This registration need only be done once for each provider as the necessary information is retained in persistent storage.</span></span>

 

 



