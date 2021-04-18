---
description: Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API.
ms.assetid: f4a4b406-3e3a-444f-b75a-0cf51bded1bc
title: Segnalazione errori e convalida parametri
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291fa2ed950d916be39b1a696f5fe8ad6f07280c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306989"
---
# <a name="error-reporting-and-parameter-validation"></a><span data-ttu-id="108dd-103">Segnalazione errori e convalida parametri</span><span class="sxs-lookup"><span data-stu-id="108dd-103">Error Reporting and Parameter Validation</span></span>

<span data-ttu-id="108dd-104">Lo schema per la segnalazione degli errori è diverso tra le interfacce SPI e API.</span><span class="sxs-lookup"><span data-stu-id="108dd-104">The scheme for error reporting differs between the SPI and API interfaces.</span></span> <span data-ttu-id="108dd-105">I provider di servizi Windows Sockets segnalano gli errori insieme alla funzione che restituisce, anziché l'approccio basato sui singoli thread usato nell'API.</span><span class="sxs-lookup"><span data-stu-id="108dd-105">Windows Sockets service providers report errors along with the function returning, as opposed to the per-thread based approach utilized in the API.</span></span> <span data-ttu-id="108dd-106">Il \_32.dll WS2 usa il codice di errore per funzione del provider di servizi per aggiornare il valore di errore per thread ottenuto tramite la funzione API [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) .</span><span class="sxs-lookup"><span data-stu-id="108dd-106">The Ws2\_32.dll uses the service provider's per-function error code to update the per-thread error value that is obtained through the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) API function.</span></span> <span data-ttu-id="108dd-107">Tuttavia, i provider di servizi sono ancora necessari per gestire l'errore basato sui socket, che può essere recuperato tramite l' \_ opzione del socket di errore so.</span><span class="sxs-lookup"><span data-stu-id="108dd-107">Service providers are still required, however, to maintain the per-socket based error which can be retrieved through the SO\_ERROR socket option.</span></span>

<span data-ttu-id="108dd-108">Il \_32.dll WS2 esegue la convalida dei parametri solo per le chiamate di funzione implementate interamente all'interno di se stesso.</span><span class="sxs-lookup"><span data-stu-id="108dd-108">The Ws2\_32.dll performs parameter validation only on function calls that are implemented entirely within itself.</span></span> <span data-ttu-id="108dd-109">I provider di servizi sono responsabili dell'esecuzione di tutta la relativa convalida dei parametri.</span><span class="sxs-lookup"><span data-stu-id="108dd-109">Service providers are responsible for performing all of their own parameter validation.</span></span>

 

 



