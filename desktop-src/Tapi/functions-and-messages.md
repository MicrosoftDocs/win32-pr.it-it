---
description: La funzione phoneDevSpecific e il \_ messaggio DEVSPECIFIC Phone associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di telefonia comuni per telefoni.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funzioni e messaggi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967467"
---
# <a name="functions-and-messages"></a><span data-ttu-id="7c64e-103">Funzioni e messaggi</span><span class="sxs-lookup"><span data-stu-id="7c64e-103">Functions and Messages</span></span>

<span data-ttu-id="7c64e-104">La funzione [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) e il messaggio [**\_ DEVSPECIFIC Phone**](phone-devspecific.md) associato consentono a un'applicazione di accedere alle funzionalità del telefono specifiche del dispositivo che non sono disponibili tramite i servizi di telefonia comuni per telefoni.</span><span class="sxs-lookup"><span data-stu-id="7c64e-104">The [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function and its associated [**PHONE\_DEVSPECIFIC**](phone-devspecific.md) message enable an application to access device-specific phone features that are unavailable through the common telephony services for phones.</span></span> <span data-ttu-id="7c64e-105">In altre parole, **phoneDevSpecific** è la funzione di escape specifica del dispositivo che consente le estensioni dipendenti dal fornitore, mentre Phone \_ DEVSPECIFIC è il messaggio specifico del dispositivo che viene inviato all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7c64e-105">In other words, **phoneDevSpecific** is the device-specific escape function that allows vendor-dependent extensions, and PHONE\_DEVSPECIFIC is the device-specific message that is sent to the application.</span></span>

<span data-ttu-id="7c64e-106">Il profilo del parametro della funzione [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) è generico in quanto la minima interpretazione dei parametri viene eseguita da TAPI.</span><span class="sxs-lookup"><span data-stu-id="7c64e-106">The parameter profile of the [**phoneDevSpecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) function is generic in that little interpretation of the parameters is made by TAPI.</span></span> <span data-ttu-id="7c64e-107">L'interpretazione dei parametri è invece definita dal provider di servizi e deve essere riconosciuta da un'applicazione che li utilizza.</span><span class="sxs-lookup"><span data-stu-id="7c64e-107">Rather, the interpretation of the parameters is defined by the service provider and must be understood by an application that uses them.</span></span> <span data-ttu-id="7c64e-108">I parametri vengono semplicemente passati tramite TAPI dall'applicazione al provider di servizi.</span><span class="sxs-lookup"><span data-stu-id="7c64e-108">The parameters are simply passed through by TAPI from the application to the service provider.</span></span> <span data-ttu-id="7c64e-109">Un'applicazione che si basa su estensioni specifiche del dispositivo non funziona in genere con altri provider di servizi, ma le applicazioni scritte nei servizi telefonici telefonici comuni funzioneranno con il provider di servizi esteso.</span><span class="sxs-lookup"><span data-stu-id="7c64e-109">An application that relies on device-specific extensions will usually not work with other service providers, but applications written to the common telephony phone services will work with the extended service provider.</span></span>

 

 



