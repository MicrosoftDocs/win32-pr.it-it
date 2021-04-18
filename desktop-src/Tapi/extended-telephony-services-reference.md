---
description: Le funzioni di telefonia estese sono elencate per categoria nelle tabelle seguenti.
ms.assetid: f16aabf1-c034-4f91-87b2-c98cdf6d67ea
title: Informazioni di riferimento sui servizi di telefonia estesa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86980d7e23b031729c493660d7a31cdb06dc45de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307194"
---
# <a name="extended-telephony-services-reference"></a><span data-ttu-id="ce641-103">Informazioni di riferimento sui servizi di telefonia estesa</span><span class="sxs-lookup"><span data-stu-id="ce641-103">Extended Telephony Services Reference</span></span>

<span data-ttu-id="ce641-104">Le funzioni di telefonia estese sono elencate per categoria nelle tabelle seguenti.</span><span class="sxs-lookup"><span data-stu-id="ce641-104">The Extended Telephony functions are listed by category in the following tables.</span></span>

## <a name="extended-telephony-functions-for-line-devices"></a><span data-ttu-id="ce641-105">Funzioni di telefonia estese per dispositivi line</span><span class="sxs-lookup"><span data-stu-id="ce641-105">Extended Telephony Functions for Line Devices</span></span>



| <span data-ttu-id="ce641-106">Funzione</span><span class="sxs-lookup"><span data-stu-id="ce641-106">Function</span></span>                                                   | <span data-ttu-id="ce641-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce641-107">Description</span></span>                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce641-108">**lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="ce641-108">**lineNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) | <span data-ttu-id="ce641-109">Consente a un'applicazione di negoziare una versione di estensione da usare con il dispositivo a linee specificato.</span><span class="sxs-lookup"><span data-stu-id="ce641-109">Allows an application to negotiate an extension version to use with the specified line device.</span></span> <span data-ttu-id="ce641-110">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="ce641-110">Asynchronous.</span></span> |
| [<span data-ttu-id="ce641-111">**lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="ce641-111">**lineDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecific)                 | <span data-ttu-id="ce641-112">Consente ai provider di servizi di accedere alle funzionalità specifiche del dispositivo non offerte da altre funzioni TAPI.</span><span class="sxs-lookup"><span data-stu-id="ce641-112">Gives service providers access to device-specific features not offered by other TAPI functions.</span></span> <span data-ttu-id="ce641-113">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ce641-113">Synchronous.</span></span> |
| [<span data-ttu-id="ce641-114">**lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="ce641-114">**lineDevSpecificFeature**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedevspecificfeature)   | <span data-ttu-id="ce641-115">Invia le funzionalità di commutazione specifiche del dispositivo al Commuter.</span><span class="sxs-lookup"><span data-stu-id="ce641-115">Sends device-specific switch features to the switch.</span></span> <span data-ttu-id="ce641-116">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="ce641-116">Asynchronous.</span></span>                                           |



 

## <a name="extended-telephony-functions-for-phone-devices"></a><span data-ttu-id="ce641-117">Funzioni di telefonia estese per i dispositivi telefonici</span><span class="sxs-lookup"><span data-stu-id="ce641-117">Extended Telephony Functions for Phone Devices</span></span>



| <span data-ttu-id="ce641-118">Funzione</span><span class="sxs-lookup"><span data-stu-id="ce641-118">Function</span></span>                                                     | <span data-ttu-id="ce641-119">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce641-119">Description</span></span>                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ce641-120">**phoneDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="ce641-120">**phoneDevSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific)                 | <span data-ttu-id="ce641-121">Funzione di escape specifica del dispositivo per consentire le estensioni dipendenti dal fornitore.</span><span class="sxs-lookup"><span data-stu-id="ce641-121">Device-specific escape function to allow vendor-dependent extensions.</span></span> <span data-ttu-id="ce641-122">Asincrona.</span><span class="sxs-lookup"><span data-stu-id="ce641-122">Asynchronous.</span></span>                          |
| [<span data-ttu-id="ce641-123">**PhoneNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="ce641-123">**PhoneNegotiateExtVersion**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | <span data-ttu-id="ce641-124">Consente a un'applicazione di negoziare una versione di estensione da usare con il dispositivo telefonico specificato.</span><span class="sxs-lookup"><span data-stu-id="ce641-124">Allows an application to negotiate an extension version to use with the specified phone device.</span></span> <span data-ttu-id="ce641-125">Synchronous.</span><span class="sxs-lookup"><span data-stu-id="ce641-125">Synchronous.</span></span> |



 

 

 



