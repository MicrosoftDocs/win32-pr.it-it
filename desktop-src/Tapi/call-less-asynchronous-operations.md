---
description: Sono disponibili cinque operazioni asincrone che non sono correlate a una particolare chiamata.
ms.assetid: d7107834-07e4-40ed-91ea-2e6127597c13
title: Operazioni asincrone senza chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f4a246ab4a9022ce01d9707a7c5dc5cdc6e9e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345696"
---
# <a name="call-less-asynchronous-operations"></a><span data-ttu-id="cd7ad-103">Operazioni asincrone senza chiamata</span><span class="sxs-lookup"><span data-stu-id="cd7ad-103">Call-less Asynchronous Operations</span></span>

<span data-ttu-id="cd7ad-104">Sono disponibili cinque operazioni asincrone che non sono correlate a una particolare chiamata.</span><span class="sxs-lookup"><span data-stu-id="cd7ad-104">There are five asynchronous operations that are not related to any particular call.</span></span> <span data-ttu-id="cd7ad-105">Le funzioni [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal)e [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) di TAPI 2. x avviano queste operazioni.</span><span class="sxs-lookup"><span data-stu-id="cd7ad-105">The TAPI 2.x [**lineDevSpecific**](/windows/win32/api/tapi/nf-tapi-linedevspecific), [**lineDevSpecificFeature**](/windows/win32/api/tapi/nf-tapi-linedevspecificfeature), [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward), [**lineSetTerminal**](/windows/win32/api/tapi/nf-tapi-linesetterminal), and [**lineUncompleteCall**](/windows/win32/api/tapi/nf-tapi-lineuncompletecall) functions initiate these operations.</span></span> <span data-ttu-id="cd7ad-106">Se un'applicazione avvia una di queste operazioni asincrone e chiama [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), il provider di servizi potrebbe non ricevere alcuna indicazione che la funzione è stata abbandonata dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="cd7ad-106">If an application initiates one of these asynchronous operations and calls [**lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose), the service provider may receive no indication that the application has abandoned the function.</span></span> <span data-ttu-id="cd7ad-107">Questo problema può verificarsi se l'applicazione non è l'unica applicazione a cui è stata aperta la riga.</span><span class="sxs-lookup"><span data-stu-id="cd7ad-107">This can occur if the application was not the only application to have the line open.</span></span> <span data-ttu-id="cd7ad-108">Se l'applicazione chiama **lineClose** con una di queste operazioni in sospeso ed è l'unica applicazione con un handle alla riga, TAPI chiama la funzione [**TSPI \_ lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) e il provider di servizi deve terminare l'operazione asincrona, chiamando la funzione di [*callback \_ proc proc*](/windows/win32/api/tspi/nc-tspi-async_completion) per ogni operazione in sospeso con il valore di \_ errore LINEERR OPERATIONFAILED.</span><span class="sxs-lookup"><span data-stu-id="cd7ad-108">If the application calls **lineClose** with one of these operations pending, and it is the only application with a handle to the line, TAPI calls the [**TSPI\_lineClose**](/windows/win32/api/tspi/nf-tspi-tspi_lineclose) function and the service provider should terminate the asynchronous operation, calling the [*Completion\_Proc*](/windows/win32/api/tspi/nc-tspi-async_completion) callback function for each such outstanding operation with the LINEERR\_OPERATIONFAILED error value.</span></span>

 

 
