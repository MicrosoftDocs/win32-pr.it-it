---
description: In TAPI sono disponibili numerose funzioni per la modifica degli handle di chiamata, per determinare la relazione tra linee, chiamate e indirizzi e così via.
ms.assetid: 283fe5e9-689f-4b87-97a6-b345c22ec6a2
title: Manipolazione dell'handle di chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 248f16088f891b1441626097de5c803a8fe14991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106309963"
---
# <a name="call-handle-manipulation"></a><span data-ttu-id="70735-103">Manipolazione dell'handle di chiamata</span><span class="sxs-lookup"><span data-stu-id="70735-103">Call Handle Manipulation</span></span>

<span data-ttu-id="70735-104">In TAPI sono disponibili numerose funzioni per la modifica degli handle di chiamata, per determinare la relazione tra linee, chiamate e indirizzi e così via.</span><span class="sxs-lookup"><span data-stu-id="70735-104">TAPI provides a number of functions for manipulating call handles, determining the relationship among lines, calls, and address, and so on.</span></span> <span data-ttu-id="70735-105">La maggior parte di questa funzionalità è implementata rigorosamente all'interno di TAPI senza riferimento al provider di servizi, ad eccezione di [**TSPI \_ lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span><span class="sxs-lookup"><span data-stu-id="70735-105">Most of this functionality is implemented strictly within TAPI without reference to the service provider, except for [**TSPI\_lineGetCallAddressID**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid).</span></span> <span data-ttu-id="70735-106">Questa funzione recupera l'identificatore dell'indirizzo di una chiamata esistente all'interno della relativa riga.</span><span class="sxs-lookup"><span data-stu-id="70735-106">This function retrieves the address identifier of an existing call within its line.</span></span> <span data-ttu-id="70735-107">I provider di servizi che modellano una linea come gruppo di identificatori di indirizzi possono scegliere un indirizzo imprevedibile per una nuova chiamata in ingresso o in uscita.</span><span class="sxs-lookup"><span data-stu-id="70735-107">Service providers that model a line as a group of address identifiers can choose an unpredictable address for a new inbound or outbound call.</span></span> <span data-ttu-id="70735-108">Questa funzione assegna a TAPI informazioni sufficienti per implementare l'operazione [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) quando viene richiamata con l' \_ opzione LINECALLSELECT Address.</span><span class="sxs-lookup"><span data-stu-id="70735-108">This function gives TAPI sufficient information to implement the [**lineGetNewCalls**](/windows/win32/api/tapi/nf-tapi-linegetnewcalls) operation when it is invoked with the LINECALLSELECT\_ADDRESS option.</span></span>

 

 
