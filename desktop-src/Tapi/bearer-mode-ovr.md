---
description: La modalità di chiamata corrisponde alla qualità della trasmissione richiesta dalla rete per stabilire una chiamata.
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: Modalità di porta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226851"
---
# <a name="bearer-mode"></a><span data-ttu-id="98eec-103">Modalità di porta</span><span class="sxs-lookup"><span data-stu-id="98eec-103">Bearer Mode</span></span>

<span data-ttu-id="98eec-104">La [**modalità**](./linebearermode--constants.md) di chiamata corrisponde alla qualità della trasmissione richiesta dalla rete per stabilire una chiamata.</span><span class="sxs-lookup"><span data-stu-id="98eec-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="98eec-105">È importante mantenere il concetto di modalità di portabilità separata da quello del [**tipo di supporto**](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="98eec-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="98eec-106">Ad esempio, la rete telefonica analoga (PSTN) fornisce solo una modalità di connessione di tipo Voice a 3,1 kHz, ma chiama che lo usa può supportare i tipi di supporto, ad esempio Voice, fax o data modem.</span><span class="sxs-lookup"><span data-stu-id="98eec-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="98eec-107">La modalità di chiamata di una chiamata viene specificata al momento dell'impostazione della chiamata o viene fornita quando viene offerta la chiamata.</span><span class="sxs-lookup"><span data-stu-id="98eec-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="98eec-108">Con i dispositivi linea in grado di rappresentare i pool di canali, un provider di servizi può consentire la creazione di chiamate con una larghezza di banda più ampia.</span><span class="sxs-lookup"><span data-stu-id="98eec-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="98eec-109">Non tutti i provider di servizi supportano l'utilizzo di queste informazioni.</span><span class="sxs-lookup"><span data-stu-id="98eec-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="98eec-110">**TAPI 2. x:** Vedere [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span><span class="sxs-lookup"><span data-stu-id="98eec-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="98eec-111">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL \_ BEARERMODE** membro of [**CALLINFO \_ Long**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span><span class="sxs-lookup"><span data-stu-id="98eec-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="98eec-112">**TSPI:** Vedere il messaggio di [**riga \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) con *dwParam1* impostato su LINECALLINFOSTATE \_ BEARERMODE.</span><span class="sxs-lookup"><span data-stu-id="98eec-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
