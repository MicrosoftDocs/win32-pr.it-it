---
description: Se un'applicazione non desidera alcuna interferenza da parte degli eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata.
ms.assetid: 0a3be209-e3ff-4177-abb2-ad0facbdf569
title: Proteggere una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00b1567303efb61f28f9c6b3e92c24287d23d4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319861"
---
# <a name="secure-a-session"></a><span data-ttu-id="1b1e4-103">Proteggere una sessione</span><span class="sxs-lookup"><span data-stu-id="1b1e4-103">Secure a Session</span></span>

<span data-ttu-id="1b1e4-104">Se un'applicazione non desidera alcuna interferenza da parte degli eventi esterni per una sessione da TAPI o dal provider di servizi, deve proteggere la chiamata.</span><span class="sxs-lookup"><span data-stu-id="1b1e4-104">If an application does not want any interference by outside events for a session from TAPI or the service provider, it should secure the call.</span></span> <span data-ttu-id="1b1e4-105">Ad esempio, in un ambiente analogo i toni di attesa delle chiamate possono eliminare una sessione fax o modem sulla chiamata originale.</span><span class="sxs-lookup"><span data-stu-id="1b1e4-105">For example, in an analog environment call-waiting tones can destroy a fax or modem session on the original call.</span></span>

<span data-ttu-id="1b1e4-106">Un'applicazione può proteggere una chiamata nel momento in cui viene effettuata la chiamata o dopo che la chiamata esiste già.</span><span class="sxs-lookup"><span data-stu-id="1b1e4-106">An application can secure a call at the time the call is made or after the call already exists.</span></span>

<span data-ttu-id="1b1e4-107">Non tutti i provider di servizi supportano l'utilizzo di questa operazione.</span><span class="sxs-lookup"><span data-stu-id="1b1e4-107">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="1b1e4-108">**TAPI 2. x:** Vedere [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span><span class="sxs-lookup"><span data-stu-id="1b1e4-108">**TAPI 2.x:** See [**lineSecureCall**](/windows/win32/api/tapi/nf-tapi-linesecurecall).</span></span>

<span data-ttu-id="1b1e4-109">**TAPI 3. x:** Vedere [**ITAddress:: inoltr**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span><span class="sxs-lookup"><span data-stu-id="1b1e4-109">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward).</span></span>

 

 
