---
description: Il tipo di supporto (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva. Un determinato dispositivo può essere in grado di gestire un solo tipo di supporto oppure può essere in grado di gestire un intervallo di tipi.
ms.assetid: fccf85e9-3889-4ebc-b1bf-a60e27ab4586
title: Tipo supporto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 369954a4b0d1f78e12f6ea42bcc2ec61ca425012
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320599"
---
# <a name="media-type"></a><span data-ttu-id="51be3-104">Tipo supporto</span><span class="sxs-lookup"><span data-stu-id="51be3-104">Media Type</span></span>

<span data-ttu-id="51be3-105">Il *tipo di supporto* (o modalità) di un dispositivo descrive il tipo di informazioni che possono essere scambiate, ad esempio la voce interattiva.</span><span class="sxs-lookup"><span data-stu-id="51be3-105">The *media type* (or mode) of a device describes the type of information that can be exchanged, such as interactive voice.</span></span> <span data-ttu-id="51be3-106">Un determinato dispositivo può essere in grado di gestire un solo tipo di supporto oppure può essere in grado di gestire un intervallo di tipi.</span><span class="sxs-lookup"><span data-stu-id="51be3-106">A given device might be able to handle only one media type, or it might be able to deal with a range of types.</span></span>

<span data-ttu-id="51be3-107">I provider di servizi espongono il tipo o i tipi di supporto supportati dai dispositivi che controllano.</span><span class="sxs-lookup"><span data-stu-id="51be3-107">Service providers expose the media type or types supported by the devices they control.</span></span> <span data-ttu-id="51be3-108">Le applicazioni eseguono una query per il tipo di supporto e quindi utilizzano queste informazioni per selezionare un indirizzo appropriato su cui avviare una sessione.</span><span class="sxs-lookup"><span data-stu-id="51be3-108">Applications query for media type and then use this information to select an appropriate address on which to initiate a session.</span></span> <span data-ttu-id="51be3-109">La risposta dell'applicazione a una sessione offerta può essere predicata anche per il tipo di supporto.</span><span class="sxs-lookup"><span data-stu-id="51be3-109">Application response to a session offered may also be predicated on media type.</span></span>

<span data-ttu-id="51be3-110">Una determinata sessione di comunicazione, o chiamata, può coinvolgere diversi tipi di supporto.</span><span class="sxs-lookup"><span data-stu-id="51be3-110">A given communications session, or call, can involve several media types.</span></span> <span data-ttu-id="51be3-111">Per ulteriori informazioni, vedere tipo di supporto per una sessione.</span><span class="sxs-lookup"><span data-stu-id="51be3-111">For further information, see Media type for a session.</span></span>

<span data-ttu-id="51be3-112">**TAPI 2. x:** Vedere [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), membro **DwAvailableMediaModes** della struttura [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) a cui puntano le [ \_ costanti](./linemediamode--constants.md) *lpAddressCaps*, LINEMEDIAMODE.</span><span class="sxs-lookup"><span data-stu-id="51be3-112">**TAPI 2.x:** See [**lineGetAddressCaps**](/windows/win32/api/tapi/nf-tapi-linegetaddresscaps), **dwAvailableMediaModes** member of [**LINEADDRESSCAPS**](/windows/win32/api/tapi/ns-tapi-lineaddresscaps) structure pointed to by *lpAddressCaps*, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="51be3-113">**TAPI 3. x:** Vedere [**ITTerminal:: Get \_ mediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE \_ costanti](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="51be3-113">**TAPI 3.x:** See [**ITTerminal::get\_MediaType**](/windows/win32/api/tapi3if/nf-tapi3if-itterminal-get_mediatype), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>
