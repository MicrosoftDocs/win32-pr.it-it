---
description: Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI ITMSPAddress ITTerminalSupport ITStreamControl e ITStream.
ms.assetid: 59560bdf-953e-48e8-b565-46c3e0123c7e
title: Scrittura di un provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782dddb9a87725bde7c104d459b71204a04de018
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351166"
---
# <a name="writing-a-media-service-provider"></a><span data-ttu-id="62990-103">Scrittura di un provider di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="62990-103">Writing a Media Service Provider</span></span>

<span data-ttu-id="62990-104">Un provider di servizi multimediali deve implementare un subset minimo di interfacce MSPI: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol)e [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span><span class="sxs-lookup"><span data-stu-id="62990-104">A media service provider must implement a minimum subset of MSPI interfaces: [**ITMSPAddress**](/windows/desktop/api/msp/nn-msp-itmspaddress), [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport), [**ITStreamControl**](/windows/win32/api/tapi3if/nn-tapi3if-itstreamcontrol), and [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream).</span></span> <span data-ttu-id="62990-105">Il supporto del sottoflusso è facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62990-105">SubStream support is optional.</span></span> <span data-ttu-id="62990-106">Inoltre, un determinato MSP può implementare metodi aggiuntivi, ad esempio i controlli necessari per l'hardware specializzato.</span><span class="sxs-lookup"><span data-stu-id="62990-106">In addition, a given MSP may implement additional methods, such as controls required for specialized hardware.</span></span>

<span data-ttu-id="62990-107">I documenti materiali seguenti:</span><span class="sxs-lookup"><span data-stu-id="62990-107">The following material documents:</span></span>

-   <span data-ttu-id="62990-108">Le [classi di base msp di TAPI 3](tapi-3-msp-base-classes.md), ovvero un set di classi C++ progettate per semplificare l'attività di compilazione di un MSP basato su DirectShow.</span><span class="sxs-lookup"><span data-stu-id="62990-108">The [TAPI 3 MSP Base Classes](tapi-3-msp-base-classes.md), which are a set of C++ classes designed to simplify the task of building a DirectShow-based MSP.</span></span> <span data-ttu-id="62990-109">Le classi base implementano tutte le interfacce MSPI in modo generico.</span><span class="sxs-lookup"><span data-stu-id="62990-109">The base classes implement all the MSPI interfaces in a generic manner.</span></span> <span data-ttu-id="62990-110">MSPs differenti possono eseguire l'override di funzioni specifiche di MSP e fornire le proprie implementazioni.</span><span class="sxs-lookup"><span data-stu-id="62990-110">Different MSPs can override MSP-specific functions and provide their own implementations.</span></span>
-   <span data-ttu-id="62990-111">[TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), che fornisce interfacce e metodi usati da un MSP per il controllo dei terminali.</span><span class="sxs-lookup"><span data-stu-id="62990-111">The [TAPI 3 Terminal Manager](tapi-3-terminal-manager.md), which provides interfaces and methods used by an MSP to control terminals.</span></span>
-   <span data-ttu-id="62990-112">[Terminali collegabili](writing-a-pluggable-terminal.md), che consentono a un'applicazione anziché a un MSP di creare terminali.</span><span class="sxs-lookup"><span data-stu-id="62990-112">[Pluggable Terminals](writing-a-pluggable-terminal.md), which allow an application instead of an MSP to create terminals.</span></span> <span data-ttu-id="62990-113">Gli sviluppatori che hanno già sperimentato la scrittura di provider di servizi saranno gli autori principali dei terminali collegabili.</span><span class="sxs-lookup"><span data-stu-id="62990-113">Developers who are already experienced at writing service providers will be the primary creators of pluggable terminals.</span></span> <span data-ttu-id="62990-114">La versione iniziale implementata per questa versione è destinata alle applicazioni server di conferenza che devono aggiungere client non Windows 2000 o non multicast alle conferenze multicast SDP/IP multiparte di TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="62990-114">The initial version implemented for this release is aimed at conferencing server applications that need to add non-Windows 2000 or non-multicast clients to TAPI 3 multi-party SDP/IP multicast conferences.</span></span>

 

 
