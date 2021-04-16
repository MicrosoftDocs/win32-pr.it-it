---
description: Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva. Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.
ms.assetid: 2eb140f0-ca07-4e60-b9f3-be2f466f4fca
title: Tipo di supporto per una sessione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc8f5c7743a5d5a85003c99b2ac1abbf13f54168
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530511"
---
# <a name="media-type-for-a-session"></a><span data-ttu-id="ead30-104">Tipo di supporto per una sessione</span><span class="sxs-lookup"><span data-stu-id="ead30-104">Media Type for a Session</span></span>

<span data-ttu-id="ead30-105">Il tipo di supporto (o modalità) descrive il tipo di informazioni scambiate, ad esempio la voce interattiva.</span><span class="sxs-lookup"><span data-stu-id="ead30-105">The media type (or mode) describes the type of information being exchanged, such as interactive voice.</span></span> <span data-ttu-id="ead30-106">Una determinata sessione di comunicazione può coinvolgere diversi tipi di supporti.</span><span class="sxs-lookup"><span data-stu-id="ead30-106">A given communications session may involve several media types.</span></span>

<span data-ttu-id="ead30-107">I provider di servizi espongono a TAPI e alle applicazioni il tipo o i tipi di supporto supportati.</span><span class="sxs-lookup"><span data-stu-id="ead30-107">Service providers expose to TAPI and to applications the media type or types they support.</span></span> <span data-ttu-id="ead30-108">Per informazioni sull'acquisizione di questi dati, vedere la panoramica del [tipo di supporto](media-type-ovr.md) per dispositivi.</span><span class="sxs-lookup"><span data-stu-id="ead30-108">See the device [media type](media-type-ovr.md) overview for information on acquiring this data.</span></span>

<span data-ttu-id="ead30-109">**TAPI 2. x:** Vedere [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**riga \_ MONITORMEDIA**](./line-monitormedia.md) Message, [LINEMEDIAMODE \_ costanti](./linemediamode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="ead30-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), [**lineSetMediaMode**](/windows/win32/api/tapi/nf-tapi-linesetmediamode), [**lineMonitorMedia**](/windows/win32/api/tapi/nf-tapi-linemonitormedia), [**LINE\_MONITORMEDIA**](./line-monitormedia.md) message, [LINEMEDIAMODE\_ Constants](./linemediamode--constants.md).</span></span>

<span data-ttu-id="ead30-110">**TAPI 3. x:** Vedere [**ITCallInfo:: Get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfo::p UT \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL \_ MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent:: Get \_ cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (restituisce [**CALLINFOCHANGE \_ cause**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC \_ MEDIATYPE**), [TAPIMEDIATYPE \_ costanti](tapimediatype--constants.md).</span><span class="sxs-lookup"><span data-stu-id="ead30-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong) with **CIL\_MEDIATYPESAVAILABLE**, [**ITCallInfoChangeEvent::get\_Cause**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfochangeevent-get_cause) (returns [**CALLINFOCHANGE\_CAUSE**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfochange_cause) of **CIC\_MEDIATYPE**), [TAPIMEDIATYPE\_ Constants](tapimediatype--constants.md).</span></span>

 

 
