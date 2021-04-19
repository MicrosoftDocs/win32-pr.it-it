---
description: L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi notificare a TAPI informazioni sulle risorse che utilizzeranno e sul modo in cui vengono usate.
ms.assetid: 2246c4d2-f8ca-4950-adc6-af9a6e214fe9
title: Inventario delle risorse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e743934f225fa4f932460eba0bbf895cc1bc21f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311877"
---
# <a name="resource-inventory"></a><span data-ttu-id="910f6-103">Inventario delle risorse</span><span class="sxs-lookup"><span data-stu-id="910f6-103">Resource Inventory</span></span>

<span data-ttu-id="910f6-104">L'applicazione deve eseguire l'inventario delle risorse di comunicazione disponibili, quindi notificare a TAPI informazioni sulle risorse che utilizzeranno e sul modo in cui vengono usate.</span><span class="sxs-lookup"><span data-stu-id="910f6-104">The application must inventory the communications resources available to it, then notify TAPI about which resources it will use and how it will use them.</span></span> <span data-ttu-id="910f6-105">Vedere [controllo del dispositivo](device-control.md) per informazioni aggiuntive sui tipi di risorse e funzionalità a cui un'applicazione può accedere.</span><span class="sxs-lookup"><span data-stu-id="910f6-105">See [Device Control](device-control.md) for additional information on the types of resources and capabilities an application might access.</span></span>

<span data-ttu-id="910f6-106">**TAPI 2. x:** Le applicazioni ottengono il numero di righe disponibili quando [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) restituisce.</span><span class="sxs-lookup"><span data-stu-id="910f6-106">**TAPI 2.x:** Applications get the number of available lines when [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa) returns.</span></span> <span data-ttu-id="910f6-107">Possono quindi eseguire [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) su ogni riga, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) per ogni indirizzo e [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) per ogni riga che verrà usata.</span><span class="sxs-lookup"><span data-stu-id="910f6-107">They can then perform [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) on each line, [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps) for each address, and [**lineOpen**](/windows/win32/api/tapi/nf-tapi-lineopen) for each line that will be used.</span></span>

<span data-ttu-id="910f6-108">**TAPI 3. x:** Le applicazioni usano gli indirizzi [**ITTAPI:: EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) o [**ITTAPI \_ :: Get**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) per individuare gli indirizzi disponibili.</span><span class="sxs-lookup"><span data-stu-id="910f6-108">**TAPI 3.x:** Applications use [**ITTAPI::EnumerateAddresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses) or [**ITTAPI::get\_Addresses**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-get_addresses) to discover the addresses available.</span></span> <span data-ttu-id="910f6-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) e [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) forniscono informazioni sui tipi di comunicazione possibili per ogni indirizzo.</span><span class="sxs-lookup"><span data-stu-id="910f6-109">[**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport) and [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) supply information on communication types possible for each address.</span></span> <span data-ttu-id="910f6-110">Se implementato dal provider di servizi, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) consente a un'applicazione di accedere a informazioni e controlli aggiuntivi.</span><span class="sxs-lookup"><span data-stu-id="910f6-110">If implemented by the service provider, [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) gives an application access to additional information and controls.</span></span>

 

 
